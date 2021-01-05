### 用于查询安卓具体机型,整合了以下两个仓库
- 查询品牌是用了，[mobile-detect](https://github.com/hgoebl/mobile-detect.js/)
- 查询具体型号是自己手写的
### 查询具体型号代码
```js
  let config_device_model;
 function contains(needle, list) {
     for (let i in list) {
       if (list[i].indexOf(needle) > 0)
         return i;
     }
     return -1;
   }
   let config_device_model;
   let sss = user_agent.split(";");
   //判断UA里边有没有Build信息，通过这个拿到安卓的具体机型
   let i = contains("Build/", sss);
   if (i > -1) {
     let newMobile = sss[i].substring(0, sss[i].indexOf("Build/"));
     console.log('newMobile', newMobile)
     config_device_model = newMobile
   }else{
     config_device_model = 'unknown'
   }
```
