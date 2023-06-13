# Charte open source

Ce document liste les points auxquels les équipes s'engagent à veiller avant
de publier leur code en open source sur
[la page GitHub de l'Etat](https://github.com/republique-et-canton-de-geneve).

## Présentation

Cette charte est divisée en 8 domaines.
Un "responsable de publication" de code s'engage à respecter cette charte 
et la faire respecter par les autres membres de l'équipe qui contribuent
à la publication du code.
Le "responsable de publication" est un membre de l'équipe du projet qui s'occupe
du processus de publication sur GitHub ;
ce rôle peut être tenu par une ou plusieurs personnes, habituellement un
ou plusieurs développeurs.

## La charte

**1. Autorisation de publier**

Comme l'autorisation de publier le code sur GitHub est d'emblée acquise,
l'équipe s'assure simplement de l'accord des parties prenantes.

- La diffusion en open source est non seulement autorisée, mais aussi recommandée
  par l'OCSIN qui a même défini et avalisé une
  [stratégie open source](https://github.com/republique-et-canton-de-geneve/strategie-open-source).
- Chaque manager soutient son équipe et établit les conditions de contrôle des
  éléments de la charte.

**2. Confidentialité**

Comme l'exposition des sources de GitHub ne doit pas fournir d'informations
d'attaque aux personnes mal intentionnées,
l'équipe s'assure qu'elle a éliminé
tous les secrets, tant dans les sources _que dans l'historique des sources_.

- Par "secret" on entend toute information sensible, pas seulement les mots de
  passe : les noms d'utilisateurs, les noms de machines, les URL internes à l'État,
  notamment.
  La procédure recommandée est de scanner les dépôts GitLab, de façon préventive.
- Pour éliminer les secrets déjà présents dans l'historique des sources, prendre
  contact avec l'équipe des Moyens de développement (voir plus bas).

**3. Sécurité**

Comme les sources publiées ne doivent pas contenir de failles de sécurité dont
une personne mal intentionnée pourrait profiter pour attaquer l'application
en production à l'État,
l'équipe s'assure qu'un scan de vulnérabilités des dépendances avec ainsi
qu'une analyse de détection de failles de sécurité dans le code ont été exécutés
avec les outils disponibles à l'OCSIN,
puis que leurs résultats ont été analysés.

- L'équipe mène ces actions non seulement avant publication, mais aussi
  par la suite.
  Si le code n'est stocké que sur GitHub (et non sur le GitLab interne), alors
  l'équipe devrait mener une analyse avec l'un des outils disponibles à l'OCSIN.
- L'équipe s'engage à rayer de la liste des mainteneurs du projet GitHub
  les membres qui ont quitté le projet ou l'OCSIN.

**4. Licence**

Comme le fait de ne pas indiquer de licence sur un code publié crée une incertitude
juridique sur celui-ci, l'équipe s'assure que les sources publiées incluent un
fichier de licence.

- Si l'équipe n'a pas d'idée sur la licence à utiliser, elle peut choisir la
  licence par défaut de l'État :
  [AGPL v3](https://www.gnu.org/licenses/agpl-3.0.fr.html).
  Si besoin, se référer à
  [cette page](https://github.com/republique-et-canton-de-geneve/squelette-github).

**5. Isolation**

Comme un utilisateur externe qui clone un dépôt GitHub doit être en mesure de
construire le logiciel (build) et de l'exécuter,
l'équipe s'assure que le code ne contient aucune adhérence sur des briques propres
à l'État, comme Gina ou un service web interne.

- Il faut s'assurer que les adhérences sont bouchonnées, tant en ce qui concerne
  les dépendances que dans le code lui-même.
  Si cela s'avère impossible, il convient de mentionner clairement dans le README
  que la construction ou l'exécution du livrable est impossible et que donc le
  code n'est publié sur GitHub que pour en permettre la consultation et l'étude.

**6. Qualité**

Comme le code exposé sur GitHub participe à la réputation de l'État,
l'équipe s'assure que ce code est de qualité.
- Des tests unitaires doivent notamment être présents.
- Le code est soumis à l'analyse d'outils de qualité, tels SonarQube,
  les failles détectées ont été éliminées et le taux de couverture par les tests
  unitaires est satisfaisant.
- Une fois que le code est publié sur GitHub, il doit être soumis à une analyse
  de qualité par un outil disponible depuis l'extérieur de l'OCSIN, comme
  SonarCloud, via une Action dans GitHub
- Cette qualité de code sert en retour la qualité de l'application en production
  en interne.
- Un exemple de configuration d'analyse est fourni par le projet
  [gitSync](https://github.com/republique-et-canton-de-geneve/git-sync/blob/master/.github/workflows/maven.yml). 
 - Le SMIL est à disposition pour fournir du support (voir plus bas).

**7. Documentation**

Comme le code exposé sur GitHub participe à la réputation de l'État,
l'équipe s'assure qu'il est correctement commenté.
- Un fichier README exhaustif est inclus dans les sources. 
  Ce fichier doit comprendre : le but du logiciel, si possible ses règles métier,
  le moyen technique de le construire (build) et le moyen de l'exécuter.
- Le code lui-même est commenté, avec une attention particulière pour les interfaces.


**8. Suivi**

Comme le respect fait partie des valeurs du monde de l'open source,
l'équipe s'engage à traiter les éventuels retours de la communauté :
questions, propositions, pull requests, etc.
- Il faut être disposé à consacrer du temps à ces retours, même quand le projet EdG de développement sera terminé.
- Il faut être attentif aux pull requests hostiles, visant par exemple à
  introduire des failles de sécurité.

## Remarques

Pour toute demande d'information ou de support, le mieux est de créer,
à l'attention de l'équipe des Moyens de développement (SCLI),
une fiche Jira dans le projet Jira OPENSRC.
