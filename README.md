# 🚌 PilarBus: Ecosistema Móvil de Transporte Público

¡Bienvenidos al repositorio oficial del proyecto **PilarBus**! Este espacio centraliza el código fuente, la gestión de versiones y la automatización del despliegue para la aplicación móvil y plataforma web destinada a los ciudadanos de Pilar.

---

## 🔄 Flujo de Trabajo y Pull Requests

Para asegurar la calidad del código y mantener una colaboración ordenada entre todos los integrantes del equipo, adoptamos una estrategia basada en ramas y **Pull Requests (PRs)**:

1. **Ramas por Funcionalidad:** Ningún integrante programa directamente sobre la rama principal (`main`). Cada nueva funcionalidad o corrección se desarrolla en una rama independiente (por ejemplo, `feature/alertas-desvios` o `feature/integracion-sube`).
2. **Revisión de Código (Code Review):** Una vez finalizada la tarea, el desarrollador abre un *Pull Request* hacia la rama de desarrollo o producción. 
3. **Aprobación:** Otro miembro del equipo revisa los cambios, verifica que cumpla con los estándares y aprueba el PR antes de que el código sea integrado oficialmente. Esto nos permite detectar errores de manera temprana y mantenernos comunicados.

---

## ⚙️ Integración y Entrega Continua (CI/CD)

Dado que **PilarBus** opera en un entorno de alta incertidumbre con requisitos y comentarios de usuarios beta que cambian semanalmente[cite: 1], es fundamental actualizar el sistema en la nube **sin interrumpir el servicio** a los pasajeros[cite: 1]. 

Para lograrlo, configuramos un pipeline de CI/CD automatizado:

* **Build y Validación Automática:** Cada vez que se genera un *Pull Request* o se realiza un *commit* importante, el servidor ejecuta scripts automáticos de compilación (*Build*) y pruebas unitarias (*Test*)[cite: 1].
* **Detección Temprana de Fallos:** Si alguna prueba falla o hay un conflicto de código, el sistema bloquea el pase a producción hasta que el equipo lo resuelva.
* **Despliegue Continuo (Deploy):** Una vez que el código pasa todas las validaciones de forma exitosa, se despliega automáticamente en la nube de forma transparente para los usuarios, asegurando alta disponibilidad y mejoras constantes en la aplicación de transporte.
