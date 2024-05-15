# ip_to_bin

### Script para convertir una dirección IP a formato binario

Este script de Bash convierte una dirección IP introducida por el usuario en formato decimal a formato binario. Aquí está el desglose del script:

#### Función `valid_ip()`

Esta función verifica si la dirección IP introducida por el usuario tiene el formato correcto. Utiliza una expresión regular para validar que la IP tenga cuatro partes separadas por puntos, y que cada parte contenga números entre 0 y 255.

#### Función `valid_byte()`

Esta función se encarga de validar cada parte de la dirección IP. Divide la dirección IP en partes utilizando el carácter punto como delimitador y luego verifica si cada parte es un número entre 0 y 255. Para cada parte válida, agrega un "0" a una cadena `valid_code`, y para cada parte inválida, agrega un "1". Al final, comprueba si `valid_code` es "0000", lo que indica que todas las partes son válidas.

#### Función `uint_to_bin()`

Esta función convierte cada parte decimal de la dirección IP en su equivalente binario. Utiliza un bucle para iterar sobre cada parte decimal de la IP. Para cada parte, convierte el número decimal a binario y lo agrega a una cadena `binary_all`, separando cada parte binaria con un punto. Al final, imprime la cadena `binary_all` que contiene la IP en formato binario.

#### Uso del script

El script solicita al usuario que introduzca una dirección IP. Luego, valida la IP utilizando la función `valid_ip()`. Si la IP es válida, se llama a la función `valid_byte()` para validar cada parte. Si todas las partes son válidas, se llama a la función `uint_to_bin()` para convertir la IP a binario y mostrarla en la salida.

Si alguna parte de la IP es inválida, se muestra un mensaje de error y el script termina.

Este script proporciona una manera rápida y sencilla de convertir una dirección IP de formato decimal a binario utilizando Bash.