# Classificação de clientes propícios ao Churn utilizando SVM

## 1.0 OBJETIVO DO CASE 💻

🗣 Churn é uma métrica utilizada para mostrar o número de clientes que cancelam serviço em um determinado período de tempo. Ela é importante pois ajuda a medir a expansão da sua empresa, já que é preciso que o número de novos negócios exceda esse indicador.

👉 O principal ponto deste case é classificar os clientes de um banco em Clientes que irão permanecer no banco (Existing Customer) e os que podem sair, ou seja realizando o Churn (Attrited Customer), baseado em suas informações.

👉 Utilizarei o algoritmo SVC (Support Vector Classifier) para a criação de um modelo de Machine Learning que possa realizar esta classificação.

## 2.0 METODOLOGIA 🔧

👉 Inicialmente realizei a leitura do dataset que possui 10.127 linhas e 20 colunas. O dataset apresenta todas as features com dados pessoais e econômicos dos clientes do banco, que serão úteis para a classificação do público.

👉 Realizei a limpeza e o tratamento dos dados verificando a existência de dados duplicados, nulos e verificando outliers de cada uma das variáveis da base de dados.

👉 Realizei análises e extração de Insights importantes relacionados ao perfil do público e ofereci possíveis soluções para o banco evitar o churn dos clientes.

👉 Tratei e preparei os dados, antes da criação do modelo, realizando utilizando o `LabelEncoder()` para tratar todos os dados do tipo categorico, balanceamento da variável target com utilizando técnica de oversampling com `SMOTE`, e por fim padronização de todos os dados presentes no dataset utilizando `StandardScaler()`.

👉 Separei os dados em X e y e em treino e teste (70% treino e 30% teste).

👉 Criei o `modelo_v1` utilizando o kernel `linear`, treinei com os dados padronizados e realizei previsões. Com isso foi possível medir a performance do modelo utilizando as seguintes métricas: `Precision`, `Recall`, `F1 Score`, `Acurácia`, `AUC`.

👉 Realizei o mesmo procedimento na criação do `modelo_v2`, porém agora utilizando o kernel `RBF` e o `GridSearch()` para buscar os melhores valores dos hiperparâmetros `C` e `gamma`.

👉 Para o `modelo_v3` o procedimento foi parecido com a construção do `modelo_v2`, porém utilizando o kernel `poly` e buscando os hiperparâmetros `gamma`, `d` e `r`.

## 3.0 RESULTADOS 🤖
👉 O resultado dos modelos podem ser vistos na Figura abaixo

![image](https://user-images.githubusercontent.com/81670585/232657360-1af9c325-b57b-4a0b-b035-e8731b5b62e1.png)

<h1 style='color: red; font-size: 32px; font-weight: bold;'>Modelo Campeão: 2️⃣</h1>

## 4.0 CONCLUSÕES 🎉

👉 Utilizei o algoritmo SVC para construir 3 modelos de classificação.

👉 O melhor modelo foi o Modelo 2, uma vez que foi campeão em grande parte das métricas em relação ao modelo 3.

👉 O modelo 2 foi construido apenas utilizando o kernel RBF e usando o GridSearch para encontrar os melhores parâmetros do modelo.

👉 Para aperfeiçoar melhor ainda o modelo, poderia ter reduzido algumas features que não possuem muita importância para o modelo, porém como muitas dessas informações chegam para o banco com os novos clientes entrantes, optei por manter.

👉 Com as análises de dados feitas no ítem 4, também obtive alguns insights como por exemplo:

* Um pouco mais da metade (52%) do público deste banco possui uma renda menor que a renda anual média de um americano (70k anual). Fonte: Indeed

![image](https://user-images.githubusercontent.com/81670585/232657847-1f9879bb-e4d7-4953-90ea-a4cfb72263d6.png)

* 70% do público possui alguma educação comprovada

![image](https://user-images.githubusercontent.com/81670585/232657880-c7c94a0e-db3d-45a9-95c3-09205d480d4c.png)

* Metade dos clientes possui menos que 36 meses e a outra metade mais que 36 meses, isso são mais ou menos 3 anos no mesmo banco.

![image](https://user-images.githubusercontent.com/81670585/232657970-0bded001-3fc8-4d09-bfb6-1cc7e477972f.png)

* Há um número maior de evasão nos clientes com 2 à 3 anos de banco, portanto o banco deve focar sua atenção em um público mais fiel ao mesmo do que novos entrantes.

![image](https://user-images.githubusercontent.com/81670585/232658019-291023fc-5694-4eef-9101-09fd46a0781c.png)

* Clientes com mais produtos são os que menos realizam Churn. O banco deve oferecer mais produtos interessantes de acordo com o seu apetite de risco e que interessem o cliente em continuar com o banco.

![image](https://user-images.githubusercontent.com/81670585/232658044-c6b23751-56a7-41c3-b614-041a447deadc.png)
![image](https://user-images.githubusercontent.com/81670585/232658066-ecad1aa8-d1ce-4d22-9a61-347e8b63bc0d.png)

* Podemos ver que quanto maior o limite do cartão de crédito, menor a taxa de Churn, ou seja, aumentar o limite do cartão pode manter o cliente no banco.

![image](https://user-images.githubusercontent.com/81670585/232658120-1c9334d4-d119-4349-bf07-667c7869c1fa.png)
![image](https://user-images.githubusercontent.com/81670585/232658138-319456fa-016e-40b7-b7a1-d8bb32e16920.png)



<h3 align="left">Contato:</h3>
<p align="left">
<a href="https://linkedin.com/in/lucassavioscarafiz" target="blank"><img align="center" src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/linked-in-alt.svg" alt="lucassavioscarafiz" height="30" width="40" /></a>
</p>

📫 **lucassavioscarafiz@gmail.com**

<h3 align="left">Linguagens e Ferramentas:</h3>
<p align="left"> <a href="https://cloud.google.com" target="_blank" rel="noreferrer"> <img src="https://www.vectorlogo.zone/logos/google_cloud/google_cloud-icon.svg" alt="gcp" width="40" height="40"/> </a> <a href="https://www.mysql.com/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/mysql/mysql-original-wordmark.svg" alt="mysql" width="40" height="40"/> </a> <a href="https://pandas.pydata.org/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/2ae2a900d2f041da66e950e4d48052658d850630/icons/pandas/pandas-original.svg" alt="pandas" width="40" height="40"/> </a> <a href="https://www.python.org" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/python/python-original.svg" alt="python" width="40" height="40"/> </a> <a href="https://scikit-learn.org/" target="_blank" rel="noreferrer"> <img src="https://upload.wikimedia.org/wikipedia/commons/0/05/Scikit_learn_logo_small.svg" alt="scikit_learn" width="40" height="40"/> </a> <a href="https://seaborn.pydata.org/" target="_blank" rel="noreferrer"> <img src="https://seaborn.pydata.org/_images/logo-mark-lightbg.svg" alt="seaborn" width="40" height="40"/> </a> </p>
