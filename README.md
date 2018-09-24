
## 为什么会有这个项目

大部分的javascript模板轮子，模板语言都是在<script></script>中实现。
剥离出来的这个轮子，可以直接在html定义好模板语言，然后引入数据实现。



  <div id="github">
  <div id="githubs">
        <a href="{{data.login1.0.url1}}">
          <h3>{{data.login1.0.url2}}</h3>
          <img src='{{data.login1.0.url3}}'>
        </a>
      </div></div>
  <script>
    dug({
		cachedData : {
		  "data": 
				{
				"login1": [
					{
						'url1':"https://avatars2.githubusercontent.com/u/1577835?v=4",
						'url2':"https://avatars2.githubusercontent.com/u/1577835?v=4",
						'url3':"https://avatars2.githubusercontent.com/u/1577835?v=4",
					},
					{
						'url1':"https://avatars2.githubusercontent.com/u/1577835?v=4",
						'url2':"https://avatars2.githubusercontent.com/u/1577835?v=4",
						'url3':"https://avatars2.githubusercontent.com/u/1577835?v=4",
					}
				]
			}
		},
      target: 'github',
      error: function(){
        console.log('error');
      },
      template: document.getElementById('githubs').innerHTML,
    });
  </script>