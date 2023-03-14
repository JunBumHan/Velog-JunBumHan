### 스프링 입문 - 김영한 선생님  View 환경 설정

이번 시간에는 thyeleaf의 간단하게 사용해 봤습니다.

# thymeleaf 란?

- thymeleaf 공식 사이트: https://www.thymeleaf.org/
- 스프링 공식 튜토리얼: https://spring.io/guides/gs/serving-web-content/
- 스프링부트 메뉴얼: https://docs.spring.io/spring-boot/docs/2.3.1.RELEASE/reference/html/spring-boot-features.html#boot-features-spring-mvc-template-engines

thymeleaf는 자바 라이브러리이며, 웹과 아닌 환격 양쪽에서 텍스트, HTML, XML, Javascript, CSS 그리고 텍스트를 생성할 수 있는 템플릿 엔진입니다.

그러면 템플릿 엔진이란 무엇일까?
### 템플릿 엔진이란 

템플릿 엔진은 웹 개발에서 사용되는 도구로, 동적(움직이는)콘텐츠를 생성하는데 사용됩니다. 즉 웹 페이지의 구조를 정의하고, 페이지 내부의 동적인 데이터를 삽입하는데 사용됩니다.



### hellospring/controller/HelloController.java

```java
// hello-spring/src/main/java/hello/hellospring/controller/HelloController.java

@Controller
public class HelloController {

    @GetMapping("hello") // url/hello 이면 아래의 메소드 실행
    public String hello(Model model/*mvc 의 model를 뜻함*/) {
        model.addAttribute("data", "hello!");
        return "hello"; //templates 안에 hello* 파일을 찾아 간다.
    }

    /*
    그러니깐 위 함수를 요약하면
    먼저 url/hello 요청이 오면, hello 함수를 실행해라 매개변수 model은 스프링에서 자동적으로 넣어 준다.
    그리고 model.addAttribute() 함수를 실행 시켜 속성 이름과 속성 값을 넘겨준다.
    그 다음 return "hello"를 하게 되는데, 이 뜻은 templates폴더 안에 hello 를 찾아 가라는 뜻이다.
    그니깐  url/hello로 들어오면 GetMapping("hello") 함수에 들어가고 메소드를 실행시킨다. 그리고
    렌더링을 하게 된다. (나는 thymeleaf를 이용했다.)

     */
}


```

### resources/templates/hello.html


```java
// resources/templates/hello.html

<!DOCTYPE HTML>
<html xmlns:th="http://www.thymeleaf.org">
<head>
    <title>Hello</title>
    <meta http-equiv="Content-Type" content="text/html; charset=UTF-8" />
</head>
<body>
<p th:text="'안녕하세요. ' + ${data}" >안녕하세요. 손님</p> <!--&{data} == "hello!"-->
</body>
</html>
```

위 HelloController.java 코드를 봐보자. <br>
먼저 @Controller 어노테이션을 이용해서, 
Controller의 역할을 수행 한다고 명시한다. (해당 클래스를 Controller로 사용한다고 Spring FrameWork에 알린다.)

@GetMapping("hello")  -> 클라이언트 측에서 ip를 적고 /hello 로 적으면 아래의 함수를 실행시킨다. 
```java
public String hello(Model model/*mvc 의 model를 뜻함*/) {
        model.addAttribute("data", "hello!");
        return "hello"; //templates 안에 hello* 파일을 찾아 간다.
    }
```
그리고 Model을 매개변수로 받는데, 이 모델을 스프링이 자동으로 인자를 넘겨준다. 
그 다음 `model.addAttribute("data", "hello!");` 함수를 실행시켜서 맵의 요소를 추가한다. 
그 다음 return 할 때 "hello"를 반환하는데 이 뜻은
`resources:templates/ +{ViewName}+ .html` 이 경로로 가서 방금 모델에 추가한 요소를 적용한다.

그렇기 때문에 &{data}가 "hello!" 치환된다.

그리고 위 상황을 하는 친구를 ViewResolver라고 한다.(?) 

근데 정확한 정보가 아니다... 

## 동작 원리를 도식화

![](https://velog.velcdn.com/images/2hanjunbum6/post/23db8c34-0d39-492c-9718-5f238c863d17/image.png)

위 사진을 보면, url/hello 요청을 받고 톰캣에서 helloController를 찾아 GetMapping 에 해당하는 메소드를 찾고 return 값에 따라서 viewResover가 렌더링 해준다.

#### 렌더링 이란 무엇일까?
스프링 부트 렌더링이란, 스프링 부트 애플리케이션에서 웹 페이지를 생성하는 과정을 말합니다. 이 과정은 서버 측에서 HTML, CSS, JavaScript 등의 리소스를 조합하여 최종적으로 클라이언트에게 전달되는 HTML 페이지를 생성하는 것이라고 한다.

스프링 부트는 일반적으로 템플릿 엔진을 사용하여 렌더링을 처리한다. 예를 들어, Thymeleaf, Freemarker, Mustache와 같은 템플릿 엔진을 사용하여 HTML 템플릿을 작성하고, 서버에서 해당 템플릿을 렌더링하여 클라이언트에게 전달한다.

스프링 부트 렌더링은 클라이언트 요청에 따라 동적으로 페이지를 생성하는 방식을 사용하며, 이를 통해 사용자에게 더 나은 사용자 경험을 제공할 수 있다. 또한, 스프링 부트의 렌더링 기능은 다양한 성능 최적화 기능을 제공하므로, 빠르고 안정적인 웹 애플리케이션을 개발할 수 있다.


- chatgpt의 대답이다.

스프링 부트는 참 좋은 것 같다.
