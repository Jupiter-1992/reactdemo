This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Available Scripts

In the project directory, you can run:

### `npm start`

Runs the app in the development mode.<br>
Open [http://localhost:3000](http://localhost:3000) to view it in the browser.

The page will reload if you make edits.<br>
You will also see any lint errors in the console.

### `npm test`

Launches the test runner in the interactive watch mode.<br>
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `npm run build`

Builds the app for production to the `build` folder.<br>
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.<br>
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.

### `npm run eject`

**Note: this is a one-way operation. Once you `eject`, you can’t go back!**

If you aren’t satisfied with the build tool and configuration choices, you can `eject` at any time. This command will remove the single build dependency from your project.

Instead, it will copy all the configuration files and the transitive dependencies (Webpack, Babel, ESLint, etc) right into your project so you have full control over them. All of the commands except `eject` will still work, but they will point to the copied scripts so you can tweak them. At this point you’re on your own.

You don’t have to ever use `eject`. The curated feature set is suitable for small and middle deployments, and you shouldn’t feel obligated to use this feature. However we understand that this tool wouldn’t be useful if you couldn’t customize it when you are ready for it.

## Learn More

You can learn more in the [Create React App documentation](https://facebook.github.io/create-react-app/docs/getting-started).

To learn React, check out the [React documentation](https://reactjs.org/).

### Code Splitting

This section has moved here: https://facebook.github.io/create-react-app/docs/code-splitting

### Analyzing the Bundle Size

This section has moved here: https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size

### Making a Progressive Web App

This section has moved here: https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app

### Advanced Configuration

This section has moved here: https://facebook.github.io/create-react-app/docs/advanced-configuration

### Deployment

This section has moved here: https://facebook.github.io/create-react-app/docs/deployment

### `npm run build` fails to minify

This section has moved here: https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify


### 个人项目推送远程仓库功能测试记录
时间：20250718
工具：Copilot
内容：分别创建main分支及master分支，推送到远程仓库reactdemo
1. 创建main分支并推送到远程仓库
2. 创建master分支并推送到远程仓库   
3. 在main分支上修改文件，提交到本地仓库
4. 切换到master分支，查看main分支的修改内容
5. 将main分支的修改内容合并到master分支
6. 将master分支的修改内容推送到远程仓库
部分过程执行见test图片
测试结果：通过
涉及命令包括：
单独推送主分支
```
git add .
git commit -m "您的提交信息"
git push reactdemo master
```
其他分支切换到主分支后再合并分支修改内容
```
git status
git log --oneline -5
git branch -a
git remote -v
git checkout -b master
git diff
git diff --cached
git push reactdemo master
git fetch reactdemo
git branch -a
git checkout master
git status
git merge main
git merge main --allow-unrelated-histories
git add .gitignore
git commit -m "Merge main branch into master"
git push reactdemo master
```
### 项目启动
```
  npm install -g serve
  serve -s build
```