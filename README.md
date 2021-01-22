# Android_Review_5
Linear Layout &amp; Click Handler


1. create a project in android studio, and design a layout using constraintLayout style, and add 7 TextViews + 2 Buttons.

       // activity_main.kt
       
       <?xml encoding="utf-8"?>
       
       <androidx.constraintlayout.widget.ConstraintLayout
        xmlns:android=""
        xmlns:app=""
        xmlns:tools=""
        tools:context=".MainActivity"
        android:id=""
       >
       
       <TextView
          android:id="@+id/text_one"
       />
       
       <TextView
           android:id="@+id/text_two"
       />
       
       <TextView
          android:id="@+id/text_three"
       />
       
       <TextView
           android:id="@+id/text_four"
       />
       
       <TextView
            android:id="@+id/text_five"
       />
       
       <TextView
            android:id="@+id/label_text"
       />
       
       <TextView
            android:id="@+id/info_text"
       />
       
       <Button
            android:id="@+id/button_red"
       />
       
       <Button/
            android:id="@+id/button_blue"
       >
       
       </androidx.constraintlayout.widget.ConstraintLayout>
       
 2. to setup properties of TextView and Button.
 
     https://github.com/google-developer-training/android-kotlin-fundamentals-apps/blob/master/ColorMyViews/app/src/main/res/layout/activity_main.xml


3. source lines of code.

       package com.android.example.katesapp
       
       [default modules]
       import androidx.appcompat.app.AppCompatActivity
       import android.os.Bundle
       
       [UI element]
       import android.widget.Button
       import android.widget.TextView
       
       [view]
       import android.view.View
       
       [kotlin]
       import kotlinx.android.synthetic.main.activity_main.*
       
       class MainActivity: AppCompatActivity(){
       
              override fun onCreate(savedInstanceState: Bundle?){
              
                     super.onCreate(savedInstanceState)
                     setContentView(R.layout.activity_main)
                     
                     functionCalled()
              
              
              }
              
              private fun functionCalled(){
              
              
              
              
              }
              
              private fun wrappedFun(){
              
              
              
              }
       
      
       }

   
