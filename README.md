# Proyecto-clasificacion-y-conteo
## Clasificacion y conteo de frutos secos

Elaborado como parte del proyecto final de fin de Master de Inteligencia artificial & Big Data

## Software - Recursos
  Python
  YOLO26 (ULTRALYTICS S.F.)
  LabelImg
  Google Colab

## Detalles

- Entrenamiento en condiciones iniciales de instalacion con cantidad de fotos limitadas.

- Seleccion del modelo: YOLO26

- En el proceso ETL para optimizar la muestra de entrenamiento
    > Balance de categorias
    > Cantidades variables
    > En todo el campo visual
    > Todas las orientaciones posibles
    > Control de iluminacion
    > Background constante
     
-> Optimizacion de parametros de entrenamiento
  > Tasa de entrenamiento
  > Augmentation en entrenamiento
  > Distintos niveles de Dropout

-> Grid search sobre parametros de inerencia

-> Evaluacion en base a las siguientes metricas:
 
    > mAp50
    > mAp50-95
    > Precision
    > Recall
    > RMSE
    > % de aciertos por categoria

-> Calculo de incertidumbre por categoria
  -> Test time augmentation
  -> Deep ensembles  sobre 5 modelos entrenados con los mejores parameteros pero con semillas distintas
  -> No se utilizo MC dropout dado que las mejores metricas se consiguieron sin dropout en entrenamiento por lo cual no hay variacion para aplicarlo en el modelo. 
  -> Comparativo de las metodologias en cuanto a latencia de inferencia
    
- Incorporacion de nuevas categorias
  > Consideraciones de composicion de las nuevas imagenes
  > Entrenamiento a partir del modelo inicial entrenado (reentrenamiento)
    > Verificacion de parametros de entrenamiento y distintos niveles de dropout.
    > Evaluacion en base a las mismas metricas del entrenamiento inicial.
  > Verificacion contra el set de val del entrenamiento anterior para verificar que no haya "degradacion de conocimiento"

## Imagenes de ejemplo


## Resultados 

## Conclusiones

link al PFM:




