# 🐱🐶 Classificação de Imagens: Gatos vs Cachorros com TensorFlow

Este projeto utiliza **Transfer Learning com MobileNetV2** para realizar a **classificação binária** entre imagens de gatos e cachorros usando o dataset `cats_vs_dogs` do TensorFlow Datasets.

## 📌 Funcionalidades

- Carregamento e pré-processamento automático do dataset `cats_vs_dogs`
- Construção de uma CNN baseada em MobileNetV2 (pré-treinada)
- Treinamento inicial + fine-tuning da rede
- Avaliação em conjunto de teste
- Predição em imagens externas
- Visualização gráfica do desempenho do modelo

## 🛠️ Tecnologias Utilizadas

- Python 3 (Google Colab)
- TensorFlow e TensorFlow Datasets
- Matplotlib e NumPy

## 🧱 Arquitetura do Modelo

- **Base:** `MobileNetV2` com pesos `ImageNet` (camadas congeladas inicialmente)
- **Camada GlobalAveragePooling2D**
- **Camada Densa final com 1 unidade (saída binária)**
- **Função de perda:** `BinaryCrossentropy(from_logits=True)`
- **Otimizador:** `RMSprop`

## 🚀 Como Executar

1. Acesse o notebook no [Google Colab](https://colab.research.google.com/drive/1UxwHMFsYvOXvADaEGNcFBca5Q31ZFRUH)
2. Certifique-se de que está com o ambiente pronto:
   ```python
   !pip install tensorflow tensorflow_datasets matplotlib numpy
3. Execute todas as células sequencialmente.

4. Para testar com uma imagem local, utilize a função de predição:
   predict_image('/content/sua_imagem.png')
   
Saída esperada:
    "Esta imagem parece ser de um cachorro com 97.32% de confiança."


