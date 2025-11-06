package com.tutlane.buttonexample;

import android.os.Bundle;
import android.view.View;
import android.widget.ImageButton;
import android.widget.Button;
import android.widget.ToggleButton;
import android.widget.Toast;
import androidx.appcompat.app.AppCompatActivity;

public class MainActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
    }

    // Step 2 & 3: Event Handlers with Toast messages
    public void onStandardButtonClick(View view) {
        Toast.makeText(getApplicationContext(), "Standard Button Clicked", Toast.LENGTH_SHORT).show();
    }

    public void onImageButtonClick(View view) {
        Toast.makeText(getApplicationContext(), "Image Button Clicked", Toast.LENGTH_SHORT).show();
    }

    public void onToggleButtonClick(View view) {
        ToggleButton toggle = (ToggleButton) view;
        if (toggle.isChecked()) {
            Toast.makeText(getApplicationContext(), "Toggle is ON", Toast.LENGTH_SHORT).show();
        } else {
            Toast.makeText(getApplicationContext(), "Toggle is OFF", Toast.LENGTH_SHORT).show();
        }
    }
}
