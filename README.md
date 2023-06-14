# Ex_No_11_Thread-Synchronization
Develop a program to perform Thread Synchronization using Android Studio 
## AIM:
To Develop a program to perform Thread Synchronization using Android Studio.

## EQUIPMENTS REQUIRED:

Android Studio(Min. required Artic Fox)


## ALGORITHM:
Step 1: Open Android Studio and then click on File -> New -> New project.

Step 2: Then type the Application name as SMSIntent and click Next.

Step 3: Select the Minimum SDK below and click Next.

Step 4: Then select the Empty Activity and click Next. Finally, click Finish.

Step 5: Design layout in activity_main.xml.

Step 6: Thread Synchronization processing is done in MainActivity.java

Step 7: Save and run the application.


## Program:
 ```
/*
Program to create an Option Menu
Developed by: S.LOKESH SAI DILEEP
RegisterNumber: 212221230111
*/
```

## MainActivity.java:
```
package com.example.threadsyn;

import androidx.appcompat.app.AppCompatActivity;

import android.os.Bundle;
import android.os.Bundle;
import android.os.Handler;
import android.util.Log;
import android.view.View;
import android.widget.TextView;
import androidx.appcompat.app.AppCompatActivity;
import java.util.concurrent.Semaphore;
public class MainActivity extends AppCompatActivity {
    private static final String TAG = "MainActivity";

    // Object used for synchronizing access to counter
    private static final Object lock = new Object();

    // Maximum number of concurrent threads
    // that can access the counter
    private static final int MAX_THREADS = 5;

    // Semaphore to limit concurrent access to the counter
    private static final Semaphore semaphore = new Semaphore(MAX_THREADS);

    // Counter to store the
    // number of button clicks
    private int counter = 0;

    // Reference to the text view to
    // display the number of button clicks
    private TextView textView;
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(
