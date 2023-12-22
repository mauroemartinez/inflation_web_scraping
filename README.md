# 🤖 Web Scraping y Visualización de la Inflación Argentina
Este proyecto utiliza Python para extraer datos de la inflación mensual de Argentina desde la página web del Banco Central de la República Argentina (BCRA), y luego los visualiza con gráficos de matplotlib y seaborn.

## 📚 Importación de librerías
Las librerías utilizadas son las siguientes:

- **time** y **datetime**: para manejar el tiempo y las fechas.
- **pandas** y **numpy**: para manipular los datos y realizar cálculos.
- **selenium**: para realizar el web scraping con un navegador automatizado.
- **matplotlib** y **seaborn**: para crear los gráficos de la inflación.

## 🤖 Web Scraping
El proceso de web scraping consiste en los siguientes pasos:

- Abrir un navegador Chrome en modo headless (sin interfaz gráfica) con las opciones adecuadas.
- Acceder a la página web del BCRA y hacer clic en el enlace de la inflación mensual.
- Obtener los valores mínimos y máximos de las fechas disponibles para filtrar los datos.
- Hacer clic en el botón de consultar y esperar a que se cargue la tabla con los datos.
- Extraer el contenido HTML de la tabla y cerrar el navegador.
- Convertir el HTML en un dataframe de pandas, ajustando el formato de los números y las fechas.

# 📊 Manipulación
- Se convierte la columna “Fecha” en el índice del dataframe, y se cambia el formato a mes-año (por ejemplo, Ene-21).
- Se calcula la inflación acumulada como el producto de los valores mensuales más uno.

📈 Visualización
- Un gráfico de barras que muestra la inflación mensual. Veremos también una advertencia sobre su lectura.
- Un gráfico de líneas que muestra la inflación acumulada, con una escala lineal que refleja el crecimiento exponencial de los precios.
- Un gráfico de líneas que muestra la inflación acumulada, con una escala logarítmica que suaviza el crecimiento y facilita la comparación de los periodos.
