# ynuWebService
영남대학교 게시판 만들기
#스프링부트 개발환경 준비하기
1.  InteliJ IDE 설치
	1. [https://www.jetbrains.com/ko-kr/idea/] 에 접속
	2.  (img)
	3. Community Version을 설치한다.
2.  Gradle Project 생성 후 , Springboot 프로젝트로 변경하기
	1. (img)
	2.  이후 build.gradle로 들어가 springboot 의존성 관리 설정하기(아래 코드 복사)
	3. buildscript{
			ext{
				springBootVersion = '2.1.7.RELEASE' as Object
			}
			repositories {
				mavenCentral()
				jcenter()
			}
			dependencies {
				classpath("org.springframework.boot:spring-boot-gradle-plugin:${springBootVersion}")
			}
		}
		apply plugin: 'java'
		apply plugin: 'eclipse'
		apply plugin: 'org.springframework.boot'
		apply plugin: 'io.spring.dependency-management'
		
		group 'com.ynuCoding.www'
		version '1.0-SNAPSHOT'
		sourceCompatibility = 1.8
		
		repositories {
			mavenCentral()
		}
		
		dependencies {
			compile('org.springframework.boot:spring-boot-starter-web')
			compile('org.projectlombok:lombok')
			compile('org.springframework.boot:spring-boot-starter-data-jpa')
			compile('com.h2database:h2')
			compile('org.springframework.boot:spring-boot-starter-mustache')
			compile('org.springframework.boot:spring-boot-starter-oauth2-client')
			compile('org.springframework.session:spring-session-jdbc')
			compile('org.mariadb.jdbc:mariadb-java-client')
			testCompile('org.springframework.boot:spring-boot-starter-test')
			testCompile('org.springframework.security:spring-security-test')
		}
	4.  플러그인 Lombok 설치
		1. Control + shift + a 누르고 Plugins 검색 (img) 
		2. 이후 Marketplace 로 들어가 Lombok 설치 (img)
	5. 
