> `Changelog:`
> - All significant changes to this project will be documented here.
---

> [1.5.0]
>
> - Changing the total module structure from the old to the latest.
> - Introduced `post-fs-data.sh` as a new core feature to handle early GPS configuration setup during boot, including creation of customized `flp.conf`, `gps.conf`, `gnss.conf`, `gps.xml`, and `system.prop` files for enhanced stability and performance.
> - Added `service.sh` as a primary feature to manage post-boot operations, focusing on granting essential permissions to `com.google.android.gms` for location services, with improved timeout handling and dynamic checks.
> - Integrated `verify.sh` for robust file integrity verification using SHA-256/SHA-512 checksums, path sanitization, and dependency checks to prevent tampering and ensure original module authenticity.
> - Added `uninstall.sh` for clean module removal, including comprehensive cache cleanup across `/data` directories and safe deletion of module files.
> - Updated `customize.sh` with new functions: `display_current_time`, `root_detect`, `display_device_info`, `display_ram_info`, `module_remove_check`, `abort_verify`, `verify_module`, and `print_random_devil_message` for better installation feedback and validation.
> - Enhanced `module.prop` with a new `banner` field pointing to a custom image URL for improved module presentation.
> - Optimized GPS configurations: Switched SUPL server from `supl.qxwz.com:7275` to `supl.google.com:7276`, updated XTRA server to `xtra3.gpsonextra.net/xtra3grc.bin`, and added NTP server `pool.ntp.org` for better accuracy and reliability.
> - Expanded `system.prop` with additional GPS properties like `ro.gps.agps_timeout`, `ro.gps.hot_start_timeout`, and `ro.gps.sensor_batching` to fine-tune performance.
> - Removed verbose sleep-based logging in `customize old.sh` and streamlined installation process in `customize.sh` for faster execution.
> - Improved permission granting in `service.sh` with fallback to `su` and package existence checks to ensure compatibility across root methods.
> - Added devil-themed random messages in `customize.sh` for a unique user experience during installation.
> - Minor optimizations: Raised minimum Android SDK support from 28 to 29, refined processor detection, and enhanced error handling throughout scripts.
---

> [1.0.0]
>
> - Initial release.
---