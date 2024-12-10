# WordPress Plugin Scanner

Una herramienta sencilla y eficiente para detectar plugins instalados en sitios de `WordPress`, identificando su versión (cuando esté disponible) para evaluar vulnerabilidades potenciales y fortalecer la seguridad del sitio.

## Características

- Escanea una lista de plugins populares de `WordPress` en un sitio objetivo.
- Identifica si un plugin está instalado y extrae su versión (cuando sea posible).
- Útil para desarrolladores, auditores de seguridad y administradores de sistemas que necesitan entender el entorno de `WordPress` de un sitio.
- Basado en Python y utiliza las bibliotecas `requests` y `colorama` para un funcionamiento rápido y con una interfaz de línea de comandos colorida.

## Instalación

### Requisitos previos

- `Python 3.6` o superior
- Las siguientes bibliotecas de Python:
  - `requests`
  - `colorama`

### Instalación de dependencias

Ejecuta el siguiente comando para instalar las dependencias necesarias:

```bash
pip install requests colorama
```

## Uso

Clona este repositorio o descarga el script.

### Ejecuta el script en tu terminal con:

```bash
python3 enumPluginsWordpress.py
```

Introduce la URL del sitio `WordPress` que deseas analizar (por ejemplo, http://example.com).

El script buscará los plugins listados en la variable plugins y mostrará los que estén presentes, junto con sus versiones, si se encuentran disponibles.

### Ejemplo de ejecución

```
[*] Bienvenido al buscador de plugins de WordPress
[*] Por favor, introduce la URL del sitio de WordPress a analizar.
Introduce la URL (ejemplo: http://example.com): http://mysite.com
[*] Comenzando la búsqueda de plugins en: http://mysite.com
[*] Plugins a buscar: jetpack, site-editor, akismet, woocommerce, contact-form-7...
--------------------------------------------------
[+] Plugin encontrado: woocommerce
    Versión detectada: 5.2.1
[+] Plugin encontrado: contact-form-7
    Versión detectada: 5.3.2
--------------------------------------------------
[*] Búsqueda completada. Sólo se muestran los plugins encontrados.
```

## Personalización

La lista de plugins a escanear se encuentra en la variable `plugins` dentro del script. Puedes agregar, `modificar o eliminar` plugins de esta lista según tus necesidades.

## Limitaciones

El script sólo verifica si existe un archivo readme.txt en la ruta estándar del plugin (`/wp-content/plugins/{plugin}/readme.txt`).
Si el archivo readme.txt no contiene información sobre la versión, esta no será detectada.
Este script asume que el sitio web utiliza rutas estándar para los plugins. Personalizaciones pueden afectar los resultados.

## Contribución

Si deseas mejorar esta herramienta, no dudes en enviar un `pull request` o abrir un issue en este repositorio.

## Advertencia

Esta herramienta está diseñada para fines educativos y de auditoría de seguridad en sistemas donde tienes permiso para realizar pruebas. El uso no autorizado de esta herramienta contra sitios ajenos está estrictamente prohibido y podría violar leyes locales e internacionales.

## Licencia

Este proyecto está licenciado bajo la Licencia `MIT`. Consulta el archivo `LICENSE` para más detalles.
