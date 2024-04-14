# TP 0

Como primer paso, seguimos las instrucciones de la propia [documentacion]([https://github.com/pandao/editor.md](https://code.visualstudio.com/docs/cpp/config-mingw) "documentacion") de VS Code donde nos guía sobre como instalar y configurar el compilador GCC, y como seleccionarlo dentro de nuestro Visual Studio Code.

Antes de seleccionar el compilador que habremos instalado, debemos abrir Visual Studio Code y crear nuestro archivo C en el directorio que deseemos. Una vez creado, debemos copiar el siguiente codigo, que imprimirá en consola "Hello, World!":

`#include <stdio.h>
int main(){
    printf("Hello, world!\n");
    return 0;
}`

Con nuestro codigo en el archivo .c creado, debemos definir algunos argumentos para nuestro compilador. Siguiendo la [documentacion]([https://github.com/pandao/editor.md](https://code.visualstudio.com/docs/cpp/config-mingw) "documentacion"), podemos facilmente crear el archivo `c_cpp_properties.json`, sobre el cual vamos a hacer foco principalemnte en la linea `cStandard": "estandar"`. En "estandar", vamos a necesitar colocar el estandar que queremos que nuestro compilador utilice. Pero no todos los compiladores pueden soportar todos los estandares de C disponibles, por lo que debemos chequear que estandar soporta nuestra version de GCC.

Es tan facil como escribir `gcc --version` y buscar en internet el manual de dicha version y verifica la compatibilidad del estandar. En mi caso, tengo la version [13.2.0]([[https://github.com/pandao/editor.md](https://code.visualstudio.com/docs/cpp/config-mingw](https://gcc.gnu.org/onlinedocs/gcc-13.2.0/gcc/Standards.html#C-Language)) "13.2.0") y utilicé el estandar C17 (2018) (ver archivo `c_cpp_properties.json`).

![properties](https://github.com/IgnacioLapko/SSL/assets/71944432/8e6b652a-7049-43ee-ad19-aa2f7f3ee629)

Llegado a este punto, podemos correr nuestro programa perfectamente. La primera vez que lo hagamos, nos consultará que compilador deseamos utilizar; y seleccionaremos `gcc`.

Si todo salio bien, deberiamos ver en el terminal `Hello, World!` y se habrá creado un archivo con el mismo nombre de nuestro .c, pero con extension .exe.

![run hello world](https://github.com/IgnacioLapko/SSL/assets/71944432/336557d1-b791-4a72-bf19-f8321e411925)

Lo unico que nos quedaría seria generar el archivo `output.txt`, en el que guardaremos lo que retorna la funcion main() de nuestro programa ("Hello, World!). Para ello, escribiremos en consola `program.exe > output.txt`

![output hello world](https://github.com/IgnacioLapko/SSL/assets/71944432/87b646a2-bc05-4055-a8ef-1756500d0982)

De esta manera, concluiriamos con el TP0.
