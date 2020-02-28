# easy-egg-plugin-demo
One of the simplest egg plug-ins
一个最简单的egg插件开发示例
注：（此插件属于应用内部插件，即需要我们在自己的项目中创建lib/plugin/egg-test3）【egg-test3即是我们新创建的插件的名字】
开发步骤：
1.创建egg-test3文件夹并打开
2.npm init egg --type=plugin
3.创建过程中有一步骤是输入插件的名字，此处直接输入你egg-test3后面的test3即可，她会自动在前面加上egg-
4.创建完毕后，可以查看一下package.json，有两处比较重要的地方"eggPlugin": { "name": "test3" } 和"name": "egg-test3"
5.我们exports.的test3就是eggPlugin中的名字
6.然后我们就可以通过this.app.我们插件当中暴露出来的方法名，属性名等调用他们


引用方式：
在config/plugin.js中配置如下
const path = require("path");
exports.test3 = {
  enable: true,
  path: path.join(__dirname, '../app/lib/plugin/egg-test3'),
}

参考：https://incca.cn/egg-framework-4/
