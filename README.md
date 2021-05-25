# Ubuntu  서버에서의 모든 중국 IP 대역 차단 프로그램
<hr/>
Copyright 2019, Made By Misty; 한국인터넷진흥원 KUCIS
<hr/>


**아오! 짜증나!! 뭐야 이 중국 IP!!!!!**
**서버를 구축했는데, 이상한 로그가 계속 찍힌다구요?**
그런 당신을 위해 만들었습니다! cidr DB를 이용한 국가단위의 IP차단 프로그램!!!


## 1. Fox_CNFilter을 만든 계기
#### Ubuntu 서버 운영시에 중국이 출처인 모든 IP대역대를 자신의 서버에 접속하지 못하도록 차단하는 자동화 프로그램

```
Fox_CNFilter는 서버 운영시에 생기는 중국 해커들의 모든 접속을 차단해줍니다.
서버를 운영하면서, 중국에서 자신의 서버에 접속할 필요가 없다던가, 중국에서 시도한 해킹 공격에서 일부분 예방이 가능합니다.

자신의 서버에 중국 트래픽이 있는 것이 마음에 안들거나,
서비스중인 기능이 중국사람이 쓸 수 없거나 혹은 중국유저가 굳이 사용하지 않아도 되는 서비스이거나.
공격자의 주소가 중국이거나 하는 경우에, 중국의 모든 IP대역을 접속하지 못하게 차단하는 역활을 자동화 해줍니다.

```
<hr>


## 2. Fox_CNFilter를 사용하면 좋은 장점
```
1. 중국의 모든 IP를 명령어 하나로 차단할 수 있다.
2. 중국 트래픽을 차단할 수 있다.
3. CIDR DB만 변경해주면 다른 나라의 모든 IP대역 또한 차단할 수 있다.
```


## 3. 다음과 같이 실행할 수 있습니다!!
```
root# python FUCK_CN.py
```


## 4. 수정이 필요합니다!
```
따로 수정할 사안은 없습니다.
다만, cidr db를 새로이 받아서 사용할 경우에는 cidr_new 변수와 cidr_old 변수를 수정하셔야합니다!
기존에 쓰인 cidr db의 이름 형식은 (국가)_ipv4-(db를 받은 날짜)입니다.

새로운 cidr DB는 아래의 링크에서 다운로드 할 수 있습니다.
원하는 국가의 DB를 다운받아 코드를 수정하세요! 
https://www.ip2location.com/free/visitor-blocker
```

## 5. 업데이트
```
- 19.05.20
FUCK_CN 중국 ip차단 프로그램의 iptables 버전 개발\n
--> CentOS, Redhat, freebsd등, iptables 설치 가능한 대부분의 리눅스 운영체제에서 구동 가능

- 19.05.20
-->리파지토리 재구축 및 각 프로그램 분리
```

## 6. Requirement
```
- python 2.x
- ufw(기본)
- iptables(iptables versions 폴더에 있는 프로그램 실행시)
```

## 7. 단점
```
대부분 공격자들의 ip가 막히게 되면 다른 ip로 공격을 시도하는데, 
이 프로그램으로 차단한 국가가 아닌 다른 국가의 ip를 사용하여 공격을 시도하게 됨.
공격자인지 일반 사용자인지 구분하는 고도의 데이터 처리능력이 요구됨.
```
<hr/>
### 태그
중국 ip 차단
ip 차단
특정 국가 ip 차단
국가 ip 차단
ufw 차단 자동화
ufw 차단
ufw 특정 국가 차단
iptables 특정 국가 차단
