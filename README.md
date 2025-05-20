# Prediccion_Instacart
## Link del dataset
https://www.kaggle.com/datasets/psparks/instacart-market-basket-analysis/data

## Diccionario del datasest
asiles: que productos se encuentran en cada pasillo  
departments: a que departamento pertenece cada producto  
products: la lista entera de productos  
order_products__prior: la lista de órdenes pasadas  
order_products__train: la lista de órdenes más recientes  
orders: características de todas las órdenes  

## Resumen del proyecto
Se utilizan los patrones de las órdenes pasadas y se comparan a las órdenes del presente 
para predecir el product que será ordenado por cada usuario  
Es una clasificación binaria así que se crearon respuestas falsas y el modelo
debe diferenciar si es un compra real o no  
El csv orders continene un valor en 'eval_set' llamado test  
Estas órdenes eran las que debían ser predichas en la competencia original  
Ya que no tenemos el ground truth (los productos de cada orden test),
se utilizan las órdenes de train y se hace un split

### Resultados
Se obtuvo más del 90% en las 5 métricas evaluadas  
Accuracy: 0.9673828191290772 - el modelo predijo correctamente 96% de las veces (positivos y negativos)  
Precision: 0.9854411014788373 - 98% de las veces que el modelo predijo una venta, era cierta (positivos)  
Recall: 0.966225 - se detectaron 96% de las ventas reales (positivos)  
F1 Score: 0.9757384498863924 - La armonía entre precisión y recall, cuantas de las  
ventas fueron predichas, y cuantas de las predicciones de una venta eran reales  
ROC AUC: 0.9937981295572228 - La capacidad del modelo de distinguir entre una venta falsa y una verdadera
