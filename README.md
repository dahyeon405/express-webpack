### 소개

Express 환경에 webpack-dev-middleware를 미들웨어로 등록하여, 서버 실행 시 webpack을 통한 번들링이 자동으로 진행되게끔 구축되어 있는 boilerplate 코드입니다.


### Feature

- babel 연동되어 있습니다.

- lodash가 설치되어 있습니다.

- ejs가 설치되어 있으며, 기본 view engine으로 설정되어 있습니다.

- SCSS 파일 사용 가능, 로더 등록 완료되어 있습니다. webpack.config.js에서 확인 가능합니다.

- source map: default로 inline-source-map이 등록되어 있습니다.
    
    수정을 원할 경우, webpack.config.js의 devtool 값을 수정하면 됩니다.
    
    source-map 비교표: 
    
    [Devtool | webpack](https://webpack.js.org/configuration/devtool/#devtool)
    
- webpack-dev-middleware가 설치되어 있습니다.

### 사용 방법

**설치**

- `npm i` 로 설치해주세요.

- package-lock.json, package.json, bin/www.js에 등록되어 있는 앱 이름(default는 “app-name”)을 수정해서 사용하세요.

**실행과 빌드**

```json
package.json 파일이 다음과 같이 설정되어 있습니다.

"scripts": {
    "start": "nodemon ./bin/www.js",
    "build": "webpack"
  },
```

- **실행**

    - `npm run start`를 입력하면 서버가 생성되고, webpack을 통한 빌드가 진행되며, 그 결과(default는 main.js)를 ejs 파일에서 불러옵니다.

    - `npm run start` nodemon을 통해 실행하게끔 설정되어 있으며, package.json 파일에서 변경 가능합니다.

- **빌드만 할 경우**

    - `npx webpack` 또는 `npm run build` 를 입력하면 빌드가 실행되며, output으로 dist/main.js가 생성됩니다.

    - 빌드 후 index.html 파일을 열면 main.js가 정상적으로 빌드되어 실행되는지 확인할 수 있습니다.

### 참고 링크

[Getting Started | 웹팩](https://webpack.kr/guides/getting-started/)
