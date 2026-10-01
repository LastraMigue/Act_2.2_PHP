# Actividad 2.2 PHP - Prueba de Concepto (PoC)

## Introducción

Para afianzar los conceptos fundamentales de sintaxis, variables, operadores y ámbitos de PHP, se ha desarrollado una Prueba de Concepto (PoC) que demuestra la generación dinámica de contenido en el servidor y su posterior interacción en el cliente a través de bloques embebidos en JavaScript. 

Todo el desarrollo se encuentra unificado en un único archivo ejecutado obligatoriamente a través del servidor web local (Apache mediante XAMPP).

## Proyecto

* **[index.php](./index.php)**

---

# UT2: Fundamentos de PHP — PoC Dinámica

## Justificación Técnica (Conceptos Clave)

* **Ciclo de Vida (Backend vs. Frontend):** PHP procesa el código en el servidor y envía solo HTML/JS plano al cliente. La función en JavaScript se ejecuta exclusivamente en el navegador sin recargar la página.
* **Directivas de Errores:** `E_ALL` y `display_errors` facilitan la depuración en **desarrollo**. En **producción** se desactivan para evitar fugas de información sensible (XSS/rutas del servidor).
* **Control de Ámbitos (Scope):** Las funciones en PHP tienen ámbito aislado. Se utiliza la palabra reservada `global` para acceder y modificar las variables declaradas fuera de la función.
* **Inyección en JS & Type Juggling:** PHP convierte implícitamente los enteros a cadena al imprimirlos dentro del script. Envolver el bloque en comillas previene errores de sintaxis en el navegador.
* **Sintaxis y Seguridad:** `<?= ... ?>` reemplaza de forma limpia a `<?php echo ... ?>`. El uso de `htmlspecialchars()` sanitiza caracteres especiales previniendo ataques de inyección (XSS).
