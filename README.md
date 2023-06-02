# VIT-Vision_Transformer
O presente trabalho tem por finalidade o experimento didático de realizar o "fine-tuning" de um modelo ViT (Vision Transformer) para classificação de imagens, tarefa típica do segmento de visão computacional. 

Descrito no artigo de autoria de  Alexey Dosovitskiy, Lucas Beyer, Alexander Kolesnikov e outros (2021), publicação que pode ser localizada no endereço https://arxiv.org/pdf/2010.11929.pdf, os autores propõem uma abordagem para o reconhecimento de imagens usando Transformers, arquitetura que tem alcançado ótimos resultados em tarefas do processamento de linguagem natural.

O conceito central do artigo é substituir a abordagem tradicional de processamento de imagens, que trata as imagens como uma grade de pixels, por uma representação textual. Eles dividem a imagem em patches de 16x16 pixels e codificam cada patch em um vetor de palavras (Embedded Patches). Esses vetores de palavras são então adicionados a vetores posicionais (Posicional embeddings) e alimentados em um modelo Transformer para análise.

Em síntese, o ViT substitui a entrada de texto por patches da imagem, aplicando as mesmas operações de atenção (self-attention layers) e transformação linear, presentes na estrutura tradicional do "Codificador" (Encoder) de um Transformer, de forma a capturar as informações importantes para a construção de uma representação latente, a qual poderá ser aplicada, em última análise, a tarefas específicas da visão computacional, como classificação de imagem ou detecção de objetos.

O ViT (Vision Transformer) é treinado em um grande número de imagens e mostra resultados promissores em diferentes conjuntos de dados de referência, em termos de precisão e escalabilidade, em comparação com modelos tradicionais de convolução.





![](/img/VIT-Vision-Transformer.jpeg)
figura 1: visão geral do modelo ViT - Vision Transformer, descrito no artigo de autoria de Vaswani e outros (2017).

### Fonte de Dados: Dataset "cats_vs_dogs" hospedado na "Hugging Face"
Como fonte de dados para o "fine-tuning", utilizou-se um subconjunto formado por imagens de gatos e cães do "dataset" conhecido como "Asirra" (Animal Species Image Recognition for Restricting Access). Desse "dataset" hospedado na plataforma "Hugging Face" 🤗 (https://huggingface.co/datasets/cats_vs_dogs), utilizou-se 8.427 (oito mil, quatrocentas e vinte e sete) imagens neste trabalho, o que corresponde a cerca de 50% do conteúdo armazenado.

Sobre o "dataset" Asirra hospedado na plataforma "Kaggle"(https://www.kaggle.com/c/dogs-vs-cats), origem do subconjunto presente na "Hugging Face"🤗, segue, abaixo, trecho da descrição extraída do próprio "Kaggle" e mantida na língua original em inglês:

The Asirra data set

Web services are often protected with a challenge that's supposed to be easy for people to solve, but difficult for computers. Such a challenge is often called a CAPTCHA (Completely Automated Public Turing test to tell Computers and Humans Apart) or HIP (Human Interactive Proof). HIPs are used for many purposes, such as to reduce email and blog spam and prevent brute-force attacks on web site passwords.

Asirra (Animal Species Image Recognition for Restricting Access) is a HIP that works by asking users to identify photographs of cats and dogs. This task is difficult for computers, but studies have shown that people can accomplish it quickly and accurately. Many even think it's fun! Here is an example of the Asirra interface:

Asirra is unique because of its partnership with Petfinder.com, the world's largest site devoted to finding homes for homeless pets. They've provided Microsoft Research with over three million images of cats and dogs, manually classified by people at thousands of animal shelters across the United States. Kaggle is fortunate to offer a subset of this data for fun and research. 

# Experimento de "Fine-Tune"
![](/img/modelo-fine-tunning-acuracia.png)

![](/img/modelo-fine-tunning-matriz-confusao.png)

# Comparando com modelo Vit disponibilizado na "huggin Face" 
![](/img/modelo-Kaggle-acuracia.png)

![](/img/modelo-Kaggle-matriz-confusao.png)
