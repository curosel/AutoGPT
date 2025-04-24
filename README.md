Bongoprahari: সম্পূর্ণ মোবাইল সলিউশনTagline: Nirapod BangladeshভূমিকাBongoprahari হল একটি সম্পূর্ণ মোবাইল-ভিত্তিক সিকিউরিটি সলিউশন যা শুধুমাত্র এন্ড্রয়েড মোবাইল ফোন ব্যবহার করে বাস্তবায়ন করা যায়। এই ডকুমেন্টে আমরা Bongoprahari সিস্টেমের সমস্ত কম্পোনেন্ট একত্রিত করে একটি সম্পূর্ণ সমাধান প্রদান করব, যা NFC ট্রান্সফার, আইপি ক্যামেরা ইন্টিগ্রেশন, এবং ইউনিভার্সাল UI/UX ডিজাইন অন্তর্ভুক্ত করে।সিস্টেম ওভারভিউBongoprahari সিস্টেম নিম্নলিখিত মূল কম্পোনেন্ট নিয়ে গঠিত:1.NFC ট্রান্সফার মডিউল: ফোন-টু-ফোন ডাটা ট্রান্সফার এবং সিস্টেম অ্যাক্টিভেশন2.আইপি ক্যামেরা মডিউল: 360° আইপি ক্যামেরা এবং অন্যান্য ক্যামেরা ইন্টিগ্রেশন3.ইউনিভার্সাল UI/UX: সকল বয়সের ব্যবহারকারীদের জন্য আকর্ষণীয় ইন্টারফেস4.সিকিউরিটি ফিচার: ডাটা এনক্রিপশন এবং সিকিউর কমিউনিকেশন5.মোবাইল-অপ্টিমাইজড পারফরম্যান্স: ব্যাটারি, মেমরি, এবং নেটওয়ার্ক অপ্টিমাইজেশনসম্পূর্ণ সিস্টেম আর্কিটেকচারহাই-লেভেল আর্কিটেকচারCopy+------------------------------------------+
|             Bongoprahari App             |
+------------------------------------------+
|                                          |
|  +-------------+       +---------------+ |
|  |    Core     |<----->|  UI/UX Layer  | |
|  |   Module    |       |               | |
|  +-------------+       +---------------+ |
|        ^                      ^          |
|        |                      |          |
|        v                      v          |
|  +-------------+       +---------------+ |
|  |     NFC     |<----->|  IP Camera    | |
|  |    Module   |       |    Module     | |
|  +-------------+       +---------------+ |
|        ^                      ^          |
|        |                      |          |
|        v                      v          |
|  +-------------+       +---------------+ |
|  |    Data     |<----->|   Security    | |
|  |   Module    |       |    Module     | |
|  +-------------+       +---------------+ |
|                                          |
+------------------------------------------+
         ^                    ^
         |                    |
         v                    v
