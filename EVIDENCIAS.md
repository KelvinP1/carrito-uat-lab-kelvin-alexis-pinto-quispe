# EVIDENCIAS – Pruebas de Aceptación de Usuario (UAT)

Este documento contiene las evidencias solicitadas en el laboratorio N°16 del curso “Construcción y Pruebas de Software”, correspondientes al módulo de carrito de compras implementado con Java, Maven y JUnit 5.

---

## 1. Ejecución de pruebas (JUnit)

Las pruebas UAT se ejecutaron utilizando Maven mediante el comando:

mvn test

T E S T S
Running com.ejemplo.model.ShoppingCartTest
Tests run: 4, Failures: 0, Errors: 0, Skipped: 0
BUILD SUCCESS

Total time: 1.8 s
Finished at: 2025-12-04


### Resultado:
- ✔ Todas las pruebas pasaron exitosamente.
- ✔ No hubo fallos ni errores.
- ✔ El comportamiento cumple con las historias de usuario y los criterios de aceptación.

---

## 2. Resumen de casos probados

### **CA-01 – Agregar producto**
- Carrito vacío → agregar A x1  
- ✔ Ítems: 1  
- ✔ Total: 10.0  

### **CA-02 – Actualizar cantidad**
- Carrito con A x1 → actualizar a x3  
- ✔ Ítems: 3  
- ✔ Total: 30.0  

### **CA-03 – Eliminar producto**
- Eliminar A  
- ✔ Carrito vacío  

### **CA-05 – Producto inexistente**
- Intento de eliminar “X”  
- ✔ Excepción esperada: “El producto no está en el carrito”

---

## 3. Validación de funcionalidades clave

Se verificó correctamente:

- Agregar productos  
- Sumar cantidades  
- Calcular totales  
- Actualizar cantidades  
- Eliminar productos  
- Vaciar carrito  
- Manejo de errores por acciones inválidas  

Todas las funcionalidades cumplen con las expectativas del usuario final en una tienda online.

---

## 4. Reflexión final

Las pruebas de aceptación de usuario (UAT) permitieron validar comportamientos completos del sistema desde la perspectiva del usuario.  
A diferencia de las pruebas unitarias, una UAT verifica flujos completos como agregar productos, modificar cantidades o eliminar ítems, asegurando que el módulo funcione como espera un usuario real.

Si estas funcionalidades fallaran en producción, podrían provocar errores en los montos finales, productos incorrectos en pedidos, problemas de facturación y mala experiencia del cliente.  
Este laboratorio refuerza el valor de definir criterios de aceptación claros y automatizar pruebas para garantizar calidad funcional antes del despliegue.

---

## 5. Checklist del laboratorio

- [x] Proyecto Java (Maven) creado correctamente  
- [x] Dependencias JUnit configuradas en `pom.xml`  
- [x] Clases `Product`, `CartItem` y `ShoppingCart` implementadas  
- [x] Historias de usuario y criterios de aceptación documentados  
- [x] Tabla de casos de prueba completada  
- [x] Pruebas de aceptación implementadas en JUnit  
- [x] Ejecución de pruebas exitosa  
- [x] Evidencias documentadas en este archivo  