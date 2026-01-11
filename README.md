# Análise Preditiva de Estoque Inteligente com Amazon SageMaker Canvas

## 1. Entendimento do Problema de Negócio
O objetivo deste projeto é desenvolver uma **previsão inteligente de estoque**, utilizando técnicas de Machine Learning para antecipar a demanda futura de produtos.

A solução busca apoiar a tomada de decisão, permitindo:
- Redução de rupturas de estoque  
- Evitar excesso de produtos parados  
- Melhor planejamento de compras e reposição  
- Uso estratégico de dados históricos  

A previsão é baseada em dados de vendas e estoque, utilizando o **Amazon SageMaker Canvas**, uma ferramenta no-code da AWS.

---

## 2. Preparação dos Dados
Antes da modelagem, os dados precisam estar organizados e estruturados corretamente.

### Tipos de dados utilizados
- Histórico de vendas
- Informações dos produtos
- Dados de estoque
- Datas para análise temporal

### Formato dos dados
- Arquivo CSV
- Cada linha representa um registro histórico
- Colunas bem definidas e padronizadas

### Exemplo de colunas
- `data`
- `produto_id`
- `quantidade_vendida`
- `estoque_atual`
- `categoria`

---

## 3. Acesso ao Amazon SageMaker Canvas
1. Acessar o **AWS Management Console**
2. Entrar no serviço **Amazon SageMaker**
3. Selecionar a opção **Canvas**
4. Criar ou acessar um workspace

O SageMaker Canvas permite criar modelos de Machine Learning sem necessidade de programação.

---

## 4. Importação dos Dados
Dentro do SageMaker Canvas:
1. Selecionar **Import data**
2. Fazer upload do arquivo CSV ou conectar a um bucket S3
3. Verificar se as colunas foram reconhecidas corretamente
4. Ajustar tipos de dados, se necessário (numérico, categórico ou data)

Essa etapa garante que o modelo interprete corretamente as informações.

---

## 5. Definição do Tipo de Problema
Após a importação:
1. Criar um novo modelo
2. Selecionar o tipo de problema como **Time Series Forecasting**
3. Definir a variável alvo, por exemplo:
   - `quantidade_vendida`

Esse tipo de modelagem é ideal para previsões baseadas em histórico temporal.

---

## 6. Configuração da Previsão de Estoque Inteligente
Nesta etapa são definidos:
- Coluna de data
- Frequência temporal (diária, semanal ou mensal)
- Horizonte de previsão (ex: 7, 15 ou 30 dias)
- Identificador do item (ex: `produto_id`)

O SageMaker Canvas realiza automaticamente:
- Detecção de padrões
- Identificação de sazonalidade
- Seleção do melhor modelo de Machine Learning

---

## 7. Treinamento do Modelo
Com as configurações definidas:
1. Iniciar o treinamento do modelo
2. O Canvas testa diferentes algoritmos automaticamente
3. O modelo com melhor desempenho é selecionado

Todo o processo ocorre de forma automatizada e sem código.

---

## 8. Avaliação dos Resultados
Após o treinamento, o SageMaker Canvas apresenta:
- Métricas de desempenho do modelo
- Gráficos comparando valores reais e previstos
- Insights automáticos sobre os dados

Esses resultados ajudam a validar a qualidade da previsão.

---

## 9. Geração das Previsões de Estoque
Com o modelo treinado:
1. Gerar previsões de demanda futura
2. Analisar os resultados por produto ou categoria
3. Identificar possíveis riscos de:
   - Ruptura de estoque
   - Excesso de produtos

Essa abordagem torna o estoque mais **proativo e inteligente**.

---

## 10. Exportação dos Resultados
Os resultados podem ser exportados em formato CSV ou utilizados em:
- Relatórios
- Dashboards
- Sistemas de gestão de estoque

Isso permite a integração da previsão com outras ferramentas de negócio.

---


Exemplos:
https://github.com/aws/amazon-sagemaker-examples
