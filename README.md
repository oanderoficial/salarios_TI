<h1>Salários Notebook</h1> 

Notebook jupyter contendo os dados fornecidos pela Forbes sobre a Média e a Máxima salarial em TI.

<h2> Gráficos utilizando Plotly </h2>

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

```
