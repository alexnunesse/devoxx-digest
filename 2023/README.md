# Devoxx2023
Digest 2023
Autres talks potentiellement intéressant: 
- "Ah, tu peux faire ça en CSS maintenant"
- ""

## Quickie: Avoir un journal de codeur
par Sandrine Banas  
[Description]()

### Exemples de journaux professionels célèbres
Leonard de Vinci, Darwin, Carl Jung, Marie Curie

### Un journal professionnel répond à un besoin
Lequel pour vous?
Exemple: capitaliser des connaissances, suivre la carrière, suivre et affiner sa voie d'expert, ...

### Type de traces
traces informatives: succès, oroblétaqiues, solution, échange collègue, ...  
indicateur SMART: smiley, checkbox, 1 to 10, pourcentage, ...  
traces visuelles: sketchstorm, facilitation graphique, schéma euristique  
traces techniques: DDR, UML, Dos/Dont, Archi, bug, commades, ...  
snippets: extension chrome, github, gitlab, ...  

### Tips
indexation des points importants  
(!) sécurité  
fine tuning: relire chaque jour la veille / 1 semaine / 1 mois  

### Avis perso
Sujet intéressant car on perd souvent de l'information, intéressant d'avoir un rex d'une développeuse avec 20 ans d'XP en Java.

---

