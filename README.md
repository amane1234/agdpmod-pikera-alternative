# agdpmod=pikera alternative (AppleGraphicsDevicePolicy patch)

**OpenCore** kernel patch that replicates the functionality of the boot argument `agdpmod=pikera` — used to disable `board-id` checks within **AppleGraphicsDevicePolicy**

---

## How to

1. Open your `config.plist` in **ProperTree** or **OpenCore Configurator**.
2. Navigate to:

   ```
   Kernel → Patch
   ```
3. Add the provided dictionary entry.

```xml
<array>
    <dict>
        <key>Arch</key>
        <string>x86_64</string>
        <key>Base</key>
        <string></string>
        <key>Comment</key>
        <string>AppleGraphicsDevicePolicy (board-id to board-ix) Patch</string>
        <key>Count</key>
        <integer>1</integer>
        <key>Enabled</key>
        <true/>
        <key>Find</key>
        <data>Ym9hcmQtaWQ=</data>
        <key>Identifier</key>
        <string>com.apple.driver.AppleGraphicsDevicePolicy</string>
        <key>Limit</key>
        <integer>0</integer>
        <key>Mask</key>
        <data></data>
        <key>MaxKernel</key>
        <string></string>
        <key>MinKernel</key>
        <string></string>
        <key>Replace</key>
        <data>Ym9hcmQtaXg=</data>
        <key>ReplaceMask</key>
        <data></data>
        <key>Skip</key>
        <integer>0</integer>
    </dict>
</array>
```

4. Save and reboot.
5. You **no longer need** to use the `agdpmod=pikera` and `whatevergreen.kext`.

---