+------------------+  +-------------------+
| External Devices |  | Network Services  |
| (NFC, Bluetooth) |  | (IP Cameras, API) |
+------------------+  +-------------------+
কম্পোনেন্ট ইন্টারঅ্যাকশন1.কোর মডিউল: সিস্টেমের কেন্দ্রীয় কম্পোনেন্ট, অন্যান্য সকল মডিউলের মধ্যে সমন্বয় সাধন করে2.UI/UX লেয়ার: ইউজার ইন্টারফেস এবং ইউজার এক্সপেরিয়েন্স প্রদান করে3.NFC মডিউল: NFC কমিউনিকেশন এবং ডাটা ট্রান্সফার হ্যান্ডল করে4.আইপি ক্যামেরা মডিউল: ক্যামেরা ডিসকভারি, কানেকশন, এবং ভিডিও স্ট্রিমিং হ্যান্ডল করে5.ডাটা মডিউল: ডাটা স্টোরেজ, রিট্রিভাল, এবং সিঙ্ক্রোনাইজেশন হ্যান্ডল করে6.সিকিউরিটি মডিউল: এনক্রিপশন, অথেনটিকেশন, এবং সিকিউর কমিউনিকেশন প্রদান করেইনস্টলেশন এবং সেটআপ গাইডপ্রয়োজনীয় সফটওয়্যার1.Termux: কমান্ড লাইন টুলস এবং ডেভেলপমেন্ট এনভায়রনমেন্ট2.AIDE: এন্ড্রয়েড ডেভেলপমেন্ট IDE3.Sketchware Pro: ভিজ্যুয়াল অ্যাপ ডেভেলপমেন্ট টুল4.Git: ভার্সন কন্ট্রোল সিস্টেমইনস্টলেশন স্টেপস1.Termux ইনস্টল করুন:•F-Droid থেকে Termux ডাউনলোড করুন: https://f-droid.org/•Termux ইনস্টল করুন এবং খুলুন•প্রয়োজনীয় প্যাকেজ ইনস্টল করুন:Copypkg update && pkg upgrade -y
pkg install -y git openssh nodejs-lts openjdk-17 gradle python clang
termux-setup-storage
2.AIDE ইনস্টল করুন:•Google Play Store থেকে AIDE ডাউনলোড করুন•AIDE খুলুন এবং প্রয়োজনীয় SDK কম্পোনেন্ট ডাউনলোড করুন3.প্রজেক্ট সেটআপ করুন:•Termux এ প্রজেক্ট ফোল্ডার তৈরি করুন:Copymkdir -p ~/projects/bongoprahari
cd ~/projects/bongoprahari
•প্রজেক্ট ইনিশিয়ালাইজ করুন:Copy# Git ইনিশিয়ালাইজ করুন
git init
     
# প্রজেক্ট স্ট্রাকচার তৈরি করুন
mkdir -p app/src/main/java/com/bongoprahari/app
mkdir -p app/src/main/res/layout
mkdir -p app/src/main/res/drawable
mkdir -p app/src/main/res/values
4.AIDE এ প্রজেক্ট ওপেন করুন:•AIDE খুলুন•"Open an existing Android Studio project" সিলেক্ট করুন•/storage/emulated/0/projects/bongoprahari পাথ সিলেক্ট করুনNFC ট্রান্সফার সিস্টেম ইমপ্লিমেন্টেশনNFC ট্রান্সফার ওয়ার্কফ্লোCopy+----------------+       +----------------+       +----------------+
| Device A       |       | Device B       |       | Device B       |
| (Sender)       |       | (Receiver)     |       | (Activated)    |
+----------------+       +----------------+       +----------------+
| 1. Initiate    |       |                |       |                |
| Transfer       |       |                |       |                |
+----------------+       +----------------+       +----------------+
        |                        |                        |
        v                        v                        v
+----------------+       +----------------+       +----------------+
| 2. Touch       |------>| 3. Receive     |       | 5. System     |
| Devices        |       | NFC Data       |       | Activated     |
+----------------+       +----------------+       +----------------+
        |                        |                        |
        v                        v                        v
+----------------+       +----------------+       +----------------+
| 4. Send        |------>| 4. Process     |------>| 6. Full       |
| System Data    |       | System Data    |       | Functionality |
+----------------+       +----------------+       +----------------+
NFC ট্রান্সফার ইমপ্লিমেন্টেশনCopy// NfcTransferActivity.java
public class NfcTransferActivity extends AppCompatActivity {
    
