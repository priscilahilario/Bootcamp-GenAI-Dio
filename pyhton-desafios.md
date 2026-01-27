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
```
---


## 🏦 Desafio: Padronização de Nomes em Transferências Bancárias

### 📖 Contexto
Você acaba de ser contratado como estagiário no setor de tecnologia de um grande banco digital.  
Seu primeiro desafio é ajudar a equipe de atendimento a identificar rapidamente possíveis erros de digitação em transferências bancárias.  

Frequentemente, clientes digitam acidentalmente letras minúsculas em campos que deveriam conter apenas letras maiúsculas, como o nome do destinatário.  
Para evitar problemas, o gerente pediu que você desenvolva um programa que leia o nome digitado pelo cliente e retorne o mesmo nome, mas com todas as letras convertidas para maiúsculas.  

Assim, o sistema poderá padronizar os registros e evitar falhas em futuras operações automatizadas.  
Sua solução precisa ser simples, eficiente e fácil de integrar ao sistema já existente do banco, sem o uso de bibliotecas externas.

---

### 🎯 Objetivo
Implemente um programa que:
- Leia uma **string** representando o nome do destinatário de uma transferência.  
- Retorne essa mesma string com todas as letras convertidas para **maiúsculas**.  
- Preserve espaços e outros caracteres que não sejam letras (como números e símbolos).  

---

### 📥 Entrada
- Uma única linha contendo uma string com o nome do destinatário da transferência.  

### 📤 Saída
- Uma única linha contendo a mesma string da entrada, mas com todas as letras convertidas para maiúsculas.  

---

### 🖥️ Exemplo de Código em Python

```
# Lê o nome do destinatário da transferência
nome_destinatario = input()

# TODO: Converta todas as letras da variável 'nome_destinatario' para maiúsculas e imprima o resultado
print(nome_destinatario.upper())

```


## 💰 Desafio: Cálculo de Saldo Diário de Lançamentos Bancários

### 📖 Contexto
Você faz parte da equipe de tecnologia de um grande banco e recebeu uma missão importante: ajudar o setor financeiro a organizar rapidamente os lançamentos diários de despesas e receitas.  

Cada lançamento é registrado como uma string contendo o tipo (**D** para despesa, **R** para receita) seguido do valor em reais, separados por espaço.  

Sua tarefa é criar uma função que, ao receber uma lista desses lançamentos em uma única linha, calcule o **saldo final do dia**.  
O saldo é a soma de todas as receitas menos a soma de todas as despesas.  

O resultado deve ser apresentado com **duas casas decimais**, mesmo que o valor seja inteiro.  
Não utilize bibliotecas externas.

---

### 🎯 Objetivo
- Ler uma linha contendo lançamentos separados por vírgula.  
- Processar cada lançamento conforme o tipo e valor.  
- Calcular o saldo final do dia.  
- Imprimir o saldo com duas casas decimais.  

---

### 📥 Entrada
- Uma única linha contendo lançamentos separados por vírgula.  
- Cada lançamento é composto por uma letra (**D** ou **R**) seguida de um espaço e um valor decimal positivo.  

### 📤 Saída
- Uma única linha contendo o saldo final do dia, com duas casas decimais.  

---

### 🖥️ Exemplo de Código em Python

```python
def calcular_saldo():
    # Lê a linha de entrada
    entrada = input().strip()
    
    # Divide os lançamentos separados por vírgula
    lancamentos = entrada.split(",")
    
    saldo = 0.0
    
    # Processa cada lançamento
    for lancamento in lancamentos:
        tipo, valor_str = lancamento.strip().split()
        valor = float(valor_str)
        
        if tipo == "R":
            saldo += valor
        elif tipo == "D":
            saldo -= valor
    
    # Imprime o saldo final com duas casas decimais
    print(f"{saldo:.2f}")

# Executa a função
calcular_saldo()

```

## 🏦 Desafio: Remoção de Transações Duplicadas no Extrato Bancário

### 📖 Contexto
O Banco ByteSafe é conhecido por sua eficiência digital, mas recentemente um bug no sistema causou a duplicação de algumas transações em seu extrato online.  

Como analista de dados do banco, você foi encarregado de criar uma ferramenta que ajude a identificar e remover essas inconsistências.  

Cada linha do extrato é uma sequência de identificadores de transações, separados por espaço, e pode conter transações repetidas.  
Sua missão é garantir que cada transação apareça apenas **uma vez**, mantendo a ordem da primeira ocorrência.  

Assim, o extrato ficará limpo e sem duplicatas, facilitando a conferência dos clientes e a auditoria do banco.

---

### 🎯 Objetivo
Implemente uma função que:
- Receba uma string com identificadores de transações separados por espaço.  
- Retorne uma nova string, também separada por espaço, contendo apenas a primeira ocorrência de cada transação.  
- Preserve a ordem original das transações.  
- Não utilize bibliotecas externas para manipulação de listas ou conjuntos.  

---

### 📥 Entrada
- Uma única linha contendo identificadores de transações separados por espaço.  
- Cada identificador é uma sequência de caracteres alfanuméricos sem espaços.  

### 📤 Saída
- Uma única linha contendo os identificadores de transações, separados por espaço, sem repetições e na ordem da primeira ocorrência.  

---

### 🖥️ Exemplo de Código em Python

```
# Leitura da linha de identificadores de transações
entrada = input()

# Cria uma lista com as transações separadas por espaço
transacoes = entrada.split()

# Lista para armazenar apenas a primeira ocorrência
transacoes_unicas = []

# Percorre cada transação e adiciona à lista apenas se ainda não estiver presente
for t in transacoes:
    if t not in transacoes_unicas:
        transacoes_unicas.append(t)

# Imprime o resultado sem duplicatas
print(' '.join(transacoes_unicas))

