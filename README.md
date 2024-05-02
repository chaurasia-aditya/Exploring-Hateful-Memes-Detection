# Hateful Memes

Hateful memes can significantly impact the mental health of internet users. Therefore, it is imperative to filter and promptly remove such content from platforms, while also imposing restrictions on their posting and sharing. Deep learning holds promise in detecting hateful content effectively. Stateof-the-art algorithms, utilizing Vision Language models, have demonstrated promising results (80.8 % Accuracy, 89.2 AUROC), comparable to human performance (84.7 % Accuracy, 82.7 AUROC). 

We aim to replicate these outcomes using both unimodally and multimodally trained algorithms. Leveraging the hateful memes challenge dataset, containing images and text for each meme, we classify them based on their hatefulness. Our experimentation involves RoBERTa with ResNet, VGG, and GoogleNet, as well as a BERT model pretrained on hate speech with ResNet, and the MMBT model with CLIP encoder algorithms. In this paper, we conduct a comparative analysis of these algorithms. Our best results are achieved with the MMBT algorithm, attaining a test accuracy of 73.30%.

## Results

| Method                  | Validation accuracy | Validation AUROC | Test accuracy | Test AUROC |
|-------------------------|---------------------|------------------|---------------|------------|
| ConcatBERT (baseline)   | 59.04%              | 53.48            | 60.80%        | 54.06      |
| LateFusion (baseline)   | 58.94%              | 53.97            | 58.94%        | 55.04      |
| ConcatXLM-R             | 57.60%              | 51.69            | 59.30%        | 51.77      |
| LateFusion-RoBERTa      | 57.11%              | 50.24            | 56.63%        | 50.01      |
| RoBERTa+VGG             | 60.00%              | 55.01            | 60.83%        | 54.74      |
| RoBERTa+GoogleNet       | 58.85%              | 53.83            | 58.67%        | 50.00      |
| ConcatBERT-hatexplain   | 61.15%              | 57.32            | 63.80%        | 59.31      |
| MMBT-one-embed          | 67.50%              | 72.89            | 67.90/70.85%  | 77.51/75.01|
| MMBT-four-embed         | 69.90%              | 74.13            | 69.70/73.30%  | 80.09/77.51|
