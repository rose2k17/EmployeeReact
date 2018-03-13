# EmployeeReact
### Antes de seguir el tutorial de <a href="http://coenraets.org/blog/2017/01/react-native-sample-app-tutorial/">EmployeeDirectory</a>
  1. Instalar NPM 4, ya que React Native no soporta npm 5:
  ```
  npm install -g npm@4
  ```

  2. Instalar yarn: 
  ```
  npm install -g yarn
  ```
   3.  Seguir las instrucciones de React Native en <a href="https://facebook.github.io/react-native/docs/getting-   started.html">getting started</a>, la opción <b>Building Projects with Native Code</b> para la instalación.
   AVISO: antes de hacer el comando <b>react-native run-android o ios</b>, hay que tener el VD operativo.
   
## Solución a algunos errores

En el tutorial hay un error en: <b>import {Navigator, Text, TouchableOpacity, Image, StyleSheet} from 'react-native';</b> en EmployeeDirectoryApp.js, ya que hay unas funciones depreciadas de <b>Navigator</b>, en la libreria de react-native. entonces la solución seria (aunque está cambiada) es:
  - Instalar la librería: 
  ```
  npm install react-native-deprecated-custom-components
  ```
  - Añadir este: <b>import { Navigator } from 'react-native-deprecated-custom-components';</b> y eliminar "Navigator" del otro  import.
### Problemas con las variables de entorno

Poner el adb en Path, el adb está en el directorio de instalación (ruta)/Sdk/platform-tools
 
### Problemas al sacar el Virtual Device

- Si es un problema con el procesador AMD: 
  Android Studio tiene problemas de sacar el VD con estos procesadores sacando un mensaje como este:
  <b>Your cpu doesn't support required features (vt-x or svm)</b>
  En StackOverflow hay una <a href="https://es.stackoverflow.com/questions/16371/emulador-android-studio-en-amd-fx"> solución</a> muy buena de descargarse un VD externo con <a href="https://www.genymotion.com/download/">Genymotion</a>, hay otros como Nox o BlueStacks.
  Con Genymotion (instalado):
    1. Ir a Android Studio en <b>File > Settings</b>.
    2. Seleccionar Plugins,  y click en <b>Browse Repositories</b>, buscar el plugin <b>Genymotion</b> e instalarlo.
    3. Despues de reiniciar Android Studio, en <b>Settings > Other Settings > Genymotion</b> añadir  la ruta: <b>C:\Program
Files\Genymobile\Genymotion</b>.
    3. Desplegar el Toolbar en <b>View > Toolbar</b>.
