AccelerometerPlayActivity extens Activity
	onCreate() -> setView(SimulationView)
	Created class -> SimulationView extends View implements SensorEventListener
						 Created Class -> Particle, ParticleSystem
						 View Callbacks -> View.OnsizeChanged() View.OnDraw()
						 Sensor Callbacks -> OnSensorChanged(), OnAccuracyChanged

AlarmActivity extends Activity
	onCreate() -> clicklisteners added to two buttons
					(one to start AlarmService)
					(one to stop AlarmService)

AlarmService extends Service
	onCreate() -> ShowNotification()
				  Start new Thread with a Runnable Task;
	onDestroy() -> showNotification()
				   stop thread.


Beam extends Activity implements CreateNDEFMessageCallback, OnNDEFPushCompleteCallback
	onCreate, onResume, onNewIntent, onCreateOptionsMenu, onOptionsItemSelected
			callback -> CreateNDEFMessage(NFCEvent event)
			callback -> onNDEFPushComplete(NFCEvent event)
	a handler
	
BusinessCardActivity extends Activity
	onCreate() -> (buttonclick)PickContact() -> startActivityforResult() ->(callback)onActivityResult ->loadContactInfo -> starts AsyncTask ->binds results

CompassActivity extends Activity implements Renderer, Sensoreventlistener
		Renderer callbacks -> onDrawFrame, onSurfaceChanged, onSurfaceCreated
		Sensor callbacks -> onAccuracyChanged, onSensorChanged

ContactManager extends Activity
	onCreate() -> click listeners added to two buttons
					(one starts an Intent of another activity)
					(one shows contacts)
	showcontacts button click -> populatecontactlist() -.getContacts() -> then populate
