# Part 3 JavaScript & jQuery

# 第12章 JavaScript 基本語法
###

>*Hello JavaScript!
```
<!doctype html>  
<html>
  <head>
    <meta charset="utf-8">
	<title>第一個JavaScript程式</title>
	<script language="javascript">
      <!--
        alert("Hello JavaScript!");
      //-->
    </script>
  </head>	
  <body>    
  </body>
</html>
...

###

>*hello2
...
<!doctype html>  
<html>
  <head>
    <meta charset="utf-8">
	<title>第一個JavaScript程式</title>	
  </head>	
  <body>
    <script language="javascript">
      <!--
        alert("Hello JavaScript!");
      //-->
    </script>
  </body>
</html>
...

###

>*hello3
...
<!doctype html> 
<html>
  <head>
    <meta charset="utf-8">
    <title>第一個JavaScript程式</title>	
  </head>	
  <body>
    <h1 onclick="javascript:alert('Hello JavaScript!')">歡迎光臨JavaScript的世界！</h1>
  </body>
</html>
...

###

>*hello4
...
<!doctype html> 
<html>
  <head>
    <meta charset="utf-8">
    <title>第一個JavaScript程式</title>	
    <script src="FirstJavaScript.js" language="javascript"></script>
  </head>	
  <body>
  </body>
</html>
...

###

>*if1
...
<!doctype html> 
<html>
  <head>
    <meta charset="utf-8">
    <title>流程控制範例</title>
    <script language="javascript">
      var X = prompt("請輸入0-100的數字", "");
      if (X >= 60) alert("及格！");
    </script>
  </head>
  <body>
  </body>
</html>

...

###

>*if2
...
<!doctype html> 
<html>
  <head>
    <meta charset="utf-8">
    <title>流程控制範例</title>
    <script language="javascript">
      var X = prompt("請輸入0-100的數字", "");
      if (X >= 60) 
        alert("及格！");
      else
        alert("不及格！");
    </script>
  </head>
  <body>
  </body>
</html>

...

###

>*if3
...
<!doctype html> 
<html>
  <head>
    <meta charset="utf-8">
    <title>流程控制範例</title>
    <script language="javascript">
  var X = prompt("請輸入0-100的數字", "");
  if (X >= 90)
    alert("優等！");
  else if (X < 90 && X >= 80)
    alert("甲等！");
  else if (X < 80 && X >= 70)
    alert("乙等！");
  else if (X < 70 && X >= 60)
    alert("丙等！");
  else
    alert("不及格！");
    </script>
  </head>
  <body>
  </body>
</html>

...

###

>*switch
...
<!doctype html>
<html>
  <head>
    <meta charset="utf-8">
    <title>流程控制範例</title>
    <script language="javascript">
  var X = prompt("請輸入1-5的數字", "");
  switch(X)
  {
    case "1":    	//當使用者輸入1時
      alert("ONE");
      break;
    case "2":    	//當使用者輸入2時
      alert("TWO");
      break;
    case "3":    	//當使用者輸入3時
      alert("THREE");
      break;
    case "4":    	//當使用者輸入4時
      alert("FOUR");
      break;
    case "5":    	//當使用者輸入5時
      alert("FIVE");
      break;
    default:    	//當使用者輸入1-5以外的數字時
      alert("您輸入的數字超過範圍！");
      break;
  }
    </script>
  </head>
  <body>
  </body>
</html>

...

###

>*for
...
<!doctype html>
<html>
  <head>
    <meta charset="utf-8">
    <title>流程控制範例</title>
    <script language="javascript">
  var X = prompt("請輸入正整數", "");
  var Total = 0;
  for (var i = 1; i <= X; i++)
  {
    Total = Total + i;			//這行敘述也可以改寫為Total += i;
  }
  alert(Total);

    </script>
  </head>
  <body>
  </body>
</html>

...

###

>*while
...
<!doctype html>
<html>
  <head>
    <meta charset="utf-8">
    <title>流程控制範例</title>
    <script language="javascript">  
        var Number = prompt("請輸入1-10的數字", "");
  while(Number != 6)
  {
    if (Number > 6)       									//太大了繼續做答
    {
      alert("太大了！請重新輸入！");
      Number = prompt("請輸入1-10的數字", "");
    }
    else if (Number < 6)  										//太小了繼續做答
    {
      alert("太小了！請重新輸入！");
      Number = prompt("請輸入1-10的數字", "");
    }
  }
  alert("答對了！");

    </script>
  </head>
  <body>
  </body>
</html>

...

###

>*do
...
<!doctype html>
<html>
  <head>
    <meta charset="utf-8">
    <title>流程控制範例</title>
    <script language="javascript">
  do
  {
    Number = prompt("請輸入1-10的數字", "");
    if (Number > 6)        	//太大了繼續做答
    {
      alert("太大了！請重新輸入！");
    }
    else if (Number < 6)  		//太小了繼續做答
    {
      alert("太小了！請重新輸入！");
    }
  }while(Number != 6)
  alert("答對了！");
  </script>
  </head>
  <body>
  </body>
</html>

...

###

>*forin
...
<!doctype html>
<html>
  <head>
    <meta charset="utf-8">
    <title>流程控制範例</title>
    <script language="javascript">
      var Students = new Array("三上悠亞", "蒼井空", "波多野結衣");	//宣告包含三個元素的陣列
      for (var i in Students)
      {
        alert(Students[i]);
      }
    </script>
  </head>
  <body>
  </body>
</html>

...

###

>*func1
...
<!doctype html>
<html>
  <head>
    <meta charset="utf-8">
    <title>函式範例</title>
    <script language="javascript">
      function Greeting()		//宣告函式
      {
        var UserName = prompt("請輸入您的大名", "");
        alert(UserName + "您好！歡迎光臨！");
      }
      Greeting();				//呼叫函式
    </script>
  </head>
  <body>
  </body>
</html>

...

###

>*func2
```
<!doctype html>
<html>
  <head>
    <meta charset="utf-8">
    <title>函式範例</title>
    <script language="javascript">
      function Greeting()		//宣告函式
      {
        var UserName = prompt("請輸入您的大名", "");
        alert(UserName + "您好！歡迎光臨！");
      }      
    </script>
  </head>
  <body>
    <h1><a href="javascript:Greeting()">點取此處以顯示歡迎訊息</a></h1>
  </body>
