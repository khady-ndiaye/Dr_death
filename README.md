# 🩺 Dr Death - Analyse Power BI du tueur en série Harold Shipman

🎯 Objectif du projet
Ce projet a pour objectif d’explorer les données liées aux meurtres commis par Harold Shipman, considéré comme le tueur en série le plus prolifique du Royaume-Uni. À travers la création d’un dashboard interactif sur Power BI, nous cherchons à répondre à la question centrale :

Quels types de personnes Harold Shipman a-t-il assassinées, et quand sont-elles mortes ?

Ce travail mêle analyse de données et visualisation interactive pour mieux comprendre les tendances, les profils de victimes, ainsi que les anomalies temporelles dans ses crimes.

## 📁 Structure du repository

```
dr-death/
├── README.md                  # Présentation complète du projet
├── datasets/                  # Données brutes utilisées
│   ├── shipman-confirmed-victims.csv
│   └── shipman-times-comparison.csv
├── rapport/                   # Captures du dashboard Power BI
│   ├── visualisation_1.png
│   ├── visualisation_2.png
│   └── ...
└── dr-death-dashboard.pbix    # Fichier Power BI principal
```

## 🔗 Sommaire


## 🔗 Sommaire
<!-- Tu peux compléter cette section avec des liens vers les différentes parties du README -->


## Sommaire

1. VEILLE TECHNOLOGIQUE SUR Power BI
2. SHIPMAN ANALYSIS

   1. CHARGEMENT DES DONNÉES
   2. NETTOYAGES ET TRANSFORMATIONS DES DONNÉES AVEC POWER QUERY
   3. VISUALISATIONS

      * PROFIL DES VICTIMES
      * ANALYSE TEMPORELLE
      * ANALYSE DES LIEUX DE DÉCÈS
      * ÉTUDE DE LA CORRÉLATION
      * COMPARAISONS SHIPMAN VS AUTRES MÉDECINS
   4. CONCLUSION

## 1. VEILLE TECHNOLOGIQUE SUR Power BI

**Power BI** est une solution de Business Intelligence développée par Microsoft, conçue pour transformer des données brutes en visualisations interactives et décisionnelles. Elle permet de centraliser, nettoyer, analyser et présenter des données issues de sources hétérogènes.

🔧 **Fonctionnalités principales**

* **Importation de données multiples** (Excel, CSV, bases de données, API…)
* **Power Query** pour le nettoyage et la transformation des données
* **DAX (Data Analysis Expressions)** pour créer des mesures et indicateurs personnalisés
* **Canvas interactif** pour construire des rapports dynamiques avec filtres, segments et drill-down

✅ **Avantages**

* **Connexion et transformation de données multiples** facilement, sans affecter les bases d'origine
* **Visualisations dynamiques et interactives**, accessibles même pour les utilisateurs non techniques
* **Intégration fluide avec l'écosystème Microsoft** (Excel, Teams, SharePoint, Azure…)
* **Capacité à combiner différents types de données** (structurées et semi-structurées) dans une même analyse
* Interface intuitive avec glisser-déposer
* Performances solides même sur des jeux de données conséquents

❌ **Inconvénients**

* Courbe d'apprentissage pour les fonctions avancées (notamment DAX et M)
* Limitations dans la version gratuite concernant le partage et la collaboration
* Moins adapté aux modèles prédictifs complexes par rapport à des outils comme Python ou R

**Contexte d'usage ici** Dans cette étude, Power BI est utilisé pour analyser des données sensibles et complexes liées à une série de crimes. L'objectif est de **faire parler les données** pour mieux comprendre les schémas criminels de Harold Shipman : profils des victimes, anomalies horaires, lieux de décès, comparaisons régionales.

## 2. SHIPMAN ANALYSIS

### 📚 Contexte de l'affaire

Harold Shipman, surnommé **« Dr Death »**, est considéré comme le **tueur en série le plus prolifique de l'histoire du Royaume-Uni**. Médecin généraliste respecté à Hyde, dans le Grand Manchester, il a assassiné au moins **215 patients entre 1975 et 1998**, principalement des femmes âgées, en leur administrant des doses létales de morphine.

Son comportement a commencé à éveiller des soupçons lorsqu'il a falsifié le testament d'une patiente, ce qui a déclenché une enquête plus large. Celle-ci a révélé des **modifications frauduleuses dans les dossiers médicaux**, des anomalies horaires dans les décès, et des motifs répétitifs dans le profil des victimes. L'affaire a bouleversé le système médical britannique, révélant les dangers d'un **abus de confiance institutionnalisé**.

Ce projet vise à **analyser ces éléments de manière visuelle et interactive**, à l'aide de Power BI, pour dégager les **schémas sous-jacents de ses meurtres**.

### 2.1 CHARGEMENT DES DONNÉES

Deux fichiers principaux ont été utilisés pour conduire l'analyse :

📁 `shipman-confirmed-victims.csv`
Ce fichier contient les données des **victimes officiellement identifiées** de Harold Shipman entre 1975 et 1998.

* **Colonnes clés** : `Name`, `Date_of_death`, `Age`, `Gender`, `Place_of_death`, `Postal_code`
* **Objectif** : Permet de dresser un **profil statistique des victimes**, de visualiser la **chronologie des décès** et d'identifier des **patterns géographiques**.

📁 `shipman-times-comparison.csv`
Ce fichier compare la répartition horaire des décès chez les patients de Shipman avec ceux d'autres médecins généralistes du Grand Manchester.

