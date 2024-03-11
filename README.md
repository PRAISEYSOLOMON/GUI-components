# Ex.No: 1 To develop an application that uses GUI Components with Fonts and Colors. 
Note: Create button for colors and fonts while clicking color or font button should change 


## AIM:

To create an application that uses GUI Components with Fonts and Colors using Android Studio.

## EQUIPMENTS REQUIRED:

Latest Version Android Studio

## ALGORITHM:

1.Start a new project in Android Studio.

2.Design a simple layout(.xml File).

3.Inside MainActivity.java , create the button function

4.Create button for colors and fonts while clicking color or font button should change the color and font.

5.Display corresponding changes in application.

## PROGRAM:
```
/*
Program to print the text “GUIcomponent”.
Developed by: PRAISEY S
Registeration Number : 212222040117
*/
```
## activity_main.xml
```
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">

    <TextView
        android:id="@+id/textView"
        android:layout_width="175dp"
        android:layout_height="61dp"
        android:layout_marginTop="180dp"
        android:text="Hello..!"
        android:textSize="48sp"
        app:layout_constraintBottom_toTopOf="@+id/button"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        tools:ignore="UnknownId" />

    <Button
        android:id="@+id/button1"
        android:layout_width="214dp"
        android:layout_height="68dp"
        android:layout_marginTop="344dp"
        android:text="Change font size"
        android:textColorLink="#471E1E"
        app:layout_constraintBottom_toTopOf="@+id/button2"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.497"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.0" />

    <Button
        android:id="@+id/button2"
        android:layout_width="221dp"
        android:layout_height="71dp"
        android:text="Change font color"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.515"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.68" />
</androidx.constraintlayout.widget.ConstraintLayout>
```
## MainActivity.java
```
package com.example.guicomponents;

import android.graphics.Color;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.TextView;

import androidx.appcompat.app.AppCompatActivity;

public class MainActivity extends AppCompatActivity
{
    int ch=1;
    float font=30;
    @Override
    protected void onCreate(Bundle savedInstanceState)
    {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        final TextView t= (TextView) findViewById(R.id. textView);
        Button b1= (Button) findViewById(R.id.button1);
        b1.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                t.setTextSize(font);
                font = font + 5;
                if (font == 50)
                    font = 30;
            }
        });
        Button b2= (Button) findViewById(R.id.button2);
        b2.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                switch (ch) {
                    case 1:
                        t.setTextColor(Color.RED);
                        break;
                    case 2:
                        t.setTextColor(Color.GREEN);
                        break;
                    case 3:
                        t.setTextColor(Color.BLUE);
                        break;
                    case 4:
                        t.setTextColor(Color.CYAN);
                        break;
                    case 5:
                        t.setTextColor(Color.YELLOW);
                        break;
                    case 6:
                        t.setTextColor(Color.MAGENTA);
                        break;
                }
                ch++;
                if (ch == 7)
                    ch = 1;
            }
        });
    }
}
```

## OUTPUT

![op 1 1](https://github.com/PRAISEYSOLOMON/GUI-components/assets/119394259/9c07c8a4-876e-48c3-a39e-f525f2d1efd8)

![op 1 2](https://github.com/PRAISEYSOLOMON/GUI-components/assets/119394259/1cc812c0-b5ea-4c01-8a12-4fd5d363a5f0)

![op 1 3](https://github.com/PRAISEYSOLOMON/GUI-components/assets/119394259/cac42761-922b-4935-b864-9b3976f7ab64)

![out 1 4](https://github.com/PRAISEYSOLOMON/GUI-components/assets/119394259/90182463-8931-4c21-a757-b3db9eb654db)


## RESULT
Thus a Simple Android Application that uses GUI Components with Fonts and Colors using Android Studio is developed and executed successfully.


