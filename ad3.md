# Ejercicio con Python para lograr un scraping de una web
Aquí el ejercicio en Python [EjercicioPython](https://github.com/nebrijas/2022online-AngelicaTrejos/blob/990e3f93538d24f05902d167d26660761ebffca0/docs/Ad3.ipynb)

Iniciamos con el ejercicio de programacion literaria con Python para lograr un scraping de una web, este ejercicio es importante puesto que las paginas web son constantemente modificadas y actualizadas, sus contenidos cambian con el tiempo, puede que cambie su diseño, por ejemplo, o que se les añadan nuevos elementos. Los web scrapers (programa el cual tiene como finalidad extraer información de sitios web) se desarrollan teniendo en cuenta la estructura específica de una página web, de forma que, si dicha estructura cambia, el scraper también debe modificarse. Este proceso resulta especialmente sencillo con Python.

Por lo anterior, a continuacion te explicaremos como se hace: Lo primero es importar las librerías y módulos, pero antes te presentaremos el codigo fuente con el que se trabajara durante el ejercicio y luego, lo iremos comentando para que pueda entenderse y aplicarse.

## Código fuente:


```python
import requests
import time
import csv
import re
from bs4 import BeautifulSoup
import os
import pandas as pd
from termcolor import colored

resultados = []

req = requests.get("https://resultados.elpais.com")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup = BeautifulSoup(req.text, 'html.parser')

tags = soup.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)

req2 = requests.get("https://elpais.com/internacional")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup2 = BeautifulSoup(req2.text, 'html.parser')

tags = soup2.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)

req3 = requests.get("https://elpais.com/opinion")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup3 = BeautifulSoup(req3.text, 'html.parser')

tags = soup3.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)

req4 = requests.get("https://elpais.com/espana/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup4 = BeautifulSoup(req4.text, 'html.parser')

tags = soup4.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)

req5 = requests.get("https://elpais.com/economia/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup5 = BeautifulSoup(req5.text, 'html.parser')

tags = soup5.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)

req6 = requests.get("https://elpais.com/sociedad/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup6 = BeautifulSoup(req6.text, 'html.parser')

tags = soup6.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)

req7 = requests.get("https://elpais.com/educacion/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup7 = BeautifulSoup(req7.text, 'html.parser')

tags = soup7.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)

req8 = requests.get("https://elpais.com/clima-y-medio-ambiente/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup8 = BeautifulSoup(req8.text, 'html.parser')

tags = soup8.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)

req9 = requests.get("https://elpais.com/ciencia/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup9 = BeautifulSoup(req9.text, 'html.parser')

tags = soup9.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)

req10 = requests.get("https://elpais.com/cultura/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup10 = BeautifulSoup(req10.text, 'html.parser')

tags = soup10.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)

req11 = requests.get("https://elpais.com/babelia/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup11 = BeautifulSoup(req11.text, 'html.parser')

tags = soup11.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)

req12 = requests.get("https://elpais.com/deportes/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup12 = BeautifulSoup(req12.text, 'html.parser')

tags = soup12.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)

req13 = requests.get("https://elpais.com/tecnologia/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup13 = BeautifulSoup(req13.text, 'html.parser')

tags = soup13.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)

req14 = requests.get("https://elpais.com/tecnologia/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup14 = BeautifulSoup(req14.text, 'html.parser')

tags = soup14.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)

req15 = requests.get("https://elpais.com/gente/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup15 = BeautifulSoup(req15.text, 'html.parser')

tags = soup15.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)

req16 = requests.get("https://elpais.com/television/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup16 = BeautifulSoup(req16.text, 'html.parser')

tags = soup16.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)

req17 = requests.get("https://elpais.com/eps/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup17 = BeautifulSoup(req17.text, 'html.parser')

tags = soup17.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)


os.system("clear")

print(colored("A continuación se muestran los titulares de las páginas principales del diario El País que contienen las siguientes palabras:", 'blue', attrs=['bold']))
print(colored("Feminismo", 'green', attrs=['bold']))

str_match = [s for s in resultados if "feminismo" in s]
print("\n".join(str_match))

print(colored("Igualdad", 'green', attrs=['bold']))

str_match = [s for s in resultados if "igualdad" in s]
print("\n".join(str_match))

print(colored("Mujeres", 'green', attrs=['bold']))

str_match = [s for s in resultados if "mujeres" in s]
print("\n".join(str_match))

print(colored("Mujer", 'green', attrs=['bold']))

str_match = [s for s in resultados if "mujer" in s]
print("\n".join(str_match))

print(colored("Brecha salarial", 'green', attrs=['bold']))

str_match = [s for s in resultados if "brecha salarial" in s]
print("\n".join(str_match))

print(colored("Machismo", 'green', attrs=['bold']))

str_match = [s for s in resultados if "machismo" in s]
print("\n".join(str_match))

print(colored("Violencia", 'green', attrs=['bold']))

str_match = [s for s in resultados if "violencia" in s]
print("\n".join(str_match))

print(colored("Maltrato", 'green', attrs=['bold']))

str_match = [s for s in resultados if "maltrato" in s]
print("\n".join(str_match))

print(colored("Homicidio", 'green', attrs=['bold']))

str_match = [s for s in resultados if "homicidio" in s]
print("\n".join(str_match))

print(colored("Género", 'green', attrs=['bold']))

str_match = [s for s in resultados if "género" in s]
print("\n".join(str_match))

print(colored("Asesinato", 'green', attrs=['bold']))

str_match = [s for s in resultados if "asesinato" in s]
print("\n".join(str_match))

print(colored("Sexo", 'green', attrs=['bold']))

str_match = [s for s in resultados if "sexo" in s]
print("\n".join(str_match))

```

### luego, instalamos las librerías:


```python
pip install requests bs4 pandas termcolor
```

    Requirement already satisfied: requests in c:\users\angelica\anaconda3\lib\site-packages (2.28.1)
    Collecting bs4
      Downloading bs4-0.0.1.tar.gz (1.1 kB)
      Preparing metadata (setup.py): started
      Preparing metadata (setup.py): finished with status 'done'
    Requirement already satisfied: pandas in c:\users\angelica\anaconda3\lib\site-packages (1.4.4)
    Collecting termcolor
      Downloading termcolor-2.1.1-py3-none-any.whl (6.2 kB)
    Requirement already satisfied: charset-normalizer<3,>=2 in c:\users\angelica\anaconda3\lib\site-packages (from requests) (2.0.4)
    Requirement already satisfied: idna<4,>=2.5 in c:\users\angelica\anaconda3\lib\site-packages (from requests) (3.3)
    Requirement already satisfied: urllib3<1.27,>=1.21.1 in c:\users\angelica\anaconda3\lib\site-packages (from requests) (1.26.11)
    Requirement already satisfied: certifi>=2017.4.17 in c:\users\angelica\anaconda3\lib\site-packages (from requests) (2022.9.14)
    Requirement already satisfied: beautifulsoup4 in c:\users\angelica\anaconda3\lib\site-packages (from bs4) (4.11.1)
    Requirement already satisfied: numpy>=1.18.5 in c:\users\angelica\anaconda3\lib\site-packages (from pandas) (1.21.5)
    Requirement already satisfied: python-dateutil>=2.8.1 in c:\users\angelica\anaconda3\lib\site-packages (from pandas) (2.8.2)
    Requirement already satisfied: pytz>=2020.1 in c:\users\angelica\anaconda3\lib\site-packages (from pandas) (2022.1)
    Requirement already satisfied: six>=1.5 in c:\users\angelica\anaconda3\lib\site-packages (from python-dateutil>=2.8.1->pandas) (1.16.0)
    Requirement already satisfied: soupsieve>1.2 in c:\users\angelica\anaconda3\lib\site-packages (from beautifulsoup4->bs4) (2.3.1)
    Building wheels for collected packages: bs4
      Building wheel for bs4 (setup.py): started
      Building wheel for bs4 (setup.py): finished with status 'done'
      Created wheel for bs4: filename=bs4-0.0.1-py3-none-any.whl size=1257 sha256=71de9df0a3e0e1c2a21afa98a5a15644f355608dd12a556eab53e6a4df91015c
      Stored in directory: c:\users\angelica\appdata\local\pip\cache\wheels\73\2b\cb\099980278a0c9a3e57ff1a89875ec07bfa0b6fcbebb9a8cad3
    Successfully built bs4
    Installing collected packages: termcolor, bs4
    Successfully installed bs4-0.0.1 termcolor-2.1.1
    Note: you may need to restart the kernel to use updated packages.
    

### Ahora importamos las librerías internas:

Las librerías de Python son conjuntos de funciones que permiten realizar distintas funciones, ahorrando tiempo y esfuerzo al programador. Gracias a la amplia variedad de librerías existentes, Python es uno de los lenguajes más flexibles y potentes que pueden utilizar. Iniciamos con la explicación de las internas y luego, realizaremos las externas.

Con time podemos utilizar sus funciones manipular la fecha y hora:


```python
import time
```
posteriormente, usamos el formato para importar y exportar hojas de cálculo y bases de datos.

```python
import csv
```

Seguidamente, el código que proporciona operaciones de coincidencia de expresiones regulares similares o en cadena.


```python
import re
```

Avanzamos con la función que permite ver en python las funcionalidades del sistema operativo


```python
 import os
```

### A continuación procedemos a importar las librerías externas:

Iniciamos con termcolor, que sirve para imprimir mensajes de colores, es decir, el texto coloreado.


```python
from termcolor import colored
```

luego, avanzamos con la opción requests, que es una especie de biblioteca de python para trabajar con HTTP.


```python
import requests
```

Insertamos bs4, que es la librería que facilita extraer información de páginas web.


```python
from bs4 import BeautifulSoup
```

Seguidamente "Pandas", paquete de herramientas de análisis de datos de Python.


```python
import pandas as pd
```

### Es momento de poner los *objetos/variables

Se crea un objeto vacío denominado resultados en el que se añadirán los resultados del scrapping 


```python
resultados = []
```

Si pasamos a la función type() permite observar que es un objeto de tipo lista de python, lo que es básico y fundamental para organizar los datos.


```python
type (resultados)
```




    list



### solicitud de acceso a los datos de un sitio web


```python
Se agrega una variable para utilizar la solicitud req=requests.get
```


```python
req = requests.get("https://resultados.elpais.com")
```


```python
Después escribimos la función type() y esa es la respuesta de requests.
```


```python
type(req)
```




    requests.models.Response



Se utiliza el condicional if para que cuando el status no sea 200 el valor de regreso no pueda leerse. El valor 200 significa que la solicitud fue exitosa.


```python
# Si el estatus no es 200 no se puede leer la página
if (req.status_code != 200):
    raise Exception("No se puede hacer Web Scraping en"+ URL)
    
```

### Beautiful soup

Agregamos otra variable para aplicar el Web Scrapping


```python
soup = BeautifulSoup(req.text,'html.parser')
```

Ademas agregamos la variable que funciona para encontrar todas las etiquetas "h2" dentro de la página anteriormente especificada.


```python
tags = soup.findAll("h2")
```

Se indica a través de un for, que se encuentren todos los h2 dentro de la variable anterior y se imprima el texto dentro de la etiqueta. Luego con resultados.append(h2.text) se añaden todos los textos dentro de las etiquetas a la lista inicial resultados


```python
for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)
```

### Todo el proceso se repite en las diferentes categorías o secciones del medio de comunicación El País, es decir, el mismo código pero cambia según la sección *(Educación, económicas, internacional, deportes, opinión, etc)


```python
req2 = requests.get("https://elpais.com/internacional")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup2 = BeautifulSoup(req2.text, 'html.parser')

tags = soup2.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)

```

    Las protestas se extienden en China contra la política de covid cero
    Hartazgo, estragos económicos y accidentes mortales: claves para entender las protestas en China
    El último Iphone, perfumes de Chanel o un Rolex: las marcas occidentales llenan los escaparates rusos pese a las sanciones
    Publicar no es un delito
    La vida bajo los bombardeos rusos
    Democracias a la defensiva
    La UE vista desde el G-20 de Bali 
    El arte ruso de la provocación
    China y Estados Unidos, condenadas a entenderse y a rivalizar
    Lecciones en Ucrania para ser reportero de guerra: explosiones de fogueo, torniquetes y campos de minas
    De la manifestación al patíbulo: el régimen iraní amenaza con la horca para sofocar las protestas
    Publicar no es un delito
    Los medios de los cables de WikiLeaks piden a EE UU que no persiga a Assange
    La gestión del frío enfrenta a Zelenski y al alcalde de Kiev
    El sueño hecho realidad del refugiado sirio del selfi con Merkel
    Los trabajadores migrantes de provincias en China estallan contra los confinamientos por covid
    Sobrevivir bajo cero en Ucrania
    La UE teme que los ataques rusos contra la red eléctrica de Ucrania fuercen otra oleada de refugiados
    Encuentran el cadáver de una niña desaparecida en el corrimiento de tierra en la isla italiana de Ischia
    Justin Trudeau justifica el uso de la Ley de emergencia para desalojar a los camioneros antivacunas
    La nota del autor de la matanza del Walmart de Virginia: “Se reían de mí y decían que era un asesino en serie”
    La pobreza se ceba con los menores de 18 años en América Latina
    Tres horas libres en el trabajo para ver el partido… ¡Bienvenidos a Brasil!
    Petro y López Obrador estrenan un eje latinoamericano con el éxito de la negociación de Venezuela como trasfondo
    

### En este apartado dedicamos espacio para los titulares con las palabras más buscadas

En esta parte usaremos os.system(clear) para se haga una limpieza después de realizar el web scrapping.


```python
os.system("clear")
```

A continuación se mostrarán los títulares en negrita (stilo) con la siguiente función

De la misma manera se utilizará la función "for" para verificar que contenga la palabra clave:


```python
print(colored("A continuación se muestran los titulares de las páginas principales del diario El País que contienen las siguientes palabras:", 'blue', attrs=['bold']))
print(colored("Feminismo", 'green', attrs=['bold']))
```

Ahora se repite el mismo procedimiento con las demás palabras clave en el resto de las secciones:


```python

```


```python
print(colored("A continuación se muestran los titulares de las páginas principales del diario El País que contienen las siguientes palabras:", 'blue', attrs=['bold']))
print(colored("Feminismo", 'green', attrs=['bold']))

str_match = [s for s in resultados if "feminismo" in s]
print("\n".join(str_match))

print(colored("Igualdad", 'green', attrs=['bold']))

str_match = [s for s in resultados if "igualdad" in s]
print("\n".join(str_match))

print(colored("Mujeres", 'green', attrs=['bold']))

str_match = [s for s in resultados if "mujeres" in s]
print("\n".join(str_match))

print(colored("Mujer", 'green', attrs=['bold']))

str_match = [s for s in resultados if "mujer" in s]
print("\n".join(str_match))

print(colored("Brecha salarial", 'green', attrs=['bold']))

str_match = [s for s in resultados if "brecha salarial" in s]
print("\n".join(str_match))

print(colored("Machismo", 'green', attrs=['bold']))

str_match = [s for s in resultados if "machismo" in s]
print("\n".join(str_match))

print(colored("Violencia", 'green', attrs=['bold']))

str_match = [s for s in resultados if "violencia" in s]
print("\n".join(str_match))

print(colored("Maltrato", 'green', attrs=['bold']))

str_match = [s for s in resultados if "maltrato" in s]
print("\n".join(str_match))

print(colored("Homicidio", 'green', attrs=['bold']))

str_match = [s for s in resultados if "homicidio" in s]
print("\n".join(str_match))

print(colored("Género", 'green', attrs=['bold']))

str_match = [s for s in resultados if "género" in s]
print("\n".join(str_match))

print(colored("Asesinato", 'green', attrs=['bold']))

str_match = [s for s in resultados if "asesinato" in s]
print("\n".join(str_match))

print(colored("Sexo", 'green', attrs=['bold']))

str_match = [s for s in resultados if "sexo" in s]
print("\n".join(str_match))
```

### conclusiones: Este ejercicio en el que se conjuga las tres herramientas estudiadas permite agilizar todos los procesos de una página web a la hora en que necesitamos extraer datos o información muy específica que necesitemos. Agiliza no solo en tiempos, sino también en trabajo ya que a través de los códigos trabajados, relacionados y ejecutados adecuadamente podremos tener resultados casi que al instante y sin mayores complicaciones. Es una herramienta súper útil para la programación y este conjunto de elementos permitirán al periodista ir un paso adelante.
