---
name: markdown-to-presentation
description: Convierte un archivo Markdown en una presentación PowerPoint listo para presentar.
---

# Markdown to Presentation

Transforma un archivo `.md` del workspace en un material de presentación terminado. Responde en español, salvo que el usuario pida otro idioma.

## Flujo

1. Localiza el archivo Markdown indicado por el usuario. Si no se especifica, pregunta cuál debe usar; no elijas arbitrariamente entre varios archivos.
2. Confirma el formato de salida: PowerPoint (`.pptx`). Si el usuario ya indicó uno, no vuelvas a preguntarlo.
3. Si faltan decisiones de presentación que afecten mucho el resultado (público, duración o tono), pregunta de forma breve. Si no son imprescindibles, usa opciones razonables y continúa.
4. Lee el documento completo y conserva sus ideas, datos, nombres y conclusiones. No inventes hechos ni referencias. Puedes resumir y reorganizar para mejorar la narrativa; marca cualquier dato ambiguo en vez de resolverlo por conjetura.
5. Crea el archivo de salida en la misma carpeta que el Markdown, con el mismo nombre base y la extensión elegida. Si ya existe, evita sobrescribirlo: crea un nombre alternativo y avisa.
6. Comprueba el archivo generado y comunica su ruta y cualquier limitación relevante.

## PowerPoint

- Genera un `.pptx` real y editable, no solo un guion ni instrucciones para crear uno.
- Usa una secuencia clara: título, contexto, desarrollo de ideas, evidencia y cierre. Ajusta el número de diapositivas al contenido y a la duración solicitada; evita comprimir todo el Markdown en unas pocas láminas.
- Mantén cada diapositiva enfocada en una idea, con títulos informativos, texto breve y jerarquía visual consistente. Convierte tablas o listas extensas en visualizaciones legibles cuando sea posible, sin alterar los datos.
- Usa notas del presentador para detalles que no quepan en la diapositiva, cuando la herramienta de generación lo permita.
- Reutiliza imágenes proporcionadas por el usuario cuando tengan relación. No presentes imágenes decorativas como evidencia ni inventes atribuciones.
- Usa una herramienta de generación disponible en el entorno, preferentemente `python-pptx` si está instalada. Si falta una dependencia, intenta una alternativa disponible; no afirmes que el `.pptx` está creado si solo generaste código o un esquema.

## Respuesta final

Indica qué archivo fuente usaste, el formato creado y un enlace a la ruta de salida. Resume en una frase la estructura o el número de diapositivas/secciones. Menciona con claridad si alguna validación no pudo ejecutarse.