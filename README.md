# TP 1 de Systèmes d'informations répartis


Objectifs du TP

1. Comprendre le fonctionnement de maven.
2. Utiliser les artifacts
3. Configurer un projet eclipse avec maven.
4. Créer son propre MOJO
5. Générer des rapports maven
6. Utiliser Git pour sauvegarder le code source de votre projet
7. Utiliser un système d’Intégration Continue

## Norme de codage

Nous avons utiliser la norme de google pour ce tp et c'est pour ça que il faut créer le fichier de configuration de google 
donc nous avons créé un fichier qui s'appelle g.xml et il faut ajouter le plugin maven-checkstyle-plugin, lui mettre un
tag configuration, y mettre un tag configLocation avec le nom du fichier de configuration qu'on veut.

## Le plugin JXR de maven

Le plugin JXR produit une "cross-reference" des sources du projet et aussi des rapports générés permettent des comprende des lignes de codes spécifiques pour les utilisateurs.

## Les rapports d'erreur avec PMD

Il faut ajouter le plugin pmd pour savoir la duplication de code.

```
<plugins>
	<plugin>
		<groupId>org.apache.maven.plugins</groupId>
		<artifactId>maven-pmd-plugin</artifactId>
		<version>2.5</version>
	</plugin>
</plugins>

```

CPD Report: 

il permet d'analyser le code source en trouvant le code dupliqué.	

PMD Report: 

il permet d'analyser le code source Java. Il contient un certain nombre de règles qui assurent la qualité de code : le code inutile, les imbrications 
trop complexes.Il permet d'obtenir le résultat par le biais d'un rapport.

## Activité du projet

Maven-changelog-plugin génère les rapports en regardant les dernières activités qui s'est faite dans votre software configuration management ou SCM. Ces rapports contiennent des rapports de changelog ou le rapport d'activité de développeur

```
<plugin>
	<groupId>org.apache.maven.plugins</groupId>
	<artifactId>maven-changelog-plugin</artifactId>
</plugin>
```
## Mettre une connection sur github:
Ça nous permet de créer une connexion de github.

```
<scm>
		<connection>scm:git:git://github.com/baouz06/tpSir.git</connection>
		<url>https://github.com//baouz06/tpSir/</url>
</scm>
```
