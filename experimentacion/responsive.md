# Auto layout

Todos nuestros experimentos están montados con **Auto layout**, porque de esta manera podemos simular como se va a **adaptar** en el caso de que alguna de sus partes sea alterada, ya sea por cualquier **modificación**.

![](<../.gitbook/assets/Apr-28-2021 18-50-26.gif>)

En este caso vemos como al modificar el ancho de este experimento se adapta no solo la caja que lo contiene, sí no que también lo hacen los textos, líneas, imagen y botón.

![](<../.gitbook/assets/Apr-28-2021 19-24-47.gif>)

Como podemos ver en este caso si quitamos partes como el head o el título, el contenido se adapta, pero lo hace hacia arriba porque la x que tenemos en la parte superior es flotante y esa se puede montar con autolayout.

![](<../.gitbook/assets/Apr-28-2021 19-36-47.gif>)

Tener esta "x" flotante es muy común en los experimentos y para solucionar este pequeño "bug", lo que hacemos es que cuando quitamos alguna parte del experimento hacemos click en el icono de _Resize to fit_ ![](<../.gitbook/assets/Captura de pantalla 2021-04-28 a las 19.38.48.png>) . Esto ajustará el tamaño del frame al tamaño actual del contenido, por último solo tenemos que alinear el experimento a la zona donde estaba con las opciones de alineación en la parte superior ![](<../.gitbook/assets/Captura de pantalla 2021-04-28 a las 19.45.34.png>) , en este caso abajo a la izquierda.

![](<../.gitbook/assets/Apr-30-2021 12-49-04.gif>)

Montar los experimentos con Auto layout nos permite poder ocultar partes del componente como hemos visto en estos ejemplos y esto ayuda mucho a que desarrollo pueda saber como se va a comportar algo en el caso de que growth decida no añadir alguna parte. Recordar que siempre podéis duplicar el documento para probar sin afectar al documento original, junto al nombre podéis desplegar las opciones del fichero, entre estas opciones, pulsáis en "Duplicate to your drafts" y tendréis una copia.

![](../.gitbook/assets/Duplicar.png)
