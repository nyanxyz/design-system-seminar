# 디자인 시스템

- 염수연(@SooyeonYeom) 님께서 작성해주신 세미나 필기본입니다.

## 강의 자료

- [디자인 시스템.pdf](https://github.com/nyanxyz/design-system-seminar/blob/main/%EB%94%94%EC%9E%90%EC%9D%B8%20%EC%8B%9C%EC%8A%A4%ED%85%9C.pdf)

## 소개

- 서울대학교 컴퓨터공학 19학번 23세
- 웹에 들어가는 TDS 운영 설계 및 프레이머 툴 관리
- 와플에서 식샤 웹 개발
- 최근 눈썹 문신
- 4일 후 (2022년 10월 23일 기준) 남자친구 휴가

# 디자인 시스템이란?

## 구글 디자인 시스템 Material UI

- 컴포넌트 : 재사용이 가능하고 특정한 기능을 하는 요소

<aside>
🗣 디자인 시스템은 컴포넌트의 모음이다.
</aside>

## 라인 디자인 시스템 Line Design System

- ux guideline
- foundation

<aside>
🗣 디자인 시스템은 토큰과 컴포넌트의 명세이다
</aside>

\*토큰 : 컬러, 타이포그래피 등 값

\*명세 : 유즈케이스, 제약 등

## 토스 디자인 시스템 Toss Design System

- 토큰
- 컴포넌트
- 템플릿, 퍼널
- UX 라이팅
- 디자인 에디터 (Framer)
- 코드 제너레이터
- 기타 (스크린 센터 Mobbin 리소스 센터 Flaticon)

<aside>
🗣 디자인하고 구현하기 까지 사용하는 모든 시스템 제품을 구성하는 하나의 언어이다.
</aside>

# 디자인 시스템의 존재 이유 및 목적

## 1) 생산성 개선

미니멈 퀄리티 향상을 통해 생산성이 파괴적으로 증가한다

디자이너는 쉽게 디자인, 개발자는 쉽게 구현!

프레이머 역시 이에 큰 영향

## 2) 통일성 있는 사용자 경험

전부 다른 사일로가 개발하지만 같은 사용자 경험을 줄 수 있다

- 폰트 컬러 룰 적용
- UX 라이팅 툴 적용 (에디터 단에서 강제할 수 있음)
- 접근성 대응 (컴포넌트 단에서 레이아웃, 보이스오버 대응 / 컬러 토큰 자체에 다크모드대응)
- 퍼널 재사용 (인증과정에 대한 퍼널화)

# 디자인 시스템의 구현 방법

## 컴포넌트의 조건

- 재사용이 가능한가?
- 유즈케이스가 확실한가?

(예)

Tab

- 정보의 종류가 동일하지 않을때

Segmented Control

- 정보의 종류가 동일할때

## 컴포넌트 디자인

- 변할 수 있는 것과 없는 것을 정해라
  - 들어갈 수 있는 모든 옵션을 추가했다고 생각하고 구멍을 뚫어 놓아야 한다 (→ 개발의 용이성 증대)
  - 변하는 것 : Text / 나타나는 시점 / 색상
  - 변하지 않는 것 : 글자 크기
  - 제한
- 모든 플랫폼의 개발자가 확인할 수 있는 가이드를 만든다
- 컴포넌트를 개발한다
  - 커스텀을 유의해 너무 strict하게 type를 제한하지 않는다
  - 웹 / 앱 / 디자인 모두 property 통일
- 문서화
  - 디자인, 개발할때 볼 수 있는 컴포넌트 명세 - 프레이머로 확인가능
  - 디자인 명세 : 어떤 옵션을 변경할 수 있는지 개발자가 쉽게 확인할 수 있게
  - 개발 명세 : 어떤 옵션이 어떤 값에 의해 변경되는 지 쉽게 확인할 수 있게 (ex. storybook)

# 더 고도화된 디자인 시스템은?

## 인터랙션 디자인 시스템

- 애니메이션 (햅틱 등)
- easing, delay 등 motion 설정

## QA

- 수행해야 할 테스트를 자동으로 생성한다
- 디자인 에디터 속 화면과 일치하는지 자동으로 검사한다

## 로깅

- 컴포넌트에 로깅 로직을 붙인다

# 첨언

- 기존 컴포넌트 제약에 반하는 변경 시,
  미적 주관이 아닌, `CTR`과 `개발 생산성`을 저울질 해야한다.
