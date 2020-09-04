
<html>
 <head> 
  <meta charset="utf-8"> 
  <style>
    body{
      background-color: powderblue;
    }
     p { color:black;
     text-align:center;
     padding:5px;
       }
  table {
  font-family: Verdana;
  border-collapse: collapse;
  margin: 50px auto;
  width: 50%;
}
td, th {
  border: 1px solid #dddddd;
  text-align: left;
  padding: 5px;
  font-size: small;
  background-color: #82E0AA;
  font-weight: 400;
  font-family: sans-serif;
}

   </style> 
  <title>
      student details</title> 
 </head> 
 <body style="text-align: center;"> 
  <h1><i>STUDENT DETAILS</i></h1> 
  <div id="Details"> 
   <div id="division" class="input">
    <i><b> Name:</b> </i> 
    <input id="name" type="text" placeholder="Type your Name"> 
   </div> 
   <br> 
   <div class="input"> 
    <i><b> Reg-No: </b> </i> 
    <input id="rollno" type="text" placeholder="Type your Regno"> 
   </div> 
   <br> 
   <div class="input"> 
    <i><b> Mail Id: </b> </i> 
    <input id="email" type="email" placeholder="Type your mail"> 
   </div> 
   <br> 
   <button id="values"> <b>click me..!</b></button> 
   <br> 
  </div> 
  <br> 
  <br> 
  <table id="display"> 
   <tbody> 
    <tr> 
     <th><b> Name</b></th> 
     <th><b>Reg-no</b></th> 
     <th><b>E-mail</b></th> 
    </tr> 
   </tbody> 
  </table> 
  <script>
    
    var values = document.getElementById("values"); 

values.addEventListener("click", displayfunction);
var row = 1;
function displayfunction() {
  var name = document.getElementById("name").value; 
  var rollno = document.getElementById("rollno").value;
  var email = document.getElementById("email").value;

  if (!name || !rollno || !email) {
    alert("Required Details must be Filled");
    return;
  }
  var display = document.getElementById("display"); 
  var newRow = display.insertRow(row);
  var cell1 = newRow.insertCell(0);
  var cell2 = newRow.insertCell(1);
  var cell3 = newRow.insertCell(2);
  cell1.innerHTML = name;
  cell2.innerHTML = rollno;
  cell3.innerHTML = email;
  row++;
}
  </script> 
 </body>
</html>
