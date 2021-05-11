<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<meta name="viewport" content="width=device-width,initial-scale=1">
		<title></title>
		<link rel="stylesheet" href="../css/bootstrap.min.css">
		
	</head>
	<body>
		<div class="container">
			<h3 class="text-center text-info">警告框alert</h3>
		<div class="alert alert-danger" id="alert">
			<a href="#" class="close" data-dismiss="alert">&times;</a>
	<strong> 警告</strong>
	
		</div>
		
		<!-- 在alert以外的div的button要想关闭警告框则需要 使用data-dismiss="alert" data-target="#alert" -->
		<button class="close" data-dismiss="alert" data-target="#alert" type="button">关闭</button>
		</div>
	</body>
	<script src="../js/jquery-3.4.1.min.js" ></script>
	<script src="../js/bootstrap.min.js" ></script>
	<script>
		$(document).ready(function(){
			$(".alert").alert();
			$(".alert").on("close.bs.alert",function(){
				alert("close.bs.alert");	
			}).on("closed.bs.alert",function(){
				alert("closed.bs.alert");
			})
		})
	</script>
</html>
