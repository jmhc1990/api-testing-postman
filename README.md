<div align="center">

# 🐾 Pruebas de API con Postman y Newman

### Petstore · Automatización de pruebas para una API REST

[![Postman](https://img.shields.io/badge/Postman-Collection-orange?logo=postman&logoColor=white)](Tienda%20de%20mascotas.postman_collection.json)
[![Newman](https://img.shields.io/badge/Newman-6-6A4C93)](https://www.npmjs.com/package/newman)
[![Resultado](https://img.shields.io/badge/Tests-23%20aprobados-brightgreen)](#-resultado-de-la-ejecución)

**Práctica de API testing realizada con Postman y ejecutada desde la terminal con Newman.**

[Colección](Tienda%20de%20mascotas.postman_collection.json) · [Informe HTML](reports/informe.html)

</div>

---

## 📌 Sobre el proyecto

La colección verifica el ciclo de vida de un usuario en la API pública [Swagger Petstore](https://petstore.swagger.io/): crea un usuario, consulta sus datos, los actualiza y comprueba su eliminación.

El objetivo de esta práctica es aplicar comprobaciones funcionales y de respuesta HTTP, y poder ejecutar la colección fuera de Postman mediante Newman.

## ✅ Qué se comprueba

| Operación | Comprobaciones principales |
|---|---|
| Crear usuario | Estado HTTP, código de respuesta, tipo de contenido y tiempo de respuesta |
| Consultar usuario | Estado HTTP, tipo de contenido, tiempo de respuesta y username |
| Actualizar usuario | Estado HTTP, tipo de contenido y tiempo de respuesta |
| Verificar actualización | Datos actualizados del usuario, estado HTTP, tipo de contenido y tiempo de respuesta |
| Eliminar usuario | Estado HTTP, tipo de contenido y tiempo de respuesta |
| Confirmar eliminación | Respuesta `404`, tipo de contenido y tiempo de respuesta |

Las comprobaciones de tiempo esperan una respuesta inferior a **2000 ms**.

## 🧰 Herramientas

- **Postman** — diseño y exportación de la colección.
- **Newman 6** — ejecución de la colección desde la línea de comandos.
- **htmlextra** — generación de un informe HTML de la ejecución.
- **Swagger Petstore** — API pública bajo prueba.

## 🚀 Cómo ejecutarlo

Necesitas [Node.js y npm](https://nodejs.org/). Desde la raíz del repositorio:

1. Instala las dependencias del informe:

   ```bash
   npm install
   ```

2. Ejecuta la colección y genera el informe:

   ```bash
   npx newman@6 run "Tienda de mascotas.postman_collection.json" -r cli,htmlextra --reporter-htmlextra-export reports/informe.html
   ```

El resultado detallado queda disponible en [`reports/informe.html`](reports/informe.html).

## 📊 Resultado de la ejecución

En la última ejecución verificada:

| Métrica | Resultado |
|---|---:|
| Peticiones ejecutadas | 6 |
| Tests/assertions ejecutados | 23 |
| Aprobados | 23 |
| Fallidos | 0 |

> Petstore es un servicio público; su disponibilidad y sus tiempos de respuesta pueden variar entre ejecuciones.

## 📁 Contenido

```text
├── Tienda de mascotas.postman_collection.json
├── reports/
│   └── informe.html
├── package.json
├── package-lock.json
└── README.md
```

---

<div align="center">

Proyecto de práctica · API Testing · Postman + Newman

</div>
