# Medicine-Service - 약 복용 알리미
<br>
<p align="center"> <img src="https://user-images.githubusercontent.com/62025746/95682260-4bca4a00-0c1f-11eb-800a-84f91a25a2f6.png" width="600px"> </p>
<br><br><br>

**"약 먹는 시간을 자주 깜빡하거나, 복용하고 있는 약의 정보 및 효과를 보고 싶은 사람들을 위한 서비스"**

<br><br>
## 목차

  1. [프로젝트 목표](#프로젝트-목표)
  1. [프로젝트 핵심기능](#프로젝트-핵심기능)
  1. [개발환경](#개발환경)
  1. [기능구현](#기능구현)

  
<br><br>

## 프로젝트 목표

  <a name="프로젝트-목표--아날로그-방식-개선목적"></a><a name="1.1"></a>
  - [1.1](#프로젝트-목표--아날로그-방식-개선목적) **아날로그 방식 개선 목적 :** 식사시간을 기준으로 정하는 아날로그 방식에서 `복용알림 서비스로의 개선 목적.`
  
  <a name="프로젝트-목표--복용효과-100%받기"></a><a name="1.2"></a>
  - [1.2](#프로젝트-목표--복용효과-100%받기) **복용효과 100%받기 :** 약 동력의 기반하여 `최적의 재 복용 시간`을 알려 줌.
  
  <a name="프로젝트-목표--체내-약효능-시기-인지하기"></a><a name="1.3"></a>
  - [1.3](#프로젝트-목표--체내-약효능-시기-인지하기) **체내 약효능 시기 인지하기 :** 체내에 약의 효과가 작용하고 있는 것을 `시각적 그래프`로 알려 줌.
  
 <br><br> 
  
## 프로젝트 핵심기능

  <a name="프로젝트-핵심기능--약-정보-검색"></a><a name="2.1"></a>
  - [2.1](#프로젝트-핵심기능--약-정보-검색) **약 정보 검색** : 복용 중인 약의 기본 정보, 효능, 용법, 주의사항, 부작용 안내
  
  <a name="프로젝트-핵심기능--약-복용-그래프"></a><a name="2.2"></a>
  - [2.2](#프로젝트-핵심기능--약-복용-그래프) **약 복용 그래프** : 복용 주기에 맞춘 약 효능 그래프
  
  <a name="프로젝트-핵심기능--문자-발송"></a><a name="2.3"></a>
  - [2.3](#프로젝트-소개--문자-발송) **문자 발송** : 약 복용 주기를 등록하여 복용 시간에 맞춰 문자 메세지 전송
  
  <a name="프로젝트-핵심기능--약국-지도-API"></a><a name="2.4"></a>
  - [2.4](#프로젝트-소개--약국-지도-API) **약국 지도 API** : 전국 약국위치를 파악 할 수 있는 지도
  
  <br><br>
  
## 개발환경

* 언어
  * JAVA SE1.8 `JDK 8`
  * HTML5/CSS3
  * JavaScript
  <br>
* 프레임 워크
  * Jquery
  * node.js `v12.0`
  <br>  
* 서버(WAS)
  * Apache Tomcat `v8.0`
  <br>
* 개발도구
  * Eclipse-JEE-Mars-2
  * MySQL WorkBench 
  <br>
* 커뮤니티
  * Github
  
  <br><br>
  
## DATABASE

<br>
<img src="https://user-images.githubusercontent.com/62025746/95739084-39a2e700-0cc5-11eb-9577-6fb907f23a17.png" width="600px">
<br><br>

## 기능구현 
* [검색 기능](#검색-기능)
* [복용 그래프](#복용-그래프)
* [전국 약국 지도](#전국-약국-지도)
* [실시간 채팅 상담](#실시간-채팅-상담)
<br><br>


### 검색 기능
<br>

  <a name="기능구현--검색-기능--1."></a><a name="4.1"></a>
  - [4.1](#기능구현--검색-기능--1.) 공공데이터 에서 약 `53000개`의 약 정보를 파싱하여 DB에 저장함.
  
  <br>
  
  <br> 
  
 <img src="https://user-images.githubusercontent.com/62025746/96236326-dff93000-0fd6-11eb-8dae-3d63a0ae12c4.png" width="600px">
  
  <br>
  
  <a name="기능구현--검색-기능--2"></a><a name="4.2"></a>
  - [4.2](#기능구현--검색-기능--2)  공공데이터 에서  `48개`의 약 부작용 정보를 파싱하여 DB에 저장함.
  
  <br>
  
  <img src="https://user-images.githubusercontent.com/62025746/96236465-09b25700-0fd7-11eb-9d03-f46f0f31beed.png" width="600px">
  
  <br>
	
	
  <a name="기능구현--검색-기능--3"></a><a name="4.3"></a>
  - [4.3](#기능구현--검색-기능--3) Jquery의 AutoComplete 기능을 이용하여 검색 시 `자동완성` 기능을 추가함.
  
  
   <br> 
  
 <img src="https://user-images.githubusercontent.com/62025746/96236828-7decfa80-0fd7-11eb-8f03-fcb553015e1c.png" width="600px">
  
  <br>
  
  

<hr>
<br>




### 복용 그래프
<br>


 <a name="기능구현--복용-그래프--1."></a><a name="4.4"></a>
  - [4.4](#기능구현--복용-그래프--1.) 임의로 만든 약 동력 그래프를 시간에 따라 그리게 되고, 복용주기가 끝나면 그래프는 멈추도록 설계함.
  
  
  <a name="기능구현--복용-그래프--2."></a><a name="4.5"></a>
  - [4.5](#기능구현--복용-그래프--2.) 약의 효과가 발현하는 40% 지점부터 (임의로 지정) 약 효과가 발현하고 있다는 신호를 주기위해 `gif 이미지를 띄워 표시함.`
  
 
  
  <br>
  
 <img src="https://user-images.githubusercontent.com/62025746/96237136-e3d98200-0fd7-11eb-8318-57ceafa54f92.gif" width="600px">
  
  <br>
  
  
  <a name="기능구현--복용-그래프--3."></a><a name="4.6"></a>
  - [4.6](#기능구현--복용-그래프--3.) 입력한 재복용 주기만큼 시간이 지나면 사용자의 휴대전화로 `재복용 알람 문자 메세지를 전송함.`
  
  
   <br> 
  
 <img src="https://user-images.githubusercontent.com/62025746/96237280-15524d80-0fd8-11eb-9083-1b3b520caacf.png" width="600px"> 
  
  <br>

<hr>

<br>

### 전국 약국 지도
<br>

 <a name="기능구현--전국-약국-지도--1."></a><a name="4.7"></a>
  - [4.7](#기능구현--검색-기능--1.) 공공데이터에서 약 `22000개`의 전국 약국정보를 파싱하고 `XML`에서 `JSON`으로 바꾼 뒤, ndate.js파일에 넣음.
  
  <br><br>
  


<br>
  
   <a name="기능구현--전국-약국-지도--2."></a><a name="4.8"></a>
  - [4.8](#기능구현--검색-기능--2.) 해당 약국의 위치를 표시하기 위해서` Marker` 기능을 사용하였고, 해당 마커의 정보를 표기하기 위해 `InfoWindow` 기능을 사용함.

   
  <br> 
  
 <img src="https://user-images.githubusercontent.com/62025746/96237865-c2c56100-0fd8-11eb-8102-5ff8c326eacb.png" width="600px"> 
  
  <br>
  
  
   
  <br>
  
   <a name="기능구현--전국-약국-지도--3."></a><a name="4.9"></a>
  - [4.9](#기능구현--검색-기능--3.) Marker가 한 곳에 밀집되어 있을 때, 밀집된 Marker의 수를 표시하기 위해서 `Clusterer` 기능을 구현함.
  
  <br>
 
  <img src="https://user-images.githubusercontent.com/62025746/96238011-f1433c00-0fd8-11eb-9032-756ba7abc77a.png" width="600px">
  
  <br>
  
  <hr>

### 실시간 채팅
<br>

 <a name="기능구현--실시간-채팅--1."></a><a name="4.10"></a>
  - [4.10](#기능구현--실시간-채팅--1.) Admin으로 접속 했을 때에는 관리자 채팅 표시가 나타나게 하고, 일반 유저일 경우 실시간 상담 로고만 나타나도록 설정함.
  
   <a name="기능구현--실시간-채팅--2."></a><a name="4.11"></a>
  - [4.11](#기능구현--실시간-채팅--2.) 관리자 채팅으로 접속 시, 일반 유저들이 작성 한 채팅창이 뜨게 작성하였고 `실시간 채팅`이 가능하도록 구현함.
  
  <a name="기능구현--실시간-채팅--3."></a><a name="4.12"></a>
  - [4.12](#기능구현--실시간-채팅--3.) 일반 유저가 실시간 상담을 종료하면 관리자 채팅에서의 `채팅방도 사라지게 구현함.`
  

 <br> 
  
<img src="https://user-images.githubusercontent.com/62025746/96238150-22237100-0fd9-11eb-91c7-2b57e63149b8.png" width="600px">
  
  <br>


```

