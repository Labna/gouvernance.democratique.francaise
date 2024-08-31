# Projet de réglementation démocratique citoyenne française

## En bref

Ce titre n'a aucun sens, donc une petite explication s'impose:
Mon projet est une gestion de l'évolution législative (création, modification, suppression) des lois et de la constitution française par un système de  rédaction, de proposition et d'élection décentralisé, synchronisé et individualisé.

## En détail

### C'est quoi ?
Une paire de client (lourd et léger), donnent accès à tous les éléments suivant. Un identifiant (issu d'un hashage peut-être), à priori basé sur le numéros de Sécurité social et une autre information privé/unique permet de limiter à un vote par personne (reste à concevoir une vérification si c'est bien un humain avec la nationalité française).  

### ça sert à quoi ?

L'objectif est de donner le pouvoir de rédaction des codes:

- civil
- pénal
- de la route
- judiciaire
- du travail
- de la fonction publique
- ...

D'abord, chacun peut rédiger et modifier les textes de loi, comparer les proposition et rédiger une version fusionné des propositions.  
Toutes ces proposition peuvent être poussé en haut du classement afin d'être voté lors de la prochaine session de vote, selon moi un vote hebdomadaire devrait suffire pour poussez une modification de loi. Toute loi voté sera applicable exactement 1 an après la date de clôture de son vote.
Soit un total de 56 modifications par ans, je considère qu'un texte de loi étant construit pour des générations n'a pas besoin d'être modifier un millier de foi par an.

Le même processus existe pour les modifications de la constitution, mais seulement un vote de modification par an.

Pour allez encore plus loin, il serait envisageable de mettre en place le vote des élus (locaux, nationaux ou autre) via ce logiciel. Néanmoins le seul type de vote que je proposerai ici sera un vote "de confiance" où chacun met une note (entre -10 et 10) pour chaque candidat, c'est selon moi le type de vote qui à le moins de lacune.

### Pourquoi ce projet

Je suis dégoûté du système politique et législatif français qui selon moi n'a rien de démocratique, c'est une oligarchie exploitant les failles du système de vote direct, les élections local n'ont aucun sens. Et pire encore, les personnes élus sont incompétentes, occupé à des tâches qui ne devraient pas être de leur ressort et n'ont plus aucune considération envers les "administrés" qu'ils sont censé représenté.

J'ai pas mal ruminé tout ça et considère qu'une initiative citoyenne, suffisamment structuré pouvait supplanté les systèmes en place sans violence, pas simple adhésion individuel.

### Comment je rejoins le mouvement

Un convention, ou plutôt une sorte de contrat contenant les principaux points :

- Atteste sur l'honneur n'avoir aucune poursuite juridique en cours
- Être reconnu de nationalité et de citoyenneté française selon les droits applicables en date de la signature
- La renonciation à tous les droits et les devoirs d'un citoyen de la 5e république française.
- L'accord inconditionnel au devoirs et au droits des textes de ce projet

La conséquence est que l'état républicain français peut vous poursuivre légalement pour tout actes répréhensible (se ses texte de loi) jusqu’à la date de renonciation, à cette date vous répondez au devoir de respect de la législation de ce projet. 

### Comment je revendique ma nouvelle citoyenneté

Le mot d'ordre est la non-violence. Chacun est libre de rejoindre ou non ce mouvement.  
Si par le plus grand des hasards, vous vous retrouviez en groupe, il vous êtes alors possible d'organisé des réunions citoyennes de débat et de construction local. S'il vous sied, l'élection d'un représentant local, (votre porte parole et votre représentant politique). Vous avez également la possibilité de mettre en place de la désobéissance citoyenne envers la 5e république, par exemple, pour collecté les impôts locaux et entamer la construction de projets citoyens (pas forcement en bâtiment) afin de montrer l’énergie issu d'une gouvernance direct (vous ne connaissez sans doute pas toute la marge de manœuvre qu'ont les maires, renseignez-vous sur leur droits et devoirs).

## La technique

Cette section fait l'inventaire des besoins techniques du projet.

### Le réseau

Un réseau en peer-to-peer met en lien les nœuds qui se synchronises en continu. Les clients légers peuvent se connecter à n'importe quel nœud et enregistrer des modifications/vote.
(issu d'un hash-age peut-être)

Les réseaux en P2P sont varié, certains on fait leur preuves comme le Torrent, mais un seul protocole réseau me semble trop facile à détournez et à bloquer, j'empilerai donc plusieurs protocoles afin d'obtenir un maximum de support.

### Le fonctionnement interne

Cela fonctionne comme un Git customisé, les modfication sont des branches et les votes provoquent les merges de ces branches dans le principal. Ceci est construit et sauvegarder pas une Block-chain très légère (merci Gridcoin).

Les identifiants devront être un version hash d'information unique mais retrouvable (informations personnels confidentiels) comme le numéro de sécurité social. Au début du projet je comptais utiliser l'API du site gouv.fr mais il n'ont pas crée d'API pour rendre unique les utilisateurs (ce qui à mon sens n'est pas très malin, beaucoup de services/site/plateforme aurai grand besoin d'un accès à une API qui dit si c'est une vrai personne encore en vie...)).

Sur certains serveur git des systèmes de vote, de commentaire des propositions de modification (push) sont fonctionnel, c'est exactement ça, je rassemblerai les bonnes idées et interfaces existantes.

L'application devra être écrite dans plusieurs langage, pour un maximum de support, sur toutes les plateformes possible.  
En plus de la version bureau (Windows et Linux), une attention toute particulière sera donné pour les Raspberry, Arduino et autres carte ([nano-ordinateur](https://fr.wikipedia.org/wiki/Nano-ordinateur) ou mini-PC) afin que les personnes qui auraient déjà en place ce type de système puissent l'ajouter avec un minimum de contraintes.

### L'hébergement et le maintien

Par défaut le projet sera maintenu sur toutes les plateformes GIT que je pourrais trouver. Si vous possédez une instance de serveur GIT n'hésitez pas à la rajouter dans ce projet.

<style>
h1, h2, h3{
	text-decoration: none;
}
</style>