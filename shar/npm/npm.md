内容大纲

PDF

 PDF



补充
1. npmignore
使用npm发布包的时候，在当前文件夹下有些文件是不希望发布的，可以创建一个 .npmignore 文件里面包含 /test，这样在运行 npm publish 打包时，可以避免将该文件夹打包到项目中。

相对应的 

使用npm发布包的时候, 想要指定某个文件夹发布到npm, 可以设置package.json中的files字段

注意：npm 会默认包含 README，package.json 和一些其他文件，因此你不需要特意指定它们。

2. npm pack
npm pack 打包 package.tgz
npm install package.tgz   # 安装压缩包


3. 发布npm包流程
https://juejin.im/post/6877768129745944589



4. package.json全属性介绍（后续可补充）
属性	作用	例子
Description
包的描述	略
name
包名	略
version
包版本	1.1.0
keywords
包关键词	略
homepage
项目主页的地址

https://github.com/vuejs/vue
bugs
项目问题跟踪的issue url和邮件地址。这些对遇到包问题的人很有帮助。

{

"url" : "https://github.com/owner/project/issues"，
"email" : "project@hostname.com"
}

license
许可证，开源许可证为MIT

{ "license" : "BSD-3-Clause" }

or 

{

"license" : {

   "type" : "ISC",
    "url" : "https://opensource.org/licenses/ISC"
  }
}

funding
可以指定一个对象，该对象包含一个URL，该URL提供有关帮助您的包开发资金的最新信息，或者指定一个字符串URL，或者一个数组

"funding": [
{
"type" : "individual",
"url" : "http://example.com/donate"
},
"http://example.com/donateAlso",
{
"type" : "patreon",
"url" : "https://www.patreon.com/my-account"
}
]

files
指定npm要发布的目录	"files": ["src"]
main
定义 npm 包在 node 环境下的入口文件, 它是程序的主要入口点。也就是说，如果包名为foo，并且用户安装了它，然后确实需要require（“foo”），那么将返回主模块的exports对象。

推荐文章https://segmentfault.com/a/1190000019438150

browser
定义 npm 包在 browser 环境下的入口文件
module
定义 npm 包在 esmodule 环境下的入口文件
repository
指定代码所在的位置。这对那些想做贡献的人很有帮助

"repository": {
"type" : "git",
"url" : "https://github.com/npm/cli.git"
}

"repository": {
"type" : "svn",
"url" : "https://v8.googlecode.com/svn/trunk/"
}

scripts
可以执行node脚本	
dependencies
生产依赖	
devDependencies
开发依赖	
peerDependencies

推荐文章

https://www.cnblogs.com/wonyun/p/9692476.html

bundledDependencies
可以指定npm pack时 一起pack的包	
optionalDependencies

推荐文章

https://docs.npmjs.com/cli/v6/configuring-npm/package-json#optionaldependencies

engines
指定node版本	
os
指定操作系统	
private
为true时 拒绝发布	
