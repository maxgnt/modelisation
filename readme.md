# Installation GIT

git : 
git init 
git status piur etat du depot 
ajouter des fichiers :  git add .
sauvergarder le travail : git commit -m "votre message de commit" 

Merise : etudier une entreprise et transformer le processus en systeme d'information 

Flux de données : suivre le trajet de la donnée -> système d'information 
3 systèmes : système de pilotage, di'formation et d'opérant 

Une valeur prise par une information elementaire est une occurence 
Une info elementaire doit être atomique

Approche nivelée :
- Le niveau conceptuel 
- Le niveau organisationnel 
-Le niveau logique 
-Le niveau physique 

Collecte d'infos 

# Différents Types de Modèles: 

MCD (modèle conceptuel de donneés), MOD(modèle organisationnel des doonées), MCT(modéliser les traitements de l'entreprise) et MOT (modèle organisationnel des traitements)

Niveau physique : organisation réelle des données 
niveau logique : modéliser les données 

Méthode de Merise : structurer les besoins des décideurs ; améliore la communication entre les acteurs du processus de développement 

# Les dependances fonctionnelles 

Il faut classer, trier et organiser les données :
- Chaine de caractères, format texte 
- type alphanumérique, format texte
- le type numerique (integrer, float)
- le type de date (date, datetime, timestamp)
- le logique ou boolen (true, false)

Après cela, il faut centraliser les informations et règles de gestion au sein d'un document = dictionnaire des données 
(image d'un dictionnaire de données)

dictionnaire de données : rencense les données, les propriétés des données, les contraintes d'integrite, les dependances fonctionnelles. Permet de recenser les données du systeme d'information.


# Les dependances fonctionnelles 

Relation entre deux attributs d'une table 
Une donnée A depend d'une donnée B lorsque la valeur B détermine la valeur de A



# Les dependances fonctionnelles composées 
Fait intervenir plus de deux attributs 

# Les dependances fonctionnelles elementaires 

une dependance fonctionnelle A->B est elementaire s'il n'existe pas une donnée C, sous ensemble de A, decrivant une dependance fonctionne type C->B

Exemple : 

RefProduit -> LibelleProduit 
Numcommande Refproduit -> Quantité commande
~~NumCommande RefProduit -> Designation Produit~~
 

# Dependance fonctionnelle elementaire directe 
"On dit que la dépendance fonctionnelle A-> B est directe s'il n'existe aucun attribut C tel que l'on puisse avoir A->C et C->B. CEla singifie que la dépendance fonctionnelle entre A et B ne peut etre obtenue par transivité. 


Exo cf excel et correction 

# Partie conceputelle MCD :

MCD est un schéma conceptuel qui permet de représenter les donées d'une entreprise 
Propriétés
Entités
Relations 

Les propriétés sont les informations de base d'un système d'information. Elles disposent d'un type et d'une longueur. Nous n'allons pas décrire en détail les propriétés. Nous allons simplement les nommer. 

Les entittés ou objets : 
Les entittés sont un ensemble de propriétés qui décrivent un objet du système d'information. Elles sont représentées par un rectangle.

L'identifiant : 
L'une de ces propriétés est l'identifiant. L'indetifiant est une propriété qui permet d'identifier de manière unique une entité. Il est représenté par un souligné. 


Relation ou Association : 
Les relations permettent de relier les entités entre elles. 
Par exemple : Un client peut passer une ou plusieurs commandes 




Lundi aprem : 

Les cardinalités : nombre de fois ou l'occurence d'une entité participe aux occurences de la relation 
"Combien de fois au minimum un client peut-il commander un article?" 
"Combien de fois au maximum un client peut-il commander un article?"
1 c'est cardinalité minimale et n cardinalité maximale 

"Cardinalité inversée" : le sujet est les articles :
"Combien de fois au minimum un article peut-il être commandé?"
"Combien de fois au maximum un article peut-il être commandé?"

La cardinalité maximale quand elle est connue il faut la noter

Exemple :
photo exemple 
Les cadinalités sont 1 mère peut élever un ou plusieurs enfants 
un enfant peut être élevé par une et une seule mère 



# Relation proteuse (propiété) :

Une relation porteuse possède des propriétés 
intervenir deux entités : relation binaire 
trois entités : relation ternaire 
(photo avec 3 entités -> date)

# Les relations reflexives : 

Une relation est dite reflexive si elle relie une entite a elle meme 
(photo reflexive)


# Règles d'usage :

Toute entité doit forcément avoir un identifiant
Toutes les propriétés de l'entité dépendent fonctionnelement de l'idenfifiant 
Le nom d'une propiété doit apparaitre une seule fois dans un modèle de propriété (tout le MCD) 
On peut utiliser un préfixe ou suffixe 


# Notion d'entite forte et d'entite faible 

Forte : peut exister seule (pas besoin d'autres entités)
Faible : a besoin d'une autre entite pour exister 


# Contraintes d'integrite fonctionnelle (CIF)

Une CIF est definie par le fait qu'une des entites de l'assocation est completement determinee par la connaissance d'une ou plusieuurs entites participant à l'association 
(photo contrainte integrite)
![Alt text](Capture%20d%E2%80%99%C3%A9cran%202024-08-20%20%C3%A0%2008.49.20.png)




Mardi : 

Correction exo MCD 


# MLD :

Pour représenter une relation, on utilise une clé étrangère 
Dans les cas ou la cardinalité max est n des deux côtés, on cree une entite intermediaire qui va contenir les deux cles etrangeres des deux entites.

Lorsque l'on passe du MCD au MLD c'est la cardinalité qui a maximale = 1 recevra l'identifiant ou les identifiants ayant les cardinalités maximales les plus fortes 
Les relations ayant toutes leurs entités avec des cardinalités maximales supérieures à 1 se transformeront en entité en absorbant les identifiants des entités jointes.


# MPD (Modèle Physique de données) :

Le MPD permet de passer du modèle logique au modèle physique (SQL)
1ere etape :il faut créer un schéma relationnel (écrire ce que l'on voit)
2eme étape : vérifier que tout est ok

Convention de nommage de SGBD 


 # Exo de la matinée et après-midi : 
![Alt text](Capture%20d%E2%80%99%C3%A9cran%202024-08-21%20%C3%A0%2009.31.27.png)

![Alt text](Capture%20d%E2%80%99%C3%A9cran%202024-08-20%20%C3%A0%2013.55.54.png)

Voici mon MCD de l'exercice 1 : les entités principales (ventes, produits et catégoties ) sont définies 

![Alt text](Capture%20d%E2%80%99%C3%A9cran%202024-08-20%20%C3%A0%2014.07.45.png!
Voici le MLD de l'exercice 1 
Modèle Logique de Données Relationnelle "MLDR" : 

Ventes  (  #Numéro de vente,   Quantité du numéro de produit,   Date de vente,   Numéro de produit,   Montant total,   Numéro du produit_Produits  )

Produits (  #Numéro du produit,   Nom produit,   Prix au kilo,   Nom de la catégorie_Catégorie  )

Catégorie (  #Nom de la catégorie  )


USE marche;

CREATE TABLE Catégorie (
    Nom_de_la_catégorie VARCHAR(255) PRIMARY KEY
);


CREATE TABLE Produits (
    Numéro_du_produit NUMERIC PRIMARY KEY,
    Nom_produit VARCHAR(255),
    Prix_au_kilo NUMERIC,
    Nom_de_la_catégorie VARCHAR(255),
    FOREIGN KEY (Nom_de_la_catégorie) REFERENCES Catégorie(Nom_de_la_catégorie)
);


CREATE TABLE Ventes (
    Numéro_de_vente NUMERIC PRIMARY KEY,
    Quantité NUMERIC,
    Date_de_vente DATE,
    Numéro_de_produit NUMERIC,
    Montant_total FLOAT,
    FOREIGN KEY (Numéro_de_produit) REFERENCES Produits(Numéro_du_produit)
);


Exercice 2 :

Voici le MLD et MCD de l'énoncé : 
![Alt text](Capture%20d%E2%80%99%C3%A9cran%202024-08-21%20%C3%A0%2009.18.55.png)
![Alt text](Capture%20d%E2%80%99%C3%A9cran%202024-08-21%20%C3%A0%2009.19.44.png)

Celui-ci était différent des autres car on partait du modèle relationnel pour créer les MCD et MLD. 


# Exercice 3 :

Voici le ditionnaire, le MCD et MLD de cet exercice : <br>
Dictionnaire: 

![Alt text](Capture%20d%E2%80%99%C3%A9cran%202024-08-21%20%C3%A0%2010.51.30.png)<br>
MCD :
![Alt text](Capture%20d%E2%80%99%C3%A9cran%202024-08-21%20%C3%A0%2011.32.17.png) <br>
MLD :
![Alt text](Capture%20d%E2%80%99%C3%A9cran%202024-08-21%20%C3%A0%2011.33.59.png)

<br>

```sql

CREATE TABLE Clients (
    Numéro_de_client INT PRIMARY KEY,
    Nom VARCHAR(100),
    Prenom VARCHAR(100),
    Ville VARCHAR(100),
    Adresse VARCHAR(255),
    CP VARCHAR(10),
    Telephone_client VARCHAR(20),
    Numéro_matériel_Matériel INT
);


CREATE TABLE Matériel (
    Numéro_matériel INT PRIMARY KEY,
    Type_matériel VARCHAR(100),
    N_de_série_matériel VARCHAR(100),
    Numéro_intervention_Intervention INT
);


CREATE TABLE Intervention (
    Numéro_intervention INT PRIMARY KEY,
    Date_intervention DATE,
    Numéro_de_client_Clients INT,
    Type_d_intervention_Prix_intervention VARCHAR(100),
    FOREIGN KEY (Numéro_de_client_Clients) REFERENCES Clients(Numéro_de_client)
);


CREATE TABLE Prix_intervention (
    Type_d_intervention VARCHAR(100) PRIMARY KEY,
    Heure_début_intervention TIME,
    Heure_fin_intervention TIME,
    Numéro_composant_Nvx_composants INT,
    Numéro_matériel_Matériel INT,
    FOREIGN KEY (Numéro_matériel_Matériel) REFERENCES Matériel(Numéro_matériel)
);


CREATE TABLE Nvx_composants (
    Numéro_composant INT PRIMARY KEY,
    Prix_de_vente_composant DECIMAL(10, 2),
    Quantité INT
);


ALTER TABLE Clients
ADD FOREIGN KEY (Numéro_matériel_Matériel) REFERENCES Matériel(Numéro_matériel);

ALTER TABLE Matériel
ADD FOREIGN KEY (Numéro_intervention_Intervention) REFERENCES Intervention(Numéro_intervention);

ALTER TABLE Intervention
ADD FOREIGN KEY (Type_d_intervention_Prix_intervention) REFERENCES Prix_intervention(Type_d_intervention);

ALTER TABLE Prix_intervention
ADD FOREIGN KEY (Numéro_composant_Nvx_composants) REFERENCES Nvx_composants(Numéro_composant);
```
Plus de facilité sur cet exercice désormais ! 
