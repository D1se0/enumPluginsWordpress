# WordPress Plugin Scanner

A simple and efficient tool to detect plugins installed on `WordPress` sites, identifying their version (when available) to evaluate potential vulnerabilities and strengthen the site's security.

## Characteristics

- Scans a list of popular `WordPress` plugins on a target site.
- Identifies if a plugin is installed and extracts its version (when possible).
- Useful for developers, security auditors, and system administrators who need to understand a site's `WordPress` environment.
- Based on Python and uses the `requests` and `colorama` libraries for fast operation and a colorful command line interface.

## Facility

### Prerequisites

- `Python 3.6` or higher
- The following Python libraries:
  - `requests`
  - `colorama`

### Installing dependencies

Run the following command to install the necessary dependencies:

```bash
pip install requests colorama
```

## Use

Clone this repository or download the script.

### Run the script in your terminal with:

```bash
python3 enumPluginsWordpress.py
```

Enter the URL of the `WordPress` site you want to analyze (for example, http://example.com).

The script will search for the plugins listed in the plugins variable and display those that are present, along with their versions, if available.

### Execution example:

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

## Customization

The list of plugins to scan is found in the `plugins` variable within the script. You can add, 'modify or remove' plugins from this list according to your needs.

## Limitations

The script only checks if a readme.txt file exists in the plugin's standard path (`/wp-content/plugins/{plugin}/readme.txt`).
If the readme.txt file does not contain version information, the version will not be detected.
This script assumes that the website uses standard paths for plugins. Customizations may affect results.

## Contribution

If you want to improve this tool, feel free to send a pull request or open an issue in this repository.

## Warning

This tool is designed for educational and security auditing purposes on systems where you have permission to perform testing. Unauthorized use of this tool against third-party sites is strictly prohibited and may violate local and international laws.

## License

This project is licensed under the `MIT` License. See the `LICENSE` file for details.
