# Pruebas de API con Postman y Newman: Petstore

Colección de Postman para probar el ciclo de vida de un usuario en la API pública Petstore (`https://petstore.swagger.io/v2`): creación, consulta, actualización, verificación, eliminación y consulta final.

## Requisitos

- Node.js (con npm).
- Newman 6.
- `newman-reporter-htmlextra` 1.23.1.

## Ejecución

Desde esta carpeta, ejecutar:

```sh
npx newman run "Tienda de mascotas.postman_collection.json" -r cli,htmlextra --reporter-htmlextra-export reports/informe.html
```

## Tests y resultados reales

Resultado de la ejecución real: **6 peticiones, 23 tests, 23 pasaron y 0 fallaron**.

| Petición | Test | Resultado |
|---|---|---|
| Crear usuario | Estado HTTP 200 | Pasó |
| Crear usuario | Tiempo de respuesta menor de 2000 ms | Pasó |
| Crear usuario | Content-Type JSON cuando hay cuerpo | Pasó |
| Crear usuario | La respuesta contiene code 200 | Pasó |
| Traer usuario | Estado HTTP 200 | Pasó |
| Traer usuario | Tiempo de respuesta menor de 2000 ms | Pasó |
| Traer usuario | Content-Type JSON cuando hay cuerpo | Pasó |
| Traer usuario | El username coincide con la variable | Pasó |
| Actualizar datos usuario | Estado HTTP 200 | Pasó |
| Actualizar datos usuario | Tiempo de respuesta menor de 2000 ms | Pasó |
| Actualizar datos usuario | Content-Type JSON cuando hay cuerpo | Pasó |
| Traer usuario (verificar cambio) | Estado HTTP 200 | Pasó |
| Traer usuario (verificar cambio) | Tiempo de respuesta menor de 2000 ms | Pasó |
| Traer usuario (verificar cambio) | Content-Type JSON cuando hay cuerpo | Pasó |
| Traer usuario (verificar cambio) | El username coincide con la variable | Pasó |
| Traer usuario (verificar cambio) | El lastName actualizado es villa | Pasó |
| Traer usuario (verificar cambio) | El email actualizado es villa@gmail.com | Pasó |
| Borrar usuario | Estado HTTP 200 | Pasó |
| Borrar usuario | Tiempo de respuesta menor de 2000 ms | Pasó |
| Borrar usuario | Content-Type JSON cuando hay cuerpo | Pasó |
| Traer usuario (esperar 404) | Estado HTTP 404 | Pasó |
| Traer usuario (esperar 404) | Tiempo de respuesta menor de 2000 ms | Pasó |
| Traer usuario (esperar 404) | Content-Type JSON cuando hay cuerpo | Pasó |
