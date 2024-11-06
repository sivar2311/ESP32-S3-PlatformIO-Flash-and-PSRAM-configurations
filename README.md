# ESP32-S3 PlatformIO Flash and PSRAM configurations

## ESP32-S3
| Module                            |    Flash    |    PSRAM    |
| --------------------------------- | :---------: | :---------: |
| [ESP32-S3-FN8](#esp32-s3-fn8)     | 8 MB (Quad) |      -      |
| [ESP32-S3-FH4R2](#esp32-s3-fh4r2) | 4 MB (Quad) | 2 MB (Quad) |
|                                   |             |             |

## ESP32-S3-WROOM-(1/1U)
| Module                                                         |    Flash     |     PSRAM     |
| -------------------------------------------------------------- | :----------: | :-----------: |
| [ESP32-S3-WROOM-(1/1U)-(N/H)4](#esp32-s3-wroom-11u-nh4)        | 4 MB (Quad)  |       -       |
| [ESP32-S3-WROOM-(1/1U)-N8](#esp32-s3-wroom-11u-n8)             | 8 MB (Quad)  |       -       |
| [ESP32-S3-WROOM-(1/1U)-N16](#esp32-s3-wroom-11u-n16)           | 16 MB (Quad) |       -       |
| [ESP32-S3-WROOM-(1/1U)-N4R2](#esp32-s3-wroom-11u-n4r2)         | 4 MB (Quad)  |  2 MB (Quad)  |
| [ESP32-S3-WROOM-(1/1U)-N8R2](#esp32-s3-wroom-11u-n8r2)         | 8 MB (Quad)  |  2 MB (Quad)  |
| [ESP32-S3-WROOM-(1/1U)-N16R2](#esp32-s3-wroom-11u-n16r2)       | 16 MB (Quad) |  2 MB (Quad)  |
| [ESP32-S3-WROOM-(1/1U)-N4R8](#esp32-s3-wroom-11u-n4r8)         | 4 MB (Quad)  | 8 MB (Octal)  |
| [ESP32-S3-WROOM-(1/1U)-N8R8](#esp32-s3-wroom-11u-n8r8)         | 8 MB (Quad)  | 8 MB (Octal)  |
| [ESP32-S3-WROOM-(1/1U)-N16R8](#esp32-s3-wroom-11u-n16r8)       | 16 MB (Quad) | 8 MB (Octal)  |
| [ESP32-S3-WROOM-(1/1U)-N16R16(V)](#esp32-s3-wroom-11u-n16r16v) | 16 MB (Quad) | 16 MB (Octal) |

## ESP32-S3-WROOM-2
| Module                                              | Flash        |    PSRAM    |
| --------------------------------------------------- | :----------- | :---------: |
| [ESP32-S3-WROOM-2-N16R8V](#esp32-s3-wroom-2-n16r8v) | 16MB (Octal) | 8MB (Octal) |
| [ESP32-S3-WROOM-2-N32R8V](#esp32-s3-wroom-2-n32r8v) | 32MB (Octal) | 8MB (Octal) |

## ESP32-S3-MINI-(1/1U)
| Module                                               |   Flash    |    PSRAM    |
| ---------------------------------------------------- | :--------: | :---------: |
| [ESP32-S3-MINI-(1/1U)-N4R2](#esp32-s3-mini-11u-n4r2) | 4MB (Quad) | 2 MB (Quad) |
| [ESP32-S3-MINI-(1/1U)-N8](#esp32-s3-mini-11u-n8)     | 8MB (Quad) |      -      |

# Configurations

## ESP32-S3-FN8
```ini
; Flash: 8MB QD, no PSRAM
[env:esp32-s3-devkitc-1]
platform = espressif32
board = esp32-s3-devkitc-1
framework = arduino

board_build.flash_mode = qio
board_upload.flash_size = 8MB
board_upload.maximum_size = 8388608
```

## ESP32-S3-FH4R2
```ini
; Flash: 4MB QD, PSRAM: 2MB QD
[env:esp32-s3-devkitc-1]
platform = espressif32
board = esp32-s3-devkitc-1
framework = arduino

board_build.arduino.memory_type = qio_qspi
board_build.flash_mode = qio
board_build.psram_type = qio
board_upload.flash_size = 4MB
board_upload.maximum_size = 4194304
board_build.extra_flags = 
  -DBOARD_HAS_PSRAM
```

## ESP32-S3-WROOM-(1/1U)-(N/H)4
```ini
; Flash: 4MB QD, no PSRAM
[env:esp32-s3-devkitc-1]
platform = espressif32
board = esp32-s3-devkitc-1
framework = arduino

board_build.flash_mode = qio
board_upload.flash_size = 4MB
board_upload.maximum_size = 4194304
```

## ESP32-S3-WROOM-(1/1U)-N8
```ini
; Flash: 8MB QD, no PSRAM
[env:esp32-s3-devkitc-1]
platform = espressif32
board = esp32-s3-devkitc-1
framework = arduino

board_build.flash_mode = qio
board_upload.flash_size = 8MB
board_upload.maximum_size = 8388608
```

## ESP32-S3-WROOM-(1/1U)-N16
```ini
; Flash: 16MB QD, no PSRAM
[env:esp32-s3-devkitc-1]
platform = espressif32
board = esp32-s3-devkitc-1
framework = arduino

board_build.flash_mode = qio
board_upload.flash_size = 16MB
board_upload.maximum_size = 16777216
```

## ESP32-S3-WROOM-(1/1U)-N4R2
```ini
; Flash: 4MB QD, PSRAM: 2MB QD
[env:esp32-s3-devkitc-1]
platform = espressif32
board = esp32-s3-devkitc-1
framework = arduino

board_build.arduino.memory_type = qio_qspi
board_build.flash_mode = qio
board_build.psram_type = qio
board_upload.flash_size = 4MB
board_upload.maximum_size = 4194304
board_build.extra_flags = 
  -DBOARD_HAS_PSRAM
```

## ESP32-S3-WROOM-(1/1U)-N8R2
```ini
; Flash: 8MB QD, PSRAM: 2MB QD
[env:esp32-s3-devkitc-1]
platform = espressif32
board = esp32-s3-devkitc-1
framework = arduino

board_build.arduino.memory_type = qio_qspi
board_build.flash_mode = qio
board_build.psram_type = qio
board_upload.flash_size = 8MB
board_upload.maximum_size = 8388608
board_build.extra_flags = 
  -DBOARD_HAS_PSRAM
```

## ESP32-S3-WROOM-(1/1U)-N16R2
```ini
; Flash: 16MB QD, PSRAM: 2MB QD
[env:esp32-s3-devkitc-1]
platform = espressif32
board = esp32-s3-devkitc-1
framework = arduino

board_build.arduino.memory_type = qio_qspi
board_build.flash_mode = qio
board_build.psram_type = qio
board_upload.flash_size = 16MB
board_upload.maximum_size = 16777216
board_build.extra_flags = 
  -DBOARD_HAS_PSRAM
```

## ESP32-S3-WROOM-(1/1U)-N4R8
```ini
; Flash: 4MB QD, PSRAM: 8MB OT
[env:esp32-s3-devkitc-1]
platform = espressif32
board = esp32-s3-devkitc-1
framework = arduino

board_build.arduino.memory_type = qio_opi
board_build.flash_mode = qio
board_build.psram_type = opi
board_upload.flash_size = 4MB
board_upload.maximum_size = 4194304
board_build.extra_flags = 
  -DBOARD_HAS_PSRAM
```  

## ESP32-S3-WROOM-(1/1U)-N8R8
```ini
; Flash: 8MB QD, PSRAM: 8MB OT
[env:esp32-s3-devkitc-1]
platform = espressif32
board = esp32-s3-devkitc-1
framework = arduino

board_build.arduino.memory_type = qio_opi
board_build.flash_mode = qio
board_build.psram_type = opi
board_upload.flash_size = 8MB
board_upload.maximum_size = 8388608
board_build.extra_flags = 
  -DBOARD_HAS_PSRAM
```

## ESP32-S3-WROOM-(1/1U)-N16R8
```ini
; Flash: 16MB QD, PSRAM: 8MB OT
[env:esp32-s3-devkitc-1]
platform = espressif32
board = esp32-s3-devkitc-1
framework = arduino

board_build.arduino.memory_type = qio_opi
board_build.flash_mode = qio
board_build.psram_type = opi
board_upload.flash_size = 16MB
board_upload.maximum_size = 16777216
board_build.extra_flags = 
  -DBOARD_HAS_PSRAM
```

## ESP32-S3-WROOM-(1/1U)-N16R16(V)
```ini
; Flash: 16MB QD, PSRAM: 16MB OT
[env:esp32-s3-devkitc-1]
platform = espressif32
board = esp32-s3-devkitc-1
framework = arduino

board_build.arduino.memory_type = qio_opi
board_build.flash_mode = qio
board_build.psram_type = opi
board_upload.flash_size = 16MB
board_upload.maximum_size = 16777216
board_build.extra_flags = 
  -DBOARD_HAS_PSRAM
```

## ESP32-S3-WROOM-2-N16R8V
```ini
; Flash: 16MB OT, PSRAM: 8MB OT
[env:esp32-s3-devkitc-1]
platform = espressif32
board = esp32-s3-devkitc-1
framework = arduino

board_build.arduino.memory_type = opi_opi
board_build.flash_mode = opi
board_build.psram_type = opi
board_upload.flash_size = 16MB
board_upload.maximum_size = 16777216
board_build.extra_flags = 
  -DBOARD_HAS_PSRAM
```

## ESP32-S3-WROOM-2-N32R8V
```ini
; Flash: 32MB OT, PSRAM: 8MB OT
[env:esp32-s3-devkitc-1]
platform = espressif32
board = esp32-s3-devkitc-1
framework = arduino

board_build.arduino.memory_type = opi_opi
board_build.flash_mode = opi
board_build.psram_type = opi
board_upload.flash_size = 32MB
board_upload.maximum_size = 33554432
board_build.extra_flags = 
  -DBOARD_HAS_PSRAM
```
## ESP32-S3-MINI-(1/1U)-N4R2
```ini
; Flash: 4MB QD, PSRAM: 2MB QD
[env:esp32-s3-devkitc-1]
platform = espressif32
board = esp32-s3-devkitc-1
framework = arduino

board_build.arduino.memory_type = qio_qspi
board_build.flash_mode = qio
board_build.psram_type = qio
board_upload.flash_size = 4MB
board_upload.maximum_size = 4194304
board_build.extra_flags = 
  -DBOARD_HAS_PSRAM
```

## ESP32-S3-MINI-(1/1U)-N8
```ini
; Flash: 8MB QD, no PSRAM
[env:esp32-s3-devkitc-1]
platform = espressif32
board = esp32-s3-devkitc-1
framework = arduino

board_build.flash_mode = qio
board_upload.flash_size = 8MB
board_upload.maximum_size = 8388608
```
