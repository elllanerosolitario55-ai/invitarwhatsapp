# WhatsApp Group Inviter 📱

Aplicación web para enviar invitaciones masivas a grupos de WhatsApp.

## ✨ Características

- **Carga de contactos**: CSV, TXT o entrada manual
- **Validación automática**: Números con formato internacional
- **Prefijos de país**: Soporte para múltiples países (España, LATAM, Europa, USA)
- **Mensajes personalizados**: Plantillas con variables dinámicas
- **Control de envío**: Pausa, reanuda o detén en cualquier momento
- **Retardo aleatorio**: Evita bloqueos de WhatsApp
- **Persistencia local**: Guarda tu progreso automáticamente
- **Exportación**: Descarga tu lista con estados
- **Diseño responsive**: Funciona en móvil y desktop

## 🚀 Despliegue en Netlify

### Opción 1: Arrastrar y soltar (más fácil)

1. Ve a [Netlify Drop](https://app.netlify.com/drop)
2. Arrastra la carpeta `whatsapp-inviter` completa
3. ¡Listo! Tu app estará disponible en segundos

### Opción 2: Desde GitHub

1. Sube este repositorio a GitHub
2. Ve a [Netlify](https://app.netlify.com)
3. Clic en "Add new site" → "Import an existing project"
4. Conecta tu repositorio de GitHub
5. Configuración de build:
   - Build command: (dejar vacío)
   - Publish directory: `.`
6. Clic en "Deploy"

### Opción 3: Netlify CLI

```bash
# Instalar CLI de Netlify
npm install -g netlify-cli

# Login
netlify login

# Desplegar
cd whatsapp-inviter
netlify deploy --prod
```

## 📋 Cómo usar

1. **Configura el enlace del grupo**
   - Abre tu grupo de WhatsApp
   - Ve a Configuración → Invitar mediante enlace
   - Copia el enlace y pégalo en la app

2. **Añade contactos**
   - **CSV**: Arrastra un archivo con columna "phone" o "telefono"
   - **Manual**: Escribe números uno a uno
   - **Bulk**: Pega múltiples números (uno por línea)

3. **Personaliza el mensaje**
   - Edita la plantilla
   - Usa `{GROUP_LINK}` donde quieras insertar el enlace

4. **Inicia el envío**
   - Clic en "Iniciar Envío"
   - Se abrirá WhatsApp Web para cada contacto
   - Confirma el envío manualmente en cada ventana

## 📁 Formato de CSV

```csv
phone,name
+34612345678,Juan García
+34698765432,María López
612111222,Pedro (se añade prefijo automáticamente)
```

También acepta archivos con un número por línea:
```
+34612345678
+34698765432
612111222
```

## ⚠️ Advertencias

- **Límites de WhatsApp**: El envío masivo puede resultar en bloqueos temporales
- **Usa retardos**: Configura tiempos de espera entre mensajes (5-15 segundos recomendado)
- **Confirma manualmente**: La app abre WhatsApp pero tú debes confirmar el envío
- **Responsabilidad**: Usa esta herramienta de forma ética y legal

## 🛠️ Tecnologías

- HTML5 / CSS3 / JavaScript (Vanilla)
- Sin dependencias externas
- Almacenamiento local (localStorage)
- API de WhatsApp (wa.me)

## 📄 Licencia

MIT - Libre para uso personal y comercial.

---

Hecho con ❤️ para MuroSocial
