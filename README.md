# Android_Review_5
Linear Layout &amp; Click Handler


1. create a project in android studio, and design a layout using constraintLayout style, and add 5 TextViews + 2 Buttons.

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


       // MainActivity.kt
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

 4. databinding without databind modules.
 

             // MainActivity.kt
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
                     
                            
                          val boxOneText = findViewById<TextView>(R.id.text_one)
                          val boxTwoText = findViewById<TextView>(R.id.text_two)
                          val boxThreeText = findViewById<TextView>(R.id.text_three)
     
                          val rootLayout = findViewById<View>(R.id.constraint_layout)

                          val redButton = findViewById<Button>(R.id.button_red)
                          val greenButton = findViewById<Button>(R.id.button_blue)
                          
                          // 將畫面中元件組成一個集合型別 List<> 的實例
                          // 這些集合中的成員皆為 View 型別
                          // val seperateView: List<View> 為宣告
                          // val seperateView: List<View> = ListOf (a, b, c) 為定義
                          
                          val seperateView: List<View> = ListOf (
                       
                            boxOneText, boxTwoText, boxThreeText, 
                            rootLayout, redButton, greenButton
                          
                          )
                          
                          // for-in loop
                          // setOnClickListner  不只可在 Button 也可以在 TextView 上添加
                          for (i in eperateView){
                             i.setOnClickListner{ wrappedFun(it) }
                          }



                     }

                     private fun wrappedFun(view: View){
                     
                            when(view.id) {
                            
                                // lambda
                                // {param -> body}
                                // (param) -> {body}
                                
                                // use color class
                                R.id.text_one -> view.setBackgroundColor(Color.BLUE)
                                R.id.text_two -> view.setBackgroundColor(Color.PURPLE)
                                R.id.text_three -> view.setBackgroundColor(Color.GREEN)
                                
                                // use customed color 
                                R.id.button_red -> text_two.setBackgroundResource(R.color.my_pink)
                                R.id.button_blue -> text_one.setBackgroundResource(R.color.my_pink) 
                                
                                else -> view.setBackgroundColor(Color.GREEN)
                            
                            
                            }

                     }

              }

