# Manual de Usuario - Chatbot Soporte Técnico Nivel 1

## ¿Qué hace este bot?

Atiende consultas de soporte técnico de forma automática. Valida tu número de
cliente, te muestra un menú de categorías frecuentes y, si conoce la
solución, te la muestra al instante. Si no puede resolverlo, genera un
ticket y lo deriva a un agente de Nivel 2.

## Pasos para usarlo

1. **Iniciar el bot**: ejecutar `python3 chatbot_soporte.py` desde la carpeta `src/`.
2. **Ingresar tu número de cliente** cuando se solicite (debe existir en `clientes.csv`).
3. **Elegir una categoría** del menú numerado que se muestra en pantalla.
4. El bot responde con la solución sugerida para esa categoría.
5. Si la solución no resolvió tu problema, el bot te lo pregunta y, en caso
   negativo, genera un ticket de derivación a Nivel 2 (queda registrado en
   `tickets.csv`) e informa el número de ticket asignado.

## Comandos / entradas válidas

- Número de cliente: solo dígitos (ej. `100001`).
- Selección de categoría: número correspondiente a la opción del menú (ej. `1`, `2`, `3`...).
- Confirmaciones: `si` / `no` (no distingue mayúsculas).

## ¿Qué pasa si me equivoco?

El bot no se cierra ante una entrada inválida: vuelve a mostrar el menú o
pide el dato nuevamente. Ver detalle de casos contemplados en
[`pruebas_estres.md`](pruebas_estres.md).
