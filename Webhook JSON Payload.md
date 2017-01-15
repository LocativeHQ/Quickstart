This is a sample payload for the Webhook sent by the [Locative Apps](https://get.locative.io).

## Payload

```
{
  "latitude": "-33.80045492553711",
  "longitude": "151.071396484375",
  "id": "Home on Android",
  "device": "42b537e8c1816c06",
  "device_type": "Android",
  "device_model": "Nexus 6P",
  "trigger": "enter",
  "timestamp": "2017-01-14 20:53:12.66"
}
```
## Glossary

### `latitude`, `longitude`

Those attributes are your Geofences location in decimal degree format.

### `id`

The `id` attribute represents the user-defined custom id, if not set in the app, it will be a randomly assigned.

### `device`

Your device's unique identifier. On Android this is retrieved by `Settings.Secure.ANDROID_ID` on iOS the `UIDevice.current.identifierForVendor` is being used, this identifier might however change if the app is uninstalled. There have been a few reportings this also happened after performing a system upgrade.

### `device_type`

The type of device the app is being used on. E.g. `Android` or `iOS`.

### `device_model`

The mode of device your using, on Android this comes from `Build.MODEL` on iOS this is returned by `UIDevice`.

### `trigger`

The `trigger` attribute either contains `enter` or `exit` depending on whether the Geofence has been enteres or left.

### `timestamp`

The events timestamp.
