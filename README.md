# Proyecto-de-analisis-de-datos
Basado en el tutorial https://learn.microsoft.com/en-us/power-bi/connect-data/desktop-python-visuals
<img width="1152" height="720" alt="python-POWERBI" src="https://github.com/user-attachments/assets/f2306ad3-84b7-4567-b37b-cb3a529553ff" />

Obtener datos - script de python : dataset a importar: 

import pandas as pd 
df = pd.DataFrame({ 
    'Fname':['Harry','Sally','Paul','Abe','June','Mike','Tom'], 
    'Age':[21,34,42,18,24,80,22], 
    'Weight': [180, 130, 200, 140, 176, 142, 210], 
    'Gender':['M','F','M','M','F','M','M'], 
    'State':['Washington','Oregon','California','Washington','Nevada','Texas','Nevada'],
    'Children':[4,1,2,3,0,2,0],
    'Pets':[3,2,2,5,0,1,5] 
}) 
print (df)

NOTA: 
para poder ejecutar cada script de python de cada grafico es necesario que los valores que se usan en cada grafico no esten "resumidos"

1 script por grafico

import matplotlib.pyplot as plt 
dataset.plot(kind='bar',x='Fname',y='Age')
# plt.title('Grafico de barras') # <- Añade esta línea exactamente aquí 
plt.show()

import matplotlib.pyplot as plt 
ax = plt.gca() 
dataset.plot(kind='line',x='Fname',y='Children',ax=ax) 
dataset.plot(kind='line',x='Fname',y='Pets', color='red', ax=ax) 
# plt.title('Grafico de lineas') # <- Añade esta línea exactamente aquí
plt.show()

import matplotlib.pyplot as plt 
dataset.plot(kind='scatter', x='Age', y='Weight', color='red', )
# plt.title('Grafico de dispersion') # <- Añade esta línea exactamente aquí
plt.show()
