<html>
  <head>
  </head>
  <body>
    <script>
    function homePageLoading() {
    url = 'https://api.blockcypher.com/v1/btc/main';
    elementID = 'https://sofiane-a.github.io/bitcoin/index.html';
    fonctionRequeteApi(url, elementID);
      var xmlhttp = new XMLHttpRequest();
      xmlhttp.onreadystatechange = function() {
      if (this.readyState == 4 && this.status == 200) {
        var myObj = this.responseText;
        var jsonPretty = JSON.stringify(JSON.parse(myObj),null,2);
        document.getElementById("demo").innerHTML = jsonPretty;
        }
      };
      xmlhttp.open("GET", "https://api.blockcypher.com/v1/btc/main", true);
      xmlhttp.send();
    }
    </script>
    <div class="row">
	<div class="col-lg-12 col-xs-6">
    	<pre>
        	<code id="demo" class="json kljs"></code>
    	</pre>
	</div>
</div>
  </body>
</html>
