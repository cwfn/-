<!DOCTYPE html>
<html>
	<head>
		<meta charset="UTF-8">
		<title></title>
	</head>
	<body>
		<div>
			<input type="button" value="点击给出随机数字" onclick="random()"/>
			<input type="button" id="inputid2" value="显示答案" onclick="show()"/>
			<p id="pid"></p>
			<br />
			<h3>请输入四位不同的数字</h3>
			<input id="inputid" type="text" />
			<input type="button" value="确定"  onclick="adjust()"/>
			<p id="pid2"></p>
			<input type="text" id="textid" style="height: 200px;"/>
		</div>
		
		<script>
			function random(){
                a=Math.ceil(Math.random()*1000000000%9);
				b=Math.ceil(Math.random()*1000000000%9);
				c=Math.ceil(Math.random()*1000000000%9);
				d=Math.ceil(Math.random()*1000000000%9);
				for(var i=0;i<1000;i++){
					if(a!=b){
						if(a!=c){
							if(a!=d){
								if(b!=c){
									if(b!=d){
										if(c!=d){	
											e=(a*1000+b*100+c*10+d);
											alert("成功给出数字");
											break;
										}
									}
								}
							}
						}
					}else{
					b=Math.ceil(Math.random()*1000000000%9);
					c=Math.ceil(Math.random()*1000000000%9);
				    d=Math.ceil(Math.random()*1000000000%9);
				    }
				}
            }
			function show(){
				document.getElementById("pid").innerHTML=e;
			}
			
			function adjust(){
				var i=document.getElementById("inputid").value;
				var d1 = parseInt(i%10);
                var c1 = parseInt((i/10)%10); 
                var b1 = parseInt((i/100)%10);
                var a1 = parseInt(i/1000);
                var count=0;
                var count1=0;
                count
                if(a1==a){count++;}
                if(a1==b){count1++;}
                if(a1==c){count1++;}
                if(a1==d){count1++;}
                
                if(b1==a){count1++;}
                if(b1==b){count++;}
                if(b1==c){count1++;}
                if(b1==d){count1++;}
                
                if(c1==a){count1++;}
                if(c1==b){count1++;}
                if(c1==c){count++;}
                if(c1==d){count1++;}
                
                if(d1==a){count1++;}
                if(d1==b){count1++;}
                if(d1==c){count1++;}
                if(d1==d){count++;}
                
                
                //document.getElementById("pid2").innerHTML=(i+"   "+count+"A"+count1+"B");
                
                var oText=document.getElementById('textid');
                oText.value=i+"   "+count+"A"+count1+"B";
                
                
                if(count!=4){
                	
                }
            }
		</script>
		
	</body>
</html>
