<b>Introduction:</b>

Notre projet vise à résoudre un problème complexe lié à la détection de texte sur des images manuscrites historiques, en particulier sur des images de basse résolution. Ces documents historiques, précieux pour leur contenu, sont souvent mal préservés et présentent des défis uniques pour la détection de texte. Pour surmonter ces obstacles, nous avons mis en place une approche innovante qui combine la super résolution d'images et l'apprentissage profond pour améliorer la qualité des images, facilitant ainsi la détection de texte.

<b>Objectif du Projet:</b>

L'objectif principal de cette phase du projet est d'exploiter des modèles de super résolution, notamment HAT (Highly Adaptive Transformer) et ESRGAN (Enhanced Super-Resolution Generative Adversarial Networks), pour augmenter la résolution d'images manuscrites historiques de basse qualité. La super résolution permettra d'améliorer la qualité des images, ce qui à son tour rendra la détection de texte plus fiable.

<b>Méthodologie</b>

<b>Préparation des Données :</b> La première étape cruciale de notre projet consiste à préparer les données.Nous avons tout d'abord créé deux ensembles d'images : les "images de référence" originales et les "images downscalées" réduites de 4 fois. Ces dernières nous permettront de calculer des mesures de performance (PSNR entre l'image de référence et l'output du moèdle) afind'évaluer l'efficacité de nos modèles de super résolution. Nous avons également introduit des techniques de data augmentation en ajoutant du bruit aux images et en effectuant des découpes pour diversifier notre ensemble de données.

<b>Sélection des Modèles Pré-Entraînés :</b> Nous avons choisi d'explorer l'utilisation de modèles de super résolution déjà pré-entraînés sur des ensembles de données tels qu'ImageNet. Ces modèles, tels que HAT et ESRGAN, ont déjà montré leur efficacité dans l'amélioration de la résolution des images. Cependant, leur application à des images manuscrites historiques est un défi distinct en raison de la nature unique de ces images.

<b>Fine-Tuning des Modèles :</b> Pour adapter les modèles à notre problème spécifique, nous avons entrepris une étape de fine-tuning. Nous avons utilisé nos propres images d'apprentissage de haute qualité pour entraîner ces modèles pré-entraînés. Le fine-tuning est essentiel pour les adapter aux caractéristiques particulières des images historiques, ce qui devrait améliorer significativement leurs performances.

<b>Évaluation des Performances :</b> Nous évaluerons les performances des modèles de super résolution après le fine-tuning en utilisant des mesures telles que la PSNR (Peak Signal-to-Noise Ratio) et la SSIM (Structural Similarity Index). Ces métriques nous aideront à quantifier l'amélioration de la qualité des images obtenue grâce à la super résolution.
