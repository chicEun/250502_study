### EIP(Ethereum Improvement Proposal)

`이더리움 개선 제안`은 이더리움 네트워크의 새로운 기능이나, 변경 사항을 기술하는 설계 문서
ethereum.org  , cyfrin.io 
등 커뮤니티 구성원이라면 누구나 개선 아이디어, 제안서를 작성하여 제출할수 있으며 
제안된 변경사항의 기술 사양과 배경 동기등을 명확히 제시하여야함
ethereum.org  , cyfrin.io  EIP의 주된 목적은 변경 사항을 투명하게  논의·검증하고 표준화 하는것
cyfrin.io
ex) EIP-20은 ERC-20 토큰 표준을 정의하여 호환성을 확보하고  cyfrin.io
모든 제안이 GitHub과 공식 사이트에 기록되어 이더리움 진화 과정을 역사적으로 남김
cyfrin.io  또한 EIP 제안과 토론에 누구나 참여할 수 있어, 코드 작성자뿐 아니라 일반 참여자도 의견 제시만으로 프로토콜 발전에 기여할 수 있다


EIP는 이더리움의 탈중앙화 거버넌스를 실현하는 핵심 도구
코인 데이터업체 코인데스크는 “EIP는 이더리움 블록체인에서 업데이트와 결정이 내려지는 중심 방식”이라고 설명

**표준화(Standardization)** 
EIP는 토큰 규격, 컨트랙트 인터페이스 등 이더리움 구성 요소 간 호환성을 높이는 표준을 제정한다
예를 들어 EIP-20은 ERC-20 토큰 표준을 정의해 지갑·거래소 등에서 일관된 토큰 연동을 가능하게 함

**투명성과 기록성**
 모든 EIP 제안과 변경 사항은 문서화되어 공개적으로 기록됨 
 GitHub의 EIP 저장소와 공식 웹사이트에는 제안된 모든 EIP와 구현 내역이 보관되어 있다

**거버넌스 참여** 
EIP 시스템 덕분에 개발자, 노드 운영자, 사용자 등 다양한 이해관계자가 제안·토론 과정에 참여할 수 있고, 
단순히 의견을 제시하는 것만으로도 프로토콜 발전 방향에 영향을 줄 수 있음

## EIP의 주요 카테고리
EIP 표준 트랙(Standard Track)은 Core, Network, Interface, ERC, Meta, Informational의 6가지 유형으로 분류됨


`Core`	    프로토콜 수준의 주요 변경(합의 알고리즘, 거래 유효성 등). 네트워크 하드포크를 수반할 수 있어 모든 노드의 적용이 필요함  

`Network`   노드 간 통신 프로토콜(DevP2P) 관련 개선으로, 메시지 전파나 네트워킹 스택 변경을 다룸  

`Interface`	 클라이언트 API/RPC, ABI, 표준 라이브러리 등 인터페이스 개선입니다. 예를 들어 JSON-RPC 인터페이스 확장이나 
             새로운 스마트컨트랙트 ABI 규격 등이 포함됨

`ERC`	   응용(애플리케이션) 레벨 표준에 해당합니다. 주로 토큰(예: ERC-20), 계정 추상화, 이름 서비스 등 스마트컨트랙트 표준을 정의gka
           ERC(Ethereum Request for Comment) 제안은 모든 노드 적용을 요구하지 않음

`Meta`	   EIP 프로세스나 거버넌스 개선 제안입니다. 예를 들어 EIP 작성 규칙 수정, 의사결정 절차 변경 등이 해당

`Informational`  	정보 제공 목적의 문서로, 구현 의무는 없고 디자인 원칙, 활용 방법 등을 설명합니다. 네트워크에 직접적인 변경을 도입하지 않았음


## 작성 및 제출 절차

아이디어 구상 및 검토 => EIP 문서 작성 => GitHub에 제출 =>  편집자 리뷰 => 커뮤니티 피드백 => 최종 검토 => 확정(Final)


1. 개선 아이디어를 정리하고, 이더리움 매지션스(Ethereum Magicians) 포럼이나 개발자 채팅(예: Discord) 등에서 커뮤니티 의견을 수렴
2. EIP-1에 명시된 양식과 규칙을 따라 제안서를 작성 
   ethereum.org coindesk.com 제안서는 GitHub Markdown 형식으로, 제목·요약·기술 사양·동기(의도) 등을 포함해야 함
3. 이더리움의 공식 EIP 저장소(ethereum/EIPs)로 포크하여 새로운 EIP 파일(eip-*.md)을 생성하고 풀 리퀘스트(PR)를 제출 iq.wiki
   ethereum.org 풀 리퀘스트에는 제안 내용을 간략히 소개하는 설명을 함께 기재
