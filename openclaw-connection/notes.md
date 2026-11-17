# Notas del proyecto openclaw-connection

1. Telegram: creé el bot con BotFather y lo agregué con `openclaw channels add`. Pegué el token con `read -rs` para que no quedara en pantalla. Dejé activo el emparejamiento (pairing) para que solo mi cuenta pueda dar órdenes a Kai.
2. Cuentas de prueba: usé una cuenta de Google de prueba (no la personal) para Docs y Calendar.
3. Zapier: creé un servidor MCP solo para OpenClaw con 6 acciones (3 de Docs y 3 de Calendar). Quité borrar eventos y la API genérica para dar el mínimo permiso.
4. Cambié el servidor a modo Managed: en modo Agentic Kai podía usar miles de acciones sin límite y mis 6 acciones no habrían sido un límite real.
5. Conexión: OpenClaw se conecta con un token en el header Authorization, no en la URL. `openclaw mcp add` falló al probar; funcionó con `openclaw mcp set` con el gateway apagado y `openclaw mcp doctor zapier --probe` dio ok.
6. Problema: el token se mostró en pantalla por un error al pegarlo. Lo regeneré y borré el historial del servidor. El token válido queda en texto en openclaw.json (fuera del workspace, no se sube a git).
7. Prueba completa: mandé un mensaje vago y Kai preguntó de qué trataba el proyecto y cuándo quería la revisión. Después creó el documento y el evento y lo confirmó por Telegram. Verifiqué en Google que ambos existen.
8. Avisos: aparecieron mensajes "The background check did not complete". El log solo muestra lentitud (servidor de 1 GB de memoria) y el flujo no se afectó, pero no confirmé la causa.
9. En Zapier el cliente OpenClaw aparece "Pending" porque no usé el atajo de pegar el prompt; la conexión por token funciona.
10. Kai agregó un enlace de Google Meet al evento sin que se lo pidiera.
