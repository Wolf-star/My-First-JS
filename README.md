# My-First-JS

<!doctype html>
<html>
<head>
<meta charset="utf-8">
<title>blur</title>
</head>
<body>
<input id="fina__amount" onblur="check()">

	
</body>
</html>	
<script>
	var input = document.getElementById('fina__amount');
	input.onblur = function check(){
		var reg = /^\d+(?=\.{0,1}\d+$|$)/;
			if(!(reg.test(input.value))){
				input.style='border:1px solid red';
				alert('金额有误，请重新输入');
			}else{
				input.style='border: 1px solid #d5d5d5';
			};
}

/*Jquery方法
$("#FinancialModal").on("blur", "#fina__amount", function(e){
    var num = $(this).val();
    if (num < 0){
        $("#FinancialModal .btn").hide()
        alert("不能小于零")
    } else {
        $("#FinancialModal .btn").show()
    }
});
*/
</script>
