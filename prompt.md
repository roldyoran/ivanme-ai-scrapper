Usa el MCP de Playwright para automatizar la siguiente tarea:

1. Navega a la url: 'https://www.ivanime.com/paste/0729087/'
2. Busca la card de descarga con calidad 1080p que indica 1.3GB
3. Encuentra el último enlace MFIRE dentro de esa card
4. Haz clic en ese enlace para navegar a la página de ouo.io
5. Espera que cargue la página de ouo.io completamente
6. Resuelve automáticamente el captcha de ouo.io usando:
    - Espera inteligente hasta que aparezca el botón de continuar
    - Si hay checkbox 'Im a Human', haz clic en él y espera la validación
    - Espera los segundos necesarios hasta que se habilite el botón de 'Get Link'
    - Haz clic en 'Get Link' para proceder
8. Espera la redirección final a MFIRE
9. Extrae la URL final de MFIRE
10. También extrae el título del anime de la página original

Devuelve EXCLUSIVAMENTE una RESPUESTA DE TU PARTE con un objeto JSON con esta estructura:
{
  \"titulo\": \"[Nombre del anime extraído]\",
  \"link\": \"[URL final de MFIRE]\",
  \"capitulo\": \"[Número del capitulo]\",
  \"calidad\": \"1080p\"
}

Requisitos importantes:
    - No incluyas explicaciones, comentarios o texto adicional
    - Si algún paso falla, reintenta con lógica de fallback
    - Usa selectores robustos (data attributes, clases específicas)
    - Maneja timeouts adecuados (mínimo 30 segundos de esperaen pasos críticos)
    - Para el captcha: usa waitForSelector y lógica dedetección automática
    - Si la redirección tarda, aumenta los timeouts gradualmente
    - Verifica que el enlace final sea válido (contenga 'mfire'o dominio similar)
    - Cierra el navegador al finalizar
        

        