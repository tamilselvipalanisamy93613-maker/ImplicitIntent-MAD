# Ex.No:3a Develop program to create a text field and a button “Navigate”. When you enter “www.gmail.com” and press navigate button it should open google page using Implicit Intents.


## AIM:

To create a navigate button using Implicit Intent to display the gmail page using Android Studio.

## EQUIPMENTS REQUIRED:

Latest Version Android Studio

## ALGORITHM:

Start the program.
Create a new Android application.
Design the layout with an EditText and a Navigate button.
Enter the website URL in the text field.
Set an OnClickListener for the Navigate button.
Create an Intent using Intent.ACTION_VIEW.
Pass the website URL using Uri.parse().
Call startActivity() to open the website in the browser.
Stop the program.


## PROGRAM:
```
/*
Program to print the text “Implicitintent”.
Developed by:TAMILSELVI P
Registeration Number :212225040460
*/
```
# Activitymain2.xml
```
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout
    xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:gravity="center"
    android:padding="20dp">

    <EditText
        android:id="@+id/url"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:hint="Enter Website"
        android:text="https://www.gmail.com"
        android:inputType="textUri"/>

    <Button
        android:id="@+id/btnImplicit"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Implicit Intent"/>

</LinearLayout>
```
# mainActivity2.java
```
package com.example.test;

import android.content.Intent;
import android.net.Uri;
import android.os.Bundle;
import android.widget.Button;
import android.widget.EditText;

import androidx.appcompat.app.AppCompatActivity;

public class MainActivity2 extends AppCompatActivity {

    EditText url;
    Button btnImplicit;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main2);

        url = findViewById(R.id.url);
        btnImplicit = findViewById(R.id.btnImplicit);

        btnImplicit.setOnClickListener(v -> {

            String website = url.getText().toString();

            Intent intent = new Intent(
                    Intent.ACTION_VIEW,
                    Uri.parse(website)
            );

            startActivity(intent);
        });
    }
}
```


## OUTPUT
<img width="1917" height="1078" alt="Screenshot 2026-11-01 135722" src="https://github.com/user-attachments/assets/bf82b0b5-6c50-4bb1-a7d3-52ae4de96dfd" />

<img width="1917" height="1078" alt="Screenshot 2026-11-01 135616" src="https://github.com/user-attachments/assets/0ee843c9-63a0-4d58-a923-b54ec9d2d75b" />

<img width="1917" height="1078" alt="Screenshot 2026-11-01 135737" src="https://github.com/user-attachments/assets/a848e930-3841-4f0a-8412-7f6edddca0f9" />

## RESULT
Thus a Simple Android Application create a navigate button using Implicit Intent to display the gmail page using Android Studio is developed and executed successfully.