    private NfcAdapter nfcAdapter;
    private PendingIntent pendingIntent;
    private IntentFilter[] intentFilters;
    private String[][] techLists;
    private TextView statusTextView;
    private Button activateButton;
    
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_nfc_transfer);
        
        statusTextView = findViewById(R.id.status_text_view);
        activateButton = findViewById(R.id.activate_button);
        
        // NFC অ্যাডাপ্টার ইনিশিয়ালাইজ করুন
        nfcAdapter = NfcAdapter.getDefaultAdapter(this);
        
        // NFC চেক করুন
        if (nfcAdapter == null) {
            statusTextView.setText(R.string.nfc_not_supported);
            activateButton.setEnabled(false);
            return;
        }
        
        if (!nfcAdapter.isEnabled()) {
            statusTextView.setText(R.string.nfc_disabled);
            showEnableNfcDialog();
            return;
        }
        
        // NFC ইন্টেন্ট সেটআপ
        pendingIntent = PendingIntent.getActivity(this, 0, 
                new Intent(this, getClass()).addFlags(Intent.FLAG_ACTIVITY_SINGLE_TOP), 0);
        
        IntentFilter ndefFilter = new IntentFilter(NfcAdapter.ACTION_NDEF_DISCOVERED);
        try {
            ndefFilter.addDataType("application/com.bongoprahari.app");
        } catch (IntentFilter.MalformedMimeTypeException e) {
            Log.e("NfcTransfer", "Failed to add MIME type", e);
        }
        
        intentFilters = new IntentFilter[] {ndefFilter};
        techLists = null;
        
        // অ্যাক্টিভেট বাটন সেটআপ
        activateButton.setOnClickListener(v -> {
            // সিস্টেম অ্যাক্টিভেশন ডাটা তৈরি করুন
            JSONObject activationData = createActivationData();
            
            // NFC মেসেজ তৈরি করুন
            NdefMessage message = createNdefMessage(activationData.toString());
            
            // NFC পুশ মেসেজ সেট করুন
            nfcAdapter.setNdefPushMessage(message, this);
            
            statusTextView.setText(R.string.ready_to_transfer);
            Toast.makeText(this, R.string.touch_devices, Toast.LENGTH_LONG).show();
        });
    }
    
    @Override
    protected void onResume() {
        super.onResume();
        
        if (nfcAdapter != null && nfcAdapter.isEnabled()) {
            nfcAdapter.enableForegroundDispatch(this, pendingIntent, intentFilters, techLists);
        }
    }
    
    @Override
    protected void onPause() {
        super.onPause();
        
        if (nfcAdapter != null && nfcAdapter.isEnabled()) {
            nfcAdapter.disableForegroundDispatch(this);
        }
    }
    
    @Override
    protected void onNewIntent(Intent intent) {
        super.onNewIntent(intent);
        
        // NFC ইন্টেন্ট হ্যান্ডল করুন
        if (NfcAdapter.ACTION_NDEF_DISCOVERED.equals(intent.getAction())) {
            Parcelable[] rawMessages = intent.getParcelableArrayExtra(NfcAdapter.EXTRA_NDEF_MESSAGES);
            if (rawMessages != null) {
                NdefMessage message = (NdefMessage) rawMessages[0];
                NdefRecord record = message.getRecords()[0];
                
                String receivedData = new String(record.getPayload());
                processActivationData(receivedData);
            }
        }
    }
    
    private JSONObject createActivationData() {
        JSONObject data = new JSONObject();
        try {
            data.put("action", "activate");
            data.put("app_id", "com.bongoprahari.app");
            data.put("timestamp", System.currentTimeMillis());
            data.put("device_id", Settings.Secure.getString(getContentResolver(), 
                    Settings.Secure.ANDROID_ID));
            data.put("version", BuildConfig.VERSION_NAME);
            
            // সিকিউরিটি টোকেন যোগ করুন
            String securityToken = generateSecurityToken();
            data.put("security_token", securityToken);
            
        } catch (JSONException e) {
            Log.e("NfcTransfer", "Failed to create activation data", e);
        }
        
        return data;
    }
    
    private String generateSecurityToken() {
        // সিকিউরিটি টোকেন জেনারেট করুন
        byte[] randomBytes = new byte[32];
        new SecureRandom().nextBytes(randomBytes);
        return Base64.encodeToString(randomBytes, Base64.NO_WRAP);
    }
    
    private NdefMessage createNdefMessage(String data) {
        NdefRecord mimeRecord = NdefRecord.createMime(
                "application/com.bongoprahari.app", data.getBytes(Charset.forName("UTF-8")));
        
        NdefRecord aarRecord = NdefRecord.createApplicationRecord("com.bongoprahari.app");
        
        return new NdefMessage(new NdefRecord[] {mimeRecord, aarRecord});
    }
    
    private void processActivationData(String data) {
        try {
            JSONObject activationData = new JSONObject(data);
            
            String action = activationData.getString("action");
            if ("activate".equals(action)) {
                // সিকিউরিটি টোকেন ভেরিফাই করুন
                String securityToken = activationData.getString("security_token");
                if (verifySecurityToken(securityToken)) {
                    // সিস্টেম অ্যাক্টিভেট করুন
                    activateSystem(activationData);
                } else {
                    statusTextView.setText(R.string.invalid_security_token);
                }
            }
            
        } catch (JSONException e) {
            Log.e("NfcTransfer", "Failed to process activation data", e);
            statusTextView.setText(R.string.invalid_data_format);
        }
    }
    
    private boolean verifySecurityToken(String securityToken) {
        // সিকিউরিটি টোকেন ভেরিফিকেশন লজিক
        // এখানে আরও কমপ্লেক্স ভেরিফিকেশন লজিক যোগ করা যেতে পারে
        return securityToken != null && !securityToken.isEmpty();
    }
    
    private void activateSystem(JSONObject activationData) {
        // সিস্টেম অ্যাক্টিভেশন লজিক
        statusTextView.setText(R.string.system_activated);
        
        // অ্যাক্টিভেশন ডাটা সেভ করুন
        SharedPreferences preferences = getSharedPreferences("activation", MODE_PRIVATE);
        preferences.edit()
                .putBoolean("is_activated", true)
                .putLong("activation_time", System.currentTimeMillis())
                .putString("activation_data", activationData.toString())
                .apply();
        
        // মেইন অ্যাক্টিভিটি লঞ্চ করুন
        Intent intent = new Intent(this, MainActivity.class);
        intent.putExtra("activation_data", activationData.toString());
        startActivity(intent);
        finish();
    }
    
    private void showEnableNfcDialog() {
        new AlertDialog.Builder(this)
                .setTitle(R.string.nfc_disabled_title)
                .setMessage(R.string.nfc_disabled_message)
                .setPositiveButton(R.string.settings, (dialog, which) -> {
                    startActivity(new Intent(Settings.ACTION_NFC_SETTINGS));
                })
                .setNegativeButton(R.string.cancel, null)
                .show();
    }
}
আইপি ক্যামেরা ইন্টিগ্রেশনআইপি ক্যামেরা ওয়ার্কফ্লোCopy+----------------+       +----------------+       +----------------+
| 1. Camera      |       | 2. Camera      |       | 3. Camera      |
| Discovery      |------>| Connection     |------>| Streaming      |
+----------------+       +----------------+       +----------------+
        |                        |                        |
        v                        v                        v
