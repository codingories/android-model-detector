### 用于查询ios具体机型,整合了以下两个仓库
- [mobile-device-js](https://github.com/joyqi/mobile-device-js),这个仓库目前不能准确识别ios显卡，于是整合了下面这个仓库解决这个问题
- [Renderer](https://github.com/51Degrees/Renderer),用于发现ios设备的显卡型号
- 如果要求不高，不需要具体型号可以直接用，[mobile-detect](https://github.com/hgoebl/mobile-detect.js/)

### 使用方法
```html
 <script src="ios-model-detector.js"></script>
  <script>
    window.onload=function(){
      let config_device_model = MobileDevice.getModels()[0]
      document.getElementById("modelText").innerHTML = config_device_model;
    }
  </script>
```
