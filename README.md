# Algoritmo Genético para redução de atributos FTIR utlizando a classificação em redes complexas
A ideia do algoritmo é simples, basicamente teremos um algorimo genético para encontrar os atributos mais relevantes buscando melhorar o resultado da média entre sensibilidade e especificidade.
### Individuo 🧬
Primeiramente vamos estabelecer o que é um individuo para o problema proposto.
- Temos que uma instância ATR-FTIR representa uma banda de infravermelho que contém extamente 1868 atributos.
- Alguns atributos não são tão relevantes no processo de classificação, por isso diversos trabalhos relacionados realizam o processo de truncamento para remover regiões do espectro que sejam indesejadas.
- Logo, o objetivo é que o individuo seja um array de 1868 posições, com valores binários em que 1 é para 'atributo ativado' e 0 para 'atributo desativado'.

### Mutação 💉
A mutação é simples, consiste em escolher aleatóriamente uma posição do array do indivíduo e muda-lá, se for 1 troca para 0 e se for 0 troca para 1.

### Crossover 👪
O crossover é ponto unico, ou seja, escolhemos dois indivíduos que serão os pais e selecionamos uma posição aleatória para ocorrer a troca de "material genético", gerando assim dois filhos.

### Torneio 🎌
No torneio selecionamos k indivíduos que irão compor a disputa, vence o inivíduo com o melhor FIT (média ente sensibilidade e especificidade).

### Sistema de avaliação do indivíduo
O Sistema que irá avaliar o fit do inidivíduo é por meio da classificação de alto nível via comformidade padrão, que é um classificador baseado em medidas de redes complexas.

As medidas de redes complexas podem ser encontradas no seguinte repositório: [Complex_network_measure](https://github.com/Ricardo50-dev/Complex_network_measure)

A Heurística utilizada para gerar a rede é a rede kNN, que também pode ser encontrada no seguinte repositório: [Graph_generator](https://github.com/Ricardo50-dev/Graph_generator)