## Loi de Conway
par Julien Topçu  
[Description](https://cfp.devoxx.fr/2023/talk/ZQW-2568/Loi_de_Conway_:_lorsque_les_bonnes_pratiques_ne_suffisent_pas)

### Résumé
Découverte de la de Conway qui dit que l'architecture d'un système informatique est fortement couplée à la structure de la société qui la porte.

### Avis perso
Bon talk, bon showman, sujet intéressant qui permet de prendre de la hauteur sur la façon de faire des choix d'architecture, le staffing des équipes, le choix de DDD, ...  
Pas d'exemple concret et de cas d'usage, plutot une sensibilisation au sujet.

4/5

---

## Java 19 & 20
par JM Doudoux  
[Description](https://cfp.devoxx.fr/2023/talk/NHF-2060/Les_nouveautes_de_Java_19_et_20)

### Amber
Record Patterns et Pattern matching

### Panama
Foreing function & memory api  
accès à des ressources natives et de la mémoire off heap  
(!) cette API évolue beaucoup !!

vector api  
optimiser les traitements sur des données vectorisée  
utilisation sur une machine avec un CPU multi coeur (dépend de l'archi x64/ARM)

### Loom
Virtual threads
threads légers, conserve l'approche 1 thread par req, optimiser l'usage des ressources
les threads virtuels hérite de thread, compatibilité débug et profiling
lien m:N entre thread virtuel et thread OS
ne pas mettre les threads virtuels dans un pool (pas de coût)

Structured concurrency
simplifier la programmation multithread
conçue pour des tâches àavec beacoup d'IO
(!) incubation

Scoped values
alternative avec gain aux threadlocal
copie de la valeur du thread parent vers les threads virtuels "enfants"

### Autres évos
Support JDK RISC-V
Evolution de la classe ThreadGroup (qui va surement être déprécié à terme)
JDK 20 ne compile plus de Java 7

### Avis perso
Digest java 19 et 20 qui ne sont pas des LTS, présentation sous forme de liste, bien complète avec la vision de JM, TOP !
C'est bas niveau, c'est précis et pointu, ça montre que Java veut rester à jour: performant et sécuriser.
Attention en Septembre prochain on passe à la LTS Java 21 !

4/5

--- 
 
## Revisiting design patterns after 20
by Edson Yanaga  
[Description](https://cfp.devoxx.fr/2023/talk/YFE-8347/Revisiting_Design_Patterns_after_20)

Design patterns 20 years later

Livecoding, replace you old design patterns with modern java 20+ Java code

github.com/yanaga/revisiting-design-patterns

### Avis perso
Bien sympa d'avoir un peu de livecoding au devoxx, des exemples concrets, pas mal de simplification en vue et donc de boulot

4/5

--- 

## Les dessous des GC
par Jean-Philippe BEMPEL  
[Description](https://cfp.devoxx.fr/2023/talk/UOK-3377/GC:_Comment_dompter_la_bete_et_en_faire_votre_meilleur_allie)

### Serial GC
GC par défaut sur les petites machines

### Parallel GC

### G1
STW
Region based
G1 veut dire Garbage 1st, on priorise le nettoyage des regions avec le plus d'objet à détruire

### Shenandoah
Low latency
Region based
Pas de génération (en cours), single space
Fully conccurent (no STW)

### Z GC
Region based
Colored pointers

### Comment choisir le bon GC
Cas d'utilisation? Throughput oriented (best parallel GC) ou Latency sensitive (best Z GC)

Outil analyse de GC online: GC easy

### Tuning
Taille de la heap, augmenter le nombre de coeur, ajuster les tailles des regions, ...
COnclusion, G1 peut s'avérer très compliqué à tune...

### Avis perso
Talk technique, qui ouvre pas mal de porte, structure du talk complexe, mais le sujet l'est aussi...

4/5

--- 

## Clean Code
by Sonar Cloud  
[Description](https://cfp.devoxx.fr/2023/talk/OBI-1145/Clean_as_You_Code_your_projects)  
https://sonarsource.com 

(Sonar ~200 développeurs)
Le code source est la base d'une aplication, il faut en prendre soin !
L'objectif c'est le clean code, OK.

### Nouveautées sonar cloud
Sonar Lint à ajouter sur son IDE
Outil d'analyse de code: Git oh Theseus

### Question Configuration
Comment configurer correctement sonar et pour des projets différents?
on/off sur les rêgles
rêgles sur la quality gate
ne pas hésiter à remonter le feedback à sonar qui en est friand

### Avis perso
Talk général, intéressant si on découvre complétement le sujet, perte de temps si on utilise déjà sonar et qu'on code correctement.
Outil excellent, talk moins bon. 1/5

--- 

## Springboot 3
by Josh Long (Spring)  
[Description](https://cfp.devoxx.fr/2023/talk/WYX-8335/Bootiful_Spring_Boot_3)

github.com/joshlong/bootiful-spring-boot-3
github.com/spring-tips
github.com/coffee-software-show

error observability support  
micrometer  
buildpack.io  
build:   
buildBootImage  
nativeCompile  
java is energy efficient (thenewstack.io least electricity)  
@GetExcahnge  
Gateaway configuration  
Spring graphql  

### Avis perso
Showtime !!!

5/5

--- 

## Quickie améliorer sa webapp angular
by Camille (takima)  
[Description](https://cfp.devoxx.fr/2023/talk/UBH-0193/6_Tips_pour_ameliorer_sa_Web_App_Angular)

Tips:
- tsconfig path alias pour les imports ts et pour le scss dans angular.json
- trackBy optimisation du tracking ngFor
- utilisation du paint splashing debugger
- unsubscribe -> Observable peuvent entrainer une fuite mémoire
- le pipe async permet d'alléger le code pour afficher des souscription simple
- les resolvers, attention à ne pas trop utiliser car bloque l'affichage de la page

### Avis perso
TOP !

5/5

--- 

## Testing concurrent data structures on JVM
by Maria Sokolova (JetBrains)  
[Description](https://cfp.devoxx.fr/2023/talk/RLK-8019/Lincheck:_Testing_concurrency_on_the_JVM)

Lib developed by Jetbrain for JVM applications
Tes your data strcutures for conccurency with this lib: Lincheck
It uses Linear analysis and byte code markers to check for potential thread unsafe usages

Cas d'utilsiation asez rare

### Avis perso
Talk très technique, mais c'est avec cela qu'on apprend le plus

4/5

--- 

## PostreSQL passez à la vitesse supérieur
par Emmanuel Rémy (Casden)  
[Description](https://cfp.devoxx.fr/2023/talk/QNE-8246/Profitez_de_PostgreSQL_pour_passer_a_la_vitesse_superieure)

Association: PostgreSQL France postgreSQL.fr

2023 v15 de PG - 1ère base des développeurs

Fonctionnalités:
- données typées
- ENUM
- DOMAIN
- génération de données generate_series
- anon génération de données anonymisées (extension PostgreSQL anonymizer) TODO JUSTINE
- partition par défaut
- création de vue anonymisé (attention par utilisateur, avec mode sécu, ...)
- row level security: sécurisation par droit au niveau de slignes
- cron TODO JUSTINE
- fonction en Java, python, ...
- foreign data wrapper, FDW, très puissant !! (et plein d'API, spreadsheet, web, GC)
- JSON: performant pour les requètes, jsonpath top, ...


### Avis perso
Présentation simple et efficace avec bcp de livecoding, au top

5/5

--- 

## Découvertes sur les stands

### Gravity by smarttesting
Coverage des tests end to end
Licence assez cher, mais produit simple et intéressant
Plusieurs usages:
- enregistre le comportement des utilisateurs (watcher js type GA)
- génère des tests basés sur les scénarios enregistrés
- calcul le coverage des tests e2e

### JFrog
check plugin xrayvjfrog intellij  
release bundle v2 release lifecycle management soon  
intégration ok avec gitlab + frogbot

---
