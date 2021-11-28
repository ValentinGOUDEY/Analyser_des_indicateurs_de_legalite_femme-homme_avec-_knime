# Analyser_des_indicateurs_de_l-galite_femme-homme_avec-_knime
Analysez des indicateurs de l'égalité femme-homme avec Knime


Projet réalisé sur Knime visant à:
-Préparer des données pour l'analyse en respectant les normes internes à l'entreprise
-Collecter des données en respectant le RGPD
-Tranférer des données vers une zone de préparation Knime
-Exporter les données traités
-Produire des graphiques d'analyse avec Knime



EXPOLARTION DES DONNÉES

Nous disposons de 3 dataset:
-Info_pro qui contient id_salarié, ancienneté en années, la distance domicile/travail, le service dans lequel le salarié travail, la présence ou non d'accident de travail et le niveau de satisfaction du salarié sur une échelle de 1 à 10.

-Rémunération qui contient id_salarié, contrat contenant le type de contrat cdd ou cdi, la durée hebdomadaire de travail, le salaire mensuel de base, le % variable, la présence ou non d'une augmentation ou promotion.

-Salarié qui contient id_salarié, le sexe des salariés, le prénom et le nom, le numéro de téléphone, la date de néssance, l'état civil et le nombre d'enfants

Nous avons ici la présence d'une colonne en commun dans les 3 jeux de données. Nous avons aussi la présence de données manquantes et aussi de données personnel.

PRÉPARATION DE DONNÉES

Données manquante dans les colonnes augmentation et promotion pour tous les contrat de type CDD, nous pouvons donc remplacer ces données manquantes par 0 car il est peu probable d'augmentation ou promotion en contrat de type CDD.
Données manquante pour la colonne état civil que nous ne pouvons pas remplacer, j'ai par la suite suprimmé cette colonne qui ne constituerait pas un élément d'analyse dans le projet.

Pour les jointures j'ai effectué une jointure sur ID_salarié qui était en commun sur les 3 jeux de données.


RGPD

Afin de respecter les 5 grand principes de la RGPD j'ai procédé à une supression de quelques colonnes, à savoir Prénom/nom, Numéro de téléphone, date de Naissance afin d'anonymizer le jeu de données. J'ai aussi par la même occasion supprimé la colonne "état civil" qui contennait des données manquantes.

EXPORTATION DES DONNÉES

Exportation des données et vérification du csv via python

VISUALISATION

J'ai choisis de comparer les vue générales de l'entreprise avec les vue par service. Sur la partie gauche des visualisations vous pourrez y voir un Pie Plot avec une vue générale entre les hommes et les femmes selon un critère. Ensuite sur la droite vous y trouverez un Bar PLot avec cette même représention mais cette fois si par Service.

CONCLUSION

L'entreprise ne présente pas de d'inégalité entre les Hommes et les Femmes, cependant certaines inégalité sont visible entre les différents service.
Le salaire un peu plus élevé des hommes est expliqué par l'ancienneté elle aussi plus élevé chez les hommes.



Voici une courte explication de ce projet sur Knime, le pdf de la présentation est disponible et les explications de chaques slides étaient présentés à l'oral.

