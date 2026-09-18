# Demostración para Instructores - Gemini Enterprise Agent Platform: agentes inteligentes para el negocio

El propósito de este documento es sugerir la demostación que el instructor puede realizar durante la entrega del seminario Introducción a Gemini Enterprise Agent Platform: agentes inteligentes para el negocio. Los siguientes pasos son generales, se entiende que el instructor tiene las habilidades para comprenderlo. Están organizados en orden de los slides de Power Point adjuntos. 

## Agentes preconstruidos

* Ejecutar un agente existente que reciba una solicitud de negocio, consulte información, procese la tarea y entregue un resultado final
* Solicitar un agente del market place, ir a Gemini Enterprise, ingresar a la app y en la sección agents ver la solicitud en "Procurenment and integration request"

## Crear un agente sencillo en el estudio de Google Agent Platform

* Crear un agente desde el agent platform usando un Pre-built template y desplegandolo en Gemini Enterprise
* Explica a graneds rasgos cloudshell, desplegarlo desde la terminal
* Probar su funcionamiento

## Configurar instrucciones y recursos del agente mediante el flujo visual

* Crear el agente desde el agent studio, sin usar código permitiendo orquestación multi-agente
* Agregar capacidad externa con MCP. Podrías usar `https://webhook.site/`, registrando un nuevo MCP server con la siguiente estructura:

```json
{
  "tools": [
    {
      "name": "enviar_notificacion",
      "description": "Envia una notificacion o mensaje al webhook externo",
      "inputSchema": {
        "type": "object",
        "properties": {
          "mensaje": {
            "type": "string",
            "description": "El contenido del mensaje o notificacion que el agente enviara"
          },
          "cliente": {
            "type": "string",
            "description": "Nombre del cliente o entidad relacionada"
          }
        },
        "required": [
          "mensaje"
        ]
      }
    }
  ]
}
```

## Probar el agente

* Usar la pestaña **Preview** para ponerlo a prueba. revisar el resultado en el Webhook.

## Modificar comportamiento del agente

* Modificar el comportamiento, agregar restricciones y filtros al agente desde el mensaje del sistema

## Ejecutar el agente desde Gemini Enterprise

* Hacer Deploy en el agente.
* En unos momentos aparecerá en Deployments en Agents Platform.
* Copia el Resource Name
* Ir a Gemini Enterprise e ingresar a la app
* En la sección agentes **+ Add agent**
* Custom agent via Runtime
* Skip autorización
* Runtime el resource name que copiaste anteriormente
  

