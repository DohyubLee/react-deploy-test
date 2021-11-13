# Create React App으로 생성한 프로젝트 github pages로 배포하기

1. Create React App으로 프로젝트 생성
2. 생성된 프로젝트에서 `gh-pages` 모듈 설치 => npm install gh-pages
3. package.json 파일에 `predeploy`, `deploy` 스크립트 명령어 추가 and `homepage`도 추가
   - scripts 명령어가 같고 앞에 `pre-` 가 붙으면 먼저 실행됨을 의미
 ```json
  "scripts":{ 
    "pre블라블라": "npm run 블라블라 실행시 여기가 먼저 실행", 
    "블라블라": "어쩌구 저쩌구",
    "post블라블라": "나중에 실행"
   }
```
```json
"scripts":{ 
  "predeploy": "react-scripts build", 
  "deploy": "gh-pages -d build", 
},
"homepage": "사용될 도메인 주소, 후에 github repo에서 확인가능"
```
4. 프로젝트 github에 올리기
5. 올린후 repo에서 settings=>pages에가서 우선 master 브랜치로 Source를 설정한뒤 배포될 주소를 발급받아 `homepage`에 입력해준다
6. 다시 프로젝트로 돌아와서 `npm run deploy`를 실행한뒤  `gh-pages` 브랜치가 생성된걸 확인후 다시 github에 올린다
7. repo에 `gh-pages`브랜치가 잘 올라왔는지 확인후 Source에서 브랜치를 `gh-pages`로 바꿔준다
8. 잠시후 이전에 받은 주소(https://dohyublee.github.io/react-deploy-test/) 로 접속해보면 배포가 된것을 확인할수있다
9. 

## Available Scripts

In the project directory, you can run:

### `npm start`

Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in the browser.

The page will reload if you make edits.\
You will also see any lint errors in the console.

### `npm test`

Launches the test runner in the interactive watch mode.\
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `npm run build`

Builds the app for production to the `build` folder.\
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.\
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.

### `npm run eject`

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

### `npm run build` fails to minify

This section has moved here: [https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify](https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify)
