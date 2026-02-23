Fiche de suivi :Joshua/Les nécéssité de santé kounafoni

### Mon Profil
**Nom :**Famory Josue Sissoko/Joshua
**Rôle :** Membre du groupe 3
###  Module : Conseils de Prévention Dynamiques
**Branche associée :** `conseils-prevention`

#### Objectif
Afficher des recommandations de santé personnalisées en fonction des pathologies ou symptômes signalés par l'utilisateur via l'interface Kounafoni.

#### Fonctionnalités à développer :

* **Moteur de filtrage :** Analyse des alertes (ex: Paludisme, Choléra) pour extraire les conseils de prévention correspondants:
    * Le moteur de filtrage est le "cerveau" logique qui fait le lien entre une alerte sanitaire et la base de connaissances médicale.

    Entrée de données (Input) : Le système reçoit une alerte contenant un code maladie (CIM-10) ou un mot-clé (ex: "diarrhée sanglante").

    Algorithme de correspondance (Matching) : * Le moteur scanne une base de données locale (JSON ou SQL) regroupant les protocoles de l'OMS et du Ministère de la Santé du Mali, il utilise une priorité par gravité : si plusieurs symptômes sont signalés, il extrait d'abord les conseils pour la pathologie la plus critique.

    Sortie (Output) : Extraction de fiches conseils structurées : Gestes immédiats, Symptômes d'alerte, et Orientation vers le centre de santé le plus proche.
  
* **Intégration IA pour automatisation :** Utilisation de l'IA pour générer des conseils de prévention contextuels et mis à jour:

#### Plan de Tests (Contenus) :
1. **Test de pertinence & Test de clarté :** S'assurer que les conseils sont compréhensibles par des non-professionnels de santé (langage vulgarisé).
   Adaptation Géographique et Climatique : * Si une alerte "Paludisme" est détectée pendant la saison des pluies à Bamako, l'IA génère automatiquement des conseils sur la gestion des eaux stagnantes spécifiques à l'environnement urbain.

Traduction et Vulgarisation : * L'IA transforme les termes médicaux complexes en instructions simples et peut traduire les conseils en langues locales (Bambara, Peul, Soninké) pour une meilleure inclusion.

Mise à jour automatique des connaissances : * Au lieu de modifier manuellement le code à chaque nouvelle épidémie, l'IA se connecte aux derniers bulletins épidémiologiques pour mettre à jour les recommandations de prévention sans intervention humaine.

### État d'avancement
- [x] Initialisation de la branche de travail
- [x] Affichage des conseils adaptés aux maladies signalées
