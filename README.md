# Multiboot avec OpenCore

Bonjour! On dirait que vous essayez d'avoir macOS et $(OtherOS) installé sur votre système, mais vous ne voulez pas non plus gâcher $(OtherOS) ou macOS dans le processus. Vous serez guidé ici à travers une multitude d'étapes pour y parvenir tout en gardant les configurations du système d'exploitation aussi inchangées que possible.

## Types de micrologiciels

Le multiboot est fortement affecté par le type de firmware que vous utilisez. Ce guide couvrira les 2 types connus qui sont :&#x20;

* UEFI
* Legacy/CSM/BIOS

Les différences sont minimes une fois que vous utilisez OpenCore, mais cela peut également être un peu difficile pour ce dernier. En dehors de cela, ce guide couvrira ces éléments :&#x20;

1. Qu'est-ce que le multiboot et comment ça marche ?
2. Partitionnement vs séparation de disque
3. UEFI
   1. Un disque pour tous les systèmes d'exploitation
   2. Différents disques pour différents systèmes d'exploitation
4. Legacy
   1. Un disque pour tous les systèmes d'exploitation
   2. Différents disques pour différents systèmes d'exploitation
5. Dépannage
6. Trucs et astuces

## <mark style="color:red;">Disclaimer</mark> <a href="#disclaimer" id="disclaimer"></a>

Nous ne sommes pas responsables des appareils qui on été briqués, des disques durs morts, de la guerre thermonucléaire ou de votre licenciement parce que vous avez eu un kernel panik et que vous n'avez pas enregistré votre travail. Vous êtes responsable de tout, lisez attentivement avant de faire quoi que ce soit. Faites vos recherches et demandez de l'aide si vous avez des questions ou des problèmes avant d'essayer des choses au hasard sur Internet parce que "c'est Internet". Si vous le faites, VOUS choisissez de suivre des choses aléatoires sur Internet, et si VOUS nous pointez du doigt pour avoir gâché votre appareil, NOUS rirons de vous.

Maintenant que nous avons réglé cela, allons-y, et bonne chance.
