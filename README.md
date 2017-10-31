# `<things-random-grid>`
## 1. 개요
#### 개발의 필요에 의하여 필요한 데이터를 그리드 설저하지 않고 내용 그대로 표현하면 되는 경우 해당 컴포넌트를 사용한다.

## 1.1 예시
```
<link rel="import" href="bower_components/things-random-grid/things-random-grid.html">
```

사용 예)
```
	<things-random-grid 
		id="grid"
		hidden-columns = "customer_id,sales_order_id"
		data-set = [[configedData]]>
	</things-random-grid>
```

아래처럼 그리트 칼럼의 스타일을 지정해 줄수 있다.
```javascript
	this.$.grid.applyColumnStyle = function(key,columnConfig,record){
              if(key == 'rownum_') {
                columnConfig.width = 50;

              } else if(key.indexOf('name')>0) {
                columnConfig.width = 200;

              } else if(key == 'id') {
                columnConfig.width = 180;

              } else if(key == 'name') {
                columnConfig.width = 150;

              } else if(key == 'description') {
                columnConfig.width = 250;

              }
              return columnConfig;
            }
```



## 2. 개발
### 2.1 Polymer-CLI 설치

First, make sure you have the [Polymer CLI](https://www.npmjs.com/package/polymer-cli) installed. Then run `polymer serve` to serve your application locally.

### 2.2 Application 수행

```
$ polymer serve
```

### 2.3 Application 빌드

```
$ polymer build
```

아래 명령어로 ` build/bundled`나 ` build/unbundled`에서 서버를 띄울수 있다.

```
$ polymer serve build/bundled
```

### 2.3 Running Tests

```
$ polymer test
```

테스트는 [web-component-tester](https://github.com/Polymer/web-component-tester)에서 설명한데로 설정완료됨.
아래 명령어로 테스트를 수행할 수 있다.
```
$ polymer test
```
