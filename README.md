# Projeto de Redução de Dimensionalidade em Imagens
### Binarização de Imagem com Python

Este projeto demonstra a redução de dimensionalidade de uma imagem colorida para preto e branco, utilizando um algoritmo de binarização simples. O objetivo é transformar uma imagem de 3 canais de cor (RGB) em uma imagem de 1 canal de dados binários, onde cada pixel é representado por apenas dois valores: 0 (preto) e 255 (branco).

A implementação é feita do zero, sem o uso de bibliotecas de processamento de imagem de alto nível como OpenCV ou Pillow para a manipulação dos pixels. Utilizamos apenas o **NumPy** para operações matemáticas e o **Matplotlib** para visualização dos resultados.

---

## 1. Algoritmo de Binarização

O processo de transformação da imagem é realizado em duas etapas principais:

1.  **Conversão para Escala de Cinza:** A imagem RGB (composta por 3 canais: Vermelho, Verde e Azul) é convertida para uma única camada de tons de cinza. Para isso, é utilizada a fórmula de luminosidade percebida:
    
    $L = 0.299 \times R + 0.587 \times G + 0.114 \times B$
    
    Esta fórmula pondera a contribuição de cada canal de cor para a percepção humana de luminosidade.

2.  **Binarização:** A imagem em tons de cinza é então convertida para preto e branco. Um **limiar** (threshold) é definido, e cada pixel é avaliado:
    * Se o valor do pixel for menor que o limiar, ele se torna **0 (preto)**.
    * Se o valor do pixel for maior ou igual ao limiar, ele se torna **255 (branco)**.

---

## 2. Implementação em Python

A implementação utiliza apenas as bibliotecas **Numpy** para manipulação dos dados da imagem e **Matplotlib** para exibição.

### Requisitos
*A biblioteca `Pillow` é usada apenas para carregar a imagem, mas a manipulação dos pixels é feita manualmente.*

### Estrutura do Código

O notebook está dividido nas seguintes etapas:
1.  **Configuração e Carregamento:** Importa as bibliotecas necessárias e permite o upload de uma imagem.
2.  **Conversão para Escala de Cinza:** Implementa a fórmula de luminosidade para converter a imagem RGB.
3.  **Binarização:** Aplica o limiar para criar a imagem binária (preto e branco).
4.  **Visualização:** Exibe a imagem original, a imagem em escala de cinza e a imagem binarizada lado a lado para comparação.

---

## 3. Resultados
## 3. Resultados

Ao executar o notebook, você poderá visualizar o passo a passo do algoritmo com as três imagens resultantes:

| Imagem Original (RGB) | Imagem em Escala de Cinza | Imagem Binarizada |
| :---: | :---: | :---: |
 ![Imagem Original](<img width="276" height="427" alt="download (1)" src="https://github.com/user-attachments/assets/d20c58ad-7490-4cc9-a009-ee1e12e7509a" />
)  ![Imagem em Escala de Cinza](<img width="276" height="427" alt="download (2)" src="https://github.com/user-attachments/assets/e442c51b-c45a-45fa-b041-deaa78e3d7f5" />
) ![Imagem Binarizada](<img width="307" height="427" alt="download (3)" src="https://github.com/user-attachments/assets/ba8f9efc-84ca-4d10-9384-829eda2169e6" />
)
 


---



## 4. Como Usar

1.  Abra o notebook no Google Colab.
2.  Execute cada célula de código em sequência (Shift + Enter).
3.  Quando solicitado, faça o upload de uma imagem do seu computador.
4.  Visualize as imagens processadas e compare os resultados.

Este projeto é ideal para quem deseja entender a **representação de imagens como dados** e os fundamentos do **processamento de imagem** em baixo nível.

