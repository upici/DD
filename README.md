<div id="table-of-contents">
<h2>Table of Contents</h2>
<div id="text-table-of-contents">
<ul>
<li><a href="#orgheadline6">1. Un problème de décomposition de domaine</a>
<ul>
<li><a href="#orgheadline1">1.1. Objectif final, très ambitieux.</a></li>
<li><a href="#orgheadline2">1.2. Première partie : recherche de resources, documentation</a></li>
<li><a href="#orgheadline3">1.3. Deuxième partie : programmation dans un cas simplifié</a></li>
<li><a href="#orgheadline4">1.4. Troisième partie : le cas général</a></li>
<li><a href="#orgheadline5">1.5. refs</a></li>
</ul>
</li>
</ul>
</div>
</div>

# Un problème de décomposition de domaine<a id="orgheadline6"></a>

## Objectif final, très ambitieux.<a id="orgheadline1"></a>

On cherche à résoudre une équation du type \( - \Delta u + \alpha u = f\) dans
l'ouvert \(\Omega = (0,1)^d\) avec \(u = 0\) au bord, en utilisant des méthodes de
décomposition de domaine.

On cherchera en particulier à savoir à quelle vitesse les algorithmes
convergent, lorsqu'ils convergent.

## Première partie : recherche de resources, documentation<a id="orgheadline2"></a>

1.  Trouver et synthétiser de la documentation sur le type d'équation dont il
    s'agit: une équation elliptique linéaire, à coefficients constant, avec
    conditions aux limites de Dirichlet.
2.  Trouver de la documentation sur les méthodes de différences finies pour cette
    équation.
3.  Décrire le système linéaire qui en découle. Quelles sont les méthodes
    numériques adaptées à la résolution de ce système linéaire ?
4.  Trouver et décrire les méthodes de décomposition de domaine de type méthode
    de Schwarz avec recouvrement pour ce problème.

## Deuxième partie : programmation dans un cas simplifié<a id="orgheadline3"></a>

On se place pour cette partie dans le cas de l'équation en dimension \(d=1\),
c'est à dire sur l'intervalle \(\Omega = (0,1)\).

1.  Détailler l'architecture du code à implémenter pour résoudre le problème sans
    décomposition de domaine, en essaynt d'avoir un code modulaire et extensible
    facilement (aux dimensions \(d=2\) et \(d=3\), au cas de la décomposition de
    domaine). Entrées et sorties ? Structuration du code en fichiers ? Quels
    outils de l'ensemble scipy/numpy ?
2.  Déterminer des problèmes modèles, dont les solutions sont connues et
    s'expriment de manière analytique. Ces solutions serviront à tester
    l'implémentation.
3.  Programmer la résolution du problème, et vérifier cette implémentation à
    l'aide des tests de la question 2.

## Troisième partie : le cas général<a id="orgheadline4"></a>

On va généraliser le code produit dans la partie précédente dans deux direction:
dimension spatiale \(2\), et décomposition de domaine.

1.  Déterminer comment le code produit précédemment peut se généraliser à la
    dimension 2. Qu'est-ce qui change ? Quels sont les fichiers à modifier ?
    Recalculer des solutions analytiques permettant de faire des tests de
    vérification.
2.  Produire le code de résolution du problème en 2D, et le vérifier à l'aide des
    tests calculés en 1.
3.  Pour la décomposition de domaine, d'abord en dimension \(d=1\), Bien refléchir,
    déterminer et expliquer tout ce qui doit changer dans la stratégie et
    l'algorithme de résolution, puis dans l'ensemble du code (les
    entrées/sorties, etc).
4.  Quels cas tests pourrait-on utiliser pour vérifier l'implémentation ?
5.  Implémenter cette résolution, d'abord sur un problème en dimension \(d=2\),
    puis \(d=2\).

## refs<a id="orgheadline5"></a>

Voir le répertoire [./refs](./refs)
