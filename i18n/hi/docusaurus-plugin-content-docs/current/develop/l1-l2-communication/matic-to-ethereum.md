---
id: matic-to-ethereum
title: पॉलीगॉन से एथेरेयम में डेटा ट्रांसफ़र करें
description: अनुबंध के ज़रिए पॉलीगॉन से एथेरेयम को स्टेट या डेटा ट्रांसफ़र करें
keywords:
  - docs
  - matic
image: https://matic.network/banners/matic-network-16x9.png
---

import useBaseUrl from '@docusaurus/useBaseUrl';

पॉलीगॉन से एथेरेयम में डेटा ट्रांसफ़र करने की मैकेनिज़्म एथेरेयम से पॉलीगॉन में यही करने से थोडी अलग है. एथेरेयम चेन पर वैलिडेटर्स द्वारा बनाए गए **चेकपॉइंट** ट्रांज़ैक्शन इसे हासिल करने के लिए का इस्तेमाल किए जाते हैं. मूल रूप से एक ट्रांज़ैक्शन को शुरू में पॉलीगॉन पर बनाया गया है. इस ट्रांज़ैक्शन को बनाते समय यह सुनिश्चित करना होगा कि  एक **इवेंट उत्सर्जित हो** और **इवेंट लॉग में वह डेटा शामिल हो जो हम** पॉलीगॉन से एथेरेयम में ट्रांसफ़र करना चाहते हैं.

समय की एक अवधि में ( लगभग 10-30 मिनट में ) यह ट्रांज़ैक्शन वैलिडेटरों द्वारा एथेरेयम चेन पर चेक-पॉइंट की जाती है. चेकपॉइंट किए जाने के बाद, पॉलीगॉन चेन पर बनाए गए ट्रांज़ैक्शन हैश को एथेरेयम चेन पर **रूट चेन मैनेजर** अनुबंध पर सबूत के रूप में प्रस्तुत किया जा सकता है. यह अनुबंध, ट्रांज़ैक्शन वैलिडेट करता है, यह वेरिफ़ाई करता है कि इस ट्रांज़ैक्शन को चेकपॉइंट में शामिल किया गया है और अंत में इस ट्रांज़ैक्शन के इवेंट लॉग्स को डिकोड करता है.

एक बार इस चरण को खत्म होने पर, हम एथेरेयम चेन पर डिप्लॉय किए गए रुट अनुबंध पर **कोई भी बदलाव करने के लिए डिकोड किए गए इवेंट लॉग डेटा** का इस्तेमाल कर सकते हैं. इसके लिए हमें यह सुनिश्चित करने की ज़रूरत है कि एथेरेयम पर स्टेट बदलने को केवल सुरक्षित तरीके से किया जाए. इसलिए, हम एक **पूर्वानुमान** अनुबंध का इस्तेमाल करते हैं जो एक विशेष प्रकार का अनुबंध है जो सिर्फ़ **रूट चेन मैनेजर** अनुबंध द्वारा ही ट्रिगर किया जा सकता है. यह आर्किटेक्चर सुनिश्चित करता है कि एथेरेयम पर स्टेट का बदलना तभी हो जब पॉलीगॉन पर ट्रांज़ैक्शन को **रूट चेन मैनेजर** अनुबंध द्वारा एथेरेयम चेन पर चेकपॉइंट और वेरिफ़ाई कर लिया गया है.

# ओवरव्यू {#overview}

