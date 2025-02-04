---
id: faq
title: FAQ
description: Polygon과 관련된 FAQ
keywords:
  - docs
  - matic
  - polygon
  - faq
image: https://wiki.polygon.technology/img/polygon-wiki.png
---

# 자주 묻는 질문 {#frequently-asked-questions}

## Polygon은 무엇인가요? {#what-is-polygon}

Polygon은 공공 블록체인에서 스케일링 솔루션입니다. 특히 이더리움에 대한 스케일링 솔루션입니다. Polygon은 보안 및 분산 방식으로 우수한 사용자 경험을 보장하면서 스케일러빌ity를 제공합니다. Kovan Testnet에서 이더리움에 대한 작업 구현을 제공합니다. Polygon은 기존 공용 블록 체인 네트워크에 스케일러빌을 제공하는 것과 함께 상호 운용성 기능을 제공할 수 있도록 향후 다른 블록체인을 지원할 계획입니다.

## Polygon은 다른 플라스마 구현과 어떻게 다를까요? {#how-is-polygon-different-from-other-implementations-of-plasma}

Polygon의 Plasma의 구현은 EVM에서 운영하는 국영 시다시피인에 구축되어 있으며, Plasma의 다른 구현은 주로 결제에 대한 UTXO를 사용하는 반면 Plasma의 다른 구현은 주로 사용됩니다. 상태 기반의 sidechain을 사용하면 Polygon을 통해 일반 스마트 계약에 대한 스케일러빌을 제공할 수 있습니다.

둘째, Polygon은 주기적으로 간격(Plasma Cash의 모든 블록이 끝난 후 체크포인트와는 달리)을 발행하여 사이드카가 빠른 속도로 조작할 수 있도록 하는 공개 체크포인팅 레이어를 사용합니다. 사기 혐의와 함께 이러한 체크포인트는 Polygon의 sidecain이 보안 방식으로 작동하도록 보장합니다.

## 귀하의 프로젝트는 플라스마 체인을 사용하여 이더리움에 확장성을 제공합니다. 그 본질은 프로토콜 또는 네이티브 블록체인입니까? {#your-project-provides-scalability-for-ethereum-using-plasma-chains-is-it-a-protocol-or-a-native-blockchain-in-itself}

Polygon 네트워크는 이더리움 주요 체인 자산이 있는 **"sidechain"** 솔루션입니다. 모든 dapps/Tokens / 프로토콜이 주요 체인의 프로토콜을 Polygon sidechain으로 이동하거나 필요할 때 필요할 때 Exacception을 Polygon으로 이동시킬 수 있습니다.

## 경쟁자에 비해 Polygon의 경쟁 장점은 무엇입니까? {#what-are-the-competitive-advantages-of-polygon-over-its-competitors}

### L2 스케일링 솔루션 {#l2-scaling-solutions}

Polygon은 분산화로 스케일을 달성하기 위해 최선을 다합니다. Polygon은 주기적 체크포인트와 사기 증명을 사용합니다. 사용자가 자산을 철회하기를 원할 때 체크포인트를 사용하여 sidechain에서 자산을 증명하고 사기 증명을 사용하여 사기 증명을 사용하여 사기 또는 나쁜 행동에 이의를 제기하고 스테이커에 슬래시할 수 있습니다.

다른 프로젝트는 또한 L2 스케일링 솔루션을 제공하고 있지만 다음 두 가지 핵심 요소가 있습니다.

1. 첫째, Polygon은 금융 거래뿐만 아니라 게임 및 기타 유틸리티 앱에 초점을 맞추고 있습니다. 또한 대출 / 거래 앱(토큰의 스왑, 마진 거래 등의 본격적인 금융 서비스에 대한 계획을 가지고 있습니다).

2. 둘째, Polygon은 1-2블록 시간(PoS 레이어를 포함)을 위해 체크포인트를 사용하지만, 많은 다른 솔루션은 이더리움 블록 시간보다 블록 곱하기 블록을 주요 체인에 밀어 넣어야 할 때 이더리움 블록 시간보다 많은 블록을 가질 수 있습니다.

### L1 스케일링 솔루션 {#l1-scaling-solutions}

그 외에도 다른 스케일링 프로젝트 중 Polygon은 상당한 수준의 분산화를 유지하면서 규모를 달성하는 능력에 의해 두드러집니다.

