### **Análise da relação entre as preferências do consumidor e vendas - Blinkit**


#### **1. Objetivo do Projeto**
Este projeto tem como objetivo a limpeza, transformação e análise dos dados da empresa Blinkit, um marketplace que vende produtos de diversas categorias, como higiene pessoal, eletrônicos, flores, entre outros. Dessa forma, busca-se otimizar o processo de vendas com base em dados quantitativos, focando na relação entre o total de vendas e outras variáveis relevantes para entender a situação atual da organização. A seguir, são explicitadas as métricas e questões de estudo consideradas fundamentais:

 **KPIs:**
 - *Total de Vendas*: total de receita resultante de todos os itens vendidos;
 - *Receita Média por Venda*: a média das receitas por venda;
 -  *Número de Itens Vendidos*: a quantidade total de produtos vendidos;
 -  *Avaliação Média do Produto*: nota média atribuída pelos consumidores aos produtos.

**Questões Analisadas:**


*Total de Vendas por gordura adicionada:*
 - Objetivo: Analisar o impacto do teor de gordura adicionada no total de vendas;

   
*Total de Vendas por Tipo de Produto:*
- Objetivo: Identificar a porcentagem das vendas de diferentes produtos alimentícios em relação ao total de vendas;


*Comparação do Total de Vendas por Loja segmentada pela Variação do Teor de Gordura Adicionada:*
- Objetivo: Segmentar o Total de Vendas de cada Loja com base no Teor de Gordura Adicionada em cada produto;

*Segmentação Demográfica por Loja:*
- Objetivo: Entender como a idade e tipo de loja influenciam nas decisões de compra dos consumidores e, consequentemente, no Total de Vendas. 

*Total de Vendas por Tamanho da Loja:*
- Objetivo: Analisar a correlação entre o Tamanho da Loja e o Total de Vendas.

*Total de Vendas pela Localização da Loja:*
- Objetivo: Entender a distribuição geográfica das vendas.

*Resumo dos KPIs utilizados em relação ao Tipo de Loja:* 
- Objetivo: Fornecer uma visão global aos gestores dos resultados para cada métrica considerada nesse projeto (Vendas Médias, Número de Itens, Avaliação Média do Produto), destacando os resultados de cada Tipo de Loja.

### English Version: 

**1. Project Objective:**

This project focuses on cleaning, transforming, and analyzing data from Blinkit, a marketplace that sells products across various categories, including personal care, electronics, flowers, and more. The goal is to optimize the sales process using quantitative data, with a focus on the relationship between total sales and other key variables that provide insights into the company's current performance.

Below are the key metrics and research questions considered essential for this study:

**Key Performance Indicators (KPIs):**

*Total Sales*: The total revenue generated from all sold items;

*Average Revenue per Sale*: The average revenue per transaction;

*Number of Items Sold*: The total quantity of products sold;

*Average Product Rating*: The average customer rating for a product.

**Research Questions:**

*Total Sales by Added Fat Content:*
- Objective: Analyze the impact of added fat content on total sales.
  
*Total Sales by Product Type:*
- Objective: Determine the share of sales from different food product categories relative to total sales.

*Comparison of Total Sales by Store segmented by Variation in Added Fat Content:*
- Objective: Compare total sales across different stores based on variations in the fat content of the products sold.

*Relationship Between KPIs:*
- Objective: Understand how average sales, the number of items sold, and product ratings correlate with variations in added fat content in food products.
  
*Demographic Segmentation by Store:*
- Objective: Analyze how demographic factors, such as customer age and store type, influence purchasing decisions and, in turn, total sales.
  
*Total Sales by Store Size:*
- Objective: Examine the correlation between store size and total sales.
  
*Total Sales by Store Location:*
- Objective: Analyze the geographical distribution of sales.
  
*Summary of KPIs by Store Type:*
- Objective: Provide managers with a comprehensive overview of key performance metrics (average sales, number of items sold, and product ratings), highlighting results for each store type.


#### **2. Descrição dos Dados**
O Dataset utilizado nesse projeto foi encontrado no Kaggle e disponibilizado no repositório do projeto. Com base nisso, é importante frisar que a base de dados está em inglês e, para facilitar o entendimento, as informações de cada coluna serão explicadas abaixo: 
- *Item Fat Content*: Teor de Gordura Adicionada presente no produto;
  
- *Item Identifier*: Código de identificação do produto;
  
