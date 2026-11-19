# Politique de confidentialité — SocFace Collecteur

Version 6.1.0 — mise à jour le 19 novembre 2026.

**Éditeur : Jean-Badoit Corp**

**Contact public : jeanbadoitcorp@outlook.fr**

## Objet

SocFace Collecteur est une extension indépendante pour collecter, vérifier et exporter localement les informations des recensements SocFace accessibles sur FranceArchives. Elle n’est pas affiliée à FranceArchives ni au projet SocFace. Elle fonctionne avec les patronymes et filtres choisis par l’utilisateur.

## Déclenchement et accès

L’extension intervient après un clic sur son icône. Elle vérifie l’adresse de l’onglet et ouvre son panneau uniquement sur une page de recherche de recensements de `https://francearchives.gouv.fr`. La collecte est ensuite commandée depuis ce panneau.

Les autorisations `activeTab` et `scripting` servent à cette ouverture volontaire. Le collecteur s’exécute dans le contexte principal de la page FranceArchives, appelé MAIN, et utilise les ressources de cette origine. Il ne consulte pas l’historique global du navigateur, les autres onglets ou les mots de passe enregistrés.

## Informations traitées

Le collecteur traite les filtres et l’URL de la recherche, les pages et exports de résultats, les notices et les listes de ménages. Ces données peuvent comprendre des noms, prénoms, âges, professions, lieux, dates, liens familiaux, références d’archives et liens vers les documents numérisés.

L’utilisateur peut aussi importer volontairement des fichiers CSV ou JSON pour reprendre sa recherche. Le contenu de ces fichiers est traité localement. Les informations de progression, de contrôle et d’erreur sont affichées dans le panneau et peuvent être conservées avec la sauvegarde ; des erreurs peuvent aussi apparaître dans la console locale du navigateur.

Le nettoyage de présentation retire uniquement des textes d’aide génériques connus dans leurs champs. Il conserve les données d’origine dans l’onglet brut du classeur. Il ne vérifie pas la vérité historique des transcriptions.

## Connexions réseau et cookies

Les requêtes du collecteur sont adressées à FranceArchives pour lire les résultats, notices et ménages nécessaires à la recherche. Le navigateur communique donc au site les adresses et paramètres demandés, ainsi que les informations de connexion qu’il transmet habituellement, notamment l’adresse IP.

Les requêtes utilisent `credentials: same-origin` : le navigateur peut joindre les cookies ordinaires du site, selon ses propres réglages. L’extension ne lit pas la valeur des cookies et ne crée pas de cookie de suivi.

L’extension ne transmet automatiquement aucun fichier, résultat ou paramètre de recherche à un serveur du développeur. Elle ne contient ni télémétrie, publicité, suivi intersites ou service d’analyse. Elle ne charge aucun code exécutable distant.

FranceArchives applique ses propres conditions et sa propre politique de confidentialité aux consultations de son site. Les fonctions normales d’Edge et du magasin, notamment la distribution et les mises à jour de l’extension, relèvent de leurs services respectifs.

## Sauvegardes et fichiers

Les sauvegardes automatiques utilisent **IndexedDB**, sous l’origine FranceArchives, dans la base `SocFaceCollector` et le magasin `snapshots`. Les enregistrements sont associés aux critères de recherche pour permettre une reprise compatible. Ils peuvent inclure les notices, ménages, paramètres, contrôles de complétude et progression.

Le collecteur peut réutiliser les anciennes sauvegardes V4/V5 compatibles présentes dans le `sessionStorage` de l’onglet. Ces sauvegardes de session suivent la durée de vie de la session du navigateur.

Ce stockage est rattaché au contexte du site FranceArchives ; ce n’est pas un espace isolé sous une origine propre à l’extension. Les sauvegardes ne sont pas envoyées au développeur et ne constituent pas un service de synchronisation fourni par l’extension.

Les exports CSV, JSON et XLSX sont créés localement et téléchargés à l’emplacement choisi ou configuré par l’utilisateur. Leur conservation, leur éventuelle synchronisation par un service de stockage du système et leur partage ultérieur dépendent de l’utilisateur et de ses réglages.

## Conservation et suppression

L’extension ne fixe pas d’expiration automatique aux sauvegardes IndexedDB. Elles restent disponibles jusqu’à leur suppression ou jusqu’à une suppression des données de site par le navigateur. Fermer le panneau ou désinstaller l’extension ne supprime pas nécessairement les données stockées sous l’origine FranceArchives.

Pour les retirer, l’utilisateur peut supprimer la base `SocFaceCollector` dans les outils de développement du site, rubrique Application → IndexedDB, ou effacer les données de site FranceArchives dans les paramètres d’Edge. Cette seconde option peut aussi supprimer les autres données et cookies de ce site. Les fichiers téléchargés se suppriment séparément depuis leur dossier ; les copies synchronisées ou partagées se gèrent auprès des services concernés.

## Partage et contrôle par l’utilisateur

L’éditeur ne reçoit pas automatiquement les recherches et ne dispose pas d’une copie distante à supprimer. Aucun achat ou compte propre à l’extension n’est requis. L’utilisateur choisit quand lancer une collecte, l’arrêter, importer un fichier ou exporter et partager ses résultats.

Si vous contactez volontairement l’éditeur, les informations et pièces que vous lui adressez sont celles que vous choisissez de communiquer. N’envoyez pas de données familiales privées pour une simple demande d’assistance ; un exemple fictif peut suffire.

## Cette page de confidentialité

La page statique fournie avec le projet n’ajoute aucun script, traceur, cookie, police distante ni formulaire. Son hébergeur peut néanmoins traiter des journaux techniques de visite selon sa propre politique. Si elle est hébergée sur GitHub Pages ou Gist, les règles de GitHub s’appliquent à la visite de cette page.

## Contact et évolution

Pour une question relative à l’extension, utilisez le contact public de l’éditeur indiqué en tête de cette politique. Toute évolution du fonctionnement ou des échanges de données doit être reflétée dans une politique mise à jour.
