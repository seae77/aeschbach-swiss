# aeschbach.swiss — DNS et mise en ligne

Préparé le 1er octobre 2026. Destination retenue : GitHub Pages, dépôt `seae77/aeschbach-swiss`. Ces enregistrements sont préparés ; ils n'ont pas été posés.

## Ordre d'exécution

1. Fusionner la pull request du site après décision explicite de Sebastian. Activer Pages sur `main`, dossier `/ (root)` et constater une publication réussie.
2. Dans les paramètres personnels GitHub → Pages → Add a domain, demander la vérification de `aeschbach.swiss`. GitHub fournit un jeton TXT propre au compte. Le recopier exactement chez Infomaniak, puis cliquer Verify dans GitHub. Le jeton n'est pas encore émis et ne peut pas être déduit.
3. Dans le dépôt → Settings → Pages, définir le domaine personnalisé `aeschbach.swiss` et enregistrer **avant** de pointer le DNS vers GitHub.
4. Dans manager.infomaniak.com, compte NATURALEX (79528), ouvrir la zone DNS d'aeschbach.swiss. Remplacer seulement les enregistrements web incompatibles pour `@` et `www`, puis saisir les valeurs ci-dessous. Conserver les enregistrements de messagerie (MX, SPF, DKIM, DMARC) et les autres TXT.
5. Après propagation, vérifier le contrôle DNS dans GitHub Pages et activer Enforce HTTPS quand le certificat est disponible. Vérifier le site au domaine racine et la redirection www. Tant que ces contrôles ne réussissent pas, ne pas annoncer le site comme publié.

## Enregistrements exacts

TTL proposé : 3600 secondes. `@` désigne la racine `aeschbach.swiss` ; si Infomaniak demande un champ vide pour la racine, laisser ce champ vide.

| Nom | Type | Valeur |
| --- | --- | --- |
| @ | A | 185.199.108.153 |
| @ | A | 185.199.109.153 |
| @ | A | 185.199.110.153 |
| @ | A | 185.199.111.153 |
| @ | AAAA | 2606:50c0:8000::153 |
| @ | AAAA | 2606:50c0:8001::153 |
| @ | AAAA | 2606:50c0:8002::153 |
| @ | AAAA | 2606:50c0:8003::153 |
| www | CNAME | seae77.github.io. |

Pour la vérification du propriétaire : nom attendu `_github-pages-challenge-seae77` (FQDN `_github-pages-challenge-seae77.aeschbach.swiss`), type TXT ; **valeur indisponible tant que GitHub ne l'a pas émise**. Reprendre le nom exact affiché par GitHub s'il diffère. Ne pas créer un TXT avec un texte provisoire. Garder le TXT après validation. Ne pas créer de wildcard DNS.

Ces instructions sont issues de la [documentation GitHub Pages](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site) et de la [vérification d'un domaine](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/verifying-your-custom-domain-for-github-pages). Les DNS actuels sont à comparer avant modification ; ce fichier n'atteste pas leur état.
