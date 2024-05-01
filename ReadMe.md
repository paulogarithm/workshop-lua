<h1 align=center> Lua Workshop </h1>

## Introduction

Bienvenue au petit bain de Epitech ! Au plat du jour: Le **lua** !
2h30 de pur plaisir où vous allez apprendre les
bases de la programation, avec le meilleur langage du monde.

### Trigger Warning

1. Le lua est mon langage de coeur <3 alors appreciez ce workshop car il est
merveilleux.

2. Ce sujet est celui que j'ai écrit initiallement pour **Cobra**. Si vous
l'avez deja fait, j'y ai rajouté des exercices.

3. Ce workshop a été édité le 30 avril 2024. La version la plus récente du lua
à ce moment precis etait lua5.4, mais allez sur
[le site du lua](https://www.lua.org/) pour obtenir la verison la plus récente.

4. Ce workshop contient des mots immatures et grossiers (`prout` et `caca`).
Si vous vous sentez offensés et que vous ne voulez pas afficher ces mots doux,
affichez à place `fleur` pour prout et `papillon` pour caca.

### Installation

Faites juste la commande suivante:
```sh
sudo dnf install lua5.4 liblua5.4-dev -y ||
sudo apt install lua5.4 liblua5.4-dev -y
```


## Hello world !

Votre première tache sera d'afficher la phrase "Hello world" lorsque vous
lancerez votre programme.

## J'aime l'alcool

Mais ai-je le droit d'en boire ? Oui, seulement si j'ai plus de 18 ans.

Créez votre **variable** nommée `age`, et donnez lui un nombre.

Faites en sorte que votre programme affiche "Je peux boire de l'alcool !" si
l'âge est plus que 18,
qu'il affiche "Joyeux anniversaire! Tiens, de la tequilla" si votre âge est 18
et afficher "Pas d'alcool pour toi mon enfant" si l'âge est en dessous de 18.


## Une pluie de Hello world ??

J'aime vraiment la phrase "Hello world", tellement que je veux que vous
me l'affichiez 100 fois.

Mais il y a un hic, vous n'avez le droit qu'à un seul print!


## Une averse de Hello world ????

Tout à l'heure, vous avez réussi à m'afficher "Hello world", 100 fois. Bravo !
Vous avez sûrement utilisé une boucle.

Maintenant, affichez moi Hello World, 100 fois en utilisant 3 boucles
différentes.


## Ma premiere fonction: myIsNeg

Créez-moi une fonction qui s'appelle myIsNeg. Elle **renvoie** `true` si le
chiffre que je te donne en **paramettre** est négatif, et `false` si le
chiffre est positif.

Voici un petit code pour vous aidez à savoir si vous avez bien réussi :
```lua
print(myIsNeg(-3)) -- true
print(myIsNeg(42)) -- false
```


## 1 + 1

Maintenant que vous avez créé votre première fonction, il est tant d'en faire
une deuxième.

Créez votre propre fonction, myAdder, qui va prendre 2 arguments en
paramètres (qui sont deux nombres), et qui va renvoyer l'addition de ces
deux derniers.

Voici un petit programme qui devrait fonctionner avec votre fonction :
```lua
print(myAdder(1, 1)) -- 2
print(myAdder(3, 4)) -- 7
```


## Hello + World

Bon, vous pouvez maintenant ajouter des chiffres entre eux. Maintenant,
c'est l'heure d'ajouter... Des chaînes de caractères !

Créez votre fonction myConcat qui va **concattener** des strings entre elles.

Ce code devrait fonctionner :
```lua
print(myConcat("hello", "world")) -- helloworld
print(myConcat("foo", "bar")) -- foobar
```


## Secure 1 + 1

Malheureusement, les gens ne sont pas tous gentils, certains vont vouloir
envoyer des chaînes de caractères a la place de chiffre dans votre myAdder,
modifie ta fonction pour qu'elle n'accepte seulement des `nombres` en
paramètre.

```lua
print(myAdder(1, 1)) -- 2
print(myAdder(1, "hello")) -- nil
```


## A table !

En lua, il existe un type qui est primordial à la programmation. Ce sont les
`tables`, qui sont très utiles pour tout et n'importe quoi.

Voici à quoi ressemble ma table :
```lua
local fruits = {"banana", "apple", "ananas", "banana"}
```

Écris-moi une fonction qui s'appelle `myPutTable` qui prends ma table en
paramètre et qui m'affiche son contenu.

Le code ci-dessous devrait marcher:
```lua
myPutTable(fruits) -- banana apple ananas banana
```


## Devinette

Je vais juste vous donner ce petit code, vous allez devoir écrire le code qui
vous permet d'avoir une table donnant ce résultat :
```lua
-- Créez votre 'myDevinette' ici

myDevinette.hello("Foo") -- "Bonjour Foo !"
myDevinette.hello("Bar") -- "Bonjour Bar !"

myDevinette.add(4, 2) -- "4 + 2 = 6"
myDevinette.add(4, "hello") -- "4 + hello, je sais pas"
myDevinette.add(1, 0) -- "1 + 0 = 1"
```

> Utilisez ce que vous avez appris avec votre adder !

## 1 + 1 + 1 ...

Moi, je ne veux vraiment pas ajouter seulement 2 nombres. J'aimerais bien en
ajouter, voyons voir... Une infinité ?

Écris la fonction `mySuperAdder`, qui te permet de d'ajouter une infinité
de chiffres ensemble.

Le code ci-dessous devrait fonctionner :
```lua
print(mySuperAdder(1, 2, 3, 4)) -- 10
print(mySuperAdder(3, 3)) -- 6
print(mySuperAdder(1)) -- 1
```


## Selfish

Dans plusieurs language, il est possible de faire ce qu'on appelle de l'OOP,
la programmation orientée object.

Voici ce que va etre votre objectif

```lua
-- Créez votre 'number' table ici

number:display() -- 0
number:add(3)
number:display() -- 3
number:dec(2)
number:display() -- 1
```

> C'est quoi ':' en lua ?

> Qu'est ce que self ?


## Meta-verse

En lua, vous avez ce qui s'appelle des `metatables`. En gros, c'est ce qui
permet de donner des attributs en plus à vos tables.

Par exemple, vous pouvez ajouter des tables ensemble !

Créez une table qui peut se faire ajouter son nombre, tel que ce code
fonctionne, mais:

### ATTENTION

Votre code ne doit pas ajouter des valeurs dand le tableau b !

```lua
local a = {
    age = 19
}
local b = {
    name = "Paul"
}

-- Votre code ici

print(b.age) -- 19
print(b.name) -- Paul
```

> C'est quoi une metatable ?

> C'est quoi une metamethod ?


## La descendance

Ok, il est temps de passer aux choses sérieuses. Vous allez fonder une famille.

Vous allez pouvoir créer... Des humains et leur descendance!

Voici le code qui devrait fonctionner:
```lua
-- Créez votre 'human' table ici

local john = human.new("john", 31)
local emma = human.new("emma", 30)
print(emma.name) -- emma
print(john.age) -- 31

john:birthday()
print(john.age) -- 32

local child = john + emma
print(child.name) -- baby john
print(child.age) -- 0
```

L'enfant devrait avoir "baby" + le nom du premier parent. Son âge doit être à
0 quand il naît.

Créez votre table human qui effectue le code attendu!


## Give me you mail

Les mails sont très utiles, mais des personnes malicieuses vous donneront
sûrement un faux mail pour eviter de recevoir des spams de votre part.

Vous devez absolument empêcher ces gens de vous donner un email invalide !
Créez votre fonction `giveMeYourMail` qui renvoie `true` si votre mail est
valide, et `false` s'il ne l'est pas:
```lua
print(giveMeYourMail("hello, world")) -- false
print(giveMeYourMail("foo@bar.com")) -- true
print(giveMeYourMail("foo@bar")) -- false
```

Un mail est constitué d'un nom, qui peut être n'importe quel caractère
**alphanumériques**, suivi d'un arobase, puis d'un nom de site, comprenant
encore des caractères alphanumériques, suivi d'un point et d'encore des
caractères alphanumériques.

`ALPHANUM @ ALPHANUM . ALPHANUM`

> Alphanumequoi ? Ca veut dire quoi alphanumérique ?

> Peut être qu'il existe une technique en lua pour
> comparer des patterns de string ?

## Hello there

Mais dis moi, je ne connais pas votre nom ?

Créez votre propre fonction `helloThere` qui permet à l'utilisateur de donner
un nom après avoir lancé ton programme, et l'affiche suivi d'un
"Hello there, ",

Voici à quoi cela devrait ressembler:
```hs
$ lua ./hellothere.lua
```
```r
What is your name ?
> General Kenobi # Ceci est ce que vous écrivez
Hello there, General Kenobi
```

> Qu'est ce que io ?

## Cobblestone generator

Vous êtes une colonie qui mine de la cobble avec des générateurs de
cobblestone.

Un générateur se construit avec de la lave et de l'eau. Lorsque l'on a les
deux, le générateur peut créer de la cobblestone.

Mais votre générateur a une certaine réserve de cobblestone, il ne peut plus
en générer si votre réserve est pleine.

Vous devriez avoir les fonctions suivantes dans chaque générateur:
- `:give(string)`: Vous permet de donner de la lave ou de l'eau à votre
générateur. <br>
Si vous lui donnez autre chose, il vous dira "Je ne prends pas ça". <br>
Si vous lui avez déja donné de l'eau, il vous dira "J'ai deja ça".

- `:generate()`: Vous permet de générer de la cobblestone. <br>
Si vous n'avez pas d'eau, il vous dira "Je n'ai pas d'eau". <br>
Si vous n'avez pas de lave, il vous dira "Je n'ai pas de lave". <br>
S'il a atteint sa limite, il vous dira "Trop de cobble !"

- `:howMany()`: Vous affiche combien de cobblestone votre générateur a.

- `:empty()`: Vide votre générateur.

Votre but est de créer une table `motherGenerator`, qui vous permet de
créer autant de générateur que vous voulez.

Voici les méthodes de votre motherGenerator:
- `.new(number?)`: Permet de créer un générateur ayant comme limite le
paramètre donné. <br>
Si aucun chiffre n'est donné, la limite est automatiquement de 5.

Voici un exemple:
```lua
-- Créez votre 'motherGenerator' table ici

local generator = motherGenerator.new(3)
generator:generate() -- Je n'ai pas d'eau
generator:give("eau")
generator:give("albert") -- Je ne prends pas ça
generator:generate() -- Je n'ai pas de lave
generator:give("lave")
generator:give("lave") -- J'ai deja ça

generator:howMany() -- 0
generator:generate()
generator:howMany() -- 1
generator:generate()
generator:generate()
generator:howMany() -- 3
generator:generate() -- Trop de cobble !
generator:generate() -- Trop de cobble !
generator:howMany() -- 3
generator:empty()
generator:howMany() -- 0
```

## Planet Mining

J'espère que vous avez aimé l'exercice précedent, car celui la est très
similaire (mais en plus dur et plus long mdr).

**N'abandonnez pas!** C'est le dernier exercice !

A la fin, je vous expliqerais le vrai pouvoir du lua...

BREF Voici l'exercice de l'enfer: __**Planet Mining**__

Vous êtes un petit mineur independant avec votre vaisseau spatial, votre but
est d'explorer de nouvelles planettes afin d'exploiter les ressources de ces
merveilleuses plannetes que sont les `Cristaux Epitechiens` que l'on
appelle communément les `CRE`, ou les `Credits Epitech`.

Un vaisseau peut avoir **plusieurs niveau**.

Un vaisseau de niveau 1 permet de miner 4 CRE par session de minage.

Quand un vaisseau a **4 fois le nombre de cristaux qu'il peut miner par
session**, il peut ainsi créer un vaisseau de niveau inferieur.

Le vaisseau de niveau 1 est la seule exception, qui permet de créer un vaisseau
de niveau 1 seulement si il a **8 fois le nombre de cristaux qu'il peut miner
par session**.

Chaque vaisseau peut créer des vaisseau de niveau infererieur. Ce qui veut
dire qu'un vaisseau de niveau 4 peut créer des vaisseaux de niveau 3, 2 et 1.

Cela n'inclut pas l'execption ci-dessus du niveau 1.

Si vous avez bien suivi, si votre vaisseau de base est niveau 2, il peut donc
miner **8 CRE par session**, et peut donc créer un vaisseau de niveau 1 à
partir de 4 * 8 CRE, ce qui equivaut à 32 CRE.

Et un vaisseau de niveau 1 peut créer un vaisseau de niveau 1 si il a
8 * 4 CRE, ce qui equivaut egalement à 32 CRE. Mais du coup ca lui prendra
deux fois plus de sessions qu'un vaisseau de niveau 2.

C'est bon ? Comment va votre cerveau ? Ca tombe bien j'ai pas fini il reste une
deuxieme partie apres celle là hahaha

Pour créer le premier vaisseau, voila comment vous y prendre:
```lua
local PlanetMining = require("planetmining")

local ship = PlanetMining.newShip(2) -- créé un vaisseau de niveau 2
```

Lorsque vous affichez votre vaisseau, il doit vous donner les informations
sur le nombre de CRE et son niveau:
```lua
print(ship)
```
```
Vaisseau de niveau 2 (8 CRE/session)
Contient 0 CRE
```

Vous pouvez aussi obtenir le nombre de CRE en utilisant `#`:
```lua
print(#ship)
```
```
0
```

Ensuite, appeller votre object permet de miner des CRE:
```lua
print(ship)
ship()
print(#ship)
ship()
print(ship)
```
```
Vaisseau de niveau 2 (8 CRE/session)
Contient 0 CRE
8
Vaisseau de niveau 2 (8 CRE/session)
Contient 16 CRE
```

La securité avant tout. Si quelqu'un essaie de recuperer la metamethode de
votre ship, affichez "prout".
```lua
print(getmetatable(ship))
```
```
prout
```

Et enfin, créer un nouvel effectif se fait de la maniere suivante:
```lua
print(ship)
local ship2 = ship >> 1 -- Créé un vaisseau de niveau 1
print(#ship)
print(ship2)
```
```
Vaisseau de niveau 2 (8 CRE/session)
Contient 40 CRE
8
Vaisseau de niveau 1 (4 CRE/session)
Contient 0 CRE
```

Bien evidemment vous devriez faire des cas d'erreur:
```lua
local ship = PlanetMining.newShip(3)
ship >> 1 -- Pas assez de CRE: il vous en manque 32.
ship >> 2 -- Pas assez de CRE: il vous en manque 64.
ship >> 3 -- Ne peut pas créer un vaisseau plus grand que 2.
```

Voici un petit code pour tester:
```lua
local lvl3 = PlanetMining.newShip(3)
print(#lvl3) -- 0
lvl3()
print(#lvl3) -- 16
for i = 0, 3 do
    lvl3()
end
print(#lvl3) -- 80
local lvl1 = lvl3 >> 1
lvl1()
print(#lvl1) -- 4
print(#lvl3) -- 48
print(getmetatable(lvl1)) -- prout
print(lvl1)
```
```
0
16
80
4
48
prout
Vaisseau de niveau 1 (4 CRE/session)
Contient 4 CRE
```

Phew quel enfer, mais c'est enfin fini !

Et non c'est une blague voici la partie 2. Ok c'est bien beau de créer des
vaisseaux de niveau inferieur mais maintenant je veux pouvoir monter en niveau.

Vous en faites pas c'est tres simple, vous pouvez ajouter les vaisseaux de
meme niveau pour monter d'un niveau !

Mais quand vous mergez vos deux vaisseau pour en créer un, ils deviennent ainsi
des `cacas`, c'est à dire des niveau 0 qui ne peuvent plus miner quoi que ce
soit.

Les cacas sont vidés de tous leurs CRE.

A la fin du programme, il dit "Caca ramassée !".

> A la fin du programme, ou quand votre objet est initialisé à nil et que
> la fonction `collectgarbage("collect")` est appellée.

> Faites attention à ce que ce texte s'affiche seulement pour les cacas, et pas
> tous vos vaisseaux bien sur.

```lua
local a = PlanetMining.newShip(1)
local b = PlanetMining.newShip(1)
a()
print(a)
local c = a + b
print(c)
print(a)
```
```
Vaisseau de niveau 1 (4 CRE/session)
Contient 4 CRE
Vaisseau de niveau 2 (8 CRE/session)
Contient 0 CRE
Vaisseau caca (0 CRE/session)
Contient 0 CRE
Caca ramassé !
Caca ramassé !
```
Les deux caca ramassés sont les variables a et b.

Vous devriez avoir un cas d'erreur lorsque a et b ne sont pas du meme niveau.

Et pour finir (je vous troll plus c'est vraiment la fin de planet mining) vous
allez créer les banques à CRE.

Une banque permet de stocker les CRE.

```lua
local bank = PlanetMining.newBank
```
Oui oui vous avez bien compris, je n'ai pas oublié les parenthèses.

Chaque bank est individuelle et a son propre nombre de CRE.

Vous pouvez print une banque et son contenu un peu comme les vaisseaux:
```lua
print(bank)
print(#bank)
```
```
La banque contient 4 CRE.
4
```

Voici comment remplir les banques.
```lua
local ship = PlanetMining.newShip(2)
local bank = PlanetMining.newBank

ship()
print(#ship) -- 8
print(#bank) -- 0
_ = ship >> bank
print(#ship) -- 0
print(#bank) -- 8
_ = ship << bank(3)
print(#ship) -- 3
print(#bank) -- 5
```

Il vous faudra aussi un petit cas d'erreur lorsque vous essayez d'envoyer un
chiffre qui ne provient pas d'une banque, et vous donnerez 0 CRE si vous
demandez un chiffre plus grand que ce que la banque peut vous offrir.
```lua
_ = ship << 1000 -- Fraude !
_ = ship << bank(1000) -- Obtiens 0 si la banque a moins de 1000 CRE.
```

Et voila c'est fini !


## Le vrai pouvoir du lua

Bon le but du lua n'est pas de vous faire détester ce langage. Ceci est 
l'utilisation "normale" du lua. Mais en realité, ce language est beaucoup
utilisé dans le jeu video, car il est très simple de le lier avec du C/C++.

En effet, vous pouvez importer du C en lua, et vice-versa, ce qui rends le
lua plus agreable ou plus performant, mais peut egalement servir à des gens
de pouvoir coder en lua pour interragir avec ce que vous faites en C.

Mais cette utilisation va se faire dans un autre workshop...

A SUIVRE (ou pas)
