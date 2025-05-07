## ERC-20
ERC-20은 이더리움 블록체인에서 대체 가능한 토큰(Fungible Token)을 생성하고 관리하기 위한 표준
이는 토큰의 전송, 잔액 조회, 승인 등의 기능을 정의하여, 다양한 애플리케이션과의 상호 운용성을 보장

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

**ERC-20 필수함수와 그외함수**

                                    
name()	                                                    토큰 이름 (예: "USDT")
symbol()	                                                심볼 (예: "USDT")
decimals()	                                                소수점 자릿수 (보통 18)
totalSupply()	                                            전체 토큰의 발행량 반환
balanceOf(addr)	                                            특정 주소의 토큰 잔액 반환
transfer(to, address recipient, uint256 amount)             호출자의 토큰을 수신자에게 전송
approve(spender, amount)	                                특정 주소가 호출자의 토큰을 일정량 사용할 수 있도록 승인(위임)
transferFrom(from, to, amount)	                            승인된 주소가 보낸 사람의 토큰을 수신자에게 전송
allowance(owner, spender)	                                spender가 owner에게서 얼마까지 꺼낼 수 있는지 확인(잔여한도)
Transfer (event)	                                        토큰 이동 알림 이벤트
Approval (event)	                                        위임 승인 알림 이벤트

# 흐름

직접 전송: transfer() 함수를 사용하여, 호출자가 자신의 토큰을 직접 다른 주소로 전송

위임 전송:

승인 단계: approve() 함수를 사용하여, 특정 주소가 자신의 토큰을 일정량 사용할 수 있도록 승인

전송 단계: 승인된 주소가 transferFrom() 함수를 사용하여, 보낸 사람의 토큰을 수신자에게 전송

이러한 구조는 탈중앙화 거래소(DEX)나 자동화된 결제 시스템에서 유용하게 사용됨