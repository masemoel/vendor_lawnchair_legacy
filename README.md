# Lawnchair built-in-system
Ideal for Oreo or lower (this Lawnchair apk supports from Q to L).

## Disclaimer
- All credits go to the Lawnchair team.

## How to implement
**1. Add this repository to your ROM source, either by adding this repo to your local_manifests 

```bash
  <project name="masemoel/vendor_lawnchair_legacy" path="vendor/lawnchair" remote="github" revision="master" />
```
  or by downloading and pasting this repo to ./vendor/lawnchair

**2. Import vendor/lawnchair/lawnchair.mk**

In case of LineageOS, this can be done by appending the following at ./vendor/cm/config/common.mk:

`$(call inherit-product-if-exists, vendor/lawnchair/lawnchair.mk)`

**3. Remove existing launcher from the build**

`ParanoidQuickStep`, `Launcher3QuickStep`, `PixelLauncher` and `TrebuchetQuickStep` packages are overriden from `priv-app/Lawnchair/Android.mk`.

If your existing launcher uses a different name, you can remove it from the build manually or post a pull request.

**4. Build your ROM :) and enjoy!**
