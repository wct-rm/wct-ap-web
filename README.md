# WCT Ads Platform Web SDK



### Import the SDK

##### Include the SDK in your project by adding the following script tag:

```
<script src="https://wct-rm.github.io/wct-ap-web/wctapsdk.js"></script>
```

### Initialize the SDK

##### Initialize the SDK with your tenant ID:

```
WCTAPSDK.initialize('your-tenant-id');
```

### Set Customer ID (Optional)

```
// Store CustomerId
WCTAPSDK.setCustomerId(customerId);

// Clear CustomerId
WCTAPSDK.clearCustomerId();
```

### Track Impressions, View and No Ads

##### Use the following code to integrate ad impressions, view and no ads:

```
// Track Impressions
WCTAPSDK.trackSponsoredImpression(adModuleInfo, impressionBeacons)
.then(response => {
  console.log('Response:', response);
})
.catch(error => {
  console.error('Error:', error);
});
```

```
// Track View
WCTAPSDK.trackSponsoredView(adModuleInfo, impressionBeacons)
.then(response => {
  console.log('Response:', response);
})
.catch(error => {
  console.error('Error:', error);
});
```

```
// Track No Ads
WCTAPSDK.trackSponsoredNoAd(adModuleInfo)
.then(response => {
  console.log('Response:', response);
})
.catch(error => {
  console.error('Error:', error);
});
```

### Ad Clicked

##### Use the following code to integrate the ad clicked method:

```
// Track Ad Clicked
WCTAPSDK.trackSponsoredClick(onClickBeacon)
.then(response => {
  console.log('Response:', response);
})
.catch(error => {
  console.error('Error:', error);
});
```

### Track Order

##### Order details and code sample to track an order:

```
const item1 = new WCTAPOrderItem("itemId1", 1, 10.00, 10.00);
const item2 = new WCTAPOrderItem("itemId2", 3, 5.00, 15.00);
const order = new WCTAPOrder("order123", 27.00, 25.00, 2.00, [item1, item2], Date.now());
WCTAPSDK.trackOrder(order);
```
