<div id="main">

<div id="menu">

<div class="select"><select id="osSelect" onchange="refresh()"><option>All</option> <option>Windows 10</option> <option>Linux</option> <option>Mac OS</option></select></div>

<div class="select"><select id="typeSelect" onchange="refresh()"><option>All</option> <option>Prank</option> <option>Malicious</option> <option>Reconnaissance</option></select></div>

<table id="mainTable"></table>

</div>

<pre id="code">GUI r
DELAY 500
STRING notepad.exe
ENTER
DELAY 1000
STRING Hello World!</pre>

</div>

<script>function clean(){ var table = document.getElementById("mainTable"); var length = table.querySelectorAll("tr").length; console.log("removing "+length+ "rows"); var length = table.rows.length; for(var x = 0; x <length; x++) { table.deleteRow(0); } } function populate(title,description,os,type,code) { console.log("populate"); var table = document.getElementById("mainTable"); var titleElement = document.createElement('p'); titleElement.className = "title"; titleElement.innerHTML = title; var descriptionElement = document.createElement('p'); descriptionElement.className = "description"; descriptionElement.innerHTML = description; var osElement = document.createElement('p'); osElement.className = "os"; osElement.innerHTML =os; var typeElement = document.createElement('p'); typeElement.className = "type"; typeElement.innerHTML = type; var sel1 = document.getElementById('osSelect'); var sel2 = document.getElementById('typeSelect'); var sel1Types = ["all","Windows 10","Linux","Mac"]; var sel2Types = ["all","Prank","Malicious","Reconnaissance"]; if ((sel1Types[sel1.selectedIndex]==os || sel1.selectedIndex==0) && (sel2Types[sel2.selectedIndex]==type || sel2.selectedIndex==0)){ console.log("other"); var row = table.insertRow(0); var cell1 = row.insertCell(0); cell1.append(titleElement,descriptionElement,osElement,typeElement); var createClickHandler = function(row) { return function() { var codeElement = document.getElementById("code"); codeElement.innerHTML = code; }; }; row.onclick = createClickHandler(row); return; } } function refresh(){ console.log("start"); clean(); $.getJSON( "test.json", function( json ) { console.log(json); for(var i = 0; i < json.length; i++) { populate(json[i].title,json[i].description,json[i].os,json[i].type,json[i].code); } }); } function func1() { refresh(); } window.onload=func1;</script>