더 중요한 것은, 이러한 스케일러빌리티 프로젝트는 "바퀴를 재발명"하는 "문제를 가지고 있습니다. 개발자 커뮤니티, 제품 생태계, 기술 문서 및 기업이 **"스크래치"에서** 구축해야 하는 새로운 블록체인을 만들고 있습니다. 반면 Polygon은 EVM을 가능하게 하는 체인이며, 버튼을 누르면 확장 가능한 모든 dApps/자산을 이더리움 메인 체인에 내장한 모든 dApp / 자산을 보유하고 있습니다.

### 결제 {#payments}

우리는 다른 솔루션에서, 발신자와 수신기가 모두 지불 채널을 만들어야하기 때문에 Polygon이 usability의 측면에서 우위를 가지고 있다고 믿습니다. 이는 사용자에게 매우 번거롭습니다. Polygon의 기본 기술을 사용하는 경우, 사용자에게 결제 채널을 요구하지 않으며 사용자들은 단지 토큰을 수령하는 유효한 이더리움 주소만 있으면 됩니다. 이는 또한 분산 응용 프로그램의 사용자 경험을 개선하려는 당사의 장기적 비전과도 부합합니다.

### 거래 및 금융 {#trading-and-finance}

Polygon은 X의 (예: 0x), 유동성 풀장(예: Kyber Network) 및 London 프로토콜(Dhara Protocol)과 같은 기타 종류의 금융 프로토콜을 플랫폼에서 사용할 수 있도록 할 것이며, Polygon 사용자가 DEXs, lone dapps, LP 등의 다양한 금융 상거래 애플리케이션에 접근할 수 있도록 합니다.

## Polygon은 다른 idechain 솔루션과 어떻게 비교할까요? {#how-does-polygon-compare-with-other-sidechain-solutions}

Polygon에서 모든 사이드 거래는 사이드 샤인과 주요 체인에서 여러 메커니즘에 의해 보장됩니다. sidechain에서 블록 프로듀서에 의해 수행되는 모든 트랜잭션을 확인하고 고도로 분산 된 체크포인팅 레이어에 의해 메인 체인에 체크포인트를 확인합니다.

sidechain에서 사기 거래가 발생하면 체크포인팅 레이어에 의해 검출되고 처리할 수 있습니다. 심지어 극단적이고 매우 가능성이 높은 시나리오에서도 블록 프로듀서 층과 콜렉션 층이 모두 콜라보레이션을 모두 모두 모두 함께 하는 주요 체인은 대중의 누구나 와서 sidechain에서 부정행위를 부정하는 거래에 이의를 제기 할 수 있는 사기 증명을 가지고 있습니다.

만약 어려움이 성공하면 지분을 슬래시됨에 따라 공모자에게 엄청난 경제적 불이익 / 재정적 처벌이 있습니다. 또한 공개 도전자는 사기 사이드 세카 배우의 슬래시된 스테이크로 보상을 받습니다.

Polygon은 idechain 거래의 높은 수준의 분산화와 보안을 가진 경제적으로 인센티브 사이시카 인 네트워크를 만듭니다.

또한 Polygon 사이드 키인의 능력과 TPS는 다른 솔루션보다 훨씬 높습니다. 특히 Polygon은 수천 개의 트랜잭션을 가질 수 있는 경우 다른 사용자가 몇 천 개의 트랜잭션을 더 제한하는 단일 사이드 헤인인 경우 더 많은 Polygon을 제공합니다.

## 어떤 원칙을 통해 새로운 sidechain을 추가 할 것인가? 민간 기업의 지역 사이드 헤인에 대한 특별 요구 사항이 있습니까? {#via-what-principles-will-new-sidechains-be-added-will-there-be-any-special-requirements-for-private-companies-local-sidechains}

상태 채널과 관련하여 플라스마는 기본적으로 사용자가 어떠한 경우에도 자금을 잃지 않을 것이라고 말하는 프레임워크에서 제공하는 보안 보장으로 인해 스케일링 프레임워크에 대한 우수한 대안이 됩니다. 물론, 돈을 회수하는 데 지연이 발생할 수 있지만 Byzantine 플라스마 운영자는 허공에서 돈을 만들거나 트랜잭션을 이중으로 소비할 수 없습니다.