+----------------+       +----------------+       +----------------+
| - Auto Scan    |       | - Authentication|      | - Video Display|
| - Manual Add   |       | - Connection    |      | - Recording    |
| - QR Scan      |       |   Testing       |      | - Screenshot   |
+----------------+       +----------------+       +----------------+
                                 |
                                 v
                         +----------------+       +----------------+
                         | 4. Camera      |------>| 5. Camera      |
                         | Control        |       | Settings       |
                         +----------------+       +----------------+
                                 |                        |
                                 v                        v
                         +----------------+       +----------------+
                         | - PTZ Control  |       | - Resolution   |
                         | - Presets      |       | - Framerate    |
                         | - Focus/Zoom   |       | - Night Mode   |
                         +----------------+       +----------------+
আইপি ক্যামেরা ইমপ্লিমেন্টেশনCopy// CameraActivity.java
public class CameraActivity extends AppCompatActivity {
    
    private SurfaceView surfaceView;
    private Button discoverButton;
    private Button connectButton;
    private Button controlButton;
    private RecyclerView cameraListRecyclerView;
    private ProgressBar progressBar;
    
    private IpCameraDiscoveryManager discoveryManager;
    private RtspStreamManager streamManager;
    private List<IpCamera> discoveredCameras = new ArrayList<>();
    private CameraListAdapter cameraListAdapter;
    
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_camera);
        
        // ভিউ ইনিশিয়ালাইজ করুন
        surfaceView = findViewById(R.id.surface_view);
        discoverButton = findViewById(R.id.discover_button);
        connectButton = findViewById(R.id.connect_button);
        controlButton = findViewById(R.id.control_button);
        cameraListRecyclerView = findViewById(R.id.camera_list_recycler_view);
        progressBar = findViewById(R.id.progress_bar);
        
        // ক্যামেরা ডিসকভারি ম্যানেজার ইনিশিয়ালাইজ করুন
        discoveryManager = new IpCameraDiscoveryManager(this, new IpCameraDiscoveryManager.CameraDiscoveryListener() {
            @Override
            public void onCameraDiscovered(IpCamera camera) {
                runOnUiThread(() -> {
                    discoveredCameras.add(camera);
                    cameraListAdapter.notifyDataSetChanged();
                });
            }
            
            @Override
            public void onDiscoveryFinished(List<IpCamera> cameras) {
                runOnUiThread(() -> {
                    progressBar.setVisibility(View.GONE);
                    Toast.makeText(CameraActivity.this, 
                            getString(R.string.cameras_found, cameras.size()), 
                            Toast.LENGTH_SHORT).show();
                });
            }
            
            @Override
            public void onDiscoveryFailed(String errorMessage) {
                runOnUiThread(() -> {
                    progressBar.setVisibility(View.GONE);
                    Toast.makeText(CameraActivity.this, 
                            getString(R.string.discovery_failed, errorMessage), 
                            Toast.LENGTH_LONG).show();
                });
            }
        });
        
        // স্ট্রিম ম্যানেজার ইনিশিয়ালাইজ করুন
        streamManager = new RtspStreamManager(this, surfaceView);
        
        // রিসাইকলার ভিউ সেটআপ করুন
        cameraListAdapter = new CameraListAdapter(discoveredCameras, camera -> {
            // ক্যামেরা সিলেক্ট করা হয়েছে
            connectButton.setEnabled(true);
        });
        
        cameraListRecyclerView.setLayoutManager(new LinearLayoutManager(this));
        cameraListRecyclerView.setAdapter(cameraListAdapter);
        
        // ডিসকভার বাটন সেটআপ করুন
        discoverButton.setOnClickListener(v -> {
            progressBar.setVisibility(View.VISIBLE);
            discoveredCameras.clear();
            cameraListAdapter.notifyDataSetChanged();
            discoveryManager.startDiscovery();
        });
        
        // কানেক্ট বাটন সেটআপ করুন
        connectButton.setOnClickListener(v -> {
            int selectedPosition = cameraListAdapter.getSelectedPosition();
            if (selectedPosition != -1) {
                IpCamera selectedCamera = discoveredCameras.get(selectedPosition);
                connectToCamera(selectedCamera);
            }
        });
        
        // কন্ট্রোল বাটন সেটআপ করুন
        controlButton.setOnClickListener(v -> {
            if (streamManager.getCurrentCamera() != null) {
                showCameraControlDialog(streamManager.getCurrentCamera());
            }
        });
        
        // ম্যানুয়ালি ক্যামেরা যোগ করার বাটন সেটআপ করুন
        findViewById(R.id.add_camera_button).setOnClickListener(v -> {
            showAddCameraDialog();
        });
    }
    
    @Override
    protected void onResume() {
        super.onResume();
    }
    
    @Override
    protected void onPause() {
        super.onPause();
        streamManager.stopStream();
    }
    
    @Override
    protected void onDestroy() {
        super.onDestroy();
        streamManager.release();
    }
    
    private void connectToCamera(IpCamera camera) {
        // ক্যামেরা কানেকশন ডায়ালগ দেখান
        ProgressDialog progressDialog = new ProgressDialog(this);
        progressDialog.setMessage(getString(R.string.connecting_to_camera, camera.getName()));
        progressDialog.setCancelable(false);
        progressDialog.show();
        
        // ব্যাকগ্রাউন্ড থ্রেডে কানেক্ট করুন
        new Thread(() -> {
            try {
                // ক্যামেরা কানেকশন টেস্ট করুন
                boolean connected = testCameraConnection(camera);
                
                runOnUiThread(() -> {
                    progressDialog.dismiss();
                    
                    if (connected) {
                        // ক্যামেরা স্ট্রিম শুরু করুন
                        streamManager.startStream(camera);
                        controlButton.setEnabled(true);
                        
                        // ক্যামেরা ডাটাবেসে সেভ করুন
                        saveCameraToDatabase(camera);
                        
                    } else {
                        Toast.makeText(this, 
                                getString(R.string.connection_failed, camera.getName()), 
                                Toast.LENGTH_LONG).show();
                    }
                });
                
            } catch (Exception e) {
                runOnUiThread(() -> {
                    progressDialog.dismiss();
                    Toast.makeText(this, 
             
