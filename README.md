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
4. datos_forraje.csv:
    - CG es gastre, 
    - CT es telsen, 
    - CPI es paso de indio, 
    - CM Mártires


## Cuadernos de Jupyter

1. Analizando datos: Miramos un poco la forma de los datos y tratamos de ver si hay variables correlacionadas. Trabajamos con datos_produccion_clima_35.csv.
2. Regresión Lineal: Miramos si los datos funcionan bien con una regresion lineal. Trabajamos con datos_produccion_clima_35.csv.