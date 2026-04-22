## Mobile Courses

Android Studio, puede usarse también para Flutter, para el profesor usa Visual Studio code (editor de texto)
herramienta de compilación para Kotlin es Gradle (java - Maven, c# - nuget)

Activiti es una pantalla, composable son una función que genera una vista,

Device : Pixel 9 Pro

### Configuración

```kotlin
package upc.edu.pe
// ES METADATA
import android.os.Bundle
import androidx.activity.ComponentActivity
import androidx.activity.compose.setContent
import androidx.activity.enableEdgeToEdge
import androidx.compose.foundation.layout.Column
import androidx.compose.foundation.layout.fillMaxSize
import androidx.compose.foundation.layout.padding
import androidx.compose.material3.Scaffold
import androidx.compose.material3.Text
import androidx.compose.runtime.Composable
import androidx.compose.ui.Modifier
import androidx.compose.ui.tooling.preview.Preview
import upc.edu.pe.ui.theme.EasyShopTheme

class MainActivity : ComponentActivity() {
    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        enableEdgeToEdge()
        setContent {
            EasyShopTheme {
                Scaffold(modifier = Modifier.fillMaxSize()) { innerPadding ->
                    Greeting(
                        name = "Android",
                        modifier = Modifier.padding(innerPadding)
                    )
                }
            }
        }
    }
}

// Es una funcion que genera vista, las funciones puedes recibir los parametros
@Composable
fun Greeting(name: String, modifier: Modifier = Modifier) {
    Column (modifier = Modifier.fillMaxSize()) {  // cuando el ultimo parametro de Column es una función
        Text(
            text = "Hello $name!",
            modifier = modifier
        )
        Text("Universidad Peruana de Ciencias Aplicadas")
    }
}

// UNIT, es para pasar parametro de una función a otra funciones

@Preview(showBackground = true)
@Composable
fun GreetingPreview() {
    EasyShopTheme {
        Greeting("Android")
    }
}

// ALT + Enter para importar en el mismpo código

// ANOTES
/*
fun Greeting(name: String, modifier: Modifier = Modifier) {
    Text( // Text es un Composable, donde ya tiene un valor por defecto
        text = "Hello $name!",
        modifier = modifier.fillMaxSize()  // es una parametro, fillMaxSize es para cubrir todo el espacio.
    )
}
*/
```

Final de la sessión, queda pendiente descarga de bibliotecas
