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

```
class Board extends React.Component {
  renderSquare(i) {
    return <Square value={i} />;
  }
}
```


## 불변성이 중요한 이유
코드에서 기존의 배열을 수정하지 않고 `.slice` 연산자를 사용하여 `squares` 배열의 복사본을 만들어 복사본을 조작한 뒤 기존 배열을 바꿔치기 하였다. 리액트를 이처럼 기존의 값을 수정하는 것을 허락하지 않는 **불변성**을 지니고 있다. 그렇다면 불변성은 왜 중요할까?

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
