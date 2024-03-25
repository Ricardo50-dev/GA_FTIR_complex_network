# Algoritmo Genético para redução de atributos FTIR utlizando a classificação em redes complexas
A ideia do algoritmo é simples, basicamente teremos um algorimo genético para encontrar os atributos mais relevantes buscando melhorar o resultado da média entre sensibilidade e especificidade.
### Individuo 🧬
Primeiramente vamos estabelecer o que é um individuo para o problema proposto.
- Temos que uma instância ATR-FTIR representa uma banda de infravermelho que contém extamente 1868 atributos.
- Alguns atributos não são tão relevantes no processo de classificação, por isso diversos trabalhos relacionados realizam o processo de truncamento para remover regiões do espectro que sejam indesejadas.
- Logo, o objetivo é que o individuo seja um array de 1868 posições, com valores binários em que 1 é para 'atributo ativado' e 0 para 'atributo desativado'.

### Mutação 💉

### Crossover 👪

### Torneio 🎌
