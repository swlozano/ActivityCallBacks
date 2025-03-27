<img width="668" alt="Captura de pantalla 2025-03-26 a la(s) 11 36 58 p  m" src="https://github.com/user-attachments/assets/b682d99e-302e-4caa-8add-e59a6152d3a5" />

<activity
            android:name=".MainActivity"
            android:exported="true"
            android:configChanges="orientation|screenLayout|screenSize"
            >

override fun onConfigurationChanged(newConfig: Configuration) {
        super.onConfigurationChanged(newConfig)
        Log.d(TAG, "onConfigurationChanged: $newConfig")
    }