Polygon은 미래에 경제적 인센티브/반대 인센티브가 주로 시스템의 보안과 안정성을 주도하는 완전히 개방된 공개 블록체인 인프라가 되기 위해 노력할 것입니다. 따라서 누구나 시스템에 가입할 수 있고 합의에 참여할 수 있어야 합니다. 그러나 네트워크의 시드 단계에서 먼저 Polygon은 사이드 케인이 가능하도록 더 큰 역할을 해야 합니다.

또한 Polygonic sidechain은 주로 공공 sidechain을 사용할 수 있습니다. 그러나 엔터프라이즈 Polygon 체인은 특정 조직에 전용 사이드 키인(비개인 정보 보호 사용)을 제공할 계획입니다. 이러한 체인의 보안 및 분산화는 여전히 메인 체인의 체크포인팅 층과 사기 증명을 사용하여 그대로 유지됩니다.

## 사이드 세카인도 메인 체인(이더리움)과 동기화될 수 있을까요? {#will-sidechains-also-be-synced-with-the-main-chain-ethereum}

당연합니다. 공용 체크포인팅 층은 sidechain에서 일어나는 모든 트랜잭션을 확인하고 메인 체인에 증거를 게시할 것입니다. sidechain 거래의 가짜 보안을 보장하기 위해 주요 체인 Plasma 계약에는 모든 sidecain 거래가 사기 활동에 대해 이의를 제기 할 수 있는 다양한 종류의 Fraud Proofs가 포함되어 있습니다. 도전자가 성공하면 사기에 관련된 사이드 헤인 배우의 지분을 줄이고 도전자로 이전됩니다. 이것은 이제까지 실행되는 높은 지분 버그 현상과 동일합니다. 이해를 위한 좋은 다이어그램은 다음과 같습니다.

![스크린샷](/img/matic/Architecture.png)

## 백서의 끝에 '잠재적 사용 사례' 목록이 있습니다. 이 목록이 모두 구현됩니까? 그 순서는 어떻게 됩니까? {#at-the-end-of-the-white-paper-there-is-a-list-of-potential-use-cases-will-all-of-that-be-implemented-in-what-order}

기본 논리는 - 이더리움에서 작업하는 dApp / 프로토콜이 있다면 낮은 트랜잭션 처리량 및 높은 트랜잭션 수수료에 의해 제한되는 경우 - 그러면 Polygon 네트워크에서 이러한 dApp / Protocol에 대한 지원을 추가할 수 있습니다.

## Polygon의 플라스마 구현을 복제하는 것이 왜 어렵습니까? {#why-will-it-be-difficult-to-replicate-polygon-s-plasma-implementation}

네트워크가 다른 네트워크보다 더 잘 확장 / 성장할 수 있는 측면에서 네트워크 효과에 대해 더 많은 경우에도, 블록체인 솔루션은 사용자가 사용하는 실제 자산을 포함하기 때문에 오픈소스여야 합니다.

모든 오픈 소스 프로젝트가 있는 경우입니다. 저희는 저희가 구현한 것을 사용하는 모든 사람에게 그들의 코드를 의무적으로 오픈 소스로 공개할 것을 요구하는 GPL 라이선스를 마련할 것이기 때문에 이는 저희가 구현하는 것뿐만 아니라 다른 경쟁자가 구현하는 것에도 동일하게 적용됩니다. 그러나 다시 말하지만, 코드 복제가 Bitcoin, 이더리움 및 기타 프로젝트에 적용된다는 포인트는 해당 프로젝트가 달성할 수 있는 네트워크 효과에 대해 더 많이 알고 있습니다.

## Polygon 네트워크의 플라스마 구현이 특별한 점은 무엇입니까? {#what-s-special-about-polygon-network-s-plasma-implementation}

Polygon Plasma는 UTXO 시스템이 아닌 계정 기반 모델 시스템을 사용합니다. Polygon 체인에서 EVM을 사용하여 Eygon 생태계, 개발자 도구, 통합 라이브러리 등을 모두 활용할 수 있는 큰 이점을 제공합니다.

Polygon 네트워크는 ESC20 토큰에 대한 변경을 요구하지 않고 dfs에서 사용할 수 있습니다. 또한 체크포인팅 레이어를 사용하면 체크포인트에서 개별 블록의 증거를 배치하기 때문에 다른 Plasma 구현이 더 빨리 이루어질 수 있습니다.

## 중앙 집중화 문제를 어떻게 해결할 예정입니까? {#how-are-you-going-to-solve-the-issues-with-centralization}

이것은 일부 맥락을 보여주는 도표입니다.

