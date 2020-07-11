# Eslint

- eslint는 일종의 문법규칙이며 코드작성시 문법오류의 최소화를 위해 ;(세미콜론) 과 ,(콤마)의 작성을 습관화 하도록 경고나 오류를 발생시킨다.
- eslint 설정을 끄기 위한 방법
  - /* eslint-disable */ 주석을 컴포넌트마다 스크립트 부분에 넣어준다. - 번거로워 진다.
  - package.json과 같은 경로에 vue.config.js파일을 생성한 뒤, module.exports = { lintOnSave: false } 를 작성한다. 이렇게 하면 저장할 때 마다 eslint를 검사하던 것이 사라진다.
    - https://cli.vuejs.org/config/#lintonsave

