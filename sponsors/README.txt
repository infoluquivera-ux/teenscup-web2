LOGOS DE SPONSORS
==================

La sección de sponsors en la página tiene 6 espacios (con texto por defecto).

Para reemplazar el texto por logos reales:

1. Poné los logos de sponsors en esta carpeta. Recomendado:
   - estudiantes.png
   - sponsor-2.png
   - sponsor-3.png
   - etc.

2. Abrí index.html con un editor de texto

3. Buscá la sección que dice "SPONSORS" o "Confían en nosotros".
   Vas a ver 6 bloques así:
       <div class="sponsor">Estudiantes<br>La Plata</div>

4. Reemplazá el texto adentro por una imagen, así:
       <div class="sponsor">
         <img src="sponsors/estudiantes.png" alt="Estudiantes" style="max-height:60%; max-width:80%;">
       </div>

RECOMENDADO:
- Formato: PNG con fondo transparente
- Color: logos blancos o claros (la sección tiene fondo oscuro)
- Tamaño: 400x300 px aproximadamente
- Si el logo es oscuro, podés usar la versión blanca o invertirlo