![스크린샷](/img/matic/Merkle.png)

먼저, PoA 노드가 대표자가 될 것입니다 (Solvency 증명)과 KYC는 기본적으로 EOS 스타일 위조된 Processor (DPoS) 또는 그들에게 위임된 Fault Fault) 노드인 DBFT와 같은 PoS 층에 의해 선택됩니다.

둘째, 모든 대표자 (또는 2/3)를 돌려 잘못된 블록을 생성합니다. 그런 다음 모든 블록을 검증할 PoS 레이어 스테이커(PoS 레이어 스테이커)를 가지고 있으며, 만약 사기가 커밋 된 경우 대표단의 스테이크가 슬래시되고 시정 동작을 위해 체크킹됩니다.

셋째, 스테이커 PoS 층(많은 노드가 될 경우)도 나빠지고 콜라보레이드로 인해 잘못된 체크 포인트를 생성합니다. e는 모든 PoA가 부패하고 PoS가 부패하고 PoS가 부패합니다. 그럼에도 불구하고 Plasma 철학에 따라 우리는 많은 큰 프로젝트에서 시청하는 **Fraud Procement, Fraud** Procements 중 하나를 작성하고 있습니다(워치는 시크인 클리닉에서 저장소 감시자로 볼 수 있음). 이 사기 증명 메커니즘을 사용하면 누구나 메인 체인인 이더리움에서 모든 거래에 이의를 제기 할 수 있습니다.

## 매틱 토큰은 왜 필요합니까? {#why-is-matic-token-required}

다음 이유로 MATIC 토큰을 갖는 필요성을 강조합니다.

### Polygon은 공공 블록체인에 대한 일반적인 목적 확장 솔루션이 될 것입니다. {#polygon-intends-to-be-a-general-purpose-scaling-solution-for-public-blockchains}

우리는 첫 번째 베이시샤인으로 이더리움에서 시작되지만, 미래의 Polygon에서 여러 베이시샤인에 배포될 수 있습니다. 곧 다른 베이스체인이 추가될 것이므로 사이드체인에서 수수료를 지불하기 위해 하나의 통화(이더)를 사용하는 것은 불합리합니다. 어떤 기본 자산에 대한 네이티브 자산으로 해당 기본 자산을 갖는 경우 해당 기본 어셋의 통화가 스케일링 네트워크를 무력화시킬 수 있습니다. 따라서 Polygon의 자체 네트워크 토큰을 기반으로 스테이커 생태계를 구축하는 것이 중요합니다.

### Appcoon 보안 모델 {#appcoin-security-model}

Polygon은 Kyber와 같은 유동성 풀을 사용하여 토큰 스왑 메카니즘을 추상화함으로써 Dapp이 Polygon 수수료를 Dapp 코인으로 지불할 수 있게 하려고 합니다. 사용자는 단순히 그녀의 dApp-동전을 사용하여 수수료를 지불합니다. 배경에서 dApp-코인이 MATIC 토큰을 위해 교환됩니다. 따라서 매끄러운 사용자 경험을 제공하려는 DApp 개발자는 Polygon 유동성 풀의 유지를 도울 것입니다.

### 초기 단계에서 네트워크를 보내기 {#seeding-the-network-in-nascent-stages}

저희는 고도로 분산된 유효성 검사자 층과 블록 프로듀서에게 Eth를 배포할 수 없으므로, 처음에 네트워크에 txns가 거의 또는 전혀 없을 때 시스템에 시딩하는 것은 사실상 불가능합니다. 매틱 토큰을 이용해 저희는 블록 생산자, 체크포인터 스테이크를 시딩하기 위해 배포될 토큰의 큰 비율을 프로비저닝했으며, 그 이후에 블록 보상을 제공합니다. 이 공급은 설령 네트워크가 네트워크 효과를 부담하는 데 시간이 걸리더라도 스테이커가 보상을 받을 수 있게 합니다. 이는 비트코인에 대해 블록 마이닝 보상이 유지된 이유와 유사하며, 네트워크 보안을 유지하기 위해 이러한 방식으로 스테이커 및 블록 프로듀서에게 인센티브를 줄 수 있습니다.

