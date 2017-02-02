Class et id : différences et utilisation avancée

Il existe une différence notable entre les deux attributs class et id : chaque id doit avoir une valeur unique tandis que plusieurs attributs class peuvent posséder la même valeur.

En effet, rappelez vous de nos liens de type ancre. Il s’agit bel et bien du même attribut id qu’on utilise aujourd’hui, avec des finalités différentes.

Il est donc strictement interdit de donner la même valeur à deux id différents dans une même page HTML. En revanche, on peut tout à fait attribuer la même valeur à plusieurs attributs class appartennant à différents éléments HTML.

Cette particularité de l’attribut class va notamment nous permettre d’appliquer le même style à différents (types) d’éléments HTML d’un coup.

<!DOCTYPE html>

<html>
    <head>
        <title>lool</title>
        <meta charset= "utf-8">
        <link rel="stylesheed" href="style.css">
    </head>

    <body>
        <!-- on donne la class à notre titre et à un paragraphe -->
        <h1 class="p1">Un titre de niveau 1</h1>
        <p id="p1">Un paragraphe contenant</p>
        <p class="p1">Un deuxieme paragraphe</p>
        <p>Un troisieme paragraphe</p>
    </body>




</html>



Sélecteurs d'attributs
Un sélecteur CSS peut faire référence à un attribut d'un élément HTML. Les deux attributs les plus couramment utilisés sont class et id mais il est possible de se référer à n'importe quel attribut. La classe class permet d'attribuer des styles génériques (par exemple une classe petit pour mettre du texte plus petit) alors que l'identifiant id sert à repérer un élément différent des autres dans la page (par exemple la zone de menu).

Sélecteur de classes
Le sélecteur de classe s'applique typiquement à des éléments redondants dans la page. Il est spécifié en CSS par un point ( . ) et peut concerner tous les éléments HTML utilisant cette classe ou seulement l'un d'entre eux. La syntaxe CSS est la suivante :

.nom_de_classe {
     /* déclaration(s) */
}
élément.nom_de_classe {
     /* déclaration(s) */
}
Dans le document HTML, on se réfère à cette classe de la sorte (exemple pour l'élément P) :

<p class="nom_de_classe">...</p>
N'importe quel élément HTML de la page peut utiliser cette classe :

 <p class="nom_de_classe">...</p>
 <ul class="nom_de_classe">
   <li>...</li>
   <li>...</li>
 </ul>
Ce qui n'empêche pas par la suite de définir des règles communes à tous ces éléments et d'autres spécifiques à certains d'entre eux :

.nom_de_classe {
     color: gray;
}
p.nom_de_classe {
     font-style: italic;
}
Ici les éléments de classe nom_de_classe sont affichés en gris et les paragraphes de cette classe ont en plus leur texte en italique.

Sélecteur d'identifiant[modifier | modifier le wikicode]
Le sélecteur d'identifiant (ID) ne peut être appliqué qu'à un seul élément dans le code HTML, par exemple un seul paragraphe. Il concerne donc les éléments uniques de structuration du document, comme les blocs principaux (logo, en-tête, colonne(s), pied de page...).

Le sélecteur d'identifiant est spécifié en CSS par un dièse ( # ), la syntaxe est la suivante :

élément#nom_id {
     /* déclarations */
}
ou :

#nom_id {
     /* déclarations */
}
Théoriquement seule cette dernière syntaxe devrait être utilisée puisqu'un seul élément peut être affublé de l'identifiant nom_id dans la page. Il est toutefois courant de voir la première syntaxe utilisée pour des raisons de lisibilité du code.

Dans un document HTML, si l'identifiant nom_id se rapporte à un élément de type div, on ne doit écrire qu'une seule et unique fois dans la page :

<div id="nom_id">...</div>
