# 📰 Résumeur extractif d'articles de presse
Mini-project · AKDIM Hiba · Master SDIA, ENSA El Jadida

Un outil qui résume un article en sélectionnant ses phrases les plus pertinentes. Il est entraîné sur le dataset [CNN / Daily Mail](https://www.kaggle.com/datasets/gowrishankarp/newspaper-text-summarization-cnn-dailymail) et comparé à la baseline des premières phrases.

## Méthode

1. **Données** : 10 000 paires (article, résumé).
2. **Prétraitement** : nettoyage, découpage en phrases, étiquetage « pertinente / non pertinente ».
3. **Représentation** : embeddings Sentence-BERT.
4. **Modèle** : classifieur binaire (gradient boosting).
5. **Sélection** : probabilité du modèle + similarité avec l'article, sans redondance, dans l'ordre original.
6. **Évaluation** : précision, rappel et ROUGE, comparés à la baseline.

## Utilisation

Ouvrir `akdim-nlp.ipynb` dans Google Colab (GPU conseillé) et exécuter les cellules dans l'ordre. Le notebook lance une interface Gradio pour tester le résumeur.

## Technologies

Python · Sentence-Transformers · scikit-learn · NLTK · rouge-score · Gradio
