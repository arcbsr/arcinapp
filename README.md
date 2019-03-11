# arcinapp


    implementation 'com.github.arcbsr:arcinapp:111'
//adb shell pm clear com.android.vending -->> clearin app test billing
// @Override 
// protected void onActivityResult(int requestCode, int resultCode, Intent data) { 
// if (!arcInAppBilling.getBillingProcessor().handleActivityResult(requestCode, resultCode, data)) { 
// super.onActivityResult(requestCode, resultCode, data); 
// } 
// } 

InAppBillingBaseActivity.startActivityForPurchase(MainActivity.this, 1000, Settings.KEY_INAPP_TEST);
@Override protected void onActivityResult(int requestCode, int resultCode, Intent data) { 
super.onActivityResult(requestCode, resultCode, data); 
if (requestCode == 1000) { Log.w("onActivityResult", data.getStringExtra(InAppBillingBaseActivity.KEY_PRODUCT_ID)); 
Log.w("onActivityResult", data.getStringExtra(InAppBillingBaseActivity.KEY_RESULTMSG)); } 
}
