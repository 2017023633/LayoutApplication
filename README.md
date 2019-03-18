# LayoutApplication
layout  
**代码功能：**  
实现线性布局，约束布局，表格布局。  
**线性布局代码：**  
```
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"
    tools:context=".LinearlayoutActivity"
    android:orientation="vertical">
    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:orientation="horizontal">
        <Button
            android:id="@+id/b11"
            android:layout_width="0dp"
            android:layout_weight="1"
            android:layout_height="wrap_content"
            android:text="One,One"
            android:textAllCaps="false" />
        <Button
            android:id="@+id/b12"
            android:layout_width="0dp"
            android:layout_weight="1"
            android:layout_height="wrap_content"
            android:text="One,Two"
            android:textAllCaps="false"/>
        <Button
            android:id="@+id/b13"
            android:layout_width="0dp"
            android:layout_weight="1"
            android:layout_height="wrap_content"
            android:text="One,Three"
            android:textAllCaps="false"/>
        <Button
            android:id="@+id/b14"
            android:layout_width="0dp"
            android:layout_weight="1"
            android:layout_height="wrap_content"
            android:text="One,Four"
            android:textAllCaps="false"/>
    </LinearLayout>
    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:orientation="horizontal">
        <Button
            android:id="@+id/b21"
            android:layout_width="0dp"
            android:layout_weight="1"
            android:layout_height="wrap_content"
            android:text="Two,One"
            android:textAllCaps="false" />
        <Button
            android:id="@+id/b22"
            android:layout_width="0dp"
            android:layout_weight="1"
            android:layout_height="wrap_content"
            android:text="Two,Two"
            android:textAllCaps="false"/>
        <Button
            android:id="@+id/b23"
            android:layout_width="0dp"
            android:layout_weight="1"
            android:layout_height="wrap_content"
            android:text="Two,Three"
            android:textAllCaps="false"/>
        <Button
            android:id="@+id/b24"
            android:layout_width="0dp"
            android:layout_weight="1"
            android:layout_height="wrap_content"
            android:text="Two,Four"
            android:textAllCaps="false"/>

    </LinearLayout>
    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:orientation="horizontal">
        <Button
            android:id="@+id/b31"
            android:layout_width="0dp"
            android:layout_weight="1"
            android:layout_height="wrap_content"
            android:text="Three,One"
            android:textAllCaps="false" />
        <Button
            android:id="@+id/b32"
            android:layout_width="0dp"
            android:layout_weight="1"
            android:layout_height="wrap_content"
            android:text="Three,Two"
            android:textAllCaps="false"/>
        <Button
            android:id="@+id/b33"
            android:layout_width="0dp"
            android:layout_weight="1"
            android:layout_height="wrap_content"
            android:text="Three,Three"
            android:textAllCaps="false"/>
        <Button
            android:id="@+id/b34"
            android:layout_width="0dp"
            android:layout_weight="1"
            android:layout_height="wrap_content"
            android:text="Three,Four"
            android:textAllCaps="false"/>
    </LinearLayout>
    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:orientation="horizontal">
        <Button
            android:id="@+id/b41"
            android:layout_width="0dp"
            android:layout_weight="1"
            android:layout_height="wrap_content"
            android:text="Four,One"
            android:textAllCaps="false" />
        <Button
            android:id="@+id/b42"
            android:layout_width="0dp"
            android:layout_weight="1"
            android:layout_height="wrap_content"
            android:text="Four,Two"
            android:textAllCaps="false"/>
        <Button
            android:id="@+id/b43"
            android:layout_width="0dp"
            android:layout_weight="1"
            android:layout_height="wrap_content"
            android:text="Four,Three"
            android:textAllCaps="false"/>
        <Button
            android:id="@+id/b44"
            android:layout_width="0dp"
            android:layout_weight="1"
            android:layout_height="wrap_content"
            android:text="Four,Four"
            android:textAllCaps="false"/>
    </LinearLayout>
</LinearLayout>
```
**线性布局截图：**  
![image text](https://github.com/2017023633/hello-world/blob/master/image/%E5%AE%9E%E9%AA%8C2.1%E6%88%AA%E5%9B%BE.png)  
  
**约束布局代码:**  
```
<?xml version="1.0" encoding="utf-8"?>
<android.support.constraint.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:id="@+id/b1"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:background="@android:color/background_dark">

    <Button
        android:id="@+id/button"
        android:layout_width="66dp"
        android:layout_height="61dp"
        android:background="@android:color/holo_red_dark"
        android:text="RED"
        android:textColor="@android:color/background_dark"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent" />

    <Button
        android:id="@+id/button2"
        android:layout_width="wrap_content"
        android:layout_height="61dp"
        android:layout_marginStart="72dp"
        android:layout_marginLeft="72dp"
        android:background="@android:color/holo_orange_dark"
        android:text="ORANGE"
        app:layout_constraintStart_toEndOf="@+id/button"
        app:layout_constraintTop_toTopOf="parent" />

    <Button
        android:id="@+id/button3"
        android:layout_width="92dp"
        android:layout_height="63dp"
        android:background="@color/colorAccent"
        android:text="YELLOW"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintTop_toTopOf="parent" />

    <Button
        android:id="@+id/button5"
        android:layout_width="66dp"
        android:layout_height="58dp"
        android:layout_marginStart="72dp"
        android:layout_marginLeft="72dp"
        android:layout_marginTop="56dp"
        android:background="@android:color/holo_green_light"
        android:text="GREEN"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/button" />

    <Button
        android:id="@+id/button6"
        android:layout_width="64dp"
        android:layout_height="60dp"
        android:layout_marginStart="24dp"
        android:layout_marginLeft="24dp"
        android:layout_marginTop="56dp"
        android:background="@android:color/holo_blue_dark"
        android:text="BLUE"
        app:layout_constraintStart_toEndOf="@+id/button5"
        app:layout_constraintTop_toBottomOf="@+id/button2" />

    <Button
        android:id="@+id/button7"
        android:layout_width="65dp"
        android:layout_height="58dp"
        android:layout_marginStart="24dp"
        android:layout_marginLeft="24dp"
        android:layout_marginTop="56dp"
        android:background="@android:color/holo_purple"
        android:text="INDIGO"
        app:layout_constraintStart_toEndOf="@+id/button6"
        app:layout_constraintTop_toBottomOf="@+id/button2" />

    <Button
        android:id="@+id/button8"
        android:layout_width="406dp"
        android:layout_height="84dp"
        android:layout_marginStart="8dp"
        android:layout_marginLeft="8dp"
        android:layout_marginEnd="8dp"
        android:layout_marginRight="8dp"
        android:layout_marginBottom="228dp"
        android:background="@color/colorPrimary"
        android:text="VIOLET"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent" />

</android.support.constraint.ConstraintLayout>
```
**约束布局截图:**  
![image text](https://github.com/2017023633/hello-world/blob/master/image/%E5%AE%9E%E9%AA%8C2.2%E6%88%AA%E5%9B%BE.png)  
  
**表格布局代码:**  
```
<?xml version="1.0" encoding="utf-8"?>
<TableLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:background="#ff000000"
    android:stretchColumns="1">
    <TableRow>
        <TextView
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="Open..."
            android:textColor="#FFFFFF"
            android:gravity="left"
            android:layout_column="0"/>
        <TextView
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="Ctrl-O"
            android:textColor="#FFFFFF"
            android:gravity="right"
            android:layout_column="1"/>
    </TableRow>
    <TableRow>
        <TextView
            android:text="Save..."
            android:textColor="#FFFFFF"
            android:layout_column="0"
            android:gravity="left"/>
        <TextView
            android:text="Ctrl-S"
            android:textColor="#FFFFFF"
            android:layout_column="1"
            android:gravity="right"/>
    </TableRow>
    <TableRow>
        <TextView
            android:text="Save As..."
            android:textColor="#FFFFFF"
            android:layout_column="0"
            android:gravity="left"/>
        <TextView
            android:text="Ctrl-Shift-S"
            android:textColor="#FFFFFF"
            android:layout_column="1"
            android:gravity="right"/>
    </TableRow>
    <View
        android:layout_height="1dp"
        android:layout_width="match_parent"
        android:background="#FFFFFF"/>
    <TableRow>
        <TextView
            android:text="X Import..."
            android:textColor="#FFFFFF"
            android:layout_column="0"
            android:gravity="left"/>
    </TableRow>
    <TableRow>
        <TextView
            android:text="X Export..."
            android:textColor="#FFFFFF"
            android:layout_column="0"
            android:gravity="left"/>
        <TextView
            android:text="Ctrl-E"
            android:textColor="#FFFFFF"
            android:layout_column="1"
            android:gravity="right"/>
    </TableRow>
    <View
        android:layout_height="1dp"
        android:layout_width="match_parent"
        android:background="#FFFFFF"/>
    <TableRow>
        <TextView
            android:text="Quit"
            android:textColor="#FFFFFF"
            android:layout_column="0"
            android:gravity="left"/>
    </TableRow>
</TableLayout>
```
**表格布局截图:**  
![image text](https://github.com/2017023633/hello-world/blob/master/image/%E5%AE%9E%E9%AA%8C2.3%E6%88%AA%E5%9B%BE.png)


