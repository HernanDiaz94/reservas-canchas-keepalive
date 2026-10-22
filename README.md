# reservas-canchas-keepalive

Ping automatico cada 5 minutos a https://reservas-canchas-1.onrender.com/health.

Existe por una sola razon: el plan gratuito de Render duerme el backend a los
15 minutos sin trafico, y el arranque en frio (50-90 segundos) le aparece al
usuario como "No se pudo conectar con el servidor" en el login.

El repo es publico porque los minutos de GitHub Actions en repos publicos son
ilimitados. No hay credenciales ni codigo de la app aca: el workflow solo hace
un GET a un endpoint publico.

Si GitHub lo desactiva por 60 dias sin actividad, se reactiva desde la pestana
**Actions** -> keepalive -> **Enable workflow**.
