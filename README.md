# dcyou.github.io

Page d'accueil publique du portfolio d'applications **dcyou** — https://dcyou.co (à venir) / https://dcyou.github.io

HTML + CSS statiques, un seul fichier (`index.html`), zéro dépendance externe :
pas de framework, pas de CDN, pas de police distante. Thème clair et sombre via
`prefers-color-scheme`.

- `index.html` — la page
- `icons/` — icônes des apps, copiées depuis chaque dépôt (SVG autonomes)
- `favicon.svg` — marque dcyou

## Applications non sorties

**Aucune application non lancée n'apparaît sur cette page** : ni son nom, ni son
sujet, ni son concept, ni le nom de fichier de son icône. Une idée annoncée avant
sa sortie est une idée qu'on se fait prendre.

La page n'annonce pas non plus d'apps à venir : **il n'y a plus de section
« En préparation »**, pas même une carte teaser anonyme.

**Le nombre d'apps en préparation n'est jamais affiché**, volontairement :
il ne sert à rien au visiteur, et surtout il fuit par différence. Quelqu'un qui
suit la page verrait le compteur passer de 5 à 4 et saurait exactement quelle
sortie vient d'avoir lieu, et à quel rythme le portfolio avance.

Une app ne rejoint « À essayer maintenant » — avec son nom, sa description et son
icône dans `icons/` — que **le jour où elle est publiquement accessible**.

**Cette règle s'applique au commit, pas seulement à la page.** Sur un dépôt
public, un commit reste servi par `raw.githubusercontent.com` et par l'API même
après que son contenu a été retiré de la page, et les anciens SHA restent
énumérables via l'API `events`. Retirer un nom dans un commit suivant ne
l'efface donc pas : ça le laisse une URL plus loin. Un nom non sorti ne doit
jamais entrer dans un commit — c'est le seul moment où la décision est encore
réversible.

## Langues

La page est traduite dans les **30 langues de LettersCatch** (l'union de ce que
parle le portfolio : les apps simples sont FR/EN, LettersCatch couvre les 30).
Personne ne perd donc sa langue en passant de l'accueil à une app.

Tout tient dans `index.html` : le dictionnaire est l'objet `T` du script en bas
de page, et c'est **la source** — il s'édite à la main.

- La langue vient de `localStorage`, sinon du navigateur (`navigator.languages`),
  sinon l'anglais.
- Le **français est la version de référence** : c'est lui qui est écrit en dur
  dans le HTML, donc c'est lui qui s'affiche si JavaScript est coupé.
- `<html lang>` et `<html dir>` suivent la langue active. L'arabe passe en RTL ;
  la marque `dcyou.`, les noms d'apps et l'adresse e-mail restent isolés en LTR.
- Pas de balises `hreflang` : toutes les langues vivent sur **une seule URL**, il
  n'y a donc pas d'alternative à déclarer. Seuls `og:locale` et ses
  `og:locale:alternate` décrivent les langues disponibles.

Les noms d'applications ne se traduisent jamais.

Mentions légales par application : https://dcyou.github.io/legal/
Contact : support@dcyou.co
