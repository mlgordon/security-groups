---



copyright:
  years: 2017
lastupdated: "2017-08-08"


---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Directrices de los grupos de seguridad
Tenga en cuenta las siguientes directrices cuando trabaje con grupos de seguridad:

## Reglas

* Cada grupo de seguridad define distintos conjuntos de reglas de red que definen el tráfico de entrada y de salida para una instancia de servidor virtual. Se pueden especificar reglas tanto para IPv4 como para IPv6.
* Cuando se crea un nuevo grupo de seguridad utilizando la interfaz Portal de cliente, el comportamiento predeterminado consiste en crear una única regla que permite todo el tráfico de salida desde la instancia de servidor virtual. Desmarque el recuadro de selección "Crear grupo con una regla predeterminada que permita todo el tráfico saliente" para crear el grupo de seguridad sin reglas. Un grupo de seguridad sin reglas bloquea todo el tráfico (tanto el entrante como el saliente).
* Para permitir el tráfico entrante, el tráfico saliente, o ambos, debe añadir al menos un grupo de seguridad que incluya las reglas de grupo de seguridad que permiten el tráfico. 
* Las reglas de grupo de seguridad solo pueden ser permisivas. El tráfico está bloqueado de forma predeterminada.
* Los usuarios con el privilegio Gestionar grupos de seguridad pueden añadir, editar o suprimir reglas de un grupo de seguridad. 
* Los cambios realizados en las reglas de grupos de seguridad se aplican automáticamente y se pueden modificar en cualquier momento.
* El orden de las reglas en el grupo de seguridad no tiene importancia. La prioridad siempre recae en la regla menos restrictiva.
* Los grupos de seguridad no sustituyen a los cortafuegos del sistema operativo en el servidor virtual. Si el sistema operativo dispone de un cortafuegos más restrictivo que el aplicado por los grupos de seguridad, se aplicarán las reglas del sistema operativo.
* Si el servidor virtual necesita acceder a servicios internos, como un servidor de actualización, un almacenamiento adjunto en red (NAS) o la supervisión avanzada, asegúrese de que las reglas de los grupos de seguridad ajusten el tráfico a dichos servicios internos. Para obtener más información, consulte [What IP ranges do I allow through the firewall? ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://knowledgelayer.softlayer.com/faqs/6#154) y [Accessing Block Storage on Linux ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://knowledgelayer.softlayer.com/procedure/block-storage-linux).

## Interfaces

* Un grupo de seguridad se puede aplicar a una red privada, pública o a ambos tipos de interfaz de red.
* Puede añadir uno o varios grupos de seguridad a la lista de grupos de seguridad asignados a una interfaz de red. Las reglas de grupos de seguridad de cada grupo de seguridad se aplican a las instancias de servidor virtual asociadas. 
* La primera vez que asigne un grupo de seguridad existente a una interfaz de red (pública o privada), será necesario reiniciar cada interfaz.  Sin embargo, si la interfaz pública y la privada se asignan al grupo de seguridad de forma simultánea, solo se deberá reiniciar una vez.  Tras el reinicio, los cambios se aplican automáticamente.

## Acceso
 
* Todos los usuarios de una cuenta pueden leer, conectar y desconectar grupos de seguridad de las instancias de servidor virtual a las que tienen acceso. Solo los usuarios con el privilegio Gestionar grupos de seguridad en Permisos de red pueden crear, actualizar y suprimir grupos de seguridad.
* No se pueden asignar grupos de seguridad a servidores nativos.

## Supresión

* No se puede suprimir un grupo de seguridad asignado a una o varias instancias de servidores virtuales en ejecución.
* No se puede suprimir un grupo de seguridad al que haga referencia otro grupo de seguridad en una de sus reglas. 
