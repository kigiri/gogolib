# libft

## Description
Ce premier projet en tant qu'étudiant de 42 va vous faire consolider vos acquis de piscine. Vous allez recoder un certain nombre de fonctions de la librairie C standard, ainsi que d'autres fonctions utilitaires que vous réutiliserez tout au long de votre cursus.

## Type
T1

## Team 
solo

## ETA
about 1 week

## Objectives
- Bases de C 
- Libc 
- Génération d'une libraire statique 

## Skills
- Imperative programming 
- Rigor 
- Algorithms & AI 

## Videos
[notion 1](https://elearning.intra.42.fr/notions/20)

## Subject

### Résumé
Ce projet a pour but de vous faire coder en C une bibliothèque de fonctions
usuelles que vous pourrez utiliser dans tous vos projets.

![](https://i.imgur.com/NmGFOFU.png)

### Introduction
Le projet libft reprend le concept du D06 de la piscine, à savoir vous faire écrire une
bibliothèque de fonctions utiles que vous pourrez ensuite utiliser dans la vaste majorité
de vos projets de C cette année et ainsi vous faire gagner beaucoup de temps. Ce projet
vous demande d’écrire beaucoup de code que vous avez déja réalisé pendant la piscine,
ce qui en fait un excellent moment pour faire le point sur votre avancement.

### Objectifs
La programmation en C est une activité très laborieuse dès lors qu’on a pas accès à
toutes ces petites fonctions usuelles très pratiques. C’est pourquoi nous vous proposons
à travers ce projet de prendre le temps de réécrire ces fonctions, de les comprendre et
de vous les approprier. Vous pourrez alors réutiliser votre bibliothèque pour travailler
efficacement sur vos projets en C suivants.
Ce projet est également pour vous l’occasion d’étendre la liste des fonctions demandées
avec les vôtres et ainsi de rendre votre bibliothèque encore plus utile. N’hésitez pas à
compléter votre libft tout au long de votre scolarité une fois que ce projet ne sera plus
qu’un souvenir pour vous.

### Consignes générales
- Les fonctions sont à réaliser dans l’ordre que vous souhaitez et vous êtes très encouragés à utiliser les fonctions déja codées pour réaliser les suivantes. La difficulté n’est pas croissante et l’ordre du sujet parfaitement arbitraire. C’est un peu comme dans un jeu vidéo où vous pouvez réaliser des quêtes dans l’ordre que vous voulez et utiliser le loot des précédentes pour vous faciliter les suivantes.
- Votre projet doit être à la Norme
- En aucun cas vos fonctions ne doivent quitter de façon inattendue (Segmentation fault, bus error, double free, etc) en dehors des comportements indéterminés. Votre projet serait alors considéré comme non fonctionnel et recevra la note de 0 en soutenance.
- Toute mémoire allouée sur le tas doit être libérée proprement quand nécéssaire.
- Vous devez rendre, à la racine de votre dépôt de rendu, un fichier auteur contenant votre login suivi d’un ’\n’ :
```bash
$> cat -e auteur
xlogin$
```
- Vous devez rendre un fichier C par fonction à réaliser ainsi qu’un fichier libft.h qui contiendra tous leurs prototypes ainsi que les macros et les typedefs dont vous pourriez avoir besoin. Tous ces fichiers devront se trouver à la racine de votre dépot.
- Vous devez rendre un Makefile qui compilera vos sources vers une bibliothèque statique nommée libft.a.
- Votre Makefile doit au moins proposer les règles $(NAME), all, clean, fclean et re dans l’ordre qui vous paraîtra le plus adapté.
- Votre Makefile doit compiler votre travail avec les flags de compilation -Wall, -Wextra et -Werror.
Seules les fonctions suivantes de la libc sont autorisées : malloc(3), free(3) et
write(2) et leur utilisation est restreinte, voir plus bas.
- Vous devez bien entendu inclure l’include système nécessaire pour utiliser l’une ou l’autre des 3 fonctions autorisées dans votre fichier .c concerné. Le seul include système que vous êtes autorisés à utiliser en plus est string.h pour avoir accès à la constante NULL et au type size_t. Tout le reste est interdit.
- Nous vous encourageons à réaliser un ou plusieurs programmes de test pour votre bibliothèque. Bien que ce travail ne soit pas à rendre sur votre dépot et ne sera pas évalué, il vous permettra de tester facilement votre travail et celui des autres. Hormis dans le cadre de la piscine à distance qui n’en contient pas, vous trouverez une utilité particulière pour ces tests lors des soutenances. Vous êtes dans ce cadre là libres d’utiliser vos tests ou ceux du souteneur/soutenu voire même les deux si cela vous fait plaisir et la logistique sous-jacente est à votre discrétion.

### Partie obligatoire

#### Considérations techniques
- Votre fichier libft.h peut contenir des macros et des typedefs selon vos besoins.
- Une chaine de caractères est TOUJOURS terminée par un ’\0’, même si cela
a été omis dans la description d’une fonction. Dans le cas contraire, cela serait
explicitement indiqué.
- Interdiction d’utiliser des variables globales.
- Si vous avez besoin de fonctions auxiliaires pour l’écriture d’une fonction complexe,
vous devez définir ces fonctions auxiliaires en static dans le respect de la Norme.
Savoir ce qu’est une fonction statique est un bon début : http:
//codingfreak.blogspot.com/2010/06/static-functions-in-c.html
- Vous devez prêter attention à vos types et utiliser judicieusement les casts quand
c’est nécéssaire, en particulier lorsqu’un type void * est impliqué. Dans l’absolu,
évitez les casts implicites, quels que soient les types concernés. Exemple :
```c
char *str;
str = malloc(42 * sizeof(*str)); /* Wrong ! Malloc retourne un void * (cast implicite) */
str = (char *) malloc(42 * sizeof(*str));
```
#### Part 1 - Fonctions de la libc
Dans cette première partie, vous devez recoder un ensemble de fonctions de la libc
telles que décrites dans leur man respectif sur votre système. Vos fonctions devront avoir
exactement le même prototype et le même comportement que les originales. Leur nom
devra être préfixé par “ft_”. Par exemple strlen devient ft_strlen.
Certains prototypes des fonctions que vous devez recoder utilisent
le qualifieur de type "restrict". Ce mot clef fait parti du standard
c99, vous devez donc ne pas le mettre dans vos prototypes et ne pas
compiler avec le flag -std=c99.
Vous devez recoder les fonctions suivantes :
• memset
• bzero
• memcpy
• memccpy
• memmove
• memchr
• memcmp
• strlen
• strdup
• strcpy
• strncpy
• strcat
• strncat
• strlcat
• strchr
• strrchr
• strstr
• strnstr
• strcmp
• strncmp
• atoi
• isalpha
• isdigit
• isalnum
• isascii
• isprint
• toupper
• tolower
