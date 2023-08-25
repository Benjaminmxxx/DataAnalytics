# Análisis de datos del mercado de criptomonedas & Top 2 compañías de Tecnología

Brindando el servicio de "Analista de Datos" a una empresa de servicios financieros interesada en el mercado de criptomonedas por su crecimiento exponencial se realiza un análisis exhaustivo entre el mercado de las criptomonedas y dos de las mayores empresas de tecnología en el mundo (Apple Inc. & Microsoft Corporation).
Para la obtención de los datos se usaron las API's CoinGecko y Yahoo Finance.

Debido a que la fuente de información contiene más de 4000 monedas, se decidió usar el top 1 Layer 1 (se refiere a la capa base de una blockchain, donde se construye la estructura fundamental de la criptomoneda) de las principales categorías de criptomonedas según su capitalización de mercado.  
De ahí se escogieron las siguientes 10 monedas con mayor capitalización y datos de un año histórico:

['bitcoin', 'ethereum', 'binancecoin', 'cardano', 'solana', 'polkadot', 'avalanche-2', 'cosmos', 'hedera-hashgraph', 'bitcoin-cash']

(A) ETL:

Después de realizar el ETL (Extraer, Transformar, Cargar) de los datos se obtuvieron dos archivos 'csv': 

1.- "DataCriptos" conformado por datos de 364 días (2022-08-21 a 2023-08-19) dentro los que se encuentran: Cripto: diferentes criptomonedas, prices2: precio de la cripto,   market_caps2: capitalización de mercado, total_volumes2: volumen del mercado, precios de Apertura, alto, bajo y cierre; ratio del cuerpo de la vela que nos proporciona información sobre la fortaleza de una tendencia y el retorno diario que es un porcentaje de retorno respecto al precio del día anterior.

2.- "DataTec" conformado por datos de 362 días del (2022-08-22 to 2023-08-18) dentro de los cuales se encuentran: Company: las dos compañías, precios de Apertura, alto, bajo y cierre, volume: volumen de mercado, ratio del cuerpo y retorno diario.
 
(B) EDA:

Outliers:

Dado el comportamiento de una criptomoneda es fundamental aclarar que lo que puede parecer un Outlier, puede ser un valor real y la naturaleza de los datos nos puede indicar diferentes fechas de interés. 
**Ejemplo:Outliers en Criptos**
![Precios](/Graficas/Precios.png)

Market Cap: 

Es importante contextualizar el crecimiento de las criptomonedas y su volatilidad como se muestra a continuación:

![MarketCap](/Graficas/MarketCapCriptos.png)

También se cruzaron algunos datos en el análisis como fue el Volumen de Mercado que nos permite distinguir tendencias entre ambos mercados a pesar de la diferencia en dimensión: 

![VolumenMercado](/Graficas/VolumenTotalMercCrip.png)
![VolumenMercado2](/Graficas/VolumenTotalMercadoTec.png)

Analizando mas las variables a partir de los diferentes precios se tienen el ratio de cuerpo, que permitió realizar una clasificación sobre la tendencia que se pervive para las criptomonedas y las compañías, ejemplo:

![Tendencias](/Graficas/Tendencias.png)

Finalmente se analizo el porcentaje de retornos diarios que se calculo,que nos puede decir cuantos datos están por debajo de tener algún retorno a lo largo del año, entre otras cosas, ejemplo:

![RetornosApple](/Graficas/RetornosDiarios.png)
![RetornosMicro](/Graficas/RetornosDiariosMicros.png)

Después de realizar todo el EDA se encontraron relaciones interesantes entre diferentes variables por lo que se dispuso hacer un Dashboard en donde se presentan, cruces de variables entre cada una de las criptomonedas y las compañías analizadas.

Pudiendo sugerir 3 KPI's relacionados con dichos cruces de datos: 

1.- Diferencia de Volumen del mercado entre una criptomoneda y una compañía en un periodo de tiempo estipulado: puede proporcionarte información valiosa sobre la actividad y el interés en ambos activos financieros dependiendo el análisis. 

2.-Balance de Retorno de una compañía seleccionada y una criptomoneda en un periodo de tiempo estipulado: puedes obtener información sobre el rendimiento relativo de ambos activos financieros y cómo han generado ganancias o pérdidas en ese período.

3.-Indicador de Trading: Nos muestra el precio promedio de una criptomoneda en un periodo de tiempo, para el mismo tiempo nos muestra el precio mas bajo y el mas alto, obteniendo así un indicador sobre la posible ganancia obtenida en ese lapso, tomando las mejores decisiones.

A continuación se muestra uno de los gráficos que acompañan a nuestros KPI's:

![Parametros](/Graficas/Parametros.png)
![VolumeCripto_Tec](/Graficas/VolumenMercado.png)

