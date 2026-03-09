# caelestia-lover
from caelestia dot file, but bypass/ignore the cava lib

i create ts cuz my cava not found and cava on caelestia cant find [cava.pc](https://github.com/LukashonakV/cava.git) so i crate one and its works to me. im already tried before and ask and searching.
Initial Problem (CMake Error): Initially, the build failed because CMake couldn't find the cava library (PkgConfig::Cava). Initial Investigation: I checked the system and confirmed that the development files for cava (i.e., cava.pc, libcava.so, cava.h) were missing. The installed cava package only contained the program. Fix (Bypassing Cava in CMake): To resolve the CMake error, I edited plugin/src/Caelestia/Services/CMakeLists.txt. I removed everything related to CavaProvider so that the build process would no longer look for it and could complete.
[SOURCE](https://github.com/caelestia-dots/shell.git)

## INSTALLING
```
git clone https://github.com/Bangkit-eldhian24/caelestia-lover.git caelestia/
cd caelestia
cmake -B build -G Ninja -DCMAKE_BUILD_TYPE=Release -DCMAKE_INSTALL_PREFIX=/
cmake --build build
sudo cmake --install build
```
others
```
yay -S --overwrite '*' caelestia-shell
```
```
yay --rebuild quickshell-git
```
## Done :)

![WhatsApp Image 2026-01-21 at 21 20 44](https://github.com/user-attachments/assets/09b57cd1-a5af-4eb2-921b-84270209432c)

![WhatsApp Image 2026-01-21 at 20 07 13](https://github.com/user-attachments/assets/1a7b74f5-f8e4-4e3e-831c-2b834b18dc13)

cava checking
```
find /usr -name "cava.pc" 2>/dev/null
```
some issues

```
ayanagi@noshiro ~/.c/q/caelestia (main)> cmake -B build -G Ninja -DCMAKE_BUILD_TYPE=Release -DCMAKE_INSTALL_PREFIX=/
-- Could NOT find WrapVulkanHeaders (missing: Vulkan_INCLUDE_DIR) 
-- Could NOT find WrapVulkanHeaders (missing: Vulkan_INCLUDE_DIR) 
-- Checking for module 'cava'
--   Package 'cava' not found
CMake Error at /usr/share/cmake/Modules/FindPkgConfig.cmake:1093 (message):
  The following required packages were not found:

   - cava

Call Stack (most recent call first):
  /usr/share/cmake/Modules/FindPkgConfig.cmake:1166 (_pkg_check_modules_internal)
  plugin/src/Caelestia/CMakeLists.txt:6 (pkg_check_modules)
```

