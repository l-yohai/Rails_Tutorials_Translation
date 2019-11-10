# Ruby on Rails Tutorial：실제 예를 통해 배워보자.

<div style="text-align:right">원작자 Michael Hartl (마이클 허틀)</div>
※본 자료는 Ruby on Rails Tutorial의 원본과 일어판을 번역한 것으로, 개인적인 공부를 위해 번역을 한 것입니다.

 - 원 본 [Learn Web Development with Rails: Michael Hartl’s Ruby on Rails Tutorial |  Softcover.io](https://www.railstutorial.org/)
- 일어판  [https://railstutorial.jp/](https://railstutorial.jp/) 

---

본 튜토리얼에 대한 과제물의 레포지토리는 아래에 링크를 해놓습니다.

또한 본 튜토리얼에서는 AWS C9을 이용한 개발을 추천하고 있으나, 본인은 로컬환경에서 [RubyMine](https://www.jetbrains.com/ruby/)을 설치하여 진행하였습니다.

- 1장의 결과물 [Repository](https://github.com/Yoodahun/HelloWorldRubyMine)
- 2장의 결과물 [Repository](https://github.com/Yoodahun/ToyApplication_RailsTutorial)
- 3장 이후의 결과물 Sample Application [Repository](https://github.com/Yoodahun/sample_application)





---

## Rails Tutorial이란 ??

Rails Tutorial은, 실제 Web Application의 개발에서 공개까지, 실제로 개발해가며 배워보는 대형 튜토리얼입니다.📕✨ 

~~Rails Tutorial은, 원작자 Michael Hartl로 부터 정당한 허가를 받아 번역, 공개, 판매하고 있습니다. 원작과 마찬가지로 온라인판은 무료로 공개하고 있습니다. 본 튜토리얼이 여러분의 학습에 도움이 되었으면 좋겠습니다.~~

**※본서는 개인적인 학습을 위해 번역한 것입니다.**

- - - -
- [ ] 제 4판 목차
	- [ ] 추천의 말씀 (생략)
	- [ ] 감사의 말씀 (생략)
	- [x] [저자](Documentation/auther.md)
	- [x] [저작권과 라이센스](Documentation/license.md)
	- [x] [제 1장 제로부터 배포까지](Documentation/Chapter1.md)
		- [x] 1.1 [처음에는](Documentation/Chapter1.md#11-처음에는) 
			- [ ] 1.1.1 [전제 조건](Documentation/Chapter1.md#111-전제-조건)
			- [ ] 1.1.2 [본 튜토리얼에서의 약속](Documentation/Chapter1.md#112-본-튜토리얼에서의-약속)
		- [x] 1.2 [일단 구동시켜보자](Documentation/Chapter1.md#12-일단-구동시켜보자)
			- [ ] 1.2.1 [개발 환경](Documentation/Chapter1.md#121-개발-환경)
			- [ ] 1.2.2 [Rails를 설치해보자.](Documentation/Chapter1.md#122-Rails를-설치해보자.)
		- [x] 1.3 [첫 Application](Documentation/Chapter1.md#13-첫-Application)
			- [ ] 1.3.1 [Bundler](Documentation/Chapter1.md#131-bundler)
			- [ ] 1.3.2 [rails server](Documentation/Chapter1.md#132-rails-server)
			- [ ] 1.3.3 [Model-View-Controller (MVC)](Documentation/Chapter1.md#133-model—view—controller-(mvc))
			- [ ] 1.3.4 [Hello, world!](Documentation/Chapter1.md#134-hello,-world!)
		- [x] 1.4 [Git을 이용한 버전 관리](Documentation/Chapter1.md#14-git을-이용한-버전-관리)
			- [ ] 1.4.1 [설치](Documentation/Chapter1.md#141-설치)
			- [ ] 1.4.2 [Git을 쓰면 좋은 점](Documentation/Chapter1.md#142-git을-쓰면-좋은-점)
			- [ ] 1.4.3 [Bitbucket](Documentation/Chapter1.md#143-bitbucket)
			- [ ] 1.4.4 [Branch, Edit, Commit, Merge](Documentation/Chapter1.md#144-branch,-edit,-commit,-merge)
		- [x] 1.5 [배포해보자](Documentation/Chapter1.md#15-배포해보자)
			- [ ] 1.5.1 [Heroku 설치](Documentation/Chapter1.md#151-heroku의-설치)
			- [ ] 1.5.2 [Heroku에 배포해보자 (1)](Documentation/Chapter1.md#152-heroku에-배포해보자-(1))
			- [ ] 1.5.3 [Heroku에 배포해보자 (2)](Documentation/Chapter1.md#153-heroku에-배포해보자-(2))
			- [ ] 1.5.4 [Heroku 명령어](Documentation/Chapter1.md#154-heroku-명령어)
		- [x] 1.6 [마지막으로](Documentation/Chapter1.md#16-마지막으로)
			- [ ] 1.6.1 [1장의 정리](Documentation/Chapter1.md#161-1장의-정리)
	- [x] [제 2장 Toy Application](Documentation/Chapter2.md)
		- [x] 2.1 [Application의 설계](Documentation/Chapter2.md#21-어플리케이션의-계획)
			- [ ] 2.1.1 [User Modeling](Documentation/Chapter2.md#211-user-modeling)
			- [ ] 2.1.2 [Micropost Modeling](Documentation/Chapter2.md#212-micropost-modeling)
		- [x] 2.2 [Users 리소스](Documentation/Chapter2.md#22-user-리소스)
			- [ ] 2.2.1 [Users 화면을 움직여보자](Documentation/Chapter2.md#221-users-화면을-움직여보자)
			- [ ] 2.2.2 [MVC의 처리](Documentation/Chapter2.md#222-mvc의-처리)
			- [ ] 2.2.3 [Users 자원의 결점](Documentation/Chapter2.md#223-users-자원의-결점)
		- [x] 2.3 [Microposts 리소스](Documentation/Chapter2.md#23-microposts-리소스)
			- [ ] 2.3.1 [Microposts 화면을 움직여보자](Documentation/Chapter2.md#231-microposts-화면을-움직여보자)
			- [ ] 2.3.2 [Microposts를 micro하게 해보자](Documentation/Chapter2.md#232-microposts를-micro하게-해보자)
			- [ ] 2.3.3 [유저는 많은 Microposts를 가지고 있다.](Documentation/Chapter2.md#233-유저는-많은-microposts를-가지고-있다.)
			- [ ] 2.3.4 [상속의 계층](Documentation/Chapter2.md#234-상속의-계층)
			- [ ] 2.3.5 [어플리케이션을 배포하자](Documentation/Chapter2.md#235-어플리케이션을-배포하자)
		- [x] 2.4 [마지막으로](Documentation/Chapter2.md#24-마지막으로)
			- [ ] 2.4.1 [2장의 정리](Documentation/Chapter2.md#241-2장의-정리)
	- [x] [제 3장 정적인(Static) 페이지의 작성](Documentation/Chapter3.md)
		- [x] [3.1 프로젝트 생성](Documentation/Chapter3.md#31-프로젝트-생성)
		- [x] [3.2 정적인 페이지](Documentation/Chapter3.md#32-정적인-페이지)
			- [ ] [3.2.1 Static Page를 생성해보자](Documentation/Chapter3.md#321-Static-Page를-생성해보자)
			- [ ] [3.2.2 Static Page를 편집해보자](Documentation/Chapter3.md#321-Static-Page를-편집해보자)
		- [x] [3.3 테스트를 해보자](Documentation/Chapter3.md#33-테스트를-해보자)
			- [ ] [3.3.1 첫 번째 테스트](Documentation/Chapter3.md#331-첫-번째-테스트)
			- [ ] [3.3.2 Red](Documentation/Chapter3.md#322-Red)
			- [ ] [3.3.3 Green](Documentation/Chapter3.md#333-Green)
			- [ ] [3.3.4 Refactor](Documentation/Chapter3.md#334-Refactor)
		- [x] [3.4 조금은 Dynamic한 페이지](Documentation/Chapter3.md#34-조금은-Dynamic한-페이지)
			- [ ] [3.4.1 타이틀을 테스트해보자 (Red)](Documentation/Chapter3.md#341-타이틀을-테스트해보자-(Red))
			- [ ] [3.4.2 타이틀을 추가해보자 (Green)](Documentation/Chapter3.md#342-타이틀을-추가해보자-(Green))
			- [ ] [3.4.3 레이아웃과 html에 직접 쓰는 Ruby (Refactor)](Documentation/Chapter3.md#343-레이아웃과-html에-직접-쓰는-Ruby-(Refactor))
			- [ ] [3.4.4 Route의 설정](Documentation/Chapter3.md#344-Route의-설정)
		- [x] [3.5 마지막으로](Documentation/Chapter3.md#35-마지막으로)
			- [ ] [3.5.1 3장의 정리](Documentation/Chapter3.md#351-3장의-정리)
		- [x] [3.6 조금 난이도가 있는 환경설정](Documentation/Chapter3.md#36-조금-난이도가-있는-환경설정)
		   - [ ] [3.6.1 minitest reporters](Documentation/Chapter3.md#361-minitest-reporters)
		  - [ ] [3.6.2 Guard를 이용한 테스트 자동화](Documentation/Chapter3.md#362-Guard를-이용한-테스트-자동화)
	- [x] [제 4장 Rails의 향기가 나는 Ruby](Documentation/Chapter4.md)
		- [ ] [4.1 작성 동기](Documentation/Chapter4.md#41-작성동기)
			- [ ] [4.1.1 Helper](Documentation/Chapter4.md#411-Helper)
			- [ ] [4.1.2 Custom Helper](Documentation/Chapter4.md#412-Custom-Helper)
		- [x] [4.2 문자열과 메소드](Documentation/Chapter4.md#42-문자열과-메소드)
			- [ ] [4.2.1 코멘트](Documentation/Chapter4.md#421-코멘트)
			- [ ] [4.2.2 문자열 ](Documentation/Chapter4.md#422-문자열)
			- [ ] [4.2.3 오브젝트와 메세지 송수신](Documentation/Chapter4.md#423-오브젝트와-메세지의-송수신)
			- [ ] [4.2.4 Method의 정의](Documentation/Chapter4.md#424-Method의-정의)
			- [ ] [4.2.5 다시 Title Helper](Documentation/Chapter4.md#425-다시-한-번-Title-Helper)
		- [x] [4.3 다른 데이터 구조](Documentation/Chapter4.md#43-다른-데이터-구조)
			- [ ] [4.3.1 배열과 범위 연산자](Documentation/Chapter4.md#431-배열과-범위연산자)
			- [ ] [4.3.2 블록](Documentation/Chapter4.md#432-블록)
			- [ ] [4.3.3 Hash와 Symbol](Documentation/Chapter4.md#433-Hash와-Symbol)
			- [ ] [4.3.4 다시 한 번 CSS](Documentation/Chapter4.md#434-다시-한-번-CSS)
		- [x] [4.4 Ruby에서의 Class](Documentation/Chapter4.md#44-Ruby에서의-Class)
			- [ ] [4.4.1 Constructor](Documentation/Chapter4.md#441-Constructor)
			- [ ] [4.4.2 Class의 상속](Documentation/Chapter4.md#442-Class의-상속)
			- [ ] [4.4.3 기본 Class의 변경](Documentation/Chapter4.md#433-기본-Class의-변경)
			- [ ] [4.4.4 Controller Class](Documentation/Chapter4.md#444-Controller-Class)
			- [ ] [4.4.5 User Class](Documentation/Chapter4.md#445-User-Class)
		- [x] [4.5 마지막으로](Documentation/Chapter4.md#45-마지막으로)
			- [ ] [4.5.1 4장의 정리](Documentation/Chapter4.md#451-4장의-정리)
	- [x] [제 5장 레이아웃의 작성](Documentation/Chapter5.md)
		- [x] [5.1 구조를 추가해보자](Documentation/Chapter5.md#51-구조를-추가해보자)
			- [ ] [5.1.1 Navigation](Documentation/Chapter5.md#511-Navigation)
			- [ ] [5.1.2 Bootstrap과 커스텀 CSS](Documentation/Chapter5.md#512-Bootstrap과-커스텀-CSS)
			- [ ] [5.1.3 파셜(Partial)](Documentation/Chapter5.md#513-파셜Partial)
		- [x] [5.2 Sass와 Asset Pipeline](Documentation/Chapter5.md#52-Sass와-Asset-Pipeline)
			- [ ] [5.2.1 Asset Pipeline](Documentation/Chapter5.md#521-Asset-Pipeline)
			- [ ] [5.2.2 멋진 문법과 준비된 스타일 시트](Documentation/Chapter5.md#522-멋진-문법과-준비된-스타일-시트)
		- [x] [5.3 레이아웃의 링크](Documentation/Chapter5.md#53-레이아웃의-링크)
			- [ ] [5.3.1 Contact 페이지](Documentation/Chapter5.md#531-Contact-페이지)
			- [ ] [5.3.2 Rails의 Route URL](Documentation/Chapter5.md#532-Rails의-Route-URL)
			- [ ] [5.3.3 이름이 붙은 Path](Documentation/Chapter5.md#533-이름이-붙은-Path)
			- [ ] [5.3.4 링크의 테스트](Documentation/Chapter5.md#534-링크의-테스트)
		- [x] [5.4 User의 등록 : 첫 테스트](Documentation/Chapter5.md#54-User의-등록-첫-테스트)
			- [ ] [5.4.1 Users Controller](Documentation/Chapter5.md#541-Users-Controller)
			- [ ] [5.4.2 Users 등록용 URL](Documentation/Chapter5.md#542-User-등록용-URL)
		- [x] [5.5 마지막으로](Documentation/Chapter5.md#55-마지막으로)
			- [ ] [5.5.1 5장의 정리](Documentation/Chapter5.md#551-5장의-정리)
	- [x] [제 6장 유저의 모델을 작성해보자](Documentation/Chapter6.md)
		- [x] [6.1 User 모델](Documentation/Chapter6.md/#61-User-모델)
			- [ ] [6.1.1 Database](Documentation/Chapter6.md#611-Database)
			- [ ] [6.1.2 Model 파일](Documentation/Chapter6.md#612-Model-파일)
			- [ ] [6.1.3 User Object를 생성해보자](Documentation/Chapter6.md#613-User-Object를-생성해보자)
			- [ ] [6.1.4 User Object를 검색해보자](Documentation/Chapter6.md#614-User-Object를-검색해보자)
			- [ ] [6.1.5 User Object를 수정해보자](Documentation/Chapter6.md#615-User-Object를-수정해보자)
		- [x] [6.2 User를 검증해보자](Documentation/Chapter6.md#62-User를-검증해보자)
			- [ ] [6.2.1 유효성을 검증해보자](Documentation/Chapter6.md#621-유효성을-검증해보자)
			- [ ] [6.2.2 존재성을 검증해보자](Documentation/Chapter6.md#622-존재성을-검증해보자)
			- [ ] [6.2.3 길이를 검증해보자](Documentation/Chapter6.md#623-길이를-검증해보자)
			- [ ] [6.2.4 포맷을 검증해보자](Documentation/Chapter6.md#624-포맷을-검증해보자)
			- [ ] [6.2.5 유니크성을 검증해보자](Documentation/Chapter6.md#625-유니크성을-검증해보자)
		- [x] [6.3 안전한 비밀번호를 추가해보자](Documentation/Chapter6.md#63-안전한-비밀번호를-추가해보자)
			- [ ] [6.3.1 해시화된 비밀번호](Documentation/Chapter6.md#631-해시화된-비밀번호)
			- [ ] [6.3.2 유저가 안전한 비밀번호를 가지고 있는지?](Documentation/Chapter6.md#632-유저가-안전한-비밀번호를-가지고-있는지)
			- [ ] [6.3.3 비밀번호의 최소문자수](Documentation/Chapter6.md#633-비밀번호의-최소문자수)
			- [ ] [6.3.4 유저 생성과 인증](Documentation/Chapter6.md#634-유저-생성과-인증)
		- [x] [6.4  마지막으로](Documentation/Chapter6.md#64-마지막으로)
			- [ ] [6.4.1 6장의 정리](Documentation/Chapter6.md#641-6장의-정리)
	- [x] [제 7장 유저의 등록](Documentation/Chapter7.md)
		- [x] [7.1 유저를 표시해보자](Documentation/Chapter7.md#71-유저를-표시해보자)
			- [ ] [7.1.1 Debug와 Rails 환경](Documentation/Chapter7.md#711-Debug와-Rails-환경)
			- [ ] [7.1.2 Users Resource](Documentation/Chapter7.md#712-Users-Resource)
			- [ ] [7.1.3 Debugger 메소드](Documentation/Chapter7.md#713-Debugger-메소드)
			- [ ] [7.1.4 Gravatar 이미지와 사이드바](Documentation/Chapter7.md#714-Gravatar-이미지와-사이드바)
		- [x] [7.2 유저 등록 Form](Documentation/Chapter7.md#72-유저-등록-Form)
			- [ ] [7.2.1 Form_for를 사용해보자](Documentation/Chapter7.md#721-Form_for를-사용해보자)
			- [ ] [7.2.2 Form HTML](Documentation/Chapter7.md#722-Form-HTML)
		- [x] [7.3 유저 등록 실패](Documentation/Chapter7.md#73-유저-등록-실패)
		  - [ ] [7.3.1 올바른 Form](Documentation/Chapter7.md#731-올바른-Form)
		  - [ ] [7.3.2 Strong Parameters](Documentation/Chapter7.md#732-Strong-Parameters)
		  - [ ] [7.3.3 에러 메세지](Documentation/Chapter7.md#733-에러-메세지)
		  - [ ] [7.3.4 등록 실패시의 테스트](Documentation/Chapter7.md#734-등록-실패시의-테스트)
		
		- [x] [7.4 유저 등록 성공](Documentation/Chapter7.md#74-유저-등록-성공)
		  - [ ] [7.4.1 등록 Form의 완성](Documentation/Chapter7.md#741-등록-Form의-완성)
		  - [ ] [7.4.2 flash](Documentation/Chapter7.md#742-flash)
		  - [ ] [7.4.3 실제 유저 등록](Documentation/Chapter7.md#743-실제-유저-등록)
		  - [ ] [7.4.4 유저 등록 성공시의 테스트](Documentation/Chapter7.md#744-유저-등록-성공시의-테스트)
		- [x] [7.5 프로의 배포](Documentation/Chapter7.md#75-프로의-배포)
		  - [ ] [7.5.1 실제 배포환경에서의 SSL](Documentation/Chapter7.md#751-실제-배포환경에서의-SSL)
		  - [ ] [7.5.2 실제 배포환경용의 Web서버](Documentation/Chapter7.md#752-실제-배포환경용의-Web서버)
		  - [ ] [7.5.3 실제 배포환경으로의 배포](Documentation/Chapter7.md#753-실제-배포환경으로의-배포)
		- [x] [7.6 마지막으로](Documentation/Chapter7.md#76-마지막으로)
		  - [ ] [7.6.1 7장의 정리](Documentation/Chapter7.md#761-7장의-정리)
		
	- [x] [제 8장 기본적인 로그인 기능](Documentation/Chapter8.md#제-8장-기본적인-로그인-기능)
		- [x] [8.1 Session](Documentation/Chapter8.md#81-Session)
			- [ ] [8.1.1 Sessions Controller](Documentation/Chapter8.md#811-Sesssions-Controller)
			- [ ] [8.1.2 Login Form](Documentation/Chapter8.md#812-Login-Form)
			- [ ] [8.1.3 유저의 검증과 인증](Documentation/Chapter8.md#813-유저의-검증과-인증)
			- [ ] [8.1.4 Flash Message를 표시해보자](Documentation/Chapter8.md#814-Flash-Message를-표시해보자)
			- [ ] [8.1.5 Flash의 테스트](Documentation/Chapter8.md#815-Flash의-테스트)
		- [x] [8.2 Login](Documentation/Chapter8.md#82-Login)
			- [ ] [8.2.1 Log_in Method](Documentation/Chapter8.md#821-Log_in-Method)
			- [ ] [8.2.2 로그인 되어있는 유저](Documentation/Chapter8.md#822-로그인-되어있는-유저)
			- [ ] [8.2.3 레이아웃 링크를 변경해보자](Documentation/Chapter8.md#823-레이아웃-링크를-변경해보자)
			- [ ] [8.2.4 레이아웃의 변경을 테스트해보자](Documentation/Chapter8.md#824-레이아웃의-변경을-테스트해보자)
			- [ ] [8.2.5 회원가입 후의 로그인](Documentation/Chapter8.md#825-회원가입-후의-로그인)
		- [x] [8.3 Logout](Documentation/Chapter8.md#83-Logout)
		- [x] [8.4 마지막으로](Documentation/Chapter8.md#84-마지막으로)
			- [ ] [8.4.1 8장의 정리](Documentation/Chapter8.md#841-8장의-정리)
	- [x] [제 9장 진보된 로그인 구조](Documentation/Chapter9.md)
		- [x] [9.1 Remember me 기능](Documentation/Chapter9.md#91-remember-me-기능)
			- [ ] [9.1.1 Remember Token과 암호화](Documentation/Chapter9.md#911-remember-token과-암호화)
			- [ ] [9.1.2 로그인 상태의 저장](Documentation/Chapter9.md#912-로그인-상태의-저장)
			- [ ] [9.1.3 유저 정보 파기](Documentation/Chapter9.md#913-유저-정보-파기)
			- [ ] [9.1.4 2개의 눈에 띄지않는 버그](Documentation/Chapter9.md#914-2개의-눈에-띄지않는-버그)
		- [x] [9.2 「Remember me」  Checkbox](Documentation/Chapter9.md#92-remember-me-체크박스)
		- [x] [9.3 「Remember me」 의 테스트](Documentation/Chapter9.md#93-remember-me-의-테스트)
			- [ ] [9.3.1 「Remember me」 박스를 테스트해보자](Documentation/Chapter9.md#931-remember-me-박스를-테스트해보자)
			- [ ] [9.3.2 「Remember me」 를 테스트해보자](Documentation/Chapter9.md#932-remember-me-를-테스트해보자)
		- [x] [9.4 마지막으로](Documentation/Chapter9.md#94-마지막으로)
			- [ ] [9.4.1 9장의 정리](Documentation/Chapter9.md#941-9장의-정리)
	- [ ] 제 10장 유저의 업데이트, 출력, 삭제
		- [ ] 10.1 유저를 업데이트해보자.
			- [ ] 10.1.1 Update Form
			- [ ] 10.1.2 Update의 실패
			- [ ] 10.1.3 Update에 실패했을 때의 테스트
			- [ ] 10.1.4 TDD로 편집을 성공시켜보자
		- [ ] 10.2 허가
			- [ ] 10.2.1 유저에게 로그인을 요구해보자 
			- [ ] 10.2.2 올바른 유저로 로그인을 요구해보자
			- [ ] 10.2.3 Friendly Forwarding
		- [ ] 10.3 모든 유저를 표시해보자
			- [ ] 10.3.1 유저 리스트를 표시해보자
			- [ ] 10.3.2 Sample User
			- [ ] 10.3.3 Pagination
			- [ ] 10.3.4 유저 리스트의 테스트
			- [ ] 10.3.5 Partial Refactoring
		- [ ] 10.4 유저를 삭제해보자
			- [ ] 10.4.1 관리자
			- [ ] 10.4.2 Destroy Action
			- [ ] 10.4.3 유저 삭제 테스트
		- [ ] 10.5 마지막으로
			- [ ] 10.5.1 10장의 정리
	- [ ] 제 11장 Account의 유효화
		- [ ] 11.1 AccountActivations 리소스
			- [ ] 11.1.1 AccountActivations Controller
			- [ ] 11.1.2 AccountActivation DataModel
		- [ ] 11.2 Account의 유효화와 메일 보내기
			- [ ] 11.2.1 보내는 메일의 Template
			- [ ] 11.2.2 보내는 메일의 Preview
			- [ ] 11.2.3 보내는 메일 테스트
			- [ ] 11.2.4 User의 create action을 수정해보자
		- [ ] 11.3 account를 유효하게 해보자
			- [ ] 11.3.1 authenticated? Method의 추상화
			- [ ] 11.3.2 edit action에서의 유효화
			- [ ] 11.3.3 유효화의 테스트와 Refactoring
		- [ ] 11.4 실제 배포환경에서의 메일 송신
		- [ ] 11.5 마지막으로
			- [ ] 11.5.1 11장의 정리
	- [ ] 제 12장 비밀번호의 재설정
		- [ ] 12.1 PasswordResets 리소스
			- [ ] 12.1.1 PasswordResets Controller
			- [ ] 12.1.2 새로운 비밀번호 설정
			- [ ] 12.1.3 create action에서의 비밀번호 재설정
		- [ ] 12.2 비밀번호 재설정 메일
			- [ ] 12.2.1 비밀번호 재설정 메일과 Template
			- [ ] 12.2.2 보내는 메일 테스트
		- [ ] 12.3 비밀번호를 재설정해보자
			- [ ] 12.3.1 edit action에서의 재설정
			- [ ] 12.3.2 비밀번호를 갱신해보자
			- [ ] 12.3.3 비밀번호 재설정을 테스트해보자
		- [ ] 12.4 실제 배포환경에서의 메일 송신(이어서)
		- [ ] 12.5 마지막으로
			- [ ] 12.5.1 12장의 정리
		- [ ] 12.6 증명: 기한이 지난 것과의 비교 
	- [ ] 제 13장 유저의 Microposts
		- [ ] 13.1 Micropost model
			- [ ] 13.1.1 기본적인 모델
			- [ ] 13.1.2 Micropost의 Validation
			- [ ] 13.1.3 User/Micropost의 관련짓기
			- [ ] 13.1.4 Microposts를 개선해보자
		- [ ] 13.2 Microposts를 표시해보자
			- [ ] 13.2.1 Microposts의 표시
			- [ ] 13.2.2 Microposts의 sample
			- [ ] 13.2.3 프로필화면의 Microposts를 테스트해보자
		- [ ] 13.3 Microposts를 조작해보자
			- [ ] 13.3.1 Microposts의 접근제어
			- [ ] 13.3.2 Microposts를 작성해보자
			- [ ] 13.3.3 피드의 원형
			- [ ] 13.3.4 Microposts를 삭제해보자
			- [ ] 13.3.5 피드화면의 Microposts를 테스트해보자
		- [ ] 13.4 Microposts의 영상 업로드
			- [ ] 13.4.1 기본적인 영상 업로드
			- [ ] 13.4.2 영상의 검증
			- [ ] 13.4.3 영상 리사이즈
			- [ ] 13.4.4 실제 배포환경에서의 영상 업로드
		- [ ] 13.5 마지막으로
			- [ ] 13.5.1 13장의 정리
	- [ ] 14장 유저를 Follow해보자 
		- [ ] 14.1 Relationship Model
			- [ ] 14.1.1 데이터 모델의 문제 ( 및 해결책)
			- [ ] 14.1.2 User/Relationship의 관련짓기
			- [ ] 14.1.3 Relationship의 Validation
			- [ ] 14.1.4 Follow하고 있는 유저
			- [ ] 14.1.5 Follower
		- [ ] 14.2  「Follow」 의 Web Interface
			- [ ] 14.2.1 Follow 의 Sample data
			- [ ] 14.2.2 통계와 「Follow」 유저
			- [ ] 14.2.3  「Following」 과  「Followers」  페이지
			- [ ] 14.2.4 「Follow」 버튼 (기본편)
			- [ ] 14.2.5 「Follow」 버튼 (Ajax편)
			- [ ] 14.2.6 フォローをテストする
		- [ ] 14.3 Status Feed
			- [ ] 14.3.1 작성동기와 계획
			- [ ] 14.3.2 피드를 처음으로 작성해보자
			- [ ] 14.3.3 Subselect
		- [ ] 14.4 마지막으로
			- [ ] 14.4.1 Sample Application의 기능을 확장해보자
			- [ ] 14.4.2 읽을거리
			- [ ] 14.4.3 14장의 정리
			- [ ] 14.4.4 역자의 후기


