<h1>Salários Notebook</h1> 

Notebook jupyter contendo os dados fornecidos pela Forbes sobre a Média e a Máxima salarial em TI.
Dados por forbes.com.br (2022).


<h2> Gráficos utilizando Plotly </h2>
<br> 

```Python
import pandas as pd
import plotly.express as px

data = {'Cargo': ['Diretores de tecnologia', 'Diretores de engenharia', 'Diretores de infraestrutura'], 
        'Média salarial': [29250, 27500, 24600],
        'máxima salarial': [38750,32500,30000]}
df = pd.DataFrame(data)

figura = px.bar(df, x='Cargo', y= ['Média salarial', 'máxima salarial'],
    title='Salário dos Diretores',
    color_discrete_map={'Média salarial':'#3CB371', 'máxima salarial': '#2F4F4F'},
    template='plotly_dark',
    barmode='group')

figura.update_layout(yaxis=dict(tickformat="R$,.2f"))
figura.show()

```
<br> <br> 

````python

import pandas as pd 
import plotly.express as px

data = {'Cargo': ['Gerentes e heads de desenvolvimento', 'Profissionais de segurança', 'Gerentes e heads de dados', 'Heads de produto', 'gerentes de tecnologia '], 
        'Média salarial': [24875, 21775, 22250,17750,25500],
        'máxima salarial': [36000,27000,31075,24750,32000]}
df = pd.DataFrame(data)

figura = px.bar(df, x='Cargo', y= ['Média salarial','máxima salarial'],
    title='Salário dos Gerentes',
    color_discrete_map={'Média salarial':'#3CB371', 'máxima salarial': '#2F4F4F'},
    template='plotly_dark',
    barmode='group')

figura.update_layout(yaxis=dict(tickformat="R$,.2f"))
figura.show()

````
<br><br>

````Python
import pandas as pd 
import plotly.express as px

data = {'Cargo': ['Tech leads', 'Product managers', 'Product owners', 'Product designers', 'Profissionais de SRE e DevOps', 'Arquitetos de software', 'Agile coaches e Scrum masters', 'Engenheiros de QA', 'Engenheiros de dados','Cientistas de dados e BI'], 
        'Média salarial': [17500, 14750, 10750,11000,14500,16500,13500,12500,11500,7750],
        'máxima salarial': [21000,18750,13500,13000,18500,18500,16000,15000,16500,12000]}
df = pd.DataFrame(data)

figura = px.bar(df, x='Cargo', y= ['Média salarial','máxima salarial'],
    title='Salários dos engenheiros e líderes',
    color_discrete_map={'Média salarial':'#3CB371', 'máxima salarial': '#2F4F4F'},
    template='plotly_dark',
    barmode='group')

figura.update_layout(yaxis=dict(tickformat="R$,.2f"))
figura.show()

