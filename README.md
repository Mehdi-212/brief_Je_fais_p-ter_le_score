# Projet pour le brief sur l'audio

Projet qui contient le code nécessaire au développement du brief audio

# Contexte

Après une première version de votre projet en reconnaissance sonore, vous devez améliorer vos performances de reconnaissance entre voitures et camions en jouant uniquement avec les modèles.

# Mon Approche

Pour ce projet d'amelioration je suis partie sur une amelioration manuelle des parametres.
Vous vous demandez pourquoi je n'ai pas utilisé un gridSearch ou un randomsearch pour trouvé les paramétres optimaux, j'ai preferer tester les parametres un a un car je voulais comprendre comment marche le modele et a quoi servent ses parametres.
J'ai donc testez chaque parametres avec des valeurs differentes pour trouvez les plus optimaux.


# SVM
J'ai essayé le modele SVM.
Pour ameliorer le modele j'ai modifier le Parametre C en essayant plusieurs chiffre
(model = svm.SVC(C=100, kernel='rbf', class_weight=None, probability=False)
).
Ensuite j'ai modifier le kernel est ce qui correspond le mieux est le kernel rbf plutot que le lineaire.

la meilleur accuracy obtenu est : 0.91.

![](iMG/SVM.PNG)


# Xgboost
J'ai essayé le modele Xgboost.
Pour ameliorer le modele j'ai modifier les Parametres(n_estimators=10, max_depth=10).

la meilleur accuracy obtenu est : 0.89.

![](iMG/xgboost.PNG)




# RandomForest
J'ai essayé le modele RandomForest.
Pour ameliorer le modele j'ai modifier les Parametres(n_estimators=100, max_depth=None, min_samples_split=2, random_state=42).

la meilleur accuracy obtenu est : 0.89.

![](iMG/Randomforest.PNG)



# MLPClassifier
J'ai essayé le modele MLPClassifier.
Pour ameliorer le modele j'ai modifier les Parametres (hidden_layer_sizes=(500, 500), max_iter=500, activation= 'tanh', solver= 'adam').

la meilleur accuracy obtenu est : 0.89.

![](iMG/MLP.PNG)


# CatBoostClassifier
J'ai essayé le modele CatBoostClassifier.
le decoupage audio a 0.5.
Pour ameliorer le modele j'ai modifier les Parametres (iterations=275, depth=10).

la meilleur accuracy obtenu est : 0.90.

![](iMG/catboost.PNG)
