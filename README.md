# Introduction:

Notre projet vise à résoudre un problème complexe lié à la détection de texte sur des images manuscrites historiques, en particulier sur des images de basse résolution. Ces documents historiques, précieux pour leur contenu, sont souvent mal préservés et présentent des défis uniques pour la détection de texte. Pour surmonter ces obstacles, nous avons mis en place une approche innovante qui combine la super résolution d'images et l'apprentissage profond pour améliorer la qualité des images, facilitant ainsi la détection de texte.

# Objectif du Projet:

L'objectif principal de cette phase du projet est d'exploiter des modèles de super résolution, notamment HAT (Highly Adaptive Transformer) et ESRGAN (Enhanced Super-Resolution Generative Adversarial Networks), pour augmenter la résolution d'images manuscrites historiques de basse qualité. La super résolution permettra d'améliorer la qualité des images, ce qui à son tour rendra la détection de texte plus fiable.

# Méthodologie:

## Préparation des Données:
La première étape cruciale de notre projet consiste à préparer les données.Nous avons tout d'abord créé deux ensembles d'images : les "images de référence" originales et les "images downscalées" réduites de 4 fois. Ces dernières nous permettront de calculer des mesures de performance (PSNR entre l'image de référence et l'output du moèdle) afind'évaluer l'efficacité de nos modèles de super résolution. Nous avons également introduit des techniques de data augmentation en ajoutant du bruit aux images et en effectuant des découpes pour diversifier notre ensemble de données.

## Sélection des Modèles Pré-Entraînés:
Nous avons choisi d'explorer l'utilisation de modèles de super résolution déjà pré-entraînés sur des ensembles de données tels qu'ImageNet. Ces modèles, tels que HAT et ESRGAN, ont déjà montré leur efficacité dans l'amélioration de la résolution des images. Cependant, leur application à des images manuscrites historiques est un défi distinct en raison de la nature unique de ces images.

## Fine-Tuning des Modèles:
Pour adapter les modèles à notre problème spécifique, nous avons entrepris une étape de fine-tuning. Nous avons utilisé nos propres images d'apprentissage de haute qualité pour entraîner ces modèles pré-entraînés. Le fine-tuning est essentiel pour les adapter aux caractéristiques particulières des images historiques, ce qui devrait améliorer significativement leurs performances.

## Évaluation des Performances:
Nous évaluerons les performances des modèles de super résolution après le fine-tuning en utilisant des mesures telles que la PSNR (Peak Signal-to-Noise Ratio) et la SSIM (Structural Similarity Index). Ces métriques nous aideront à quantifier l'amélioration de la qualité des images obtenue grâce à la super résolution.

# Exemple d'images manuscrites:

![image_example](https://github.com/AmineM89/Super-resolution_of_historical_documents/assets/93427646/f61cff6b-5ba5-41ff-9a51-ac9ddf423e6c)

# Résultats:
## Exemple de reconstruction d'images:
Image de référence:

<img width="439" alt="reference_image" src="https://github.com/AmineM89/Super-resolution_of_historical_documents/assets/93427646/4b6e5b98-ed70-472a-b0d3-7bc6d3fafb45">

Image downscalé:

<img width="361" alt="downscale_image" src="https://github.com/AmineM89/Super-resolution_of_historical_documents/assets/93427646/91420d24-aee3-4721-a44c-cad441be678a">

Image reconstruite:

<img width="445" alt="reconstructed_image" src="https://github.com/AmineM89/Super-resolution_of_historical_documents/assets/93427646/44be778e-42d0-4c8e-8b7d-f1503053062e">

## Performance des modèles:
Le modèle HAT: Hybrid Attention Transformer for Image Restoration semble le mieux adapté pour la super-résolution d'images manuscrites. Le modèle HAT est de loin le meilleur modèle avec un PSNR=32.2 et un SSIM=0.9. Les résultats des expérientation se trouve dans la figure ci-dessous

<img width="639" alt="results" src="https://github.com/AmineM89/Super-resolution_of_historical_documents/assets/93427646/2e3cf4e6-6f6d-47f1-afd3-f635cffdaec9">