- किसी ट्रांज़ैक्शन को पॉलीगॉन चेन पर डिप्लॉय किए गए चाइल्ड अनुबंध पर एग्जीक्यूट किया जाता है.
- इस ट्रांज़ैक्शन में एक इवेंट भी उत्सर्जित होता है. इस इवेंट के पैरामीटर्स में **वह डेटा शामिल होता है जिसे** पॉलीगॉन से एथेरेयम में ट्रांसफ़र करना होता है.
- पॉलीगॉन नेटवर्क पर वैलिडेटर इस ट्रांज़ैक्शन को समय के एक खास अंतराल में उठाता है( संभवतः 10-30 मिनट), उन्हें वैलिडेट करता है और एथेरेयम पर **चेकपॉइंट में जोड़ता है**.
- **रूट चेन** अनुबंध पर चेकपॉइंट ट्रांज़ैक्शन बनाई जाती है और चेकपॉइंट के शामिल होने को इस [स्क्रिप्ट](https://github.com/rahuldamodar94/matic-learn-pos/blob/transfer-matic-ethereum/script/check-checkpoint.js) का इस्तेमाल कर जाँचा जा सकता है
- चेकपॉइंट जोड़ने के पूरा होने पर, **matic.js** लाइब्रेरी का इस्तेमाल **रूट चेन मैनेजर** अनुबंध के **बाहर निकलने** वाले फंक्शन का सहारा लेने के लिए किया जा सकता है. जैसा कि इस [उदाहरण](https://github.com/rahuldamodar94/matic-learn-pos/blob/transfer-matic-ethereum/script/exit.js) में दिखाया गया है. **बाहर निकालने** के फ़ंक्शन का सहारा matic.js लाइब्रेरी का इस्तेमाल कर किया जा सकता है.

- स्क्रिप्ट रन करना, एथेरेयम चेन पर पॉलीगॉन ट्रांज़ैक्शन हैश के शामिल होने को वेरिफ़ाई करता है और फिर बदले में [भविष्यवाणी](https://github.com/rahuldamodar94/matic-learn-pos/blob/transfer-matic-ethereum/contracts/CustomPredicate.sol) अनुबंध के **exitToken** फ़ंक्शन का सहारा लेता है.
- यह सुनिश्चित करता है कि **रूट चेन अनुबंध पर स्टेट बदलना** हमेशा **सुरक्षित** तरीके से और **केवल भविष्यवाणी अनुबंध के माध्यम से** किया जाता है.
- यहाँ नोट करने की महत्वपूर्ण बात यह है कि पॉलीगॉन से **ट्रांज़ैक्शन हैश की वेरिफ़िकेशन** और **भविष्यवाणी अनुबंध को ट्रिगर करना** **एक अकेली ट्रांज़ैक्शन** में होता है और इस प्रकार रुट अनुबंध पर किसी भी स्टेट बदलने की सुरक्षा सुनिश्चित करता है.

# लागू करना {#implementation}

यह इसका एक सरल नमूना है कि पॉलीगॉन से एथेरेयम में डेटा कैसे ट्रांसफ़र किया जा सकता है. यह ट्यूटोरियल पूरी चेन में uint256 वैल्यू ट्रांसफ़र करने का एक उदाहरण दिखाता है. लेकिन आप डेटा की किस्म ट्रांसफ़र कर सकते हैं. लेकिन डेटा को बाइट में एन्कोड करना और फिर चाइल्ड अनुबंध से उसे उत्सर्जित करना ज़रूरी है. इसे आखिर में रूट अनुबंध पर डिकोड किया जा सकता है.

1. पहले रूट चेन और चाइल्ड चेन अनुबंध बनाएँ. यह सुनिश्चित करें कि जो फ़ंक्शन स्टेट में बदलाव करता है, वह एक इवेंट भी उत्सर्जित करे. इस इवेंट में ट्रांसफ़र किए जाने वाला डेटा एक पैरामीटर्स के रूप में ज़रूर शामिल होना चाहिए. चाइल्ड और रूट अनुबंध कैसे दिखने चाहिए उसका एक सैम्पल फ़ॉर्मैट नीचे दिया गया है. यह एक बहुत ही सरल अनुबंध है जिसमें एक डेटा वेरिएबल होता है जिसकी वैल्यू को एक setData फ़ंक्शन का इस्तेमाल कर सेट किया जाता है. setData फ़ंक्शन का सहारा लेने से इवेंट डेटा उत्सर्जित करता है. अनुबंध की बाकी चीजों को इस ट्यूटोरियल के आगामी खंडों में समझाया जाएगा.

क. चाइल्ड अनुबंध

```javascript
contract Child {

    event Data(address indexed from, bytes bytes_data);

    uint256 public data;

    function setData(bytes memory bytes_data) public {
     data = abi.decode(bytes_data,(uint256));
     emit Data(msg.sender,bytes_data);
    }

}
```

ख रूट अनुबंध

रूट अनुबंध कंस्ट्रक्टर में `_predicate` के लिए वैल्यू के रूप में `0x1470E07a6dD1D11eAE439Acaa6971C941C9EF48f` पास करें.

```javascript
contract Root {

    address public predicate;
    constructor(address _predicate) public{
        predicate=_predicate;
    }

   modifier onlyPredicate() {
        require(msg.sender == predicate);
        _;
    }

    uint256 public data;

    function setData(bytes memory bytes_data) public onlyPredicate{
        data = abi.decode(bytes_data,(uint256));
    }

}
```

2. एक बार पॉलीगॉन और एथेरेयम चेन पर चाइल्ड और रूट अनुबंध के क्रमशः डिप्लॉय हो जाने के बाद, इन अनुबंधों को पॉस ब्रिज का इस्तेमाल कर मैप करना होगा. यह मैपिंग सुनिश्चित करती है कि विभिन्न चेन में इन दोनोंं अनुबंध के बीच कनेक्शन बनाए रखा जाए. यह मैपिंग करने के लिए पॉलीगॉन टीम को [डिस्कॉर्ड](https://discord.com/invite/0xPolygon) पर संपर्क किया जा सकता है.

3. नोट करने की एक महत्वपूर्ण बात यह है कि रूट अनुबंध में, केवल एक ही भविष्यवाणी करने वाला परिवर्तक होता है. हमेशा इस परिवर्तक का इस्तेमाल करने की सलाह दी जाती है क्योंकि यह सुनिश्चित करता है कि केवल भविष्यवाणी अनुबंध ही रुट अनुबंध पर स्टेट बदले. भविष्यवाणी अनुबंध एक खास अनुबंध है जो रुट अनुबंध को तभी ट्रिगर करता है जब पॉलीगॉन चेन पर हुई ट्रांज़ैक्शन को एथेरेयम चेन पर रूट चेन मैनेजर द्वारा वेरिफ़ाई किया जाता है. यह रुट अनुबंध पर स्टेट का सुरक्षित बदलना सुनिश्चित करता है.

उपरोक्त लागू होने को टेस्ट करने के लिए, हम चाइल्ड अनुबंध के **setData** फ़ंक्शन का सहारा लेकर पॉलीगॉन चेन पर ट्रांज़ैक्शन बना सकते हैं. हमें इस समय चेकपॉइंट पूरा होने का इंतज़ार करना होगा. चेकपॉइंट के शामिल होने को इस [स्क्रिप्ट](https://github.com/rahuldamodar94/matic-learn-pos/blob/transfer-matic-ethereum/script/check-checkpoint.js) का इस्तेमाल कर जाँचा जा सकता है. चेकपॉइंट पूरा होने पर matic.js SDK का इस्तेमाल कर रूट चेन मैनेजर के बाहर निकलें फ़ंक्शन का सहारा लें.

```jsx
const txHash =
  "0xc094de3b7abd29f23a23549d9484e9c6bddb2542e2cc0aa605221cb55548951c";

const logEventSignature =
  "0x93f3e547dcb3ce9c356bb293f12e44f70fc24105d675b782bd639333aab70df7";

const execute = async () => {
  try {
    const tx = await maticPOSClient.posRootChainManager.exit(
      txHash,
      logEventSignature
    );
    console.log(tx.transactionHash); // eslint-disable-line
  } catch (e) {
    console.error(e); // eslint-disable-line
  }
};
```

जैसा कि ऊपर स्क्रीनशॉट में दिखाया गया है, **txHash** पॉलीगॉन चेन पर डिप्लॉय किए गए चाइल्ड अनुबंध पर हुई ट्रांज़ैक्शन का ट्रांज़ैक्शन हैश है.

**logEventSignature** डेटा इवेंट का keckack-256 हैश है. यह वही हैश है जिसे हमने भविष्यवाणी अनुबंध में शामिल किया है. इस ट्यूटोरियल के लिए इस्तेमाल किए गए सभी अनुबंध कोड और बाहर निकलने की स्क्रिप्ट को [यहाँ](https://github.com/rahuldamodar94/matic-learn-pos/tree/transfer-matic-ethereum) पाया जा सकता है

बाहर निकलने की स्क्रिप्ट के पूरा होने पर, एथेरेयम चेन पर रुट अनुबंध को वेरिफ़ाई करने के लिए क्वेरी किया जा सकता है अगर चाइल्ड अनुबंध में सेट की गई वेरीअबल **डेटा** वैल्यू को रुट अनुबंध के **डेटा** वेरिएबल में भी परिलक्षित किया गया है.
