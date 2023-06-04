# build-cli
自动化打包脚本

## 设计使用 
模板选择
1.下载模板
2.使用模板
	输入模板地址 -> 校验正确性
	启用多线程打包
### 模板
```
module.export = {
	// 项目名称作为key
	webName: {
		tarName: '', // 压缩项目名，默认为项目名称
		branch: '', // 打包分支，默认为 dev
		mainDirection: '', // 主指令，拥有最高权限，会覆盖npmName指令，如需要多条指令，使用 `&&` 进行分隔 
		npmDirection: '', // 打包指令，默认为 build
		beforeNpmDirection: '', // 打包前额外指令，如需要多条指令，使用 `&&` 进行分隔 
		outputDir: '', // 打包输出到的文件夹，默认当前文件夹下 ./build
		outLog: true, // 是否进行日志输出，默认是
		isBuild: true, // 是否进行项目打包
	}，
	...
}
```js