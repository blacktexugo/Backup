<?php
$usuario_recebido = $_GET['login'];
$senha_recebida   = $_GET['senha'];

#---------------------------
$database      = 'controle';
$table         = 'logins';
$host          = 'localhost';
$usuario_banco = 'root';
$senha_banco   = 'fatec';
#---------------------------

# Conecta-se ao SGBD
mysql_connect($host, $usuario_banco, $senha_banco);

# Seleciona a database de trabalho
mysql_select_db($database);

# Especificamos o comando SQL
$query = "SELECT COUNT(*) FROM $table WHERE username = '$usuario_recebido' AND password = '$senha_recebida'";

# Executamos o comando SQL
$consulta = mysql_query($query);

# Processamento o Vetor $consulta
$resultado = mysql_fetch_array($consulta);

if ($resultado[0])
   echo "LOGIN OK";
else
   echo "ERRRRRROU";

?>
