# goland项目External Libaries下没有Go Modules

- 项目代码之前都正常运行，一段时间后再打开提示找不到依赖包
- 本地`go get`可以正常下载依赖包
- 新建项目可以正常使用依赖包
- goland终端里`go get`依赖包报错`go list -m: github.com/gohouse/e@v0.0.3-rc.0.20200724104652-25ebf8c9c305: invalid pseudo-version: preceding tag (v0.0.3-rc) not found`
- 找到网上文章说`go mod`记录版本时间戳和远程不一致[https://blog.cocktail1024.top/archives/130.html](https://blog.cocktail1024.top/archives/130.html)
- 想直接重建本地当前项目modules
- 查找`go mod`并测试到`go mod why`
- 惊奇发现问题解决
- 但这命令说明也不是更新依赖包
