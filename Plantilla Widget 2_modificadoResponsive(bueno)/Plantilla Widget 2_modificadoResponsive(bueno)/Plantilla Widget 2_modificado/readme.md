Esta es la plantilla para la creación de widgets en el generador de webs dinámico. A continuación, se detallan los puntos clave a tener en cuenta:

- Visualización y funcionamiento en local:
El componente debe poder verse y funcionar correctamente de manera local simplemente abriendo el index.html en un navegador.

- Ubicación del HTML del widget:
El HTML del widget debe ir dentro del index.html, específicamente entre las etiquetas <!--/body--> y <!--body/-->. El sistema solo validará el contenido HTML que se encuentre dentro de estas etiquetas, como se muestra en el ejemplo.

- Dependencias CSS y JS:
Todas las dependencias necesarias para el funcionamiento del widget deben colocarse en las carpetas css_inyections y js_inyections. El sistema tomará automáticamente estas dependencias y las integrará al generar la web.

- Uso de variables globales en root.css:
El archivo root.css contiene las variables globales que se aplicarán según la configuración de la web. Al crear el widget, puedes usar estas variables para asignar los valores que necesites. Sin embargo, al integrarse en la web final, las variables se sobrescribirán según la configuración de la misma.
Por ejemplo, si creas una topbar y defines --primary_color como azul en la plantilla, al usar el widget en una web donde --primary_color está configurado como rojo, la topbar se mostrará en rojo.

- En los widgets se pueden interpolar distintos valores por defecto:
    - {PRIMARY_COLOR} -> Color Primario
    - {SECONDARY_COLOR} -> Color Secundario
    - {THIRD_COLOR} -> Color Terciario
    - {LOGO} -> Devuelve la ruta del Logo de la web, ejemplo: <img src="{LOGO}" class="img-fluid">

- Todas las imágenes asociadas al widget, irán dentro de la carpeta splashes y la ruta de las imágenes serían así: /splashes/icon.png