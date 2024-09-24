# Bot-CVE-Notif

```
_____________   _______________            _______   ___________________.______________
\_   ___ \   \ /   /\_   _____/            \      \  \_____  \__    ___/|   \_   _____/
/    \  \/\   Y   /  |    __)_    ______   /   |   \  /   |   \|    |   |   ||    __) 
\     \____\     /   |        \  /_____/  /    |    \/    |    \    |   |   ||     \ 
 \______  / \___/   /_______  /           \____|__  /\_______  /____|   |___|\___  /
        \/                  \/                    \/         \/                  \/1.0
```

> Fork de [BotPEASS](https://github.com/carlospolop/BotPEASS/)

Utilice este bot para supervisar las nuevas CVE de los proveedores definidos y enviar alertas a Slack, Telegram, Discord, Pushover y/o MS Teams.

## Ejemplo con Microsoft Teams

![](.github/MSTeamsNotification.png)

## Configure uno para usted

**Configurar su propio BotPEASS** que le notifique los nuevos CVE que contengan palabras clave específicas es muy fácil.

- Fork a esta repo
- Modifique el archivo `config/cve-notif.yaml` y establezca sus propios proveedores
- En los **github secrets** de su repositorio fork, introduzca las siguientes claves de API:
    - **CLAVE_API_VULNERS**: (Opcional) Se utiliza para encontrar exploits disponibles públicamente. Puedes obtener una clave de API gratuita.
    - **SLACK_WEBHOOK**: (Opcional) Configura el webhook de slack para enviar mensajes a tu grupo de slack.
    - **DISCORD_WEBHOOK_URL**: (Opcional) Configura el webhook de discord para enviar mensajes a tu canal de discord.
    - **TELEGRAM_BOT_TOKEN** y **TELEGRAM_CHAT_ID**: (Opcional) Tu token de bot de Telegram y el chat_id al que enviar los mensajes
    - **PUSHOVER_DEVICE_NAME**, **PUSHOVER_USER_KEY** y **PUSHOVER_TOKEN**: (opcional) Establecer la información pushover para enviar el mensaje.
    - **MSTEAMS_WEBHOOK_URL**:(Opcional) Establezca el webhook de Microsoft Teams para enviar mensajes a su canal de Microsoft Teams 
- Comprueba `.github/wordflows/cve-notif.yaml` y configura el cron (*una vez cada 8 horas por defecto*)

*Ten en cuenta que las configuraciones de Slack, Telegram, Pushover, Microsoft Teams y Discord son opcionales, pero si no configuras ninguna de ellas no recibirás notificaciones en ningún sitio*.
