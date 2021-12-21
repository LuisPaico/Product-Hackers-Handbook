# Colores

Nuestro sistema de diseño no solo **tiene que funcionar tanto en modo Light como en Dark**, sino que además de ello, debe poder adaptarse al color de marca de cada cliente, por lo que **debe poder soportar absolutamente cualquier color**, pero si no sabemos cuál es nuestro color primario o secundario ¿cómo conseguimos que todo tenga coherencia visual y sea legible para nuestros usuarios?.

Para esto hemos creado **dos variantes en base a los colores de marca**, y aunque normalmente son un primario y un secundario, en ocasiones hay marcas con más colores complementarios, pero eso no supone ningún problema, porque cada una de ellas puede tener también sus dos variantes si es necesario.&#x20;

La primera variante la hemos llamado **Lighten**, porque se crea aclarando el color de marca que se haya definido, añadimos una capa blanca con un 80% de opacidad sobre el color base para aclararlo. \
Ejemplo: Si tenemos el color `#7350FF` definido como color "**Primary**", para crear la variante clara de este primario, necesitamos crearlo con una capa superior `#ffffff` al 80% para aclarar este color y así obtener la variante "**Lighten**".

&#x20;![](<../.gitbook/assets/Captura de pantalla 2021-04-19 a las 18.38.33.png>)  ![](<../.gitbook/assets/Captura de pantalla 2021-04-19 a las 18.37.58.png>)&#x20;

La segunda variante la hemos llamado **Darken**, porque al contrario que en el anterior caso, se crea oscureciendo el color de marca que se haya definido, en este caso añadimos una capa negra con un 40% de opacidad sobre el color base para oscurecerlo, pero no demasiado, por eso es un porcentaje menor. \
Ejemplo: Si tenemos el color `#7350FF` definido como color "**Primary**", para crear la variante oscura de este primario, necesitamos crearlo con una capa superior `#000000` al 40%% para oscurecer este color y así obtener la variante "**Darken**". &#x20;

![](<../.gitbook/assets/Captura de pantalla 2021-04-19 a las 18.38.33.png>)![](<../.gitbook/assets/Captura de pantalla 2021-04-19 a las 18.56.33.png>)

Ok, pero... Por qué creamos estas dos variantes por cada primary, secondary, etc... y que conseguimos con ello? Aquí entra en juego los contrastes y su importancia para que los textos sean legibles.

### Contrastes

Los contrastes **son muy importantes** para conseguir una buena experiencia de usuario. Queríamos mantener los colores del cliente y que todo tuviese coherencia visual sin perder accesibilidad.&#x20;

Si usamos por ejemplo el color Primary de antes `#7350FF`, funciona bien con un fondo claro como el blanco, pero nuestro sistema de diseño tiene que funcionar tanto para fondos claros como para fondos oscuros. En esta imagen vemos que en fondo blanco conseguimos un _4.86:1_ de contraste, pero en fondo negro obtenemos un _3.79:1_ de contraste. Según la [WCAG](https://www.w3.org/TR/WCAG21/) un contraste correcto en textos se obtiene a partir de un 4.5:1, exceptuando textos grandes, decorativos o gráficos, los cuales requieren un mínimo de 3:1.

![](<../.gitbook/assets/Primary contrast.png>)

Para solucionar esto creamos las variantes Lighten & Darken de las que hablamos antes. Con esto conseguimos mejora de contraste muy alta, utilizando la variante Darken en fondos claros y la variante Lighten en fondos oscuros (siempre van a la inversa, si en modo Light se crea un texto en Darken, en modo Dark este texto será Lighten).&#x20;

![](<../.gitbook/assets/Primary contrast 2.png>)

Y no solo eso, además podemos combinar estas dos variantes entre ellas para destacar más el texto sin bajar de un 4.5:1 de contraste que es el mínimo para una buena lectura.&#x20;

![](<../.gitbook/assets/Primary contrast 3.png>)

Puede que algunos casos tengamos colores primarios muy claros o muy oscuros y esta fórmula no funcione, para estos casos tenemos otra solución. Si ni el color primario o la variante correspondiente cumplen con el mínimo contraste establecido por la [WCAG](https://www.w3.org/TR/WCAG21/), estos cambiarán a blanco o negro dependiendo de cuál haga mejor contraste con el fondo. &#x20;

![](<../.gitbook/assets/Primary contrast 4.png>)

{% hint style="success" %}
Pensamos siempre en intentar mantener la identidad visual de la marca, pero no debemos olvidarnos de la **accesibilidad**. Esto tiene que funcionar para **todos nuestros clientes**, pero también para **todos los usuarios de nuestros clientes**, por eso es tan importante la accesibilidad. Debemos comprender que el contraste de color puede afectar a diferentes personas con distintas discapacidades visuales.
{% endhint %}

### Contraste en botones

En el caso específico de los botones, pensamos que al ser **uno de los componentes más utilizados** de nuestro sistema de diseño, este siempre tiene que llevar el color del cliente sin variantes. Por esta razón, decidimos detectar que según el color que el cliente establezca, el texto pasará a ser blanco o negro según cuál consiga un mejor contraste. Este es un ejemplo de como funciona:

![](<../.gitbook/assets/Oct-29-2020 14-53-49 (1).gif>)

#### Primary button

El Primary button siempre tendrá el color primario que haya definido el cliente como fondo, y el texto será blanco o negro, dependiendo de con cuál se obtenga un mejor contraste.

![](<../.gitbook/assets/Primary contrast 5.png>)

#### Secondary button

El Secondary button siempre tendrá un fondo blanco en modo Light y negro en modo Dark, junto a un borde del color primario en los dos casos, pero el texto solo tendrá el color primario si tiene buen contraste con el fondo, si esto no se cumple, el texto en modo Light será negro y en modo Dark será blanco. En este ejemplo podemos ver que en modo Dark no tiene el suficiente contraste, por lo que el texto pasa a ser blanco, pero el borde con el color primario se mantiene.

![](<../.gitbook/assets/Primary contrast 6.png>)
