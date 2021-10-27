# datos-tesina-2021
## Datos del clima, de la producción y del forraje.

1. Datos del clima extraidos de: http://sipas.inta.gob.ar/?q=agrometeorologia-listado-estaciones. 
2. Datos de producción proporcionados por el dueño del campo.
3. Datos del forraje proporcionados por Diego.


## Datos

*Sonda de Trelew*:
- id: Trelew [ Vantage Pro2 ] 
- Latitud / Longitud / altura:	43.16.21 / 65.21.42 / 13 msnm

1. datos_climaticos_anuales_35.csv: Son los promedios anuales de la sonda de Trelew:
    - fecha, el ultimo día del año ya que es el promedio anual
    - temp_media,
    - temp_min,
    - tem_max,
    - humedad,
    - cant_lluvia,
    - rad_solar,
    - vel_viento 
    - acumulado_anual: lluvia acumulada durante el año
    - acumulado_verano: lluvia acumulada durante el verano
2. datos_produccion_anual_35.csv: Son los datos de produccion anuales de un campo.
    - fecha, el ultimo día del año ya que son los datos anuales
    - esquila, cantidad de animales (ovejas, carneros, borregos, etc) esquilados (temporada de esquila)
    - ovejas, cantidad de ovejas que fueron madres (temporada de paricion)
    - corderos, cantidad de corderos nacidos (temporada de paricion)
    - kilos_lana, cantidad de lana esquilada (temporada de esquila)
    - rinde_seco, mientras mas alto el valor mejor la lana
    - finura, mientras mas bajo el valor mejor la lana
    - kilo_lana_p/animal, (temporada de esquila)
    - porcentaje_paricion (temporada de paricion)
3. datos_produccion_clima_35.csv: es una combinacion de los datasets anteriores
3. datos_produccion_clima_35_1.csv: es una combinacion de los datasets anteriores pero con valores promedios para completar aquellos que son cero.
4. datos_forraje.csv: Son los datos del forraje de dos años
    - fecha
    - gps:
        - CG es gastre, 
        - CT es telsen, 
        - CPI es paso de indio, 
        - CM Mártires
    - coordenada completa
    - latitud del punto
    - longitud del punto
    - valor pastoral
5. datos_forraje_3_sondas.csv: es una combinacion del dataset anterior con algunas variablesmas, que son:
    - dist_laguna_fría: una sonda del inta
    - distancia_telsen: una sonda del inta
    - dist_gastre: una sonda del inta
    - sonda_cercana: una de las 3 anteriores
    - acum_anual: acumulado de lluvia anual de la sonda cercana
    - acum_verano: acumulado de lluva en el verano de la sonda cercana
**Observacion: Este Dataset solo toma 200 puntos del 400, y la sonda de Gastre no tenia datos, asi que se usaron los de Laguna Fría**

## Cuadernos de Jupyter

1. Analizando datos: Miramos un poco la forma de los datos y tratamos de ver si hay variables correlacionadas. Trabajamos con datos_produccion_clima_35.csv y datos_produccion_clima_35_1.csv.
2. Regresión Lineal: Miramos si los datos funcionan bien con una regresion lineal simple. Trabajamos con datos_produccion_clima_35_1.csv.
3. Pronostico 1985- 2019 Corderos: Usamos el modelo ARIMA para interntar predecir la cantidad de corderos que van a nacer. Trabajamos con datos_produccion_clima_35.csv.
4. Pronostico 1985- 2019 Lana: Usamos el modelo ARIMA para interntar predecir la cantidad de lana que se va obtener. Trabajamos con datos_produccion_clima_35.csv.
5. Análisis Forraje: Miramos si los datos funcionan bien con una regresion lineal simṕle. Trabajamos con datos_forraje_3_sondas.csv.