# soolzip


## 수행기간
21/08/16 ~ 21/10/11

## Contetns

1. [개요](#개요)
2. [설계의 주안점](#설계의-주안점)
3. [사용기술 및 개발환경](#사용기술-및-개발환경)
4. [프로젝트 기능 구현](#프로젝트-기능-구현)
5. [주요기능](#주요-기능)
6. [Document](#Document)

## 개요
프로젝트 sool.zip은 알.zip, 반디.zip 같이 정보를 모아 압축해놓은 프로그램에서 아이디어를 얻어 이러한 부분이 프로젝트방향과 같다는 생각에 술+zip으로 정했다. 
sool.zip은 정리되지 않고 오래된 레시피들을 관리해 기존의 정보보다 편리함과 다양함이 업그레이드된 정보를 제공하며, 
애주가들이 모여 서로 혼자알기 아까운 꿀팁을 공유하는 등의 소통의 긍정적인 역할을 기대하며, 프로젝트 방향성을 잡았다.   


## 설계의 주안점
프로젝트 주안점으로두고 진행한 부분은 다른 주류 사이트들과 다르게 다양하고 새로운 정보를 정리해 관리하여 클라이언트가 간편하게  받아볼 수 있도록 제공하며,
유저간 소통, 흥미를 높이는 기능을 구현해 클라이언트의 관심과 사용횟수를 올리는데 있고, 이러한 부분을 바탕으로 주요기능을 선정하였다.

주요기능
1. 회원 비밀번호찾기 - 회원이 비밀번호찾기 클릭시 회원가입과정에서 등록한 이메일을 통해 임시빌밀번호를 발송하게하였다. 
		이후 비밀번호변경은 필수사항이아닐 선택사항으로 클라이언트의 번거로움을 줄이고 신속하게 재사용이 가능하다.  
2. 명예의전당 - 관리자페이지에서 조회수와 좋아요수가 가장 높은 레시피를 10개 선정해 투표를 시작하면 사용자들이 투표를 진행한다. 
	      그 중 가장 투표수가 많은 레시피는 명예의 전당 레시피로 등록되어, 사용자들이 직접뽑아 검증된 레시피의 정보를 받아볼 수 있다.   
3. 투표기능 - 투표가 시작되면 사용자들이 메인페이지나 메뉴를 통해 투표현황 페이지에서 투표와 각 레시피의 득표수 확인 가능하다.  
	    한사람당 한표를 행사할 수 있고, 투표기간내에는 투표 취소가 가능하다. 
4. 레시피 등록 -  레시피 등록시에 재료과정 추가등록이 가능하다. 추가등록을 통해 원하는 레시피를 보기쉽고 디테일하게 등록할 수 있게 되었으며, 필수등록사항 미기재 시 전체공개가 불가능하다. 
		이를 통해서는 클라이언트가 원하는 정보를 신속하게 받아볼 수 있는 카테고리별 정보를 제공할 수 있게되었다. 
5. 쪽지기능 - 회원페이지에서 쪽지 보내기를 클릭하면 쪽지 제목과 내용을 입력하여 쪽지를 보낼 수 있고, 마이페이지에서 받은 쪽지와 보낸 쪽지를 수신할 수 있다. 쪽지 기능을 통해 회원들간의 커뮤니케이션을 활성화 시킬 수 있다.

## 사용기술 및 개발환경
FrontEnd | HTML5, JS, CSS3, JQuery, BOOTSTRAP
BackEnd | Java
OS | Windows10
IDE | Eclipse, Visual Studio Code
Server | Tomcat(v8.5)
CI | Github
DataBase | Oracle

## DB구조 

https://www.erdcloud.com/d/uPmxAyJdK3Xsbur9X
## 프로젝트 기능 구현
1. 회원가입 / 로그인
-유효성 검사를 통해 무차별적인 가입을 방지하고 중복데이터를 방지하였습니다
2.정보찾기
-비밀번호 찾기시 회원가입중 입력한 이메일로 임시 비밀번호를 발급하여 password를 변경합니다
3.검색
-술이름, 칵테일 검색시 메인주류 검색을 할수 있습니다
4.스토리
-사진과 함께 글을 등록하여 회원들끼리 소통할수 있습니다
-자신의 스토리가 아닌 타인의 스토리에 좋아요를 표시할수 있습니다
5.레시피
-레시피 등록시 가이드폼을 주어 사용자가 편리하게 등록할수 있습니다.
-등록한 레시피에 추천을 할수있고 스크랩을 할수있습니다.
-스크랩시 마이페이지에서 따로 볼수 있습니다.
6.투표
-관리자페이지에 해당 월에 좋아요수가 많은 레시피 10개를 선택할수 있으며, 선택시 투표페이지를 오픈할수 있습니다.
-관리자가 투표를 닫기전까지 사용자는 투표를 할수있으며 투표는 1인당 1레시피만 투표가능합니다(투표취소후 다른 레시피 투표가능).
-투표를 닫으면 1위 레시피는 명예의 전당에 등록되어 테두리와 왕관 아이콘이 생깁니다
7.쪽지
-회원은 레시피 혹은 스토리 게시물을 올린 사용자에게 쪽지를 보낼수 있습니다
8.관리자페이지
-관리자는 회원을 강제탈퇴 시킬수 있습니다
-회원은 관리자에게 문의를 할수있고 관리자는 그 문의에 답변이 가능합니다
-자주하는 질문을 수정할수 있습니다
9.마이페이지
-자신이 올린 레시피, 스토리 게시물을 모아볼수 있습니다
-받은 쪽지를 볼수 있고, 보낸 쪽지를 확인할수 있습니다
-회원정보 수정을 할수 있습니다 회원정보 수정시 유효성검사를 거쳐야 합니다
                  

