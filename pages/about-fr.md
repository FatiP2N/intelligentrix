# À propos d’Intelligentrix

Intelligentrix est une plateforme gratuite d'analyse bibliométrique et de veille technologique. Elle cartographie la production scientifique et les brevets d'un sujet, d'un pays ou d'un ensemble de fichiers, à partir de bases ouvertes et de vos propres exports.

## Démarrer en trois étapes

1. Choisissez un onglet : **Recherche en direct** (publications OpenAlex), **Brevets** ou **Importer et fusionner** (vos exports Web of Science, Scopus, Publish or Perish).
2. Saisissez vos critères : un sujet, un ou plusieurs pays, une période, puis **Analyser**.
3. Lisez les indicateurs, la carte, le classement et les réseaux ; copiez les tableaux en CSV pour vos rapports.

## Recherche en direct

Les publications viennent d'**OpenAlex**, une base ouverte de plus de 300 millions de documents. Le sujet est cherché dans les titres et les résumés ; laissez-le vide pour analyser toute la production d'un pays.

- **Pays** : ajoutez un ou plusieurs pays. Un seul pays affiche son **rang mondial** et sa part de la production mondiale ; le panneau carte bascule entre le classement mondial et les **pays partenaires** (co-publications).
- **Comparer avec** : un second sujet ou un second pays, tracé sur la courbe annuelle.
- **Carte** : cliquez un pays (ou une ligne du classement) pour ouvrir son profil.
- **Actualisation automatique** : relance l'analyse toutes les 5, 15 ou 60 minutes.

## Brevets

Filtrez par mots-clés, par code **CPC** ou **CIB/IPC** (par exemple `H10K` ou `Y02E10/549`, plusieurs codes séparés par des virgules), par **déposant** et par **juridiction** (office de publication : Maroc, Office européen, OMPI…). Les données viennent de l'OEB en direct ; sans mot-clé, l'onglet affiche tous les brevets publiés l'année la plus récente, et la carte mondiale se remplit au fur et à mesure, car l'OEB limite le nombre de recherches par minute. Les déposants, leurs pays, la classification et les réseaux sont calculés sur les notices des 100 premières familles renvoyées par l'OEB. Le bouton **Voir l'échantillon** affiche un export Espacenet réel (100 familles sur le dessalement de l'eau de mer). Les comptages OEB portent sur des **publications** (une invention publiée dans cinq offices compte cinq fois) ; l'échantillon Espacenet est compté en **familles**. Le statut juridique n'est pas fourni sous forme agrégée par l'OEB : il n'est pas affiché.

- **Pays de priorité** : pays du premier dépôt, qui indique l'origine de l'invention.
- **Pays de protection** : offices où la famille du brevet est publiée.
- **Office de publication** : office qui a publié chaque document.
- **Classification** : regroupement par sous-classe (H10K), groupe (H10K30) ou sous-groupe (H10K30/50) ; cliquez une barre pour filtrer.

## Banque mondiale

L'onglet **Banque mondiale** interroge en direct l'API gratuite de la Banque mondiale (World Development Indicators). Choisissez un indicateur (dépenses de R-D, chercheurs, brevets, articles scientifiques, exportations de haute technologie, PIB, éducation, énergie, eau…) ou saisissez n'importe quel code de la Banque mondiale, puis les pays à comparer et la période. L'onglet affiche l'évolution par pays avec la valeur mondiale en pointillés, une carte et un classement mondial sur la dernière valeur disponible de chaque pays, et la définition officielle de l'indicateur. Les données se téléchargent en CSV.

## Importer et fusionner

Déposez un ou plusieurs exports ; le site reconnaît la base de chaque fichier. Les doublons sont repérés par DOI, puis par titre, année et premier auteur, puis par titre et année quand une notice n'a pas de DOI. Les titres seulement proches sont listés pour vérification, jamais fusionnés d'office. Le corpus fusionné se télécharge en CSV. **Vos fichiers ne quittent pas votre navigateur.**

- **Web of Science** : Export → « Tab delimited file », contenu « Full Record ».
- **Scopus** : tout sélectionner, Exporter → CSV avec les informations de citation, bibliographiques, résumé et mots-clés.
- **Publish or Perish** : enregistrer les résultats en CSV (Google Scholar, Crossref, OpenAlex…).

**Scopus et Web of Science par API** : avec sa propre clé (champ dans « Sources & clés API »), chacun peut interroger Scopus ou Web of Science Starter depuis l'onglet Importer et fusionner ; les résultats sont fusionnés avec les fichiers importés. Les clés restent dans le navigateur ; Web of Science transite par le proxy du site, sans enregistrement. Rien n'est stocké ni republié par le site, et chacun reste responsable de l'usage de sa clé selon la licence de son établissement.

## Lire les réseaux

Les réseaux reprennent les principes de VOSviewer. Chaque **nœud** est un mot-clé, un pays, un auteur, une institution, un code ou un déposant ; sa taille dépend du nombre de documents. Un **lien** relie deux éléments qui apparaissent dans les mêmes documents ; son épaisseur dépend du nombre de documents communs. Les **couleurs** montrent soit des groupes d'éléments fortement liés (méthode de Louvain), soit l'**année moyenne** des documents, pour repérer les thèmes émergents.

## Définitions des indicateurs

- **Indice h** : h publications citées au moins h fois chacune.
- **Indice g** : les g publications les plus citées totalisent au moins g² citations.
- **Quotient m** : indice h divisé par le nombre d'années depuis la première publication (ici : depuis le début de la période choisie).
- **Citations par publication** : nombre moyen de citations reçues par publication. En Recherche en direct, quand le corpus dépasse 200 publications, la moyenne est estimée sur 1 000 publications tirées au hasard (signe ≈).
- **Où les voir** : l'indice h et les citations par publication figurent dans les chiffres clés ; l'indice g et le quotient m sont calculés dans l'onglet Importer et fusionner (panneau « Indicateurs de citation »).
- **Comptage entier** : une publication compte pour chacun des pays de ses auteurs ; la somme des pays dépasse donc le total.
- **Part mondiale** : publications du pays divisées par les publications mondiales dont le pays est connu.
- **Accès ouvert** : or (revue ouverte), hybride (article ouvert dans une revue payante), vert (archive ouverte), bronze (lecture gratuite sans licence), diamant (sans frais de lecture ni de publication).
- **Famille de brevets** : ensemble des publications d'une même invention dans différents offices.

## Sources et limites

- **OpenAlex** (licence CC0) : couverture large, mais affiliations et pays parfois manquants ; une clé gratuite augmente le volume de requêtes.
- **Brevets** : OEB Open Patent Services (gratuit après validation du compte) et Lens.org, selon leurs conditions d'utilisation. Seuls des comptages agrégés sont affichés.
- **Scopus et Web of Science** : par vos exports (analysés localement) ou par API avec votre propre clé, dans l'onglet Importer et fusionner. **Crossref** (libre) y est aussi interrogeable.
