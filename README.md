# 💰 Decompositor de Notas e Moedas em Python

Programa em Python que recebe um valor em reais e calcula a menor quantidade de notas e moedas necessárias para representá-lo.

---

## 📋 Sobre o projeto

Dado um valor monetário (ex: `R$ 387,43`), o programa decompõe esse valor nas seguintes cédulas e moedas brasileiras:

| Tipo | Valor |
|------|-------|
| Nota | R$ 100,00 |
| Nota | R$ 50,00 |
| Nota | R$ 20,00 |
| Nota | R$ 10,00 |
| Nota | R$ 5,00 |
| Nota | R$ 2,00 |
| Moeda | R$ 1,00 |
| Moeda | R$ 0,50 |
| Moeda | R$ 0,25 |
| Moeda | R$ 0,10 |
| Moeda | R$ 0,05 |
| Moeda | R$ 0,01 |

---

## ▶️ Como executar

### Pré-requisitos

- Python 3 instalado

### Rodar

```bash
python main.py
```

### Exemplo de uso

```
Digite o valor: 387.43

3 nota(s) de R$ 100,00
1 nota(s) de R$ 50,00
1 nota(s) de R$ 20,00
1 nota(s) de R$ 10,00
1 nota(s) de R$ 5,00
1 nota(s) de R$ 2,00
0 moeda(s) de R$ 1,00
0 moeda(s) de R$ 0,50
1 moeda(s) de R$ 0,25
1 moeda(s) de R$ 0,10
1 moeda(s) de R$ 0,05
3 moeda(s) de R$ 0,01
```

---

## 🧠 Como funciona

O programa converte o valor digitado para **centavos** (multiplicando por 100), eliminando problemas com casas decimais. Em seguida, usa divisão inteira e resto (`%`) para calcular quantas notas/moedas de cada tipo cabem no valor restante, do maior para o menor.

```python
n = int(valor * 100 + 0.5)  # ex: 2.75 → 275 centavos

notas100 = n // 10000  # quantas notas de R$100 cabem?
n %= 10000             # guarda o resto para continuar
# ...e assim por diante
```

O `+ 0.5` é usado para evitar erros de arredondamento de ponto flutuante.

---


## 🛠️ Tecnologias


<img height="100" width="100" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/python/python-original.svg" />
          

