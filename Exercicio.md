# Exercício

Construir o modelo de previsão e estime λ-médio para o mês de Junho. Calcule o erro médio de precisão.

| Mês | λ (no horário de pico) | λ-médio | \|erro\| |
|-|-|:-:|:-:|
| Janeiro | 3 requisições/mês | 3 | 0 |
| Fevereiro | 5 requisições/mês | 4.2 | 0.8 |
| Março | 4 requisições/mês | 5.4 | 1.4 |
| Abril | 7 requisições/mês | 6.6 | 0.4 |
| Maio | 8 requisições/mês | 7.8 | 0.2 |
| Junho | ? | 9 | Σ\|erro\| = 2.8 |

```
λ-médio = a + (b * t)
  Σt = 15 | Σt² = 55
  Σλ = 27 | Σtλ = 93

        ┐
a = 1.8	│ ┌──────────────────────┐           
        ├ │ λ-médio = 1.8 + 1.2t │
b = 1.2 │ └──────────────────────┘
        ┘

erro-médio = 2.8/5 = 0.56

junho: λ-médio = 9 ± 0.56
    pior caso: 9.56 requisições/mês
```