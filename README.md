### 🎬 메가박스 반응형 사이트입니다 🎥

-   실행 주소: https://ginny-choi.github.io/study2/
-   참고: 웹스토리보이즈 강의

### 배운 점 👩🏻‍💻

---

10/14

-   👩🏻‍💻 웹접근성을 생각해서 h 태그 넣는거 잊지 않기
-   👩🏻‍💻 햄버거 메뉴의 터치 영역을 크게 잡게 해주는게 좋다. a태그에는 여백을 많이 줌.
-   👩🏻‍💻 하위 메뉴가 없는 곳에는 float 작성 후 부모 요소에 overflow:hidden 을 설정해줘도 좋지만 하위 요소가 있다면 안된다!
-   https://swiperjs.com/ 플러그인 참고

---

10/15

##### 웹사이트에서 이미지를 표현하는 태그

-   `<img>` : 이미지를 불러 올 때 사용
-   `<figure>` : 이미지를 표현 할 때 사용
-   `<figcaption>` : 이미지를 설명 할 때 사용
-   `<picture>` : 이미지를 화면 크기에 따라 사용 -> 반응형 할 때 사이즈별 이미지를 나타낼 때 사용. 화면 크기에 따라 이미지 크기를 다르게 구현함. source 태그와 같이 사용하며 미디어쿼리 사용 가능

-   https://webkit.org/demos/srcset/ 사용 디바이스 해상도 알려주는 사이트
-   border가 두줄로 겹쳐 보일 때 요소에 margin-left:-1px 혹은 margin-right:-1px 을 주면 한줄로 보이게 한다.

---

10/18

##### 스와이퍼 슬라이더 플러그인 오류 발생

-   display: none -> block 으로 탭메뉴를 구성했기 때문에 변경시 렌더링트리에 만들어지지 않아서 구현이 되지 않는 오류 발생
-   돔의 상태변경을 감지하는 api 활용으로 오류 해결 / oberserver, oberserveParents 옵션 적용
-   🔑 https://swiperjs.com/swiper-api#param-observer 참조
-   🔑 slick의 경우 https://deront-end.tistory.com/3 해당글 참고

\*\* img 는 inline 구조 이기 때문에 폰트 사이즈도 영역이 잡힌다. -> 여백을 없애려면 블록으로 바꿔준다.

-   이미지 스플라이트 -> background position 을 조정해서 맞는 이미지를 넣어줌
-   background img 위치를 center center(가운데정렬)로 해주면 짤리는 느낌 방지
-   svg 색상 채우기 : fill

---

10/19

-   글씨는 위치를 이동하지 않는다. 정렬을 맞추기 위해서는 다른 요소의 vertical-align 을 설정해줌
-   background에 이미지를 넣을 때. 자리 잡는 방법 중 하나 => right 10px top 10px; 직접 숫자를 정해줌

---

10/20

-   우선적으로 div 태그만 떠올리지 않고 article, dl-dd-dt 태그 사용한 것 처럼 용도에 맞는 태그를 사용하기
    dl: 정의 목록 약자, 용어를 설명하는 목록 / dt : 용어의 제목 / dd : 설명하는데 사용
-   ir 효과 : 웹접근성을 위한 숨김 텍스트를 제공할 때,의미있는 이미지의 대체 텍스트를 제공하는 경우,
    의미있는 이미지의 대체 텍스트로 이미지가 없어도 대체 텍스트를 보여주고자 할 때 사용하며 text-indent에 음수 값을 줘서 안보이게 가려준다

---

10/21

###### a 태그에 rel(relation) 속성

    - rel 속성은 연관 관계를 명시한다. 현재 문서와 링크된 문서 사이의 연관관계를 명시
    - href 속성이 설정되어야 사용 가능

-   skip menu : position:absolute; 설정 후 탑값을 조절하여 보이게 한다. active, focus시 탑값 0으로 맞추기
