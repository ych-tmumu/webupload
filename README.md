# webupload
微信内置浏览器调用手机摄像头拍照上传


# 注意点
看webuploader.js 4883-4889行
这里是兼容ios，不处理的话ios默认只打开拍照上传而无法使用相册上传
另外
```
	if (!isIos && iswx) {
		input.attr('accept', 'image/*');
        	//input.attr('capture', 'camera');
	};
```
不要加capture，要不然微信内置浏览器还是打不开摄像头，上面的accept要这样写才行
