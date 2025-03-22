### **Análise da relação entre as preferências do consumidor e vendas - Blinkit**

Observação: A versão em inglês deste projeto está localizada ao final da versão em português, logo após a seção 4 (Análise SWOT).

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

#### **2. Descrição dos Dados**
O Dataset utilizado nesse projeto foi encontrado no Kaggle e disponibilizado no repositório do projeto. Com base nisso, é importante frisar que a base de dados está em inglês e, para facilitar o entendimento, as informações de cada coluna serão explicadas abaixo: 
- *Item Fat Content*: Teor de Gordura Adicionada presente no produto;
  
- *Item Identifier*: Código de identificação do produto;
  
- *Item Type*: Tipo do produto;
  
- *Outlet Establishment Year*: Ano de inauguração da loja;
  
- *Outlet Identifier*: Código de identificação da loja;
  
- *Outlet Location Type*: Refere-se à classificação baseada no nível de desenvolvimento econômico da cidade ou região onde a loja está localizada. "Tier 1", por exemplo, representa áreas altamente desenvolvidas economicamente;
  
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

#### **3. Principais achados:**
Após a organização e elaboração de gráficos, como resultado final da análise foi estruturado um dashboard interativo, anexado nesse repositório e representado na Imagem 4: 

![Captura de tela 2025-03-11 134405](https://github.com/user-attachments/assets/f0cecb1f-8d67-458e-8aa8-d4f5839f6b61)

Imagem 4

- Para interpretar esse gráfico, é essencial compreender o comportamento do mercado e dos consumidores da empresa analisada. Segundo o relatório Global HFA 2024, publicado pela Health & Fitness Association, há um grande potencial de crescimento para o segmento saudável/fitness no mercado indiano, onde a empresa está localizada. Com esse contexto em mente, a análise dos gráficos se torna ainda mais significativa, pois demonstra que os consumidores da Blinkit acompanham essa tendência. Os dados mostram que 65% das compras incluem produtos com baixo teor de gordura adicionada em todas as categorias de localização de loja (Tier 1, 2 e 3), e frutas e verduras foram os itens mais vendidos, totalizando 178,1K, o que sugere que públicos de diferentes níveis de renda possuem preferência por produtos saudáveis. No entanto, para confirmar essa hipótese, seria necessário coletar dados sobre a renda média dos clientes. De toda forma, os números indicam uma clara preferência dos consumidores da Blinkit por produtos alinhados a um estilo de vida saudável, diante desse cenário, a empresa pode explorar estratégias para fidelizar e atrair consumidores que buscam esse tipo de produto. Para isso, seria interessante estudar o mercado e suas tendências, identificando lacunas e oportunidades nesse nicho. Uma possível iniciativa seria a criação de programas de fidelidade, oferecendo benefícios para clientes que mantêm compras recorrentes na Blinkit. Essa medida se mostra estratégica, pois indivíduos que consomem produtos saudáveis geralmente não o fazem de maneira pontual, mas sim como parte de um estilo de vida. Assim, garantir a fidelização desse público pode gerar um impacto positivo nas finanças e no posicionamento da marca, demonstrando que a empresa se preocupa com a saúde e o bem-estar de seus clientes.

Link para os principais insights do relatório: https://pt.healthandfitness.org/improve-your-club/industry-news/global-health-and-fitness-industry-poised-for-further-expansion/

![Captura de tela 2025-03-11 134000](https://github.com/user-attachments/assets/0cfb8ca8-d2ce-4464-8631-eeee7fed6b82)

Imagem 5

- De acordo com os resultados encontrados nos gráficos, é importante ressaltar que a maior parte das vendas foi realizada em localidades do tipo "Tier 3" (472,1K), seguida pelas localidades do tipo "Tier 2" (393,2K) e "Tier 1" (336,4K), ou seja, cidades/locais com menor desenvolvimento economico. Diante disso, há uma indicação que o público-alvo da Blinkit esteja nessas localidadas, o que sugere uma forte demanda por produtos acessíveis e saudáveis em regiões com menor desenvolvimento econômico. Esse dado pode indicar que os consumidores dessas áreas estão cada vez mais interessados em um estilo de vida saudável, independentemente do nível de renda. Diante desse cenário, a Blinkit pode considerar estratégias específicas para fortalecer sua presença nesses locáis. Portanto, a adoção de políticas de preços acessíveis, promoções direcionadas e parcerias com fornecedores locais podem ser alternativas viáveis para aumentar ainda mais as vendas e a fidelização desse público. 
  
![Captura de tela 2025-03-11 134100](https://github.com/user-attachments/assets/dc76ed80-e0df-42ef-9f58-05c1b84bd741)

Imagem 6

#### **4. Análise SWOT**

![swot projeto excel](https://github.com/user-attachments/assets/82af38ee-c439-4bca-8474-c8b9fe9d3dc5)

Imagem 7

*Pontos Fortes:*
- Plataforma de vendas online eficiente: A Blinkit já possui uma estrutura de vendas online bem estabelecida, permitindo um alcance rápido e conveniente para os consumidores;
  
- Ampla variedade de produtos saudáveis: A empresa já oferece uma boa gama de produtos com baixo teor de gordura, frutas e vegetais, o que atrai consumidores preocupados com a saúde;
  
- Capacidade de adaptação a diferentes mercados: Blinkit consegue operar em diversas localizações (Tier 1, 2 e 3), o que demonstra sua flexibilidade para atender a diferentes tipos de consumidores.

*Pontos Fracos:*
- Falta de dados sobre a renda dos clientes: A ausência de informações detalhadas sobre a renda média dos clientes dificulta uma compreensão mais profunda do perfil do consumidor;
  
- Capacidade limitada de personalização de ofertas: A falta de uma segmentação mais detalhada dos clientes e a personalização das ofertas podem diminuir a efetividade das campanhas de marketing e promoções;
  
- Avaliação média baixa dos clientes (4/5): A avaliação média da empresa é considerada relativamente baixa, o que pode desencorajar novos consumidores a comprarem com a Blinkit.

*Oportunidades:*
- Expansão em mercados Tier 3: O aumento de vendas em áreas com menor desenvolvimento econômico representa uma grande oportunidade de crescimento e fidelização de consumidores;
  
- Programas de fidelidade: Criar programas de fidelidade para consumidores recorrentes pode ajudar a aumentar a lealdade e engajamento do público;
  
- Aproveitamento de tendências de consumo saudável: O público que consome esse tipo de produto pode ser aproveitado para valorizar a percepção da marca no mercado e esxplorar um nicho altamente lucrativo.

*Ameaças:*
- Mudanças no comportamento do consumidor: Alterações nas preferências e hábitos dos consumidores podem afetar a demanda por produtos saudáveis e fitness;
  
- Instabilidade econômica: A instabilidade econômica no mercado indiano pode afetar o poder de compra dos consumidores, principalmente nas localidades de menor desenvolvimento econômico;
  
- Aumento da concorrência: A entrada de novos concorrentes no mercado de produtos saudáveis pode intensificar a competição, prejudicando as margens de lucro e a participação de mercado.


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

  **2. Data Description:**


The dataset used in this project was sourced from Kaggle and is available in the project repository. Therefore, the following descriptions clarify the meaning of each column:

*Item Fat Content*: The amount of added fat in the product;

*Item Identifier*: Unique identification code for the product;

*Item Type*: The category of the product;

*Outlet Establishment Year*: The year the store was established;

*Outlet Identifier*: Unique identification code for the store;

*Outlet Location Type*: It refers to the classification based on the economic development level of the city or region where the store is located. "Tier 1," for example, represents highly economically developed areas;

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

3. Key Findings

After organizing the data and creating the graphs, the final result of the analysis was the development of an interactive dashboard, attached in this repository and shown in Image 4:

![Captura de tela 2025-03-11 134405](https://github.com/user-attachments/assets/f0cecb1f-8d67-458e-8aa8-d4f5839f6b61)

Image 4

- To properly interpret this chart, it’s essential to understand the market dynamics and consumer behavior of the analyzed company. According to the *Global HFA 2024* report by the *Health & Fitness Association*, the healthy/fitness segment has strong growth potential in the Indian market, where the company operates. With this in mind, the data becomes even more significant, as it shows that Blinkit consumers are embracing this trend. The numbers reveal that 65% of purchases include low-added-fat products across all store location categories (Tier 1, 2, and 3), while fruits and vegetables were the top-selling items, totaling 178.1K. This suggests that consumers across different income levels prefer healthier options. However, to confirm this, additional data on customer income levels would be needed. Even so, the data clearly indicates that Blinkit customers prioritize products that align with a healthy lifestyle. Given this trend, the company has an opportunity to strengthen customer loyalty and attract new consumers by tapping into this demand. A key strategy could be studying market trends to identify gaps and opportunities within this niche. One effective initiative might be launching a loyalty program that rewards customers who consistently purchase healthy products from Blinkit. Since people who choose healthier foods typically see it as a long-term lifestyle commitment rather than a one-time decision, building customer loyalty in this segment could be highly beneficial. Not only would it positively impact revenue, but it would also enhance Blinkit's brand positioning by reinforcing its commitment to customer health and well-being.

Link of the research: [https://pt.healthandfitness.org/improve-your-club/industry-news/global-health-and-fitness-industry-poised-for-further-expansion/](https://www.healthandfitness.org/improve-your-club/industry-news/global-health-and-fitness-industry-poised-for-further-expansion/)


![Captura de tela 2025-03-11 134000](https://github.com/user-attachments/assets/0cfb8ca8-d2ce-4464-8631-eeee7fed6b82)

Image 5

- According to the results shown in the chart, most sales took place in "Tier 3" locations (472.1K), followed by "Tier 2" locations (393.2K) and "Tier 1" locations (336.4K), meaning that the majority of purchases were made in areas with lower economic development. This suggests that Blinkit's target audience may be concentrated in these regions, indicating a strong demand for affordable and healthy products in less economically developed areas. This data may also suggest that consumers in these locations are increasingly interested in a healthy lifestyle, regardless of their income level. Given this scenario, Blinkit could consider specific strategies to strengthen its presence in these areas. Implementing affordable pricing policies, targeted promotions, and partnerships with local suppliers could be effective ways to further increase sales and enhance customer loyalty.


![Captura de tela 2025-03-11 134100](https://github.com/user-attachments/assets/dc76ed80-e0df-42ef-9f58-05c1b84bd741)

Image 6

**4. SWOT Analysis**

![swot projeto excel (1)](https://github.com/user-attachments/assets/93830b37-6ee0-4097-a122-63653a4b16e4)

Image 7

*Strengths:*
- Efficient online sales platform: Blinkit already has a well-established online sales structure, enabling quick and convenient access for consumers;
  
- Wide range of healthy products: The company already offers a good variety of low-fat products, fruits, and vegetables, appealing to health-conscious consumers;
  
- Ability to adapt to different markets: Blinkit operates in various locations (Tier 1, 2, and 3), demonstrating flexibility in catering to different consumer types.

*Weaknesses:*

- Lack of customer income data: The absence of detailed data on customer income makes it difficult to fully understand the consumer profile;

- Limited offer customization: The lack of detailed customer segmentation and personalized offers may reduce the effectiveness of marketing campaigns and promotions;

- Low average customer rating (4/5): Although customers are generally satisfied, the average rating of 4/5 indicates room for improvement in service and product offerings.

*Opportunities:*
- Expansion in Tier 3 markets: The growing sales in less economically developed areas represent a significant growth and customer loyalty opportunity;
  
- Loyalty programs: Creating loyalty programs for repeat customers can help increase loyalty and audience engagement;
  
- Leveraging healthy consumption trends: The rising awareness of healthy eating can be leveraged to promote more products aligned with these values.

*Threats:*
- Changes in consumer behavior: Shifts in consumer preferences and habits could impact the demand for healthy and fitness product;

- Economic instability: Economic instability in the Indian market may affect consumers' purchasing power, especially in less economically developed areas;
  
- Increased competition: The entry of new players into the healthy products market could intensify competition, harming profit margins and market share.
