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
Se crearon respuestas falsas y el modelo
debe diferenciar si es un compra real o no  
El csv orders continene un valor en 'eval_set' llamado test  
Estas órdenes eran las que debían ser predichas en la competencia original  
Ya que no tenemos el ground truth (los productos de cada orden test),
se utilizan las órdenes de train y se hace un split

### Resultados
Se obtuvo más del 80% en la métrica Normalized Discounted Cumulative Gain (NDCG)
