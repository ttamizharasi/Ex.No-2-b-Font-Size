
# Ex.No:2 Develop an application that uses GUI Components with Fonts and Colors


## AIM:
To develop an application that uses GUI Components with Fonts and Colors using android studio.

## EQUIPMENTS REQUIRED:

Android Studio(Min. required Artic Fox)


## ALGORITHM:
Step 1: Create a New Android Project:
              • Click New in the toolbar.
              • In the window that appears, open the Android folder, select Android Application Project,
              and click next.
              • Provide the application name and the project name and then finally give the desired
              package name.
              • Choose a launcher icon for your application and then select Blank Activity and then click
              Next
              • Provide the desired Activity name for your project and then click Finish.

Step 2: Create a New AVD (Android Virtual Device):
        • click Android Virtual Device Manager from the toolbar.
        • In the Android Virtual Device Manager panel, click New.
        • Fill in the details for the AVD. Give it a name, a platform target, an SD card size, and
        a skin (HVGA is default).
        • Click Create AVD and Select the new AVD from the Android Virtual Device
        Manager and click Start.

Step 3: Design the graphical layout with a text view and two command buttons.

Step 4: Run the application.

Step 5:On pressing the change font size button, the size of the font gets altered.

Step 6: On pressing the Color button, the color of the text altered.
       
Step 6:Close the Android project. 


## Program:
 ```
/*
Program to Develop an application that uses Font Size using Android Studio .
Developed by: Nandhini S
RegisterNumber: 212222220028 
*/
```

## MainActivity.java:
```

package com.firstapp.fontsize;

import androidx.appcompat.app.AppCompatActivity;

import android.os.Bundle;

import android.app.Activity;
import android.graphics.Typeface;
import android.graphics.Color;
import android.view.View;
import android.widget.Button;
import android.widget.TextView;


public class MainActivity extends AppCompatActivity {
    float font = 24;
    int i = 1;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        final TextView t1 = (TextView)findViewById(R.id.textView1);
        Button b1 = (Button)findViewById(R.id.button1);
        b1.setOnClickListener(new View.OnClickListener()    {
            public void onClick(View view) {
                t1.setTextSize(font);
                font = font+4;
                if(font==40)
                    font = 20;
            }
        });


    }
}


```


## activity_main.xml:
<?xml version="1.0" encoding="utf-8"?>
<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">


    <TextView
        android:id="@+id/textView1"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_margin="70dp"
        android:gravity="left"
        android:text="HELLO WORLD"
        android:textSize="20sp"
        android:textStyle="bold"
        tools:layout_editor_absoluteX="70dp"
        tools:layout_editor_absoluteY="376dp" />

    <Button
        android:id="@+id/button1"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_margin="20sp"
        android:gravity="center"
        android:text="Change Font Size"
        tools:layout_editor_absoluteX="40dp"
        tools:layout_editor_absoluteY="456dp" />
    </RelativeLayout>


## Output:

![Screenshot 2024-09-14 133440](https://github.com/user-attachments/assets/7db27a7b-8acf-4790-8b10-1d3dc2fcda8f)

 
 ![Screenshot 2024-09-14 133518](https://github.com/user-attachments/assets/50c3cbd7-8e26-4744-900a-b2718f33d524)



## Result:
Thus, the program for android application, Font Size and color was executed successfully using Android Studio.
