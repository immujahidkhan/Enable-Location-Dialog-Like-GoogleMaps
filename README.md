# Enable-Location-Dialog-Like-GoogleMaps
Enable Location Dialog Like Google Maps

```
allprojects {
		repositories {
			...
			maven { url 'https://jitpack.io' }
		}
	}

dependencies {
	        implementation 'com.github.immujahidkhan:Enable-Location-Dialog-Like-GoogleMaps:1.0'
	}
```
#Usage

```
  new GpsUtils(this).turnGPSOn(AppConstants.GPS_REQUEST, new GpsUtils.onGpsListener() {
            @Override
            public void gpsStatus(boolean isGPSEnable) {
                // turn on GPS
                isGPS = isGPSEnable;
                Toast.makeText(MainActivity.this, "" + isGPSEnable, Toast.LENGTH_SHORT).show();
            }
        });
	
 @Override
    protected void onActivityResult(int requestCode, int resultCode, Intent data) {
        super.onActivityResult(requestCode, resultCode, data);
        if (resultCode == Activity.RESULT_OK) {
            if (requestCode == AppConstants.GPS_REQUEST) {
                isGPS = true; // flag maintain before get location
                //do What ever you want to do
            }
        }
    }
```
