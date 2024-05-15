## npm私服安装和启动
1.npm install -g verdaccio # 安装 verdaccio
2.verdaccio --listen http://192.168.40.11:4873 #服务启动
3.访问http://192.168.40.11:4873/

### 发布
0.进入需要发布的工程，例如ep-ui
1.npm adduser --registry http://192.168.40.11:4873/ #npm 账号设置
根据提示输入，例如：
Username: liangshanshan
Password: aaa111
Email: (this IS public) sandycoding@163.com
Logged in as liangshanshan on http://192.168.40.11:4873/.
2.npm publish --registry http://192.168.40.11:4873/
3.刷新http://192.168.40.11:4873/

### 安装包
1. nrm add sanjie http://192.168.40.11:4873
2. nrm use sanjie
3. npm i @sandy/ep-ui

### 关联配置
例如：
ep-ui/package.json 配置项：
"publishConfig": {
  "registry": "http://192.168.40.11:4873"
}
