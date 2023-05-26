# Charte Open Source

**Pour la publication en open source sur le**
**GitHub de la République et Canton de Genève.**

(Version 0.1 - Brouillon)

(Ce document est a usage de l'OCSIN, il est publié ici pour information, mais peut contenir des liens non fonctionnels hors services IT)

Cette page décrit les points auxquels le développeur s'engage à veiller avant de publier son code en open source sur : [https://github.com/republique-et-canton-de-geneve](https://github.com/republique-et-canton-de-geneve)

Cette charte est divisée en 8 domaines. Les responsables de publication(1) de code s'engagent à la respecter, et la faire respecter par les autres participants qui contribuent à la publication de code.

**Autorisation de publier**  : L'autorisation de publier le code sur GitHub est acquise, néanmoins il faut s'assurer de l'accord des parties prenantes.

 - La diffusion en open source est non seulement autorisée, mais aussi recommandée par l'OCSIN qui a même défini et avalisé une [stratégie open source](https://github.com/republique-et-canton-de-geneve/strategie-open-source).
 - Chaque manager soutient son équipe et établit les conditions de contrôle des éléments de la charte.

**Confidentialité**  : L'exposition des sources de GitHub ne doit pas fournir d'informations d'attaque aux personnes mal intentionnées, en s'assurant que les secrets ont été éliminés, tant dans les sources _que dans l'historique des sources_.

 - Par "secret" on entend toute information sensible, pas seulement les mots de passe : les noms d'utilisateurs, les noms de machines, les URL internes à l'État, notamment. La procédure recommandée est de scanner les dépôts GitLab, de façon préventive. (A CONTINUER)
 - Pour éliminer les secrets déjà présents dans l'historique des sources, prendre contact avec le SMIL.

**Sécurité**  : Les sources publiées ne doivent pas contenir de failles de sécurité dont un pirate pourrait profiter pour attaquer l'application en production, en s'assurant qu'un scan de vulnérabilités des dépendances avec l'outil Nexus IQ ainsi qu'unqu'une analyse SonarQube de détection de failles de sécurité dans le code ont été exécutés et leurs résultats analysés.

 - Le développeur mène ces actions non seulement avant publication, mais aussi par la suite. Si le code n'est stocké que sur GitHub (et non sur le GitLab interne), alors le développeur devrait mener une analyse SonarCloud.

**Licence**  : Le fait de ne pas indiquer de licence sur un code publié crée une incertitude juridique sur celui-ci. Il faut donc s'assurer que les sources incluent un fichier de licence des leur publication.

 - Si on a n'a pas d'idée sur la licence à utiliser, choisir la licence par défaut de l'État : AGPL v3. Si besoin, se référer à [cette page](https://github.com/republique-et-canton-de-geneve/squelette-github).

**Isolement**  : Un utilisateur externe qui clone un dépôt GitHub doit être en mesure de construire le logiciel (build) et de l'exécuter, sans être bloqué par des adhérences sur des briques propres à l'État, comme Gina ou un service web interne.

 - Il faut s'assurer que les adhérences sont bouchonnées, tant en ce qui concerne les les dépendances, que dans le code lui-même. Si cela s'avère impossible, il convient de mentionner clairement dans le README que la construction ou l'exécution du livrable est impossible et que donc le livrable n'est présent principalement pour en permettre la consultation et l'étude.

**Qualité**  : Le code exposé sur GitHub participe à la réputation de l'État, il doit donc être de qualité. Des tests unitaires doivent notamment être présents.

 - Il convient de s'assurer que le code est soumis à l'analyse SonarQube, que les failles détectées ont été éliminées et que le taux de couverture par les tests unitaires est satisfaisant.
 - Une fois que le code est publié sur GitHub, il faut également s'assurer que le code est soumis à l'analyse SonarCloud, via une Action dans GitHub
 - Cette qualité de code sert en retour la qualité de l'application en production en interne.
 - Pour l'analyse SonarCloud, un exemple de configuration est fourni par le projet [gitSync](https://github.com/republique-et-canton-de-geneve/git-sync/blob/master/.github/workflows/maven.yml). 
 - Le SMIL est à disposition pour fournir du support (voir plus bas).

**Documentation**  : Le code exposé sur GitHub participe à la réputation de l'État, il doit donc être correctement commenté, en s'assurant qu'un fichier README exhaustif est inclus dans les sources et que lecode est commenté, avec une attention particulière pour les interfaces.

- Le README doit comprendre : le but du logiciel, ses règles métier, le moyen technique de le construire (build) et le moyen de l'exécuter.

**Suivi**  : Les responsables de publication de code s'engagent à traiter les éventuels retours de la communauté : questions, propositions, pull requests, etc. en particulier en se réservant du temps pour le faire.

- Il faut être disposé à consacrer du temps à ces retours, même quand le projet EdG de développement sera terminé.

***Note : (1)*** Le "responsable de publication" est une personne de l'équipe du projet qui s'occupe du processus de publication sur GitHub. Ce rôle peut être tenu par une ou plusieurs personnes, par exemple un ou plusieurs développeurs.

Pour toute demande d'information ou de support, le mieux est de créer une fiche Jira dans le projet Jira OPENSRC. L'équipe se fera un plaisir de vous répondre et de vous aider.
