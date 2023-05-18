# Parque-Chicaque

el siguiten  codigo es el index del programa , fue creado con HTML

<!DOCTYPE html>
<html>
<head>
	<title>Formulario de contacto</title>
</head>
<body>
	<header>
		<h1>Formulario de contacto</h1>
	</header>
	
	<form action="guardar_datos.php" method="post">
		<label for="documentos">Documentos:</label>
		<input type="text" id="documentos" name="documentos"><br>

		<label for="nombre">Nombre:</label>
		<input type="text" id="nombre" name="nombre"><br>

		<label for="telefono">Telefono:</label>
		<input type="tel" id="telefono" name="telefono"><br>

		<label for="fecha">Fecha:</label>
		<input type="date" id="fecha" name="fecha"><br>

		<input type="submit" value="Enviar">
		<input type="reset" value="Borrar">
	</form>
	
	<footer>
		<p>21/04/2023</p>
	</footer>
	
</body>
</html>



// el siguiente  codigo es el que guarda los datos en la base de datos, fue creado por  PHP

<?php
// Establecer la conexión a la base de datos
$servername = "localhost";
$username = "root";
$password = "";
$dbname = "chat";

$conn = mysqli_connect($servername, $username, $password, $dbname);
if (!$conn) {
    die("Conexión fallida: " . mysqli_connect_error());
}

// Obtener los datos del formulario
$documentos = $_POST['documentos'];
$nombre = $_POST['nombre'];
$telefono = $_POST['telefono'];
$fecha = $_POST['fecha'];

// Preparar la consulta SQL
$sql = "INSERT INTO tabla_de_contactos(documentos, nombre, telefono, fecha)
VALUES ('$documentos', '$nombre', '$telefono', '$fecha')";

// Ejecutar la consulta SQL
if (mysqli_query($conn, $sql)) {
    echo "Los datos se han guardado correctamente.";
} else {
    echo "Error: " . $sql . "<br>" . mysqli_error($conn);
}

// Cerrar la conexión a la base de datos
mysqli_close($conn);
?>
