# Trafic_routier
---
# Outils d'analyse des données trafic routier (données type SIREDO)

## Calcul des 4 NSC sur un diagramme fondamental callé sur des données SIREDO : 
Le principe de définition des seuils des 4 Niveaux de Service de Circulation (NSC) sur un diagramme fondamental dans le plan débit/vitesse \((Q, V)\)
Ces seuils permettent de découper la courbe en quatre zones distinctes de fonctionnement macroscopique du trafic.

1. Les Ratios Débit / Capacité (Q/C) retenus:
Pour segmenter la branche fluide (la partie supérieure de la courbe du diagramme fondamental), l'ingénierie du trafic s'appuie sur deux seuils de débit conventionnels liés à la capacité \(C\)(le débit maximal de la voie) :
- 75 % de la capacité (\(0,75 \times C\) : Le seuil conventionnel de confort des concepteurs.
- 90 % de la capacité (\(0,90 \times C\) : Le seuil critique proche de l'instabilité.

2. Le mécanisme de projection sur le plan (Q, V):
Puisque le seul débit est ambigu (un même débit peut être observé en régime fluide ou congestionné), c'est la vitesse qui l'accompagne qui sert de critère de discrimination final :
- On identifie sur l'axe des abscisses (Débit \(Q\)) les points correspondant à \(0,75 * C\)\ et \(0,90 * C\) , ainsi que la capacité maximale \(C\).
- On projette verticalement ces valeurs sur la branche supérieure (fluide) de la courbe calibrée \(V = f(Q)\) du diagramme fondamental.
- On en déduit trois vitesses seuils clés : \(V~1~\) , \(V~2~\) et \(V~3~\) qui délimitent verticalement les 4 NSC.

. Les 4 Niveaux de Service (NSC) résultants :
| Niveau de Service | Zone sur le diagramme (Plan Débit/Vitesse) | Caractéristiques de l'écoulement |
| :--: | :--: | :--: |
| NSC 1 : Fluide |	Débit allant de \(0\) à \(0,75 * C\). Vitesse supérieure a \(V~1~\) ( proche de la Vitesse Libre) | Les conducteurs roulent à la  vitesse souhitée. Les interactions entre les véhicules sont minimes et la liberté de manoeuvre est totale. |
| NSC 2 : Dense |	Débit allant de \(0,75 * C\) à \(0,90 * C\). Vitesse comprise entre \(V~1~\) et \(V~2~\) | La liberté de manoeuvre diminue. La formation de pelotons d'automobilistes commence a restreindre le confort de la conduite |
| NSC 3 : Instable |	Débit supérieur à \(0,90 * C\) jusqu'à la capacité \(C\). Vitesse chutant entre \(V~2~\) et \(V~3~\) (Vitesse Critique) | Le Trafic est à saturation. La moindre perturbation(coup de frein, changement de file) peut rompre l'équilibre et déclencher une onde de choc |
| NSC 4 : Congestionné |	Branche inférieure (basse) de la courbe. Vitesse inférieure à \(V~3~\) (Vitesse Critique), le débit s'effondre vers 0. | Le régime est dit "forcé" ou "congestif". Les véhicules subissent des cycles d'arrêt et de redémarrage (accordéon), la densité est maximale. |
