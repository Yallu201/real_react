# 실전 리액트 프로그래밍 실습 1

## 리액트 개발 환경 직접 구축하기

    #디렉토리 구조

    index.html
    /dist           # 번들링된 파일 저장
    /src            # 번들링할 파일 저장

## 웹팩의 기본 개념 이해하기

```
다양한 기능 제공

* 파일 내용을 기반으로 파일 이름에 해시값 추가( 브라우저 캐싱 )
* 사용되지 않는 코드 제가
* 자바스크립트 압축
* JS에서 CSS, JSON, 텍스트 파일 등을 일반 모듈처럼 불러오기
* 환경변수 주입

* 웹팩을 사용하는 가장 큰 이유
=> 모듈 시스템( ESM, commonJS )을 사용하고 싶어서

* 모던 브라우저에서는 ESM을 지원합니다. 하지만
=> 오래된 브라우저 및 많은 오픈소스가 commonJS로 작성되어있습니다.
```

```javascript
// ESM( ECMAScript Module )

// file1.js
export default function fun1() {}
export function func2() {}
export const variable1 = 123;
export let variable2 = "hello";

// file2.js
import myFunc1, { func2, variable1, variable2 } from "./file1.js";

// file3.js
import { func2 as myFunc2 } from "./file1.js";
```

```html
<!-- AS IS -->
<html>
  <head>
    <script type="text/javascript" src="javascript_file_1.js"></script>
    <script type="text/javascript" src="javascript_file_2.js"></script>
    <!-- ... -->
    <script type="text/javascript" src="javascript_file_999.js"></script>
  </head>
  <!-- ... -->
</html>

<!-- TO BE -->
<html>
  <head>
    <script type="text/javascript" src="app.js"></script>
  </head>
  <!-- ... -->
</html>
```

```
# webpack 설치
yarn add webpack webpack-cli react react-dom

# webpack 실행
npx webpack
```
