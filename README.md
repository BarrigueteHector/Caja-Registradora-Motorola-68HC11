# Caja Registradora Motorola 68HC11

Proyecto
--------------------------------------------------------------------------------------------------------------------------------------------------------
Programar el software de una caja registradora en lenguaje ensamblador del **MC68HC11**.

Consideraciones
--------------------------------------------------------------------------------------------------------------------------------------------------------
- El programa debe correr en un simulador comercial del **68HC11**.
- Los productos aceptados son: **A**, **B**, **C**, **D**, **E**, **F**, **G**, **H**, **I** y **J** (solo se aceptan mayúsculas), cada uno tiene un precio predeterminado (***posteriormente se menciona***). Para ingresar los productos se utiliza un puerto serial asíncrono del simulador.
- El ingreso de los productos debe respetar el siguiente formato:

`Producto <operación> Producto <operación> ... <operación> Producto =`

- La operación debe ser **+** (agregar) o **-** (quitar).
- No hay un limite respecto a la cantidad de productos que se pueden ingresar.
- Se debe considerar un IVA del **10%** respecto al total.
- Se debe imprimir un ticket en el que sea visible: tipo y cantidad de productos comprados (incluso si no se compró nada de un producto), subtotal de la compra (la suma de los precios de todos los productos), IVA, ahorro (dinero ahorrado si se hizo un descuento) y total (la suma del **Subtotal de la compra** e **IVA**), este último en formato númerico y textual (la primera letra debe ser mayúscula y las siguientes minúsculas, los acentos se sustituyen por la letra en mayúscula).
- Para eliminar la cuenta o ticket, introducimos `n` o `=OK` en el puerto serial asíncrono del simulador.
- Los errores deben ser impresos.

Errores
--------------------------------------------------------------------------------------------------------------------------------------------------------
- No se respeta el formato
- Se pretende quitar un producto que no fue agregado anteriormente.
- Se agregó un producto que no es aceptado.
- Se realizó un operación que no es aceptada.
- La compra excede los 10 millones de dólares.

Precios y Descuentos
--------------------------------------------------------------------------------------------------------------------------------------------------------
| Producto |        Precio        |                   Descuento                   |
| :--------: | :--------------------: | :--------------------------------------------: |
|     A    |              50      | 1 |
|     B    |             100      | 1 |
|     C    |             500      | 1 |
|     D    |            1000      | 1 |
|     E    |            5000      | 2 |
|     F    |           10000      | 2 |
|     G    |           50000      | 2 |
|     H    |          100000      | 2 |
|     I    |          500000      | 3 |
|     J    |         1000000      | 3 |

**Descuentos**
- ***1***: En la compra mínima de ***4 unidades***, los demás se cobran con un ***50% de descuento***.
- ***2***: En la compra mínima de ***5 unidades***, todos los productos del mismo tipo se cobran con ***50% de descuento***.
- ***3***: En la compra de ***una unidad***, únicamente la siguiente del mismo tiene ***50% de descuento***.

Extra
--------------------------------------------------------------------------------------------------------------------------------------------------------
Para ejecutar el simulador se debe ****descargar todos los archivos*** de la carpeta [Simualdor MC68HC11](https://github.com/BarrigueteHector/Caja-Registradora-Motorola-68HC11/tree/main/Simulador%2068HC11) y se debe de ejecutar la aplicación ***thrsim11***.
