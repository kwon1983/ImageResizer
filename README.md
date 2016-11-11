# ImageResizer
* 이미지 파일을 리사이징 해줌
* 사진 첨부파일 업로드 시에 네트워크 사용을 최소화 시키기 위함
* exception!! 만약 img 태그를 사용할 경우 브라우저 보안정책에 의해 동일 도메인의 이미지만 올릴 수 있음

/**
 * 사용법
 * controller에 ImageResizer 인젝션

 *
 * option
 * image: image data(file or img) require
 * width, height or ratio 둘중 하나 require
 * width: 사이즈로 변경
 * height: 사이즈로 변경
 * ratio: 비율로 변경 (0.0 ~ 1.0)
 * returnType: blob or file(string) 리턴받을 이미지 타입 default image
 **/

## 사용법
```javascript
ImageResizer.resize({
	image: file,
	width: 140,
	height: 140,
	ratio: 0.5,
	returnType: 'blob'
}).then(function(resizeFile) {
	console.log(resizeFile);
});
```

### resieze(options)

* image(require)
 * image data(file or img)
* width, height(require)
 * 사이즈로 변경
 * ratio 둘중 하나 require
* ratio(require)
 * 비울로 변경 
* returnType
 * blob or file(string) 리턴받을 이미지 타입 default image
