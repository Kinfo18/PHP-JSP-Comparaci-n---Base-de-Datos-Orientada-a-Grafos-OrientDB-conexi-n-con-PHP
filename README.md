# PHP-JSP-Comparacion---Base-de-Datos-Orientada-a-Grafos-OrientDB-conexion-con-PHP
Contiene un cuadro comparativo entre PHP y JSP, ademas una base de datos hecha en OrientDB (NoSql Orientada a Grafos) y manual para la conexión con PHP


PhpOrient
PHPOrient es un controlador php basado en el protocolo binario de OrientDB.

Requiere
- Versión de PHP > 5.4 ( Extensión de socket habilitada )
- Orientdb versión 1.7.4 o posterior.

1. Instalar el controlador PHPOrient o podemos usar composer

//instalacion de composer

php composer.phar install

2. crear un nuevo proyecto con atributos composer y modificar las siguietes lineas:

$client = new PhpOrient();
$client->configure( array(
    'username' => 'root',
    'password' => 'root_pass',
    'hostname' => 'localhost',
    'port'     => 2424,
) );

3. Abrir base de datos:

$ClusterMap = $client->dbOpen( 'CellPhoneStore', 'root', '12345678' );

podemos listar las bases de datos existentes en el motor OrientDB:

$client->dbList();


