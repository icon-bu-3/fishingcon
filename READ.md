# README



## 랜덤제너레이션을 활용한 물고기 게임

### 설치
### git 사용법
sudo apt install git-all

git clone https://github.com/icon-bu-3/fishingcon
cd fisingcon

### ```Pycharm ```을 활용하여 모듈을 설치하시오 tbears
```
Pycharm setting-> project interperter -> '+' button click -> search tbears and install Package
```
### SCORE를 먼저 localhost에 배포하고 테스트 해 봅니다.
```
tbears start
tbears deploy ../fishingcon
```
### 배포를 성공하고 스코어주소를 확인합니다.
```
tbears txresult 010c364df5a2d9e536bce11d057585d0decbd2b791
```
### 스코어주소를 확인하고 잔액을 확인합니다
```
tbears balance cx0c364df5a2d9e536bce11d057585d0decbd2b791
```
### localhost에 fishingcon 을 배포 하고 game.js 와 app.py 스코어 주소를 변경합니다.
색칠한 부분을 본인의 스코어주소로 변경 
```
var address = getParameterByAddress("address");
var score_to = "cx0c364df5a2d9e536bce11d057585d0decbd2b791";

let current = '';
```
색칠한 부분을 본인의 스코어주소로 변경
```
# from time import sleep

#---------------------------------------Icon Service rink----------------------------------------
icon_service = IconService(HTTPProvider("http://127.0.0.1:9000/api/v3"))
_score_address = "cx0c364df5a2d9e536bce11d057585d0decbd2b791"
```
### 변경후에 게임을 하기위해선 스코어주소와 자신에 지갑이 ICX가 있어야하므로 100ICX를 로컬에서 보내시오.
tbears transfer cx0c364df5a2d9e536bce11d057585d0decbd2b791 100e18
tbears transfer hx8cfb20aae3e75e6dbfe016a73b38a6b31f3ed101 100e18

## ```Pychram ```을 활용하여 모듈을 설치하시오 flask
```
Pycharm setting-> project interperter -> '+' button click -> search flask and install Package
```
## app.py 실행 
```
#server/app.py
cd server
python app.py 
```

## 1. FishingCON 서비스
FishingCON 서비스는 임의 생성을 통해 게임 0, 1, 2를 만들었습니다. 생성 된 난수 및 생성자의 수는 3 가지 색상의 물고기에 대해 0, 1 및 2의 고유 한 값입니다. 사용자와 사수를 비교하고 생성 된 난수를 비교하십시오.
``` game_value = int.from_bytes(sha3_256(
self.msg.sender.to_bytes() + str(self.block.timestamp).encode()), "big") % 3 
if (game_value == _choice): 
Logger.warning("Win")
else:
Logger.warning("Loss")
```
## 2. FishingCON의 요구 사항 또는 플레이 방법
##1). 요구 사항
### 1.1) ICONex 월렛 필요로그인없이 사용할 수 없습니다.
### 1.2) ICX가 필요합니다.
게임을 시작한 후 선택한 물고기에게 ICX를 베팅하십시오. 잃을 때 2 배의 승수를 받고 0.8 %의 베팅 금액을 잃게됩니다.
## 2). FishingCON 게임하는 법
### 2.1) 지갑을 동기화하려면 메인 페이지에서 지갑 연결 버튼을 클릭하십시오.
### 2.2) 게임 시작 버튼을 클릭하면 물고기 선택 화면이 나타납니다.
### 2.3) 물고기를 선택한 후, ICONex 지갑 지갑 암호를 입력하고 보내십시오.
### 2.4) 로딩 화면이 표시되고 게임 결과 화면이 10 초 후에 표시됩니다.
### 2.5) 8 초간 결과 화면이 나오면 Home 버튼과 Rematch 버튼으로 화면을 출력합니다.
### 2.6) 홈 버튼을 클릭하면 메인 페이지로 이동합니다.
### 2.7) 재검색 버튼을 클릭하면 물고기 선택 화면이 다시 표시됩니다.
### 2.8) FishingCON 끝.

