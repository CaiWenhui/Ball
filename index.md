
<head>
<meta http-equiv="Content-Type" content="text/html; charset=utf-8" />
<title>小球测验</title>
<script>
        function test_ball()
        {
            var s=document.getElementById("s_num").value;
            var n=document.getElementById("n_num").value;
            
            var s_number = eval(s);
            var n_number = eval(n);

            var arrays = new Array();

            for (var i = 0; i <= s_number; ++i)
            {
                arrays[i] = new Array();
            }

            for(var i = 0; i <= n_number; ++i)
            {
                arrays[0][i] = 0;
            }

            console.log("abc");

            for (var i = 0; i <= s_number; ++i)
            {
                arrays[i][0] = 0;
            }

            for(var row = 1; row <= s_number; ++row)
            {
                var sum = 0;
                for(var col = 1; col <= n_number; ++col)
                {
                    sum += arrays[row - 1][col - 1];
                    arrays[row][col] = sum + col;
                }
            }

            var floor = arrays[s_number][n_number];

            var floor_text = document.getElementById("floor_num");
            floor_text.value = floor;
        }
</script>
</head>

<body bgcolor = "#2B3137">
<h1 align = "center"><font color="#FFFFFF">小球测验</font></h1>
<h4 align = "center"><font color="#FFFFFF">在下列框内填入小球的数目以及抛球次数等信息</font></h4>
<h4 align = "center"><font color="#FFFFFF">我们会为您求出该条件下小球可测量范围！</font></h4>
</br>
</br>
</br>
<form> 
        <table width="300" border="1" align="center" style="border:transparent; background-color: white; padding: 20px; border-radius:25px">
            <tr>
                <td style="font-size: 10px"><font color="#586069">小球数目</font></td>
            </tr>
            <tr>
                <td><input id="s_num" type=text placeholder="请输入小球数目" style="padding: 7px"/></td>
            </tr>
            <tr>
                <td style="font-size: 10px"><font color="#586069">抛球次数</font></td>
            </tr>
            <tr>
                <td><input id="n_num" type=text placeholder="请输入抛球次数" style="padding: 7px"/></td>
            </tr>
            <tr>
                <td style="font-size: 10px"><font color="#586069">可测量楼层数</font></td>
            </tr>
            <tr>
                <td><input id="floor_num" type=text style="padding: 7px"/></td>
            </tr>
            <tr>
                <td></td>
            </tr>
        </table>    
</form>
<div align="center">
<button ondblclick="test_ball()">开始测试</button>
</div>
</br>

<div align="center">
<a href =‘’ align = "center"><font color="#FFFF00">点击此处观看推导过程</font></a>
</div>
</body>
</html>
