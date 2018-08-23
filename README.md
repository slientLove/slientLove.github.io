## puppeteer做性能分析
puppeteer可以用来做比较多的东西，中文文档:https://www.v2ex.com/t/461454，
针对网页请求方面，可以通过获取类似于谷歌浏览器控制台中
的network拿到数据进行图表分析。



// projectName就是package.json里面项目名称

webpack多入口文件配置：
entry:{
   'home':"/pages/home/js/home.js",
   'coking':"./pages/coking/js/coke.js"   // 每个页面的入口js文件需要进行配置
   ...
},
output:{
  path:__dirname+'../../../dist',
  publicPath:"/futures-web-dist",     // 通过publicPath访问静态文件，存在于内存中的虚拟目录
  filename:"js/"+projectName+"/[name].js"   // [name]就是上面配置的名称，如home和coking
}
