# Débutter en PHP !

Pour débutter la notion de variable

```php runnable
<?php
//Se connecter au serveur SQL
	$user='root';
	$pass='';
//	$connexion = new PDO('mysql:host=127.0.0.1;dbname=debutterphp', $user, $pass);
	//var_dump($connexion);
	
	//Toujours debugguer sa requete SQL en la plaçant dans une variable
	$sql="SELECT * from profs";
	//var_dump($sql);
	
	//Exécution de la requete et recupération du jeu d'enregistrement (aussi appelé Curseur)
//	$jeu=$connexion->query($sql);
	//var_dump($jeu);
	
?>

<html>

	<table border="1">
		<tr>
			<th>id</th>
			<th>nom</th>
			<th>prenom</th>
		</tr>
		<?php
		//Itération Pour chaque Ligne (Row) du Jeu d'enregistrement($jeu)
		//foreach($jeu as $row){?>
		<tr>
			<td><?php //echo $row["id"] ?></td>
			<td><?php //echo $row["nom"]  ?></td>
			<td><?php //echo $row["prenom"]  ?></td>
		</tr>
		<?php } ?>
	</table>
</html>
?>
```

