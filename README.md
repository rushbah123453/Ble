# Ble
bluetooth_scan

This application is used to 1)Enable 2)Disable 3)Discover and 4)Scan bluetooth devices 
It contains 3 classes 1)MainActivity 2)DeviceListctivity 3)DeviceListAdapter and 3 xml files

Main screen includes 3 buttons 1)disable 2)paired 3)scan_devices  and 1 textView for status 1)Bluetooth is on/off

Permission added :-

  <uses-permission android:name="android.permission.BLUETOOTH" />
    <uses-permission android:name="android.permission.BLUETOOTH_ADMIN" />

Coarse location and Fine location are optional for android 5.0 and below versions

<uses-permission android:name="android.permission.ACCESS_COARSE_LOCATION"/>
    <uses-permission android:name="android.permission.ACCESS_FINE_LOCATION"/>
    
    
    Broadcast reciever is used :-
    
        private final BroadcastReceiver mPairReceiver = new BroadcastReceiver() {
	    public void onReceive(Context context, Intent intent) {
	        String action = intent.getAction();
	        
	    //if paired
            show paired device
         else 
            no paired device
      
	        	 mAdapter.notifyDataSetChanged();
	        }
	    }
	};
    