* **Colonnes clés** : `Hour`, `Shipman_deaths`, `Other_GPs_deaths`
* **Objectif** : Mettre en évidence une **anomalie horaire**, indiquant que Shipman faisait mourir ses patients à des heures spécifiques, contrairement à la norme.

### 2.2 NETTOYAGES ET TRANSFORMATIONS DES DONNÉES AVEC POWER QUERY

Vide

### 2.3 VISUALISATIONS

Vide

## 2.4 CONCLUSION

✅ **1. Un ciblage opportuniste et méthodique**
L'analyse croisée du **graphique sur le genre et l'âge des victimes** avec les données démographiques et juridiques britanniques révèle un **schéma de prédation précis** : Harold Shipman ciblait en priorité des **femmes âgées**, veuves ou proches de l'être. Cela s'explique par plusieurs facteurs :

* En Angleterre, **70 % des femmes survivent à leur conjoint**, ce qui les rend souvent seules et vulnérables.
* Leur **espérance de vie plus longue (85 ans vs 79 ans pour les hommes)** les expose davantage à une prise en charge médicale prolongée.
* En droit anglais, **l'héritage revient au dernier survivant du couple**, ce qui peut motiver la falsification de testaments. Shipman exploitait ainsi une population isolée, peu contestataire et souvent sans témoin direct, maximisant ses chances d'agir sans éveiller de soupçon.

✅ **2. Un mode opératoire calé sur le rythme d'un professionnel "ordinaire"**
Le graphique sur la **répartition hebdomadaire des meurtres** montre une concentration nette des décès entre **le lundi et le vendredi** (plus de 90 % des cas), avec une **chute drastique le week-end** (à peine 8,8 % les samedi et dimanche cumulés).

Ce schéma suggère une logique organisationnelle claire :

* **Shipman agissait comme un "professionnel des heures ouvrables"**, planifiant ses meurtres sur son temps de travail officiel, au rythme des consultations.
* **Les week-ends étaient "off"**, probablement pour préserver son image familiale ou éviter toute logistique compliquée (moins d'interventions médicales prévues, davantage de proches présents au domicile des patients, etc.).

Cette répartition **quasi-bureaucratique des homicides** est troublante : elle montre que Shipman **intégrait le meurtre à sa routine médicale**, comme un acte "technique", inséré dans une journée de travail classique. Ce fonctionnement froid et méthodique renforce le caractère prédateur, **déshumanisé et parfaitement dissimulé** de ses actes.

✅ **3. Une prédation horaire ciblant les moments de vulnérabilité maximale**
L'analyse de la **distribution horaire des décès** révèle un pic saisissant entre 14h et 17h, avec un maximum vers 15h, en contraste net avec la répartition équilibrée des décès naturels. Cette concentration temporelle s'explique par plusieurs facteurs stratégiques :

* **Shipman alignait ses meurtres sur ses visites à domicile de l'après-midi**, après ses consultations matinales en cabinet, créant ainsi une fenêtre d'action prévisible et sécurisée.
* Cette plage horaire offrait une **conjonction optimale d'isolement des victimes**, souvent des femmes âgées seules à leur domicile à ce moment précis de la journée.
* L'après-midi constituait un **moment idéal pour administrer la diamorphine létale**, signer les certificats de décès et falsifier les dossiers médicaux sans témoins.
* Ce schéma temporel lui permettait d'**intercaler ses meurtres entre des visites légitimes**, normalisant ainsi ces événements dans sa routine professionnelle.

Cette signature statistique, identifiée plus tard par le professeur David Spiegelhalter, démontre à quel point Shipman avait méthodiquement intégré ses actes criminels à une pratique médicale en apparence irréprochable. L'heure des décès constitue ainsi un "marqueur comportemental" révélateur, qui aurait pu - selon les experts - permettre sa détection dès 1996, évitant potentiellement des dizaines de victimes supplémentaires.

✅ **4. Une fluctuation révélatrice : l'impact des plaintes et de l'installation en cabinet indépendant**
L'analyse du **graphique de distribution annuelle des meurtres** révèle une anomalie significative : un **net ralentissement de l'activité criminelle entre 1990 et 1992**. Cette période coïncide précisément avec deux événements majeurs :

* **Des plaintes formelles** déposées par des patients auprès de l'autorité sanitaire locale de Donneybrook en 1990 et 1992, suggérant une période de surveillance accrue.
* La préparation puis l'ouverture de son cabinet indépendant au 21 Market Street à Hyde le 1er janvier 1992, après avoir exercé au centre médical de Donneybrook.

Cette **baisse temporaire d'activité criminelle** s'explique par plusieurs facteurs stratégiques :

* Shipman a probablement adopté une **posture de prudence extrême** suite aux plaintes, conscient d'être potentiellement sous observation.
* La période de transition professionnelle exigeait une **image irréprochable** pour attirer de nouveaux patients vers sa pratique indépendante.
* L'établissement d'un nouveau cabinet demandait un **investissement logistique et administratif** considérable, réduisant ses opportunités criminelles.

Le graphique montre ensuite une **reprise progressive** dès 1992-1993, qui s'accélère dramatiquement après 1995 pour atteindre un pic effroyable de près de 40 victimes en 1997. Cette escalade suggère que Shipman, une fois solidement établi dans son cabinet privé et ayant retrouvé un sentiment de sécurité, a non seulement repris ses activités meurtrières mais les a intensifiées de façon alarmante, fort d'une confiance renouvelée et d'une autonomie professionnelle complète.

Cette fluctuation statistique illustre parfaitement la **nature calculatrice et adaptative** de Shipman, capable de moduler temporairement son comportement criminel en fonction des risques perçus, tout en maintenant sa détermination meurtrière sur le long terme.
