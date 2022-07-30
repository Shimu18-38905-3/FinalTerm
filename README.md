# FinalTerm
<?php
$servername="localhost";
$username="root";
$password="";
$dbname="Restaurent Management";
$name="Shimu";
$name="Mehedi";
$email="Shimu@aiub.edu";
$email="M@gmail.com";
$salary= 5000;
$salary= 6000;
$conn=new mysqli($username,$email,$salary,$dbname);
if($conn->connect_error)
{
	die("Connection failed:".$conn->connect_error);
}
else
{
	//$q="CREATE TABLE DELIVERY MAN(ID INT(6) UNSIGNED AUTO_INCREMENT PRIMARY KEY, Name VARCHAR(30) NOT NULL, Email VARCHAR(30) NOT NULL)";
	//$q="INSERT INTO DELIVERY MAN(Name,Email,Salary) VALUES('".$name."','".$email."',".$salary.")";
	//$q="INSERT INTO DELIVERY MAN(Name,Email,Salary) VALUES('".$name."','".$email."',".$salary.")";
	//$q="DELETE FROM DELIVERY MAN where ID=1003";
	//

    $q= "UPDATE MyGuests SET lastname='Tamanna' WHERE id=2";
	//$q="select * from DELIVERY MAN ";
	
	$result=$conn->query($q);
	if($result->num_rows>0)
	{
		while($row=$result->fetch_assoc())
		{
			echo "ID:".$row["ID"]."Name:".$row["Name"]."Email:".$row["Email"]."Salary:".$row["Salary"]."<br>";
			echo "ID:".$row["ID"]."Name:".$row["Name"]."Email:".$row["Email"]."Salary:".$row["Salary"]."<br>";
		}
	}
	
}
?>