</html>

...

###

>*func3
```
<!doctype html>
<html>
  <head>
    <meta charset="utf-8">
    <title>函式範例</title>
    <script language="javascript">
      function Convert2F(DegreeC)	//宣告名稱為Convert2F、參數為DegreeC的函式
      {
        var DegreeF = DegreeC * 1.8 + 32;
        alert("攝氏" + DegreeC + "度可以轉換為華氏" + DegreeF + "度");
      }
      var Temperature = prompt("請輸入攝氏溫度", "");
      Convert2F(Temperature);		//呼叫函式時要將輸入的攝氏溫度當成參數傳入
    </script>
  </head>
  <body>
  </body>
</html>

...

###

>*
```

...

###

>*
```

...


# 第13章 物件、DOM 與事件處理
###

>*
```

...

# 第14章 jQuery
###

>*
```

...

#Part 4 響應式網頁設計 & Bootstrap

# 第15章 使用 Bootstrap 開發響應式網頁
###

>*
```

...

# 第16章 Bootstrap 元件
###

>*
```

...

# 第17章 jQuery 外掛
###

>*
```

...

# Part 5 行動網頁設計 & jQuery Mobile 

# 第18章 使用 jQuery Mobile 開發行動網頁 
###

>*
```

...

# 第19章 jQuery Mobile UI 元件
###

>*
```

...


