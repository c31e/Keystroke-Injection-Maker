<html>
<head>
<style>
#code {
    
    border-style: solid;
    border-width: thin;
    border-color: #000000;
    width: 49.5%;
    float: right;
	padding: 10px;
	-webkit-box-sizing: border-box; /* Safari/Chrome, other WebKit */
-moz-box-sizing: border-box;    /* Firefox, other Gecko */
box-sizing: border-box;         /* Opera/IE 8+ */
	margin: 0;
 
}
.select {
    position: relative;
    display: inline-block;
    width: 40%;
}
.select select {
    display: inline-block;
    width: 100%;
    cursor: pointer;
    padding: 10px 15px;
    outline: 0;
    border: 0;
    border-radius: 0;
    background: #e6e6e6;
    color: #7b7b7b;
    appearance: none;
    -webkit-appearance: none;
    -moz-appearance: none;
}
.select select::-ms-expand {
display: none;
}
.select select:hover, .select select:focus {
    color: #000;
    background: #ccc;
}
.select__arrow {
    position: absolute;
    top: 16px;
    right: 15px;
    width: 0;
    height: 0;
    pointer-events: none;
    border-style: solid;
    border-width: 8px 5px 0 5px;
    border-color: #7b7b7b transparent transparent transparent;
}
.select select:hover ~ .select__arrow, .select select:focus ~ .select__arrow {
    border-top-color: #000;
}
table {
	margin-top: 20px;
    border-collapse: collapse;
    width: 100%;
}
th, td {
    
    text-align: left;
    border-bottom: 1px solid #ddd;
}
tr:hover {
    background-color: #f5f5f5;
}
	
	.title{
		font-family:"atomic-age";
		font-weight:900;
		margin:5px 0 0 0;
	}
	.description{
	margin:5px 0 5px 0;
		color:#575757;
		margin: 10px 0 10px 0; 	
		
	}
	.os{
		font-size: 13px;
		float: left;
		
		margin: 0;
	}
	
	.type{
		float: right;
			font-size: 13px;
		margin: 0;
		padding:0;
		
	}
	#menu{
		width:49.5%;
		float:left;
	}
</style>
</head>
<body>
	<div id="menu">

<div class="select">
  <select>
    <option>Windows 10</option>
    <option>Linux</option>
    <option>Mac OS</option>
  </select>
  <div class="select__arrow"></div>
</div>
<div class="select">
  <select>
    <option>Prank</option>
    <option>Malicious</option>
    <option>Reconnaissance</option>
  </select>
  <div class="select__arrow"></div>
</div>
<table>
  <tr>
    	<td>
		<p class="title">Play Youtube Video</p>
		<p class="description">Opens up Youtube link in default browser, plays video and makes it full screen.</p>
	  	<p class="os">Windows 10</p>
		<p class="type">Prank</p>
		</td>
  </tr>
  <tr>
    <td>
		<p class="title">Play Youtube Video</p>
		<p class="description">Opens up Youtube link in default browser, plays video and makes it full screen.</p>
	  	<p class="os">Windows 10</p>
		<p class="type">Prank</p>
		</td>
  </tr>
  <tr>
    <td>
		<p class="title">Play Youtube Video</p>
		<p class="description">Opens up Youtube link in default browser, plays video and makes it full screen.</p>
	  	<p class="os">Windows 10</p>
		<p class="type">Prank</p>
		</td>
  </tr>
 
</table>
		</div>
<pre id="code">GUI r
DELAY 500
STRING notepad.exe
ENTER
DELAY 1000
STRING Hello World!</pre>
</body>
</html>
