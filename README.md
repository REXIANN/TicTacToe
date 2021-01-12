# Getting Started with Create React App

개발 초짜의 리액트 예습. 공식 홈페이지를 보며 하나씩 공부해보자!

⚠️ 최신버전의 노드 설치가 필요합니다!

## 시작하기

```
npx create-react-app tictactoe
```

리액트는 페이스북이 만든 프레임워크이다. 페이스북은 항상 최신 라이브러리를 사용하는 것을 권장하므로 npm 또는 yarn을 통해서 create-react-app을 설치한 경우 그 라이브러리를 **지우라고** 설명한다. npx 명령어를 통해 그때마다 제일 최신버전의 create-react-app을 사용하여 리액트앱(?)을 만들 수 있으니 참고하자.

## React란 무엇인가요?

React는 사용자 인터페이스를 구축하기 위한 선언적이고 효율적이며 유연한 JavaScript 라이브러리이다. "컴포넌트"라고 불리는 작고 고립된 코드의 파편을 이용하여 복잡한 UI를 구성하도록 돕는다. React는 몇 가지 종류의 컴포넌트를 가지지만 우리는 `React.Compoenet`의 하위 클래스를 우선 사용할 것이다.

## Props을 통한 데이터 전달

vue와 똑같은 방법으로 하위 컴포넌트에 데이터 또는 함수를 내릴 수 있다.
`<Square value={i} />`처럼 작성할 수 있다.

또한 구현부의 태그에 `onClick={() => handleEvent()}` 를 작성해서 해당 태그에서 클릭 이벤트가 발생하는 경우 수행할 동작을 지정할 수 있다.

### Vue와의 공통점

1. 우선 용어가 똑같다. 부모에서 자식 컴포넌트로 내려주는 객체를 props 라고 부른다.
2. 작성 위치와 방식이 동일하다. 똑같이 태그 안에 적어주며, `value={value}`라고 쓰면 오른쪽에 있는 value는 부모가 내려주는 데이터가 되고, 왼쪽에 있는 value는 자식이 props 객체를 받아서 사용할 때 찾기 위한 이름이 된다.

### Vue와의 차이점

1. 부모가 내려주는 데이터를 무조건 `{}`로 감싼다.
2. 부모의 함수를 props에 담아 자식 컴포넌트로 내려보낸다. Vue에서는 emit을 통해 자식 컴포넌트에서 부모 컴포넌트로 요청을 올려 보내는 방식을 사용했다.

## 불변성이 중요한 이유
코드에서 기존의 배열을 수정하지 않고 `.slice` 연산자를 사용하여 `squares` 배열의 복사본을 만들어 복사본을 조작한 뒤 기존 배열을 바꿔치기 하였다. 리액트를 이처럼 기존의 값을 수정하는 것을 허락하지 않는 **불변성**을 지니고 있다. 

그렇다면 불변성은 왜 중요할까? 직접적인 객체 변경이나 기본 데이터의 변경을 하지 않는다면 몇가지 이점을 얻을 수 있다.

### 복잡한 특징들을 단순하게 만듬

불변성은 복잡한 특징들을 구현하기 쉽게 만든다. 자습서에서는 "시간 여행" 기능을 구현하여 틱택토 게임의 이력을 확인하고 이전 동작으로 "되돌아갈 수 있다". 특정 행동을 취소하고 다시 실행하는 기능은 애플리케이션에서 일반적인 요구사항이다. 직접적인 데이터 변이를 피하는 것은 이전 버전의 게임 이력을 유지하고 나중에 재사용할 수 있게 해준다.

### 변화를 감지함

객체가 직접적으로 수정되기 때문에 복제가 가능한 객체에서 변화를 감지하는 것은 어렵다. 감지는 복제가 가능한 객체를 이전 사본과 비교하고 전체 객체 트리를 돌아야 한다. 

하지만 불변 객체에서 변화를 감지하는 것은 상당히 쉽다. 참조하고 있는 불변 객체가 이전 객체와 다르다면 객체는 변한 것이다.

### React에서 다시 렌더링하는 시기를 결정함

불변성의 가장 큰 장점은 React에서 순수 컴포넌트를 만드는 데 도움을 준다는 것이다. 변하지 않는 데이터는 변경이 이루어졌는지 쉽게 판단할 수 있으며 이를 바탕으로 컴포넌트가 다시 렌더링할지를 결정할 수 있다.

-----

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Available Scripts

In the project directory, you can run:

### `yarn start`

Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in the browser.

The page will reload if you make edits.\
You will also see any lint errors in the console.

### `yarn test`

Launches the test runner in the interactive watch mode.\
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `yarn build`

Builds the app for production to the `build` folder.\
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.\
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.

### `yarn eject`

**Note: this is a one-way operation. Once you `eject`, you can’t go back!**

If you aren’t satisfied with the build tool and configuration choices, you can `eject` at any time. This command will remove the single build dependency from your project.

Instead, it will copy all the configuration files and the transitive dependencies (webpack, Babel, ESLint, etc) right into your project so you have full control over them. All of the commands except `eject` will still work, but they will point to the copied scripts so you can tweak them. At this point you’re on your own.

You don’t have to ever use `eject`. The curated feature set is suitable for small and middle deployments, and you shouldn’t feel obligated to use this feature. However we understand that this tool wouldn’t be useful if you couldn’t customize it when you are ready for it.

## Learn More

You can learn more in the [Create React App documentation](https://facebook.github.io/create-react-app/docs/getting-started).

To learn React, check out the [React documentation](https://reactjs.org/).

### Code Splitting

This section has moved here: [https://facebook.github.io/create-react-app/docs/code-splitting](https://facebook.github.io/create-react-app/docs/code-splitting)

### Analyzing the Bundle Size

This section has moved here: [https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size](https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size)

### Making a Progressive Web App

This section has moved here: [https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app](https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app)

### Advanced Configuration

This section has moved here: [https://facebook.github.io/create-react-app/docs/advanced-configuration](https://facebook.github.io/create-react-app/docs/advanced-configuration)

### Deployment

This section has moved here: [https://facebook.github.io/create-react-app/docs/deployment](https://facebook.github.io/create-react-app/docs/deployment)

### `yarn build` fails to minify

This section has moved here: [https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify](https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify)
