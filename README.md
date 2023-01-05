## 安装脚手架

npm install -g yo generator-code

yocode



## 自定义修改

### let disposable = vscode.commands.registerCommand('demo.helloWorld', ()

​    vscode.commands.executeCommand(

​      "vscode.open",

​      vscode.Uri.parse(`https://baidu.com`)

​     );

## 打包vsix流程

- 命令行根目录安装打包依赖
  - npm -i -g vsce
- 打包前准备
  - package.json检查属性
    - "publisher"：“demo”
    - "repository": {}
  - 修改readme.md
- 文件目录命令行执行打包命令
  - vsce package

- 修改readme

# 流程

1、安装npm脚手架环境

2、打开目标路径cmd 输入yo code

3、进行初始化配置


- 个性配置项对应关系：


- ​	identifier：文件夹名


- extensionname：插件名称
- publisher：发布者
- description：插件描述


4、指令名称及跳转方法配置在package.json

5、具体指令逻辑在extension.js

6、指令依赖关系为contributes.commands	->	activationEvents	->	extension.js.registerCommand
