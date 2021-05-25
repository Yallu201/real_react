# 실전 리액트 프로그래밍 실습 1

## 리액트 개발 환경 직접 구축하기

    #디렉토리 구조

    react.development.js
    react-dom.development.js
    simple1.html
    simple1.js

[react.development.js 파일 링크](https://unpkg.com/react@16.14.0/umd/react.development.js)  
[react-dom.development.js 파일 링크](https://unpkg.com/react-dom@16.14.0/umd/react-dom.development.js)

## 바벨 사용해보기

- 바벨의 용도

  - `ES6` 코드를 `ES5`로 변환
  - 주석 제거 및 코드 압축
  - jsx 문법을 React.createElement() 변환

- 바벨 설치 방법

1. npm 초기화 ( package.json 생성 )

```
npm init -y
```

2. npm을 이용하여 바벨 프리셋 및 플러그인 설치

```
npm install @babel/core @babel/cli @babel/preset-react
```

```
* node_modules/.bin 경로에 babel의 binary 파일이 설치됩니다.

* @babel/core         : 바벨의 핵심기능을 가지고있는 패키지
* @babel/cli          : cli에서 사용할 binary 코드
* @babel/preset-react : 리액트에서 사용하기위한 플러그인 모음

* 플러그인: 하나의 변환하는 기능
* 프리셋: 특정 목적을 위한 플러그인의 모음
```

- npx로 babel 실행하여 js코드 컴파일

```
npx babel --watch src --out-dir . --preset @babel/preset-react
```

```
node_modules/.bin 경로의 binary 파일을 실행합니다.

npx bable 실행 시 bable binary 파일이 없다면 바밸 페키지를 자동으로 설치합니다.(편의 기능)

--watch     : 파일이 변경될 때 마다 새로 컴파일 합니다.
src         : src 폴더의 파일을 컴파일 합니다.
--out-dir . : 현재 경로로 컴파일합니다.
--preset    : 사용할 preset을 선택합니다.
```
