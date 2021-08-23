---
title: Videogerätekonformitätsvorlagen
description: Videogerätekonformitätsvorlagen
ms.assetid: 0a91167c-8799-4ce8-a377-c4e613567d0f
keywords:
- Windows Medienformat-SDK, Gerätekonformitätsvorlagen
- Advanced Systems Format (ASF), Gerätekonformitätsvorlagen
- ASF (Advanced Systems Format), Gerätekonformitätsvorlagen
- Windows Medienformat-SDK, Videogerätekonformitätsvorlagen
- Advanced Systems Format (ASF), Videogerätekonformitätsvorlagen
- ASF (Advanced Systems Format), Videogerätekonformitätsvorlagen
- Windows Media Video 9-Codec, Videogerätekonformitätsvorlagen
- Codecs,Windows Media Video 9-Codec
- Gerätekonformitätsvorlagen, Video
- Videogerätekonformitätsvorlagen
- Vorlagen, Videogerätekonformitätsvorlagen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df63d40152e814f879498f0f99e386c9b21ef1e32746cf0c405aa46ab9d2fa48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119584840"
---
# <a name="video-device-conformance-templates"></a>Videogerätekonformitätsvorlagen

In den folgenden Tabellen sind die Gerätekonformitätsvorlagen und die zugehörigen Parameter für den Windows Media Video 9-Codec aufgeführt.

## <a name="simple-profile-low-level"></a>Einfaches Profil, niedrige Ebene



| Parameter                                | Wert                                                                                 |
|------------------------------------------|---------------------------------------------------------------------------------------|
| Vorlagenzeichenfolge                          | "SP@LL"                                                                               |
| Geeignete Geräte                      | Drahtlose Mobiltelefone (Microsoft Windows-Powered SmartPhone-Lösung und ähnliche Geräte) |
| Maximale Auflösung                       | 176 x 144                                                                             |
| Maximale Bildfrequenz                       | 15 FPS                                                                                |
| Maximale Bitrate                         | 96 KBit/s                                                                               |
| Maximale Puffergröße (in 16384-Bit-Einheiten) | 20 (ca. 3,4 Sekunden bei maximaler Bitrate)                                            |
| Verschachtelte Codierung                      | Nein                                                                                    |



 

## <a name="simple-profile-medium-level"></a>Einfaches Profil, mittlere Ebene



| Parameter                                | Wert                                                                                |
|------------------------------------------|--------------------------------------------------------------------------------------|
| Vorlagenzeichenfolge                          | "SP@ML"                                                                              |
| Geeignete Geräte                      | Desktopcomputer und Personal Data AssistantsHigh-end wireless handsets<br/> |
| Maximale Auflösung                       | 352 x 288                                                                            |
| Maximale Bildfrequenz                       | 15 fps @ 352 x 28824 fps @ 320 x 240<br/>                                      |
| Maximale Bitrate                         | 384 KBit/s                                                                             |
| Maximale Puffergröße (in 16384-Bit-Einheiten) | 77 (ca. 3,3 Sekunden bei maximaler Bitrate)                                           |
| Verschachtelte Codierung                      | Nein                                                                                   |



 

## <a name="generic-simple-profile"></a>Generisches einfaches Profil

Einem Stream, der den algorithmischen Einschränkungen des einfachen Profils entspricht, aber nicht in eine der Ebenenspezifikationen passt, wird "SP" als Gerätekonformitätsvorlagenzeichenfolge zugewiesen.

## <a name="main-profile-low-level"></a>Hauptprofil, niedrige Ebene



| Parameter                                | Wert                                       |
|------------------------------------------|---------------------------------------------|
| Vorlagenzeichenfolge                          | "MP@LL"                                     |
| Geeignete Geräte                      | Set-Top-Felder                               |
| Maximale Auflösung                       | 352 x 288                                   |
| Maximale Bildfrequenz                       | 30 FPS                                      |
| Maximale Bitrate                         | 2 Mbit/s                                      |
| Maximale Puffergröße (in 16384-Bit-Einheiten) | 306 (ca. 2,5 Sekunden bei maximaler Bitrate) |
| Verschachtelte Codierung                      | Nein                                          |



 

## <a name="main-profile-medium-level"></a>Hauptprofil, mittlere Ebene



