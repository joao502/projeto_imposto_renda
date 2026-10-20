# 📊 Projeto Imposto de Renda

Planilha em Excel com macros (VBA) para **organizar as informações necessárias para a declaração do Imposto de Renda de Pessoa Física (IRPF)**: dados do titular, rendimentos bancários e movimentações financeiras (entradas e saídas), com anexo dos comprovantes.

## 🎯 Objetivo

Centralizar em um único arquivo tudo o que costuma ser pedido na hora de declarar o IR, evitando documentos espalhados e facilitando a conferência dos valores antes do envio.

## 🧩 Estrutura da planilha

A pasta de trabalho tem 4 abas:

### 1. TITULAR
Cadastro dos dados pessoais do contribuinte:
- Nome, CPF, data de nascimento e título de eleitor
- Cônjuge
- Endereço (completo e abreviado), CEP, telefone, celular e e-mail
- Perguntas de controle (lista suspensa **Sim/Não**):
  - Houve alterações da entrega anterior?
  - Dependente cônjuge?
  - Residente do exterior?
- O e-mail possui hiperlink com assunto pré-preenchido.
- A aba é **protegida**, para evitar alterações acidentais na estrutura.

### 2. INFORMES (Informes de Rendimentos Bancários)
Registro dos rendimentos de até **3 bancos**. Para cada banco:
- **Banco:** lista suspensa com os bancos da aba TABELAS (com mensagem de erro caso o banco não exista)
- **Valor atual:** saldo/rendimento informado
- **Anexo 📎:** ao clicar, abre o explorador de arquivos para anexar o informe em PDF
- **Total:** soma automática dos valores dos três bancos

### 3. NOTAS (Notas bancárias / extrato de holerites)
Controle mensal de receitas e despesas, em duas tabelas do Excel:
- **ENTRADAS:** data, categoria (ex.: holerite, freelancer, CNPJ) e valor
- **SAÍDAS:** data, categoria (ex.: luz, internet, comida, carro) e valor
- Painel com **Total de Entradas**, **Total de Saídas** e **Total Líquido** (entradas − saídas), calculados por fórmulas

### 4. TABELAS
Aba de apoio com a lista de bancos (código + nome) que alimenta a lista suspensa da aba INFORMES. Inclui bancos como Banco do Brasil, Caixa, Itaú, Bradesco, Santander, Nubank, Inter, C6 Bank, PicPay, entre outros.

## ⚙️ Automação (VBA)

Na aba **INFORMES**, ao clicar nas células de anexo (`D13`, `D18` e `D23`), a macro:

1. Abre o explorador de arquivos filtrado para **PDF**
2. Pega o caminho do arquivo escolhido
3. Escreve o **nome do arquivo** na própria célula, como **hiperlink** que abre o documento original

<img width="987" height="542" alt="image" src="https://github.com/user-attachments/assets/51506f65-d606-40d7-8180-d5a6604f5da7" />
<img width="1042" height="643" alt="image" src="https://github.com/user-attachments/assets/ffd22990-18d7-42b3-bb6b-33b60d31a288" />
<img width="1168" height="618" alt="image" src="https://github.com/user-attachments/assets/a145c374-a5b7-4219-b104-d5a746316ef2" />