- *Item Type*: Tipo do produto;
  
- *Outlet Establishment Year*: Ano de inauguração da loja;
  
- *Outlet Identifier*: Código de identificação da loja;
  
- *Outlet Location Type*: Tipo de localização da loja. Por exemplo, "Tier 1" refere-se a estabelecimentos que ocupam um prédio inteiro, enquanto "Tier 2" representa lojas que ocupam apenas um andar de um prédio;
  
- *Outlet Size*: Tamanho da loja;
  
- *Outlet Type*: Tipo da loja;
  
- *Item Visibility*: Visibilidade do produto (refere-se a capacidade que os consumidores tem em descobrir, identificar e se interessar pelo produto);
  
- *Item Weight*: Peso do produto;
  
- *Sales*: Total de Vendas;
  
- *Rating*: Média das avaliações do Produto pelos consumidores.

**Limpeza dos dados:**

Nesse processo podem-se destacar as seguintes ações de limpeza de dados: 

- Durante o estudo da base de dados, foi possível perceber que haviam categorias iguais nomeadas de duas formas diferentes, como em "LF" e "Low Fat" ou "reg" e "Regular", como mostra a Imagem 1. Com a intenção de padronizar os campos e facilitar as análises que serão posteriormente feitas, os termos foram unificados, como pode-se perceber na Imagem 2:
  
![Captura de tela 2025-03-10 165955](https://github.com/user-attachments/assets/5827b004-70ae-455c-af7d-8c4e9d4ac7ee)

Imagem 1 


![Captura de tela 2025-03-10 173331](https://github.com/user-attachments/assets/d8205c1a-acc8-4374-889f-b90a5f24ae3a)
Imagem 2 


- Outra questão interessante de ser mencionada é que, mesmo contendo valores vazios no dataset (vide Imagem 3), eles não foram excluídos ou modificados. Essa colocação se dá, pois eram parte da coluna "Item Weight", que, além de não ser alvo de análise, é uma categoria que não é relevante a todo tipo de produto e, portanto, não foi considerada:

![Captura de tela 2025-03-10 174420](https://github.com/user-attachments/assets/c565d235-58d2-4375-aa6c-4a247e61d6fa)

Imagem 3


### English Version: 

**2. Data Description:**


The dataset used in this project was sourced from Kaggle and is available in the project repository. Therefore, the following descriptions clarify the meaning of each column:

*Item Fat Content*: The amount of added fat in the product;

*Item Identifier*: Unique identification code for the product;

*Item Type*: The category of the product;

*Outlet Establishment Year*: The year the store was established;

*Outlet Identifier*: Unique identification code for the store;

*Outlet Location Type*: The classification of the store’s location. For example, "Tier 1" refers to standalone buildings, while "Tier 2" represents stores occupying only one floor of a building;

*Outlet Size*: The size of the store;

*Outlet Type*: The classification of the store;

*Item Visibility*: The extent to which consumers can discover, recognize, and show interest in the product;

*Item Weight*: The weight of the product;

*Sales*: Total revenue from sales;

*Rating*: The average customer rating of the product.

**Data Cleaning**

The following data cleaning actions were carried out during this process:

- While analyzing the dataset, it was observed that certain identical categories were labeled differently, such as "LF" and "Low Fat" or "reg" and "Regular," as shown in Image 1. To standardize the fields and facilitate subsequent analysis, these terms were unified, as illustrated in Image 2:
  
![Captura de tela 2025-03-10 165955](https://github.com/user-attachments/assets/5827b004-70ae-455c-af7d-8c4e9d4ac7ee)

Image 1 


![Captura de tela 2025-03-10 173331](https://github.com/user-attachments/assets/d8205c1a-acc8-4374-889f-b90a5f24ae3a)
Image 2 


- Another noteworthy point is that, despite the presence of missing values in the dataset (see Image 3), they were neither removed nor modified. This decision was made because the missing values belonged to the "Item Weight" column, which was not a focus of the analysis. Additionally, this attribute is not relevant for all product types and was therefore not considered:

![Captura de tela 2025-03-10 174420](https://github.com/user-attachments/assets/c565d235-58d2-4375-aa6c-4a247e61d6fa)

Image 3

#### **3. Principais achados**
Resumo do que foi encontrado (focar em negócios e achados desse tipo)

#### **4. Sugestão de priorização dos problemas encontrados**
GUT 
