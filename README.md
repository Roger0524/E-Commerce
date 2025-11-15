# 📦 Sistema de Almacenamiento y Consultas en MongoDB para un Catálogo E-commerce

## 📘 Descripción General
Este proyecto implementa un sistema de almacenamiento y consulta de datos en **MongoDB** basado en un caso de estudio de comercio electrónico. El proposito principal es diseñar, crear y consultar una base de datos documental denominada **e-commerce_db**, organizada en tres colecciones fundamentales: **productos**, **clientes** y **pedidos**.  
Los documentos fueron generados para simular escenarios reales de inventarios, usuarios y transacciones. A partir de este modelo, se ejecutan operaciones CRUD, consultas con filtros y pipelines de agregación que permiten analizar precios, inventario, ventas y comportamiento básico del sistema.

El proyecto sigue lineamientos sobre almacenamiento y consultas de datos en entornos NoSQL, estructurando una solución funcional, replicable y coherente con los principios del modelo documental de MongoDB.

---

## ⚙️ Tecnologías Utilizadas
- **MongoDB Community Server** (motor NoSQL)
- **MongoDB Compass** (herramienta GUI)
- **JSON** (formato de documentos creados para la base)

---

## 💾 Conjunto de Datos
La estructura representa un sistema básico de comercio electrónico.

- **Formato:** JSON  
- **Colecciones y cantidad de documentos:**
  - `productos` → **100** documentos (inventario)
  - `clientes` → **30** documentos (usuarios)
  - `pedidos` → **30** documentos (órdenes)
- **Total:** **160 documentos**

### Variables principales:

🔹 **Productos:**  
`sku`, `nombre`, `categoria`, `precio`, `cantidad`, `fecha_registro`.

🔹 **Clientes:**  
`usuario`, `telefono`, `email`, `pais`.

🔹 **Pedidos:**  
`cliente_id`, `lista_productos`, `valor_total`, `fecha_pedido`, `estado`, `direccion_envio`, `metodo_pago`.

---

## 🛠️ Modelado de la Base de Datos
La base de datos **e-commerce_db** está diseñada bajo el modelo documental de MongoDB, permitiendo almacenar información semiestructurada con flexibilidad para crecer o modificarse sin migraciones complejas.

### ✔️ Colecciones definidas:
1. **productos**  
2. **clientes**  
3. **pedidos**

Cada colección contiene documentos con identificadores únicos (`ObjectId`), tipos de datos consistentes y estructuras coherentes al contexto de un catálogo de comercio electrónico.

El diagrama del esquema se encuentra en:  
➡️ `/imagenes/esquema_bd.png`

---

## 🚀 Implementación en MongoDB Compass

### 🔹 1. Creación de la base de datos
1. Abrir MongoDB Compass  
2. Click en **Create Database**  
3. Nombre: `e-commerce_db`  
4. Primera colección: `productos`

### 🔹 2. Importación de documentos
Los archivos JSON se encuentran en la carpeta `/dataset`.

Procedimiento:
1. Ingresar a la colección **productos** → **Import Data** → seleccionar `productos.json`  
2. Repetir para:
   - `clientes.json`
   - `pedidos.json`

---

## 📂 Consultas Implementadas
Las consultas están organizadas de forma modular en `/consultas` y son completamente ejecutables en MongoDB Compass:

### ✔️ Consultas básicas (CRUD)
Inserción, selección, actualización y eliminación.  
**Archivo:** `consultas_basicas.md`

### ✔️ Consultas con filtros y operadores
Uso de operadores como `$gt`, `$lt`, `$regex`, `$and`, `$or`.  
**Archivo:** `consultas_filtros.md`

### ✔️ Consultas de agregación
Pipelines para:
- Contar documentos  
- Sumar valores  
- Calcular promedios  
- Analizar inventario  
**Archivo:** `consultas_agregacion.md`

---
