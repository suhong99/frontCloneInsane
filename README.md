홈화면
![image](https://user-images.githubusercontent.com/120103909/216041994-914b5103-e859-416c-88c6-6dfaf9ddc26d.png)

회원가입
![image](https://user-images.githubusercontent.com/120103909/216042077-484530dc-265b-403b-a5ba-7fe46cdfc9ee.png)




-에러슈팅
좋아요가 눌렀을 때, 랜더링이 비동거치리가 안됨. 
--> useEffect의 디펜던스 어레이를 잘못썻음. 서버에서 값이 들어오고 해당 값이 변경되었을 때, 한번 더 랜더링하도록 작업함.

-로그인이 되지 않았을 때 회원가입과 홈화면 말고는 접근하지 못하게 하기
LoginHeader라는 컴퍼넌트를 만들어서  
로그인 해더를 만들어서 특정페이지에 로그인이 없으면  home으로 navigate시킴
이때 checkLogin은 sessionstorage에 닉네임이 있는지를 통해서 확인함.
useEffect(() => {
    if (
      checkLogin === null &&
      locationNow.pathname !== "/" &&
      locationNow.pathname !== "/SignUp"
    ) {
      alert("로그인 해주세요.");
      goToHome();
    }
  }, [checkLogin, locationNow.pathname]);
};

리덕스 툴킷을 이용해서 스테이트를 이용한 리렌더링 구현

ref를 인풋값으로 활용

회원가입시 유효성 검사 및  버튼 disabled

# Getting Started with Create React App

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Available Scripts

In the project directory, you can run:

### `yarn start`

Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in your browser.

The page will reload when you make changes.\
You may also see any lint errors in the console.

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

**Note: this is a one-way operation. Once you `eject`, you can't go back!**

If you aren't satisfied with the build tool and configuration choices, you can `eject` at any time. This command will remove the single build dependency from your project.

Instead, it will copy all the configuration files and the transitive dependencies (webpack, Babel, ESLint, etc) right into your project so you have full control over them. All of the commands except `eject` will still work, but they will point to the copied scripts so you can tweak them. At this point you're on your own.

You don't have to ever use `eject`. The curated feature set is suitable for small and middle deployments, and you shouldn't feel obligated to use this feature. However we understand that this tool wouldn't be useful if you couldn't customize it when you are ready for it.

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