4. EIP 편집자(EIP Editors)가 문서 형식과 기술 완전성을 검토
   ethereum.org  내용이 충실하면 편집자가 EIP 번호를 부여하고 저장소에 병합하여 초안(Draft) 단계로 전환
5. 초안 상태가 되면 최소 45일 이상 검토(Review) 기간을 거치며, 추가 논의와 의견 수렴이 진행됨 cyfrin.io  필요하면 제안 내용을 수정하여 반영
6. 편집자가 EIP를 마지막 검토(Last Call) 단계로 지정하고 (통상 14일간) 최종 피드백을 받음
   cyfrin.io  이 단계에서는 큰 수정이 예상되지 않으며, 추가 변경 시 다시 검토 단계로 돌아간다
7. 편집자가 제안을 Final 상태로 마감하면 더 이상 변경할 수 없으며, 네트워크 업그레이드 대상이 된다
   cyfrin.io 이후 AllCoreDevs 회의나 이더리움 매지션스 포럼 등에서 해당 EIP를 업그레이드에 포함할지 결정 cyfrin.io

 보류(Stagnant): 초안·검토·마지막 검토 단계에서 6개월 이상 활동이 없으면 ‘Stagnant’ 상태가 된다
                cyfrin.io 필요시 저자나 편집자가 다시 활성화할 수 있다
철회(Withdrawn): 저자가 제안을 포기하면 EIP는 영구적으로 ‘Withdrawn’으로 표시되며, 동일 번호는 재사용되지 않음
                cyfrin.io

모든 단계에서 EIP 편집자는 제안의 기술적 타당성과 형식을 검토하여 승인 여부를 조정하며  ethereum.org
최종적으로 커뮤니티 합의를 거쳐 제안을 발전시킨다


## 승인 프로세스 (리뷰·피드백·최종 승인 단계)
EIP는 제안 제출 이후 Draft → Review → Last Call → Final의 단계를 거쳐 채택 여부가 결정

Draft (초안): 편집자의 승인을 받아 EIP 저장소에 공식 등록된 상태  

Review (검토): 커뮤니티의 피드백을 반영하며 최소 45일 이상 심도 있게 논의  

Last Call (최종 검토): 추가 의견 수렴을 위한 마지막 단계(약 2주)로, 이 때 큰 수정 제안이 나오면 다시 Review 단계로 돌아감

Final (확정): 더 이상의 수정 없이 확정된 상태로, 향후 네트워크 업그레이드 후보가 된다
             이 단계 이후 코어 개발자 회의(AllCoreDevs)나 이더리움 매지션스 포럼에서 해당 EIP를 특정 업그레이드에 포함할지 최종 결정

이 과정에서 EIP 편집자는 제안 내용의 기술적·형식적 적합성을 검토하고 각 단계를 조정
또한 모든 이해관계자가 의견을 제시할 수 있는 공개 논의 과정을 통해 제안이 다듬어지며, 합의된 EIP만이 네트워크에 반영됨

**EIP-20**
EIP-20은 우리가 흔히 말하는 ERC-20 토큰 표준을 정의한 문서로,
이더리움 생태계에서 모든 토큰의 공통 언어 역할을 함

이더리움 기반 토큰들이 `일정한 규칙`을 따라 동작하게 만드는 인터페이스(표준)이다

ERC-20
Ethereum Request for Comment 20 → 토큰의 표준 인터페이스
EIP-20에 정의됨	     
USDT, LINK, UNI, AAVE 등

목적
다양한 토큰을 동일한 방식으로 다루기 위해
지갑, 거래소, 스마트 계약 호환성
MetaMask에서 토큰 자동 인식

필수 함수	
토큰 전송, 잔액 조회, 승인 및 위임 처리 등
transfer, approve, transferFrom 등

필수 이벤트	
Transfer, Approval
토큰 이동 및 승인 발생 시 알림
이벤트 로그 기반 추적 가능

상태 변수	
balances, allowances
내 계좌에 얼마 있는지, 누구한테 권한을 줬는지

**ERC-20 스마트 계약은 반드시 다음을 구현해야 함**

항목	                                    설명
name()	                             토큰 이름 (예: "USDT")
symbol()	                         심볼 (예: "USDT")
decimals()	                         소수점 자릿수 (보통 18)
totalSupply()	                     전체 발행량
balanceOf(addr)	                     해당 주소의 잔액
transfer(to, amount)	             내 지갑에서 다른 주소로 전송
approve(spender, amount)	         spender 주소에 위임 허용
transferFrom(from, to, amount)	     위임받은 spender가 대신 토큰을 전송
allowance(owner, spender)	         spender가 owner에게서 얼마까지 꺼낼 수 있는지 확인
Transfer (event)	                 토큰 이동 알림 이벤트
Approval (event)	                 위임 승인 알림 이벤트