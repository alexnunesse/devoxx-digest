# devoxx-2022
Devoxx 2022 notes

## Micro Frontends REX - Diviser pour mieux régner !
> Hugo CHIAVENUTO
> [https://cfp.devoxx.fr/2022/talk/YCJ-0118/Micro_Frontends_REX_-_Diviser_pour_mieux_regner_!]
> 10h45: 241 - Paris

équipe: 3 apps, 15 devs
Manfred Steyer (dev angular)

### Lombard Odier Group
Bank à Genève
Bank As A Service
Pas mal de legacy, client lourd monolithique

### Concept
Approche Composant vs MFE
Approche horizontale -> SSR
Approche Verticale
Webpack 5 fédération de module + lazy loading

### Pratique
POC sur 1 vue à découper en micro frontend
Layout embarque des widgets
Les widgets sont autonomes (interaction serveur, ...)
Communication inter-widget par bus de communication (events)

### Challenges & pitfalls
Global state: utilisation de store + observables 
Cache Http: au niveau du service http de haut niveau
Widget State: identifier les widgets?
Gestion des modules angular: galère pour l'instant
-> solution pe dans angular 14.1 (no modules)

----

## Model-Driven Design
> Bruno BOUCARD

Problème d'interdépendance sur le schéma DB
42zkillz?
wirfs-brook.com

### Cas d'école
Réservation de place de théatre
étude 
-> event storming (atelier)
-> example mapping
-> MDD

### Livecoding
Utilisation des ValueObject entre les couches de Controller et Service

### Aller plus loin
-> deep model
analysis oattern
TDD Outside/In

### Take away
![](README/MDD.png)
Blue book Domain-Driven Design


-----

## What's cooking in maven
> Maven 4 what's new ?
> Maarten Mulders
> Commiter on maven

### Maven wrapper
Supported by apache officialy now
apache-wrapper.sh

### Build/Consumer POM
pom in vcs != pom in repo
will allow to change pom structure without breaking mvn version

### Improved reacto
In a multi module scenario (100+ modules)
Improved the reactor so that it can scan folders for modules without resolving
Use empty file .mvn to indicate that the dir is the top level of the app
Resume failing build more easily
Compile project in different directory with -f option

### Dessert: Maven deamon
Goal: make the build faster (it does ! it looks very very quick)
cool option to debug long build time: -Dmvnd.buildTime=true
Keeps things warm (memory, JVM, modules, plugins, ...)
Multi-thread the build by default
Probably wont support the wrapper

### Take away
![](README/mvn4.png)
Release date unknown

----

## Lens
> k8s graphical interface open source (talk by Mirantis)

Kubernetes IDE number 1
-> bonne outil pour démarrer avec kube
-> goto solution for Carrefour

----

## The unknowns of JUnit 5
> 

### Data table tests
RTFM !
Use @ParameterizedTest
Use @CsvSource
Nice aswell: @DyanmicTest, ...

### Wiremock
@ExtendWith (+BeforeAllClass, resolveParameter, ...) instead of inheritance
-> go WiremockExtensions

### Parallelize
@Execution (still experimental)
use junit config files

### Link to sources
{screen3}



----

## Sujets transverses
Sujet pour la formation devops 1: gitpod
Sonatype (aka nexus) OSS index (scan secu)

