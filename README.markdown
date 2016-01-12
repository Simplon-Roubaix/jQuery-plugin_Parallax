#jQuery Parallax
===============

## Utilisation du plugin Parallax

Le plugin Parallax crée un déplacement de plusieurs éléments (au schroll ou à la souris) sur des couches et à des vitesses différentes. 
Les positions des différents fonds (ou éléments à animer) vont changer, ce qui va générer un effet de profondeur. 
Ce principe concerne au minimum deux éléments et peut être appliqué à plusieurs endroits : sur les images de fond, sur un en-tête ou un pied de page, sur des images... etc.

il est possible de déplacer les éléments par rapport à la position de la souris ou du niveau de défilement (scroll). Le but va donc être de modifier les valeurs de positionnement en fonction de ces paramètres que l'on mesure.
Avec une même distance de scroll, l'élément a va parcourir une distance plus faible que l'élément b. C'est cette différence de vitesse qui crée l'effet parallaxe.

Insertion de jQuery :
 charger le script en l'insérant à la fin de votre document HTML, avant </body>.
<script type="text/javascript" src="https://ajax.googleapis.com/ajax/libs/jquery/1/jquery.min.js"></script>

Insertion et paramétrage de jQuery-Parallax :
Après téléchargement, insérez-le de la même façon après le chargement de jQuery.
<script type="text/javascript" src="script/jquery.parallax-1.1.js"></script>

Le script jQuery-Parallax va agir directement sur la propriété CSS background-position en modifiant la position verticale.
S'il s'applique à des images de fond, cela signifie qu'il faut obligatoirement créer un élément ayant un background pour réaliser cet effet. Il est impossible d'animer directement un élément img.

 La syntaxe :
$("élément").parallax(xPosition, adjuster, inertia, outerHeight);

xPosition : Position horizontale de l'élément (nomenclature CSS).
adjuster : La position verticale de départ (en pixels).
inertia : Vitesse en fonction du scroll. Exemple: 0.1 = 1/10 ème de la vitesse du scroll, 2 = deux fois la vitesse du scroll.
outerHeight : Détermine si jQuery utilise sa propre fonction outerHeight pour déterminer quand une partie est visible dans le viewport (true ou false).

 Ex : si on l'applique sur 3 <div> principales (#slide1, #slide3, #slide3) :
<script type="text/javascript">	
   $(document).ready(function(){		
   $('#slide1').parallax("center", 0, 0.1, true);
   $('#slide2').parallax("center", 900, 0.1, true);
    $('#slide3').parallax("center", 2900, 0.1, true);
   })
</script>

L'image de fond de chaque slide va être déplacée de quelques pixels lors du défilement. Cela suffit pour que la magie opère.








source :
jQuery Parallax is a script that simulates the parallax effect as seen on [nikebetterworld.com](http://www.nikebetterworld.com/).

Plugin: jQuery Parallax  
Version: 1.1.3
Author: [Ian Lunn](http://www.ianlunn.co.uk/)  
Twitter: [@IanLunn](http://www.twitter.com/IanLunn)
Demo: [jQuery Vertical Parallax Demo](http://www.ianlunn.co.uk/plugins/jquery-parallax/)  
Tutorial: [Nikebetterworld Parallax Effect Demo](http://www.ianlunn.co.uk/blog/code-tutorials/recreate-nikebetterworld-parallax/)  

Dual licensed under the MIT and GPL licenses:
http://www.opensource.org/licenses/mit-license.php
http://www.gnu.org/licenses/gpl.html

