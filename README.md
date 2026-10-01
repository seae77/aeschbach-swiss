# aeschbach.swiss

Site personnel de Sebastian Aeschbach : présentation, mandats, prises de position et contact. HTML et CSS statiques, sans dépendance ni JavaScript.

## Contenu et sources

- Mandat municipal et portrait : [PLR Ville de Genève](https://www.associations-plrge.ch/les-associations/ville-de-geneve/personnes/conseillers-municipaux).
- Mandat cantonal et adresse publique de contact : [Grand Conseil](https://ge.ch/grandconseil/m/gc/depute/2537/).
- Formation et législature municipale : [déclaration officielle de liens d'intérêts 2025](https://www.geneve.ch/document/aeschbach-sebastian-liens-interets-conseil-municipal-geneve-2025).
- Priorités politiques et première élection en 2020 : lettre personnelle de candidature municipale du 9 septembre 2024, conservée dans les archives privées du propriétaire. La lettre elle-même et les autres documents privés ne sont pas publiés dans ce dépôt.
- Portrait repris de la fiche publique PLR : `https://www.associations-plrge.ch/fileadmin/_processed_/2/f/csm_Sebastien_Aeschbach_942f0530b7.jpg`.

Les priorités sont présentées comme celles de la candidature 2025. Aucun nouveau programme, engagement ou bilan chiffré n'est ajouté. Les fiches publiques ont été consultées le 1er octobre 2026.

## Prévisualisation

Depuis ce dossier : `python -m http.server 8765 --bind 127.0.0.1`, puis ouvrir `http://127.0.0.1:8765/`.

## Hébergement retenu : GitHub Pages

GitHub Pages convient à cette page statique : pas de serveur à administrer, pas de dépendances à maintenir et pas d'hébergement supplémentaire à acheter pour un dépôt public. Le domaine reste enregistré chez Infomaniak. La procédure et les valeurs DNS figurent dans [DNS.md](DNS.md).

Les modifications passent par une branche, un commit et une pull request. La première version doit être fusionnée explicitement avant publication. Après fusion, choisir **Settings → Pages → Deploy from a branch → main / (root)**. Aucun workflow personnalisé n'est nécessaire. Une publication depuis une branche utilise néanmoins une exécution GitHub Pages : vérifier son résultat réel ; ne pas contourner les restrictions de facturation ou de protection du compte.

Le domaine personnalisé est à configurer dans Pages **avant** de modifier ses DNS. Ne pas créer de CNAME dans le dépôt avant cette étape : GitHub gère le fichier lors de la configuration du domaine. Activer **Enforce HTTPS** après émission du certificat, puis vérifier `https://aeschbach.swiss` et la redirection de `https://www.aeschbach.swiss`.

## Propriété du domaine

Le domaine aeschbach.swiss est actuellement payé par Naturalex et enregistré sur le compte Infomaniak NATURALEX (79528). Il doit être rattaché à un compte personnel de Sebastian Aeschbach ou faire l'objet d'une refacturation. Le site personnel ne représente pas Naturalex.

## Vie privée et maintenance

Aucun outil de mesure d'audience, formulaire, police distante ou cookie applicatif. Seuls l'hébergeur et, après activation d'un lien, les destinations externes peuvent traiter les données techniques de connexion. Le contact utilise l'adresse politique déjà publique au Grand Conseil. Ne jamais ajouter au dépôt de correspondance privée, de données administratives, de secrets ou de justificatifs.

Les fichiers `index.html` et `styles.css` constituent la version canonique. Mettre à jour les mandats et les liens si la situation réelle change.
