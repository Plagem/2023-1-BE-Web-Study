Spring initializr //start.spring.io (스프링 부트, 스프링에서 운영하는 사이트)
> 기본적인 Spring의 툴을 만들어준다

Project - Gradle

Dependencies - 어떤 라이브러리를 사용할건가?
 -Spring Web
  -Thymeleaf
 (아직은 뭔지 모름)
-> GENERATE (다운로드)

이후 intelliJ에서 Open or Report 항목을 클릭하여 다운받은 폴더를 선택한다
폴더 안의 buld.gradle 클릭 후 Open -> Open as project

src : main과 test 2개로 나뉘어져 있음
build.gradle : 버전 설정 & 라이브러리 땡겨오기
gitignore : 아직은 잘 모르겠음..



실행
main>java>hello.hellospring>HelloSpringApplication.java
의 main 왼쪽 화살표버튼 눌러서 실행, 터미널에 알수없는것들이 뜬다.
이후 웹 주소에 localhost:8080 검색하면 에러페이지가 출력된다

resources/static 에 있는 index.html 페이지는 Welcome page 의 역할을 한다.

Thymeleaf -> 컨트롤러, 동작을 맡음, 웹 어플리케이션에서의 첫 진입점


폴더 외부에서 서버 빌드하기
terminal 접속, 스프링 설치된 폴더로 cd
.\gradlew build > 하면 빌드가 된다
cd build를 통해 build 폴더로 이동 후 cd libs 이동
해당 libs폴더에 빌드 파일(jar)이 존재하는걸 볼 수 있다.
java -jav JAR파일명.jar 입력하면 서버가 실행된다.

-> 서버를 배포할때는 해당 jar 파일만 복사해서 서버에 넣고, 실행을 하면 된다.

MVC와 템플릿 엔진
MVC - Model, View, Controller (전부 쪼개서 따로 봄-유지보수의 유용성)
 Model -
 Controler - 서버와 관련된 처리
 View - 화면에 보이는 것

@RequestParam("name") -> 해당 주소로 이동할때 name 파라미터값을 요구한다(?)
 -> localhost:8080/hello-mvc?name=hellospring
	return : hello-template
	model(name:hellospring)

