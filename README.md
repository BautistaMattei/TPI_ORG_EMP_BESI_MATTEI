# TPI - Organización Empresarial: Chatbot de Soporte Técnico Nivel 1

**Tecnicatura Universitaria en Programación (UTN) - A Distancia**
**Cátedra:** Organización Empresarial
**Integrantes:** Bautista Mattei - Santiago Besi

##  Descripción

Trabajo Práctico Integrador que consiste en identificar un proceso administrativo
ineficiente (atención de soporte técnico nivel 1) y automatizarlo mediante un
chatbot, partiendo de un modelado de procesos en BPMN 2.0 (flujo as-is) hacia
una solución optimizada (flujo to-be), simulando persistencia de datos mediante
archivos CSV.

##  Proceso elegido

**Soporte técnico - Atención Nivel 1.** El flujo actual (as-is) es manual: el
cliente envía mail o llama, el caso queda en una cola sin prioridad y el agente
revisa y responde según disponibilidad, sin registro centralizado. El flujo
propuesto (to-be) automatiza la atención de primer nivel con un bot que valida
al cliente, ofrece soluciones conocidas para problemas frecuentes y deriva a
Nivel 2 con ticket generado cuando no puede resolver.

##  Estructura del repositorio

```
TPI_ORG_EMP_BESI_MATTEI/
├── README.md
├── .gitignore

├── chatbot_soporte.py
│  data/
│      ── clientes.csv
│      └── tickets.csv
├── docs/
│   ├── diccionario_datos.md
│   ├── manual_usuario.md
│   ├── pruebas_estres.md
│   ├── consultas_ia/
│   │   └── README.md
│   └── TPI_Organizacion_Empresarial.pdf
└── diagramas/
    ├── bpmn_soporte_tecnico_as_is.png
    └── bpmn_soporte_tecnico_nivel1.png
```

##  Cómo ejecutarlo

Requisitos: Python 3.x (sin librerías externas).

```bash
git clone https://github.com/BautistaMattei/TPI_ORG_EMP_BESI_MATTEI.git
cd TPI_ORG_EMP_BESI_MATTEI/src
python3 chatbot_soporte.py
```

El bot corre por consola. Al iniciar valida el número de cliente contra
`data/clientes.csv` y, según la categoría de consulta elegida, ofrece una
solución conocida o genera un ticket en `data/tickets.csv` derivando a
Nivel 2.

##  Diagramas BPMN

| Diagrama | Descripción |
|---|---|
| `bpmn_soporte_tecnico_as_is.png` | Proceso actual, 100% manual, sin registro centralizado |
| `bpmn_soporte_tecnico_nivel1.png` | Proceso propuesto, automatizado con el bot |

##  Persistencia de datos

Se simula base de datos mediante dos archivos CSV (ver detalle completo en
[`docs/diccionario_datos.md`](docs/diccionario_datos.md)):

- **clientes.csv**: padrón simulado de clientes, usado para validar al inicio de la conversación.
- **tickets.csv**: registro de cada consulta/reclamo generado durante la interacción con el bot.

##  Estado de las pruebas

Ver [`docs/pruebas_estres.md`](docs/pruebas_estres.md) para los casos de
entrada inválida contemplados (camino infeliz).

##  Uso de herramientas de IA

Se utilizó IA como apoyo en el diseño del diagrama BPMN y en la estructuración
del código. El detalle de prompts y respuestas está documentado en
[`docs/consultas_ia/`](docs/consultas_ia/).
