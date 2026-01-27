## Análise Simples de Alta, Baixa ou Estabilidade de Ações em Python

### 🎯 Desafio
Você acaba de ser contratado como analista júnior em uma corretora de valores que está desenvolvendo um sistema para ajudar investidores iniciantes a entenderem rapidamente se uma ação teve um bom desempenho no dia.  

Seu chefe, entusiasmado com a tecnologia, propõe um desafio: criar um programa simples que, ao receber o preço de abertura e o preço de fechamento de uma ação, informe se ela valorizou, desvalorizou ou permaneceu estável.  

Essa ferramenta será usada em treinamentos para novos investidores, ajudando-os a interpretar rapidamente os movimentos básicos do mercado financeiro.

---

### 📌 Requisitos
- Ler dois valores inteiros positivos: **preço de abertura** e **preço de fechamento** de uma ação.  
- Comparar os valores e imprimir:
  - `"ALTA"` → se o preço de fechamento for maior que o de abertura.  
  - `"BAIXA"` → se o preço de fechamento for menor que o de abertura.  
  - `"ESTAVEL"` → se os valores forem iguais.  
- Não utilizar bibliotecas externas.  
- Considerar apenas os dois valores fornecidos na entrada, separados por espaço.  

---

### 🖥️ Código em Python

```
entrada = input()
abertura_str, fechamento_str = entrada.split()

# Converte os valores para inteiros
abertura = int(abertura_str)
fechamento = int(fechamento_str)

# Compara os valores de abertura e fechamento e imprime o resultado correto
if abertura == fechamento:
    print("ESTAVEL")
elif fechamento > abertura:
    print("ALTA")
else:
    print("BAIXA")
