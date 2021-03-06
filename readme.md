## 예시
[https://dimorin.github.io/webpack-js-html/](https://dimorin.github.io/webpack-js-html/)<br>
[https://dimorin.github.io/webpack-js-html/sub.html](https://dimorin.github.io/webpack-js-html/sub.html)<br>
[https://dimorin.github.io/webpack-js-html/wavemotion.html](https://dimorin.github.io/webpack-js-html/wavemotion.html)
## 특징
1. 최소한의 설정만 한 웹팩 세팅(자바스크립트 모듈만 빌드)
> [https://github.com/jmyoow/webpack-js-html](https://github.com/jmyoow/webpack-js-html)
2. 여러 html 파일 번들링
> [여러 html을 각각 번들링 하기](https://choiyb2.tistory.com/96)<br>
> [output - 여러파일 번들링](https://velog.io/@khw970421/Webpack-5%EC%9E%A5-output-%EC%97%AC%EB%9F%AC%ED%8C%8C%EC%9D%BC-%EB%B2%88%EB%93%A4%EB%A7%81)
3. canvas wave
> [https://youtu.be/LLfhY4eVwDY](https://youtu.be/LLfhY4eVwDY)
## 사용법
1. 패키지 설치
```bash
npm i -D @babel/cli @babel/core @babel/preset-env babel-loader clean-webpack-plugin copy-webpack-plugin core-js cross-env html-webpack-plugin source-map-loader terser-webpack-plugin webpack webpack-cli webpack-dev-server
```

2. 개발용 서버 구동
```bash
npm start
```

3. 빌드(배포용 파일 생성)
```bash
npm run build
```

(!)
`npm start` 또는 `npm run build` 실행 시 에러가 난다면 Node.js를 LTS 버전(장기 지원 버전)으로 설치 후 다시 시도해 보세요.<br>
터미널에 아래 내용을 붙여 넣고 엔터를 누르면 설치할 수 있어요.
```bash
n lts
```

(!)
ERROR in unable to locate '경로...'<br>
위와 같은 에러가 발생한다면, webpack.config.js의 CopyWebpackPlugin에 설정된 파일이 있는지 확인해주세요.<br>
CSS나 이미지 폴더 등이 필요하지 않다면 webpack.config.js에서 CopyWebpackPlugin 부분 전체를 주석 처리 해주세요.


## gh-pages 사용법
1. `npm i gh-pages -D`
2. package.json 파일의 script 속성에 아래 코드 추가
```json
"deploy": "gh-pages -d dist"
```
3. package.json 파일에 homepage 속성 추가
```json
"homepage" : "https://(GitHub ID).github.io/(Repository name)/"
```
4. `npm run deploy`