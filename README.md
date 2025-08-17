# Predicción de Precio de Autos Usados en Alemania

Este proyecto tiene como objetivo **predecir el precio (`price`) de un auto usado** en Alemania a partir de sus características principales, como el año de matriculación (`yearOfRegistration`), kilometraje (`kilometer`), potencia (`powerPS`), marca (`brand`) y otros atributos del vehículo.

Se exploran distintos enfoques de **Machine Learning para regresión**, incluyendo:

* **Regresión lineal:** un modelo simple que sirve como baseline.
* **Random Forest Regressor:** capaz de capturar relaciones no lineales y manejar variables categóricas de manera efectiva.
* **Gradient Boosting / XGBoost / LightGBM:** modelos avanzados para datasets tabulares con alto rendimiento.

Se aplican técnicas de **feature engineering**, como calcular la antigüedad del auto (`antigüedad = 2025 − yearOfRegistration`) y codificar variables categóricas (`brand`, `vehicleType`, `gearbox`) mediante **OneHotEncoder** o **Target Encoding**, para optimizar el desempeño de los modelos.

El proyecto permite realizar un análisis completo del dataset, incluyendo limpieza, exploración, visualización de datos y evaluación de modelos predictivos.

## Descripción del Dataset

| Columna               | Descripción                                                                         |
| --------------------- | ----------------------------------------------------------------------------------- |
| `index`               | Índice de la fila (quedó como columna porque el CSV lo traía así).                  |
| `dateCrawled`         | Fecha y hora en que el anuncio fue recopilado de la web.                            |
| `name`                | Título del anuncio (ej. modelo y versión del auto).                                 |
| `seller`              | Tipo de vendedor (`privat` = particular, `gewerblich` = concesionario).             |
| `offerType`           | Tipo de oferta (casi siempre `Angebot` = oferta, puede aparecer `Gesuch` = pedido). |
| `price`               | Precio del auto en euros.                                                           |
| `abtest`              | Indicador de test A/B en la plataforma (`test`, `control`).                         |
| `vehicleType`         | Tipo de vehículo (`limousine`, `coupe`, `suv`, `kleinwagen` = compacto, etc.).      |
| `yearOfRegistration`  | Año de matriculación del auto.                                                      |
| `gearbox`             | Tipo de transmisión (`manuell` = manual, `automatik` = automática).                 |
| `powerPS`             | Potencia del motor en caballos de fuerza (PS = Pferdestärke).                       |
| `model`               | Modelo del vehículo (ej. `golf`, `a3`, `passat`).                                   |
| `kilometer`           | Kilometraje en kilómetros.                                                          |
| `monthOfRegistration` | Mes de matriculación del auto.                                                      |
| `fuelType`            | Tipo de combustible (`benzin` = nafta, `diesel`, `lpg`, `cng`, etc.).               |
| `brand`               | Marca del auto (`audi`, `bmw`, `volkswagen`, etc.).                                 |
| `notRepairedDamage`   | Indica si el auto tiene daños no reparados (`ja` = sí, `nein` = no).                |
| `dateCreated`         | Fecha de creación del anuncio en la plataforma.                                     |
| `nrOfPictures`        | Número de fotos en el anuncio (suele ser 0).                                        |
| `postalCode`          | Código postal del lugar donde se publicó el auto.                                   |
| `lastSeen`            | Última fecha en que el anuncio estuvo activo en la web.                             |