여러분의 우려가 개발자에 관한 것이라면, 저희 전략의 기둥 중 하나는 개발자의 진입 장벽을 매우 낮게 유지하는 것입니다. 저희는 모든 이더리움 개발 도구가 Polygon에서 즉시 작동하는지 확인했습니다. 테스트넷에서 수수료를 지불하기 위해 필요한 토큰의 측면에서 이더리움의 개발자 건물에 대해서는 이테룸에서 는 다릅니다. dev는 Eygom에 있는 것과 마찬가지로 Polygon faucet에서 테스트넷을 위해 무료 토큰을 가져옵니다. Polygon 메인넷에 배포하려는 경우에만 MATIC 토큰을 필요로 합니다. Eygon에서 가스 수수료가 이더리움보다 훨씬 낮은 경우, 약 1/100분의 1에 해당되며, 이더리움에서 지불할 트랜잭션 수수료의 약 1/100분의 1을 차지합니다.

## 매틱 토큰의 사용과 수요를 이끄는 원동력은 무엇입니까? {#what-drives-the-use-and-demand-for-matic-tokens}

토큰에는 두 가지 기본 용도가 있습니다.

1. 토큰은 네트워크에서 트랜잭션 수수료를 지불하는 데 사용됩니다.
2. 토큰은 체크포인팅 레이어 및 블록 제작 레이어를 위한 스테이크 컨센서스 메커니즘의 증거에 참여하기 위해 스테이킹에 사용됩니다.

### 토큰 수요에 대한 2차 이유 중 일부는 {#some-of-the-secondary-reasons-for-token-demand}

* Polygon 네트워크는 Kyber와 같은 유동성 풀을 사용하여 토큰 스왑 메카니즘을 추상화함으로써 Dapp이 Polygon 수수료를 Dapp 코인으로 지불할 수 있게 하려고 합니다. 사용자는 단순히 그녀의 dApp-동전을 사용하여 수수료를 지불합니다. 배경에서 dApp-코인이 MATIC 토큰을 위해 교환됩니다. 따라서 매끄러운 사용자 경험을 제공하려는 DApp 개발자는 Polygon 유동성 풀의 유지를 도울 것입니다.

* 더 빠른 엑싱을 위해 Dhara 프로토콜을 사용하여 대출 메커니즘을 구현하고 있습니다. 대출자는 일주일 후에 exit-token을 사용하여 토큰을 청구합니다. 따라서 사용자는 거의 즉시 인출할 수 있는 반면 대출자는 서비스 제공의 대가로 이자를 벌 수 있습니다.

### 프로토콜 수준의 토큰 소각 {#protocol-level-burning-of-tokens}

우리는 모든 블록에서 트랜잭션 수수료의 비율을 태울 계획입니다. 이를 통해 본질적으로 토큰을 만들고 프로토콜 수준에서 그 값 측면에서 지속적인 지원을 제공합니다.

### 낮은 진입 장벽(따라서 신속한 채택의 가능성이 높아짐) {#low-entry-barrier-and-hence-higher-chances-of-quick-adoption}

저희는 최종 사용자의 채택을 확보하기 위해 DApps에 크게 의존하게 될 것입니다. 핵심 기능 중 하나는 모든 스마트 계약, 지갑, IDE, DevOps 도구 등과 완전히 호환되는 아키텍처를 유지하는 것입니다.

모든 이더리움 Dapp은 큰 변경이 거의 없이 Polygon으로 이식될 수 있습니다. 따라서 기존 이더리움 개발자가 Polygon으로 전환하는 진입 장벽은 바이러스 dApp 입양을 시작할 수 있는 무시할 수 있습니다. 이것은 Polygon 네트워크를 중심으로 하는 네트워크 영향으로 인해 많은 유기농 수요를 가져올 수 있습니다.

## 토큰 유형은 ERC20입니까? {#is-token-type-erc20}

예. 그리고 동일한 토큰은 Polygon 체인에도 적용될 수 있습니다. 미래에 네이티브 토큰으로 이동할 필요가 없습니다.

## 이더리움 네트워크에 가져올 수 있는 예상 TPS는 무엇입니까? 현재 테스트넷에서 무엇을 실행하고 있습니까? {#what-is-the-expected-tps-you-ll-be-able-to-bring-to-the-ethereum-network-what-are-you-running-at-now-on-testnet}

단일 사이드 세카인은 초당 7,000+ 트랜잭션 용량이 있습니다. Polygon은 여러 sidechin을 추가할 수 있는 능력이 있지만 현재 우리의 초점은 네트워크를 한 sidechain으로 안정화하는 데 있습니다.
