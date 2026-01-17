Abre el MCP de playwright para luego ir a esta url: https://ouo.io/SMbwlL toma una captura y guardarla en la carpeta 'imgs-playwright' que se encuentra en la raiz del proyecto con el nombre 'ouoio.png'.



{
  "$schema": "https://opencode.ai/config.json",
  "mcp": {
    "playwright": {
      "type": "local",
      "command": [
        "npx",
        "@playwright/mcp@latest",
        "--user-data-dir=./mi-perfil-extensiones",
        "--headless"
      ],
      "enabled": true
    }
  }
}
