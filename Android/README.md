# Google AI Edge Gallery (Android)

## Build

```bash
cd src
./gradlew :app:assembleRelease
```

### Split ABI Outputs

The build produces architecture-specific APKs to reduce install size and avoid parsing errors on certain devices:

| APK | Size | Target |
|-----|------|--------|
| `app-arm64-v8a-release.apk` | ~63 MB | Most modern phones (Pixel, Samsung, Xiaomi, etc.) |
| `app-armeabi-v7a-release.apk` | ~35 MB | Older 32-bit ARM devices |
| `app-universal-release.apk` | ~73 MB | Fallback for all devices |

Outputs are located at:
```
src/app/build/outputs/apk/release/
```
