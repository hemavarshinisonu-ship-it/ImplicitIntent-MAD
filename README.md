# Ex.No:3a Develop program to create a text field and a button “Navigate”. When you enter “www.gmail.com” and press navigate button it should open google page using Implicit Intents.


## AIM:

To create a navigate button using Implicit Intent to display the gmail page using Android Studio.

## EQUIPMENTS REQUIRED:

Latest Version Android Studio

## ALGORITHM:

Step 1: Initialize the Activity

Start the onCreate() method
Create references for EditText and Button UI components
Load the activity_main.xml layout using setContentView()
Step 2: Get UI Components

Find the EditText widget (id: editText) using findViewById()
Find the Button widget (id: btn) using findViewById()
Step 3: Set Button Click Listener

Attach an OnClickListener to the button
Prepare to execute code when the button is clicked
Step 4: Handle Button Click Event

Retrieve the text entered in the EditText using getText().toString()
Store the URL in a String variable
Step 5: Create Implicit Intent

Create a new Intent object with action Intent.ACTION_VIEW
Parse the URL string using Uri.parse()
Pass the parsed URI as data to the Intent
Step 6: Start Activity with Intent

Call startActivity() with the created Intent
The system will find and launch the appropriate application (browser) to handle the URL
Step 7: End

The browser opens and displays the requested URL

## PROGRAM:
```
/*
Program to print the text “Implicitintent”.
Developed by: HEMAVAARSHINI D
Registeration Number :212225220039
*/
```
activity_main.xml
```
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:id="@+id/main"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">

    <TextView
        android:id="@+id/textView"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginBottom="148dp"
        android:text="Implecity Intent"
        app:layout_constraintBottom_toTopOf="@+id/button2"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent" />

    <Button
        android:id="@+id/button2"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginBottom="148dp"
        android:text="Clike Me"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent" />

    <EditText
        android:id="@+id/editTextText"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:ems="10"
        android:inputType="text"
        android:text="Name"
        app:layout_constraintBottom_toTopOf="@+id/textView"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.633" />

</androidx.constraintlayout.widget.ConstraintLayout><?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:id="@+id/main"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">

    <Button
        android:id="@+id/button2"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginBottom="148dp"
        android:text="Clike Me"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent" />

    <EditText
        android:id="@+id/editTextText"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:ems="10"
        android:inputType="text"
        android:text="LINK"
        android:textColorLink="#E6C2C2"
        app:layout_constraintBottom_toTopOf="@+id/button2"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.497"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent" />

    <TextView
        android:id="@+id/textView3"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="IMPLICIT_INTENT"
        android:textColorLink="#3F51B5"
        android:textSize="34sp"
        app:layout_constraintBottom_toTopOf="@+id/editTextText"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent" />

</androidx.constraintlayout.widget.ConstraintLayout>
```
Mainactivity.java
```
package com.example.implicit;

import android.content.Intent;
import android.net.Uri;
import android.os.Bundle;
import android.widget.Button;

import androidx.appcompat.app.AppCompatActivity;

public class MainActivity extends AppCompatActivity {

    Button button;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        button = findViewById(R.id.button2);

        button.setOnClickListener(view -> {
            Intent intent = new Intent(Intent.ACTION_VIEW, Uri.parse("https://mail.google.com"));
            startActivity(intent);
        });
    }
}
```
## OUTPUT
<img width="1920" height="1080" alt="Screenshot (76)" src="https://github.com/user-attachments/assets/0669f133-913a-4e00-991c-ad4a7f4cd85f" />

<img width="1920" height="1080" alt="Screenshot (77)" src="https://github.com/user-attachments/assets/330359c7-745b-4b6d-a8fc-a78cbcba8c8b" />

<img width="1920" height="1080" alt="Screenshot (65)" src="https://github.com/user-attachments/assets/33b98e9e-48ca-467c-92da-2175cfa8ed3f" />

## RESULT
Thus a Simple Android Application create a navigate button using Implicit Intent to display the gmail page using Android Studio is developed and executed successfully.


