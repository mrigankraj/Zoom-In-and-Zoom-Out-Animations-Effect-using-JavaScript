# Zoom-In-and-Zoom-Out-Animations-Effect-using-JavaScript
Basic Zoom In and Zoom Out animations using JavaScript. 
Note: Add a image of your choice in your code directory or create a separate directory for images and add it into it and use that location in this code

<html>
	<head>
 		<title>Basic Animations Part 2 - scaling</title>
		<script type="text/javascript">
		
		var width=100;
		var difference=2;
		var interveralID =0;
		//document.getElementById("img1").style.width=width;

		function increase()
		{
			clearInterval(interveralID);
			interveralID=setInterval(expand,10);
		}
		function decrease()
		{
			clearInterval(interveralID);
			interveralID=setInterval(shrink,10);
		}
		function expand()
		{
			if(width<200)
			{
				width = width+difference;
				document.getElementById("img1").style.width=width;
				console.log(width);
			}
			else
			{
				clearInterval(interveralID);
			}
			
		}
		function shrink()
		{
			if(width>100)
			{
				width = width-difference;
				document.getElementById("img1").style.width=width;
				console.log(width);
			}
			else
			{
				clearInterval(interveralID);
			}
			
		}
	
		</script>
	</head>
	<body>
	
		<br>
		<br>
		<img onmouseover="increase()" onmouseout="decrease()" id="img1" src="imgs/heart.png" width="100"/>
	</body>

</html>
