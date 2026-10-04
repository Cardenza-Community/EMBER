# Runtime Cardenza support

Based on preserved upstream `3c73a167f1a618ff5b983ee164128c7b6ecd8db7`. Default `unified` and CI-compatible alias `cardenza` use the exact M5Unified fork `203Null/M5Unified@74fe31c6d9a2bd7c04f81eb4f8f0af99262e3bc2` (upstream0.2.24), M5GFX0.2.31, M5Cardputer1.1.1. Hardware is selected at runtime using ES8156 identity; original Cardputer keyboard identity is preserved. The fork owns LED hold, no Cardenza battery ADC/RGB and codec initialization. No app-local hardware HAL or Power/RGB linker wrappers remain.

Preserved newer upstream README; runtime output choices loaded after M5 detection, no external DAC matrix pins or battery UI on Cardenza.

The independent `LAUNCHER_NVS_GUARD` and erase wrapper preserve shared Launcher NVS full-partition recovery; normal page GC and app/filesystem erase continue. The actual existing host guard test passes. Existing workflow and prepare.py bytes were preserved; prepare.py generated the raw app image and original dependency licensing notices successfully.

Final publishing-tree build PASS (`pio run -e cardenza`), 1801520 bytes, SHA-256 `10169256eb20bf09632e0943047e8a970bfb4a1a98dde4e5ed5312accae630f4`. This image was not flashed or physically validated. Historical device results for earlier images do not prove this image's hardware behavior.
