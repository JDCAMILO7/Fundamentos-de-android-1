Intentoo hacerlo pero creo que quedo mal aparte, el que vaya a calificar me recomienda algún
video? Los del curso sirvieron pero igual quede corto, aun me sigo confundiendo
esto me base en un video y en ayuda de amigos
import android.content.res.Configuration;
import android.os.Bundle;
import android.widget.ImageView;
import android.widget.TextView;
import androidx.appcompat.app.AppCompatActivity;
public class MainActivity extends AppCompatActivity {
 @Override
 protected void onCreate(Bundle savedInstanceState) {
 super.onCreate(savedInstanceState);
 setContentView(R.layout.activity_main);
 // Obtener la orientación actual de la pantalla
 int orientation = getResources().getConfiguration().orientation;
 // Cargar la imagen de fondo y el texto según el idioma y la orientación
 ImageView backgroundImageView = findViewById(R.id.backgroundImageView);
 TextView textView = findViewById(R.id.textView);
 if (orientation == Configuration.ORIENTATION_LANDSCAPE) {
 // Paisaje
 backgroundImageView.setImageResource(R.drawable.background_landscape);
 textView.setText(getString(R.string.hello));
 } else {
 // Retrato
 backgroundImageView.setImageResource(R.drawable.background_portrait);
 textView.setText(getString(R.string.hello));
 }
 }
}
Parte para la multi plantalla
<?xml version="1.0" encoding="utf-8"?>
<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
 android:layout_width="match_parent"
 android:layout_height="match_parent">
 <ImageView
 android:id="@+id/backgroundImageView"
 android:layout_width="match_parent"
 android:layout_height="match_parent"
 android:scaleType="centerCrop"
 android:src="@drawable/background_image" />
 <TextView
 android:id="@+id/textView"
 android:layout_width="wrap_content"
 android:layout_height="wrap_content"
 android:layout_centerInParent="true"
 android:text="@string/hello" />
</RelativeLayout>
Y la parte de los idiomas me perdi entre carpetas se que se usa el values-es /fr y los lenguajes pero
no se como llamarlos para que ejecuten en el programa
