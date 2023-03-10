> ### 오늘의 학습 목표
> ✅ RUST 언어의 인기에 대해 알아보자.
> ✅ RUST 언어의 장점을 알아보자.
> ✅ RUST 언어의 단점을 알아보자.

## 📈 RUST 언어의 인기

Stack Overflow는 개발을 하다 궁굼한게 생겼을 때 물어보고 답장하주는 즉, QNA 서비스 입니다. (국내에서 서비스중인 지식인 프로그래머 버전이라고 생각하시면 됩니다.) Stack Overflow 는 <span style="background-color: rgba(191, 255, 0, 0.7)">**국제적으로 많은 프로그래머가 좋아하고 애용하는 서비스 입니다.**</span>
> Stack Overflow 에서 매년 "프로그래머가 가장 좋아하는 프로그래밍 언어는 무엇인가?" 라는 주제를 가지고 Stack Overflow사용자 들에게 설문을 했는데 <span style="background-color: rgba(191, 255, 0, 0.7)">**2015 ~ 2022 까지 러스트가 1등을 차지했습니다.**</span> 이 말은 러스트가 다른 언어보다 확연한 차이 점이 존재한다는 뜻이고, 무엇보다 좋다는 뜻입니다. 그러면 왜? 이리 인기가 있을까요? 한번 장점을 알아보도록 하겠습니다.
![](https://velog.velcdn.com/images/2hanjunbum6/post/8bb52c21-dfaf-48c7-aff9-d9e669b777fa/image.png)

## 👍 RUST 언어의 장점
>#### 1. 러스트는 프로그램 동작 속도뿐만 아니라 작성 속도도 빠른 언어다!
현대로 들어와 프로그램의 속도의 의미는 과거와 많이 다릅니다. 과거에선 프로그램의 속도란 얼마나 빠른가에 대해 초점이 맞쳐줘 있는 반면에 현대는 <span style="background-color: rgba(191, 255, 0, 0.7)">**프로그램의 작성 속도에 대해 초점이 맞쳐줘 있습니다. Rust   는 동작 속도 뿐만 아니라 작성도 매우 빠른 언어 입니다.**</span>
#### 2. 너무나도 안정적이다.
러스트는 안정성을 위해 <span style="background-color: rgba(191, 255, 0, 0.7)">**여러가지 규칙들을 이용합니다.** (Ownership 규칙이 존재한다.)</span> 그 덕뿐에 실행 중 프로그램 크래시가 잘 나지 않으며 A 컴퓨터에서 작성한 main.rs 코드를 B 컴퓨터에서 실행 하면 동작이 잘 됩니다. 이처럼 Rust는 너무나도 안정적 입니다.
### 3. 러스트는 멀티코어에 특화되어 있다.
코딩을 하다 보면 스레드를 이용해 작업하게 되는 시기가 올 텐데, 스레드를 이용해 작업을 하면 매우 매우 예측이 힘듭니다. 마치 아기를 침대 위에 올려 놓는 것과 같다고 보면 됩니다. 하지만 러스트는 <span style="background-color: rgba(191, 255, 0, 0.7)">**안정성 규칙들을 이용해 여러가지 버그를 방지 해놨기 때문에 멀티코어에 특화되어 있습니다.** </span>
### 4. 너무 친철한 컴파일러
러스트 컴파일 언어입니다. 그래서 컴파일을 자주 이용하는데, 와 너무 좋습니다. 수정이 필요한 <span style="background-color: rgba(191, 255, 0, 0.7)">**소스코드를 컴파일 하면 어느 부분이 잘못되었고, 잘못된 부분에 대한 방안도 제시해 줍니다.**</span> 실제로 사용해보시면 엄청나게 좋다는 것을 알 수 있습니다.
### 5. 좋은 친구 Cargo가 있다.
러스트를 이용해 프로젝트를 진행하다 보면 Cargo라는 친구가 꼭 따라옵니다. <span style="background-color: rgba(191, 255, 0, 0.7)">**Cargo는 쉽게 말해서 프로젝트를 관리해주는 친구 입니다.**</span> 이 친구가 매우 매우 유용하게 쓰입니다.

>이뿐만 아니라 러스트를 직접 사용하다 보면 간결한 문법, 용이한 함수들이 있기에 배우다 보면 재미가 쏠쏠합니다. 하지만 장점도 있으면 단점도 있다. 한번 단점에 대해 알아보도록 하겠습니다.

## 👎 RUST 언어의 단점
>### 1. 엥? 변수가 불변이라고? 아니 이게 뭐야? 어? NULL이 없어? 이게 뭐야...
러스트 언어는 안정성을 위해 다른 언어가 가지고 있지 않은 즉, <span style="background-color: rgba(191, 255, 0, 0.7)">**자체적인 규칙을 같고 있습니다.**</span>그래서 그런지 생소한 문법과 생소한 사용법으로 인해 초보자들이 입문하기 어렵다고 소문단 언어 입니다.
### 2. 너무나도 작은 커뮤니티..
러스트를 이용해 개발하도 보면 구글링을 많이 하게 됩니다. 하지만 국내는 정보가 거의 없습니다. 그래서 <span style="background-color: rgba(191, 255, 0, 0.7)">**하드하게 구글링을 이용해야 한다는 점**</span>에서 너무나도 아쉽습니다.
### 3. 성장중인 언어 프로젝트
<span style="background-color: rgba(191, 255, 0, 0.7)">**러스트는 아직 계발중에 있는 언어 입니다**.</span> 실제로 키워드는 존재 하는데, 그 키워드는 사용하지 못합니다. 왜냐하면 계발중에 있기 때문이다. 이 처럼 러스트는 성장중인 언어 이기 때문에 언어의 불확실성을 갖습니다.

## 오늘은 이만 
오늘은 Rust의 인기, 장점, 단점에 대해 알아보았습니다. 
<span style="background-color: rgba(191, 255, 0, 0.7)">참고로 Rust 프로그래머를 러스타시안(Rustacean)이라고 부르는 호칭이 존재합니다.</span>
여러분들도 오늘 부터 러스타시안 입니다! 즐거운 하루 보내세요 ^^
이상 #0 Rust에 대해서 였습니다.

---
블로그 글을 작성할 때 아래의 글을 참조 했다 밝힙니다.

- 러스트(Rust) 언어소개! 🥪언어 특징 및 장단점 [언어탐방🔎]
```https://www.youtube.com/watch?v=-uHfu3Qhbco&t=356s```
- Rust-나무위키 
```https://namu.wiki/w/Rust```
- 러스트 언어를 좋아하는 이유, 그리고 싫어하는 이유 7가지
```https://www.itworld.co.kr/news/259252#:~:text=%EC%9E%A5%ED%99%A9%ED%95%9C%20%EC%BD%94%EB%93%9C%EB%8A%94%20%EA%B0%9C%EB%B0%9C%EC%9E%90%EA%B0%80,%EC%BD%94%EB%93%9C%EB%A5%BC%20%EC%93%B8%20%EC%88%98%20%EC%9E%88%EB%8B%A4.```