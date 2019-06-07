# Week1Day3_HW
Create an activity with an edittext for each item listed below. On a button click, have the values from the edit text save to an Person Object. populate text views for each of the items below from the person object. (You have to make the person class) 
First Name
Last Name
Street Address
City
State
Zip

Solution files:

activity_main.xml:

<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    tools:context=".MainActivity">

    <TextView
        android:id="@+id/nameFirstDisplay"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:textSize="30sp" />

    <TextView
        android:id="@+id/nameLastDisplay"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:textSize="30sp" />

    <TextView
        android:id="@+id/addressDisplay"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:textSize="30sp" />
    <TextView
        android:id="@+id/cityDisplay"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:textSize="30sp" />
    <TextView
        android:id="@+id/stateDisplay"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:textSize="30sp" />
    <TextView
        android:id="@+id/zipDisplay"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:textSize="30sp" />
    <EditText
        android:id="@+id/editNameFirstDisplay"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:hint="Enter first name:"

        />

    <EditText
        android:id="@+id/editNameLastDisplay"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:hint="Enter last name"

        />

    <EditText
        android:id="@+id/editAddressDisplay"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:hint="Enter address"

        />


    <EditText
        android:id="@+id/editStateDisplay"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:hint="Enter state "

        />

    <EditText
        android:id="@+id/editCityDisplay"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:hint="Enter city "

        />

    <EditText
        android:id="@+id/editZipDisplay"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:hint="Enter ZIP "

        />

    <Button
        android:id="@+id/btnProcessInfo"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:onClick="onClick"
        android:text="Press To Proceed" />
</LinearLayout>

MainActivity.java:

    public class MainActivity extends AppCompatActivity {

    TextView nameFirstDisplay;
    EditText editNameFirstDisplay;
    TextView nameLastDisplay;
    EditText editNameLastDisplay;
    TextView addressDisplay;
    EditText editAddressDisplay;
    TextView cityDisplay;
    EditText editCityDisplay;
    TextView stateDisplay;
    EditText editStateDisplay;
    TextView zipDisplay;
    EditText editZipDisplay;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        nameFirstDisplay = findViewById(R.id.nameFirstDisplay);
        editNameFirstDisplay = findViewById(R.id.editNameFirstDisplay);
        nameLastDisplay = findViewById(R.id.nameLastDisplay);
        editNameLastDisplay = findViewById(R.id.editNameLastDisplay);
        addressDisplay = findViewById(R.id.addressDisplay);
        editAddressDisplay = findViewById(R.id.editAddressDisplay);
        cityDisplay = findViewById(R.id.cityDisplay);
        editCityDisplay = findViewById(R.id.editCityDisplay);
        stateDisplay = findViewById(R.id.stateDisplay);
        editStateDisplay = findViewById(R.id.editStateDisplay);
        zipDisplay = findViewById(R.id.zipDisplay);
        editZipDisplay = findViewById(R.id.editZipDisplay);
    }

    public void onClick(View view) {
        String firstName = editNameFirstDisplay.getText().toString();
        String lastName = editNameLastDisplay.getText().toString();
        String address = editAddressDisplay.getText().toString();
        String city = editCityDisplay.getText().toString();
        String state = editStateDisplay.getText().toString();
        String zip = editZipDisplay.getText().toString();
        nameFirstDisplay.setText(firstName);
        nameLastDisplay.setText(lastName);
        addressDisplay.setText(address);
        cityDisplay.setText(city);
        stateDisplay.setText(state);
        zipDisplay.setText(zip);
    }
    }

![Screen Shot 2019-06-06 at 8 32 24 PM](https://user-images.githubusercontent.com/51377398/59075056-8d651b00-889c-11e9-9418-fdda2aa574d0.png)
![Screen Shot 2019-06-06 at 8 33 29 PM](https://user-images.githubusercontent.com/51377398/59075057-8d651b00-889c-11e9-8cb7-1f17a530eaf4.png)