| Parameter                                | Wert                                                                                                                  |
|------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| Vorlagenzeichenfolge                          | "MP@ML"                                                                                                                |
| Geeignete Geräte                      | Set-top boxesSlower computers using DirectX Video Acceleration<br/> Windows Medienfähige DVD-Player<br/> |
| Maximale Auflösung                       | 720 x 576                                                                                                              |
| Maximale Bildfrequenz                       | 30 fps @ 720 x 48025 fps @ 720 x 576<br/>                                                                        |
| Maximale Bitrate                         | 10 MBit/s                                                                                                                |
| Maximale Puffergröße (in 16384-Bit-Einheiten) | 611 (ca. 1 Sekunde bei maximaler Bitrate)                                                                               |
| Verschachtelte Codierung                      | Ja                                                                                                                    |



 

## <a name="main-profile-high-level"></a>Hauptprofil, hohe Ebene



| Parameter                                | Wert                                                                                                                                                                 |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Vorlagenzeichenfolge                          | "MP@HL"                                                                                                                                                               |
| Geeignete Geräte                      | Computer, die DirectX Video AccelerationHigh-Definition Windows Medienfähige DVD-Player verwenden<br/> Digitales 2016<br/> High-Definition-Streaming<br/> |
| Maximale Auflösung                       | 1920 x 1080                                                                                                                                                           |
| Maximale Bildfrequenz                       | 30 fps @ 1920 x 108060 fps @ 1280 x 720<br/>                                                                                                                    |
| Maximale Bitrate                         | 20 MBit/s                                                                                                                                                               |
| Maximale Puffergröße (in 16384-Bit-Einheiten) | 2442 (ca. 2,66 Sekunden bei maximaler Bitrate)                                                                                                                         |
| Verschachtelte Codierung                      | Ja                                                                                                                                                                   |



 

## <a name="generic-main-profile"></a>Generisches Hauptprofil

Einem Stream, der den algorithmischen Einschränkungen des Hauptprofils entspricht, aber nicht in eine der Levelspezifikationen passt, wird "MP" als Vorlagenzeichenfolge für die Gerätekonformität zugewiesen.

## <a name="complex-profile"></a>Komplexes Profil



| Parameter       | Wert                                                                                                                                  |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------|
| Vorlagenzeichenfolge | "CP"                                                                                                                                   |
| Hinweise         | Das komplexe Profil weist keine expliziten Einschränkungen auf. Es wird verwendet, um alle Codecalgorithmen zu aktivieren, in der Regel zu Demonstrationszwecken. |



 

In den folgenden Tabellen sind die Parameter der Gerätekonformitätsvorlagen für den Windows Media Video 9 Image-Codec aufgeführt.

## <a name="video-image-level-1"></a>Videobildebene 1



| Parameter                                | Wert                                       |
|------------------------------------------|---------------------------------------------|
| Vorlagenzeichenfolge                          | "I1"                                        |
| Maximale Auflösung                       | 352 x 288                                   |
| Maximale Bildfrequenz                       | 30 Fps                                      |
| Maximale Bitrate                         | 192 KBit/s                                    |
| Maximale Puffergröße (in 16384-Bit-Einheiten) | 39 (ca. 3,26 Sekunden bei maximaler Bitrate) |
| Interlaced-Codierung                      | Nein                                          |



 

## <a name="video-image-level-2"></a>Videobildebene 2



| Parameter                                | Wert                                       |
|------------------------------------------|---------------------------------------------|
| Vorlagenzeichenfolge                          | "I2"                                        |
| Maximale Auflösung                       | 1024 x 768                                  |
| Maximale Bildfrequenz                       | 30 Fps                                      |
| Maximale Bitrate                         | 384 KBit/s                                    |
| Maximale Puffergröße (in 16384-Bit-Einheiten) | 77 (ca. 3,26 Sekunden bei maximaler Bitrate) |
| Interlaced-Codierung                      | Nein                                          |



 

## <a name="generic-video-image"></a>Generisches Videobild

Einem Videobildstream, der nicht in eine der Levelspezifikationen passt, wird "I" als Vorlagenzeichenfolge für die Gerätekonformität zugewiesen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Vorlagen für die Konformität von Audio-Geräten**](audio-device-conformance-templates.md)
</dt> <dt>

[**Vorlagenparameter für Gerätekonformität**](device-conformance-template-parameters.md)
</dt> <dt>

[**Empfohlene Kombinationen von Gerätekonformitätsvorlagen**](recommended-device-conformance-template-combinations.md)
</dt> </dl>

 

 





