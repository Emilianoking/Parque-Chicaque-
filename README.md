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
