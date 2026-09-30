# Veterinary Agent with Llama Stack

Challenge desarrollado en Google Colab para implementar un agente conversacional de una veterinaria utilizando WhatsApp Cloud API, FastAPI, Ollama, Llama 3.1 8B y Llama Stack.

El agente incorpora memoria de conversación por número telefónico, límite de historial, control de concurrencia mediante locks y reglas fijas para urgencias y escalamiento a una persona.

## Validación

El flujo se probó con una conversación de cuatro mensajes y se verificó:

- recepción y respuesta mediante WhatsApp Cloud API;
- conservación máxima de seis elementos en el historial;
- activación de la regla fija de urgencia sin consultar al modelo;
- escalamiento a atención humana sin consultar al modelo;
- ausencia de errores internos durante la prueba.

Se añadió una auditoría automática de los requisitos del challenge, cuyo resultado final fue `PASS`.

## Observación

Durante las pruebas, el modelo generó horarios y disponibilidad no proporcionados como datos de entrada. En una aplicación real, esta información debería obtenerse de una fuente confiable del negocio y no depender del modelo de lenguaje.
