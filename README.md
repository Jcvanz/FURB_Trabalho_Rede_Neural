# Rede Neural Perceptron — Jogador ou Piloto?

<br>

> Trabalho Prático 02 — Processamento de Imagem  
> **FURB — Universidade Regional de Blumenau**

---

## Sobre o trabalho

O objetivo foi implementar uma rede neural do tipo **Perceptron** para resolver um problema de classificação binária: dado um conjunto de características de um atleta, o modelo deve dizer se ele é um **jogador de futebol** ou um **piloto de Fórmula 1**.

O problema foi apresentado em aula com quatro atletas conhecidos, usando três atributos binários como entrada.

---

## Dados de treinamento

| Atleta     | Ciência | Física | Filosofia | Classe        |
|------------|:-------:|:------:|:---------:|---------------|
| Neymar     |    1    |   0    |     0     | 0 — Jogador   |
| Messi      |    1    |   0    |     1     | 0 — Jogador   |
| Barichello |    1    |   1    |     0     | 1 — Piloto    |
| Massa      |    1    |   1    |     1     | 1 — Piloto    |

O atributo **Física** é o que divide as duas classes — pilotos precisam de conhecimento em física do carro, jogadores não.

---

## Como o Perceptron funciona

```
Entrada → Soma ponderada (w·x + b) → Função degrau → Saída (0 ou 1)
```

A cada erro, os pesos são ajustados pela regra de aprendizado:

```
w = w + η · (y - ŷ) · x
```

Onde `η` é a taxa de aprendizado e `(y - ŷ)` é o erro cometido. O processo se repete até o modelo classificar todos os exemplos corretamente.

---

## Estrutura do projeto

```
📁 trabalho_rede_neural/
├── perceptron_jogador_piloto.ipynb   # notebook principal com a implementação
└── README.md
```

---

## Como executar

1. Abra o arquivo `perceptron_jogador_piloto.ipynb` no Jupyter Notebook ou VS Code
2. Execute as células em ordem
3. O resultado final mostra a classificação de cada atleta e a acurácia do modelo

**Dependências:** `numpy`, `matplotlib` — ambas já vêm com o Anaconda/Jupyter padrão.

---

## Resultado

O perceptron acertou **100%** dos casos após poucas épocas de treinamento, confirmando que o problema é linearmente separável com os atributos fornecidos.

---

<br>

<p align="center">
  FURB — Universidade Regional de Blumenau &nbsp;|&nbsp; Processamento de Imagem
</p>
