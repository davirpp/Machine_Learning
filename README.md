# Algoritmos

## 1. __Perceptron Learning Algorithm (PLA)__: 
Algoritmo de aprendizado supervisionado, que é considerado uma rede neural de camada única. O Perceptron é um classificador binário que utiliza retas. 
Ou seja, ele é útil em contexto de classificação binária em que os dados podem ser separados linearmente, isto é, como na imagem abaixo: ![Imgur](https://imgur.com/WZeMWnV.png)

  * Exemplo do algoritmo:
    * Dataset classificado e com a reta solução
  
      ![Imgur](https://imgur.com/XeNq8R8.png)
      
    * Dataset com dados de treinamento de tamanho 10 em um dataset com 1000 pontos originalmente
  
      ![Imgur](https://imgur.com/gQr3IT1.png)
      
      Em rosa tracejado temos uma reta solução para esse caso, mas como podemos observar, ela é muito distante da reta solução(verde).
      
No notebook - que pode ser acessado [clicando aqui](https://github.com/davirpp/Machine_Learning/blob/master/Perception_Learning_Algorithm.ipynb) - tem exemplos com tamanhos de dados de treinamento distintos, a acurácia calculada e uma conclusão sobre o modelo.


## 2. __K-Nearest Neighbors (KNN)__:
Algoritmo de aprendizado supervisionado simples que é utilizado como classificador. O funcionamento básico do algoritmo é simples: dado um ponto novo, calcule a distância desse ponto para todos os outros pontos ja rotulados. Com isso, você pega os _k_ mais próximos - por isso geralmente o k é um número ímpar, para ter um vencedor - e considera a classificação do ponto novo o rótulo que mais apareceu nos k mais próximos. Como na imagem abaixo: 

![Imgur](https://imgur.com/mJvaDTf.png)

Nessa imagem, quando fazemos k=3, temos mais representantes da Classe B, logo com k=3, o ponto vermelho seria classificado como Classe B. Porém com k=6, temos mais representantes da Classe A, logo com k=6, o ponto vermelho seria classificado como Classe A. 
Um ponto importante a se destacar é que, apesar da imagem estar parecendo com um círculo representando o k, na realidade esse círculo é utilizado apenas para demonstrar os k pontos mais próximos e diferenciá-los dos demais.

Nesse notebook utilizei o clássico problema da classificação de dígitos escritos manualmente, logo, o algoritmo recebe um uma matriz com o tom de cinza de cada pixel. Nesse exemplo utilizei do próprio Scikit Learn em que as imagens são 8x8 pixels.
Exemplo dos dados: 

![Imgur](https://imgur.com/o8kcWNb.png)

No notebook - que pode ser acessado [clicando aqui](https://github.com/davirpp/Machine_Learning/blob/master/K_Nearest_Neighbors.ipynb) - é possível observar o passo a passo do algoritmo é observar sua acurácia, vale a pena ressaltar também que, dependendo do _k_ e _p_ escolhidos, a acurácia se altera, visto que os parâmetros do modelo estão sendo alterados.

## 3. __Regressão Linear__:
É um algoritmo que deve ser utilizado quando se deseja realizar previsões de uma variável dependente. Ela é feita ajustando os pontos do gráfico a uma reta, querendo minimizar os erros quadráticos, ou seja, minimizando o somatório das distâncias de cada ponto até a reta, como na figura abaixo:

![Imgur](https://imgur.com/Zjderf0.png)

Então após uma prova matemática, o resultado obtido que temos para calcular os pesos dessa função é tido por: 

$$ w = X^\dagger y  \text{    onde,  } X^\dagger = (X^TX)^{-1} X^T$$ 

No notebook - que pode ser acessado [clicando aqui](https://github.com/davirpp/Machine_Learning/blob/master/Linear_Regression.ipynb) - tem exemplo de uma previsão da renda mensal brasileira, super simples.
