<!DOCTYPE html>
<html lang="en">

<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Table Display</title>

<style>
table {
	font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
	width: 40%;
	border: 1px solid black;
	border-collapse: collapse;
	margin: 20px 0;
	font-size: 18px;
	text-align: center;
}

th,td{
	padding: 10px;
	border: 1px solid black;
	text-align: center;
}

th{
	background-color: #ff9999;
	color: black;
	font-weight: bold;
}

tr:nth-child(odd){
	background-color: #fae3d9;
}

tr:nth-child(even){
	background-color: white);
}

</style>
</head>

<body>

<h1>Table Result Display</h1>

<hr>

<h2>Table 1</h2>
<table id="table1">
<thead>
<tr>
<th>Index</th>
<th>Value</th>
</tr>
</thead>
<tbody>
</tbody>
</table>
 
<hr>
 
<h2>Table 2</h2>
<table id="table2">
<thead>
<tr>
<th>Category</th>
<th>Value</th>
</tr>
</thead>
<tbody>
</tbody>
</table>
    
<script>
// Table 1 values
const table1Values = [ 41, 18, 21, 63, 2, 53, 5, 57, 60, 93, 28, 3, 90, 39, 80, 88, 49, 60, 26, 28 ];
        
// Table 1
const table1Body = document.querySelector('#table1 tbody');
table1Values.forEach((value, index) => {
const row = document.createElement('tr');
const indexCell = document.createElement('td');
indexCell.textContent = 'A' + (index + 1);
const valueCell = document.createElement('td');
valueCell.textContent = value;
row.appendChild(indexCell);
row.appendChild(valueCell);
table1Body.appendChild(row);
});
        
// Calculate Table 2 values
const alpha = table1Values[4] + table1Values[19]; 
const beta = table1Values[14] / table1Values[6];  
const charlie = table1Values[12] * table1Values[11]; 
        
// Table 2
const table2Body = document.querySelector('#table2 tbody');
const categories = [
{ name: 'Alpha', value: alpha },
{ name: 'Beta', value: beta },
{ name: 'Charlie', value: charlie }
];
        
categories.forEach(category => {
const row = document.createElement('tr');
const nameCell = document.createElement('td');
nameCell.textContent = category.name;
const valueCell = document.createElement('td');
valueCell.textContent = category.value;
row.appendChild(nameCell);
row.appendChild(valueCell);
table2Body.appendChild(row);
})
</script>
</body>
</html>
