# maven-dependency

## pom.xml
1. cmd
2. cd 워크스페이스
3. mvn archetype:generate
4. java : 1195, web : 1200
5. archetype version : 
6. groupid : (package)
7. artifactld : (프로젝트명)
8. version : 1.0-snapshot
9. package : 

### dependency
    pom.xml > project > dependencies > dependency
[dependency 검색](https://mvnrepository.com)

### scope
* compile : 기본영역으로 아무것도 지정되지 않은 경우 사용됨. compile 의존관계에 있는 것은 프로젝트의 모든 클래스에서 사용가능함. 또한, 이와 같은 의존관계는 의존관계에 있는 프로젝트에 포함됨.

* provided : compile 과 매우 유사히지만, 실행시 의존관계를 제공하는 JDK나 컨테이너에 대해서 적용됨. 예를 들어, JEE에 대한 웹 어플리케이션을 만드는 경우, 웹 컨테이너가 서블릿 API와 Java EE API관련 클래스들을 제공하기 때문에 provided 영역으로 의존관계가 세팅되어야 함. 이 영역은 컴파일과 테스트의 클래스패스 용으로 사용되며, 자동영역임.

* runtime : 의존관계가 컴파일시 필요하지 않지만, 실행시 필요함을 의미함. 실행시와 테스트 클래스패스에 속하지만, 컴파일 클래스패스에는 속하지 않음.

* test : 일반적인 어플리케이션 사용에 대해서는 의존관계가 필요없고, 테스트 컴파일과 실행 시점에만 사용됨.

* system : 명시적으로 해당 JAR를 포함하는 것이 제공되어야 한다는 것을 제외하고 provided와 유사함. artifact는 항상 사용가능하며 레파지토리에서 검색하지 않음.

* import (Maven 2.0.9 이후에서만 적용) : 이 영역은 <dependencyManagement>에서 pom의 의존관계에 대해서 사용됨. 지정된 POM이 해당 POM의 <dependencyManagement> 영역에 있는 의존관계로 대체됨을 의미함. 이것들이 대체되기 때문에 import 영역의 의존관계들은 실질적으로 의존에 대한 제약에 대해 관여하지 않음.
      
