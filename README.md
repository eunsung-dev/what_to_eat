# 슬기로운 의무경찰 생활👮‍♀️(a.k.a. 슬의생)
Development Environment

<img src="https://img.shields.io/badge/Swift-5.0-ff69b4?style=flat"/> <img src="https://img.shields.io/badge/Xcode-13.2.1-yellow?style=flat"/> <img src="https://img.shields.io/badge/iOS-15.2-blue?style=flat"/>
## Background
> 운전병 후임: 최은성님, 오늘은 뭐 드시겠습니까?<br>
> 나: 음.. OOO 식당에서 먹을까?<br>
> 운전병 후임: OOO 식당은 최근에 먹어서 질립니다.😱<br>
> 나: 그럼 거기 말고 다른 괜찮은 곳 없으려나...(좋은 생각 없을까?🤔)

의무경찰로 군 복무를 했던 나는 광화문, 여의도 등 도심 속에서 주로 식사를 하였다.<br>
밖에서 식사를 한다는 것은 부대 내에서 먹는 것보다는 아무래도 맛있지만 아무 식당이나 갈 수 있는 게 아니라 의무경찰 식대가 6,000원이기 때문에 이 가격으로 먹을 수 있는 식당을 찾아야 하는 어려움이 있었다.<br>
이렇게 군 생활 동안 불편함을 느낀 나는 굳이 식당마다 일일이 전화로 식대를 맞춰줄 수 있는지 묻지 않고 식대를 맞춰주는 식당을 한눈에 볼 수 있는 앱을 만들면 좋지 않을까라는 생각을 해서 NAVER Map iOS SDK를 활용한 앱을 만들게 되었다.

## Getting started
NAVER Map iOS SDK를 사용하기 위해 기본적인 세팅은 아래를 참고한다.<br>
https://navermaps.github.io/ios-map-sdk/guide-ko/1.html

그리고 현재 위치를 가져오기 위해 ```info.plist```에 아래와 같이 추가한다.
```swift
<key>NSLocationWhenInUseUsageDescription</key>
<string>내 위치 확인을 위해 권한이 필요합니다.</string>
<key>NSLocationAlwaysAndWhenInUseUsageDescription</key>
<string>내 위치 확인을 위해 권한이 필요합니다.</string>
```
마지막으로 네이버 지도 URL Scheme을 사용하기 위해 ```info.plist```에 아래와 같이 추가한다.
```swift
<key>LSApplicationQueriesSchemes</key>
<array>
	<string>nmap</string>
</array>
```
## Features
#### ✔️ 마커 클릭 시, 현재 위치로부터 해당 위치까지 길찾기 기능
![resource1](https://user-images.githubusercontent.com/39147372/148570283-bd58864d-6f35-4ef4-af0f-7775022e8225.gif)

#### ✔️ 식당 검색 기능
![resource2](https://user-images.githubusercontent.com/39147372/148570411-7fcabe55-64f9-4343-b652-31ac28a78876.gif)

#### ✔️ 쉬운 데이터 추가
```TotalString```에 아래와 같이 추가하면 해당 마커가 생긴다. 식당을 검색한 구글 지도 url에서 ```http://``` 또는 ```https://```를 제외해야 한다.<br>
```swift
Address(str: "www.google.co.kr/maps/place/남산왕돈까스/@37.5646729,126.9838466,17z/data=!4m8!1m2!2m1!1z7KSR6rWt64yA7IKs6rSAIOuCqOyCsOyZleuPiOq5jOyKpA!3m4!1s0x357ca2ee2b660ea7:0xf995a84313ac1eea!8m2!3d37.5646729!4d126.9838466?hl=ko")
```
<image src="https://user-images.githubusercontent.com/39147372/148570779-59a0f9c5-9dc1-451d-94e6-4268360c4db5.PNG" width="300" height="650">
