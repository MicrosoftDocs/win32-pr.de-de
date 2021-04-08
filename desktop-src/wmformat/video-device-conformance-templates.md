---
title: Vorlagen für die Konformitäts Konformität von Video Geräten
description: Vorlagen für die Konformitäts Konformität von Video Geräten
ms.assetid: 0a91167c-8799-4ce8-a377-c4e613567d0f
keywords:
- Windows Media-Format-SDK, Geräte Konformitäts Vorlagen
- Advanced Systems Format (ASF), Geräte Konformitäts Vorlagen
- ASF (Advanced Systems Format), Geräte Konformitäts Vorlagen
- Windows Media-Format-SDK, Videogeräte-Konformitäts Vorlagen
- Advanced Systems Format (ASF), Videogeräte-Konformitäts Vorlagen
- ASF (Advanced Systems-Format), Vorlagen für Videogeräte Konformität
- Windows Media Video 9-Codec, Vorlagen für Video Geräte Konformität
- Codecs, Windows Media Video 9-Codec
- Geräte Konformitäts Vorlagen, Video
- Vorlagen für die Konformitäts Konformität von Videogeräten
- Vorlagen, Konformitäts Vorlagen für Videogeräte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc6735d029bc2339296fa2a0af8a48ace3303ae3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856920"
---
# <a name="video-device-conformance-templates"></a>Vorlagen für die Konformitäts Konformität von Video Geräten

In den folgenden Tabellen sind die Geräte Konformitäts Vorlagen und die zugehörigen Parameter für den Windows Media Video 9-Codec aufgeführt.

## <a name="simple-profile-low-level"></a>Einfaches Profil, niedrige Ebene



| Parameter                                | Wert                                                                                 |
|------------------------------------------|---------------------------------------------------------------------------------------|
| Vorlagen Zeichenfolge                          | "SP@LL"                                                                               |
| Entsprechende Geräte                      | Drahtlos Handsets (Microsoft Windows-Powered Smartphone-Lösung und ähnliche Geräte) |
| Maximale Auflösung                       | 176 x 144                                                                             |
| Maximale Framerate                       | 15 fps                                                                                |
| Maximale Bitrate                         | 96 Kbit/s                                                                               |
| Maximale Puffergröße (in 16384-Bit-Einheiten) | 20 (ungefähr 3,4 Sekunden bei maximaler Bitrate)                                            |
| Zeilen Sprung Codierung                      | Nein                                                                                    |



 

## <a name="simple-profile-medium-level"></a>Einfaches Profil, mittlere Ebene



| Parameter                                | Wert                                                                                |
|------------------------------------------|--------------------------------------------------------------------------------------|
| Vorlagen Zeichenfolge                          | "SP@ML"                                                                              |
| Entsprechende Geräte                      | Hand Held Computer und persönliche Daten assistantshigh-End Wireless Handsets<br/> |
| Maximale Auflösung                       | 352 x 288                                                                            |
| Maximale Framerate                       | 15 fps @ 352 x 28824 fps @ 320 x 240<br/>                                      |
| Maximale Bitrate                         | 384 Kbit/s                                                                             |
| Maximale Puffergröße (in 16384-Bit-Einheiten) | 77 (etwa 3,3 Sekunden bei maximaler Bitrate)                                           |
| Zeilen Sprung Codierung                      | Nein                                                                                   |



 

## <a name="generic-simple-profile"></a>Generisches einfaches Profil

Ein Stream, der den algorithmischen Beschränkungen des einfachen Profils entspricht, jedoch nicht in eine der ebenenspezifikationen passt, wird "SP" als zugehörige Geräte-Konformitäts Vorlagen-Zeichenfolge zugewiesen.

## <a name="main-profile-low-level"></a>Hauptprofil, niedrige Ebene



| Parameter                                | Wert                                       |
|------------------------------------------|---------------------------------------------|
| Vorlagen Zeichenfolge                          | "MP@LL"                                     |
| Entsprechende Geräte                      | Set-Top-Boxes                               |
| Maximale Auflösung                       | 352 x 288                                   |
| Maximale Framerate                       | 30 fps                                      |
| Maximale Bitrate                         | 2 Mbit/s                                      |
| Maximale Puffergröße (in 16384-Bit-Einheiten) | 306 (etwa 2,5 Sekunden bei maximaler Bitrate) |
| Zeilen Sprung Codierung                      | Nein                                          |



 

## <a name="main-profile-medium-level"></a>Hauptprofil, mittlere Ebene



| Parameter                                | Wert                                                                                                                  |
|------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| Vorlagen Zeichenfolge                          | "MP@ML"                                                                                                                |
| Entsprechende Geräte                      | Set-Top boxess Lower Computers using DirectX Video Acceleration<br/> Windows Media-fähige DVD-Player<br/> |
| Maximale Auflösung                       | 720 x 576                                                                                                              |
| Maximale Framerate                       | 30 fps @ 720 x 48025 fps @ 720 x 576<br/>                                                                        |
| Maximale Bitrate                         | 10 Mbit/s                                                                                                                |
| Maximale Puffergröße (in 16384-Bit-Einheiten) | 611 (ungefähr 1 Sekunde bei maximaler Bitrate)                                                                               |
| Zeilen Sprung Codierung                      | Ja                                                                                                                    |



 

## <a name="main-profile-high-level"></a>Hauptprofil, hohe Ebene



| Parameter                                | Wert                                                                                                                                                                 |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Vorlagen Zeichenfolge                          | "MP@HL"                                                                                                                                                               |
| Entsprechende Geräte                      | Computer mit DirectX-Video AccelerationHigh-Definition Windows Media-fähigen DVD-Playern<br/> Digitales Kino<br/> High-Definition-Streaming<br/> |
| Maximale Auflösung                       | 1920 x 1080                                                                                                                                                           |
| Maximale Framerate                       | 30 fps @ 1920 x 108060 fps @ 1280 x 720<br/>                                                                                                                    |
| Maximale Bitrate                         | 20 MBit/s                                                                                                                                                               |
| Maximale Puffergröße (in 16384-Bit-Einheiten) | 2442 (etwa 2,66 Sekunden bei maximaler Bitrate)                                                                                                                         |
| Zeilen Sprung Codierung                      | Ja                                                                                                                                                                   |



 

## <a name="generic-main-profile"></a>Allgemeines Hauptprofil

Ein Stream, der den algorithmischen Einschränkungen des Haupt Profils entspricht, jedoch nicht in eine der ebenenspezifikationen passt, wird "MP" als zugehörige Geräte-Konformitäts Vorlagen Zeichenfolge zugewiesen.

## <a name="complex-profile"></a>Komplexes Profil



| Parameter       | Wert                                                                                                                                  |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------|
| Vorlagen Zeichenfolge | Erfolgen                                                                                                                                   |
| Bemerkungen         | Das komplexe Profil weist keine expliziten Einschränkungen auf. Sie wird verwendet, um alle Codec-Algorithmen zu aktivieren, die in der Regel zu Demonstrationszwecken verwendet werden. |



 

In den folgenden Tabellen sind die Parameter der Geräte Konformitäts Vorlagen für den Windows Media Video 9-Bildcodec aufgeführt.

## <a name="video-image-level-1"></a>Video Bild Ebene 1



| Parameter                                | Wert                                       |
|------------------------------------------|---------------------------------------------|
| Vorlagen Zeichenfolge                          | I1                                        |
| Maximale Auflösung                       | 352 x 288                                   |
| Maximale Framerate                       | 30 fps                                      |
| Maximale Bitrate                         | 192 KBit/s                                    |
| Maximale Puffergröße (in 16384-Bit-Einheiten) | 39 (etwa 3,26 Sekunden bei maximaler Bitrate) |
| Zeilen Sprung Codierung                      | Nein                                          |



 

## <a name="video-image-level-2"></a>Video Bild Ebene 2



| Parameter                                | Wert                                       |
|------------------------------------------|---------------------------------------------|
| Vorlagen Zeichenfolge                          | I2                                        |
| Maximale Auflösung                       | 1024 x 768                                  |
| Maximale Framerate                       | 30 fps                                      |
| Maximale Bitrate                         | 384 Kbit/s                                    |
| Maximale Puffergröße (in 16384-Bit-Einheiten) | 77 (etwa 3,26 Sekunden bei maximaler Bitrate) |
| Zeilen Sprung Codierung                      | Nein                                          |



 

## <a name="generic-video-image"></a>Bild des generischen Videos

Einem Video Bild Datenstrom, der nicht in eine der ebenenspezifikationen passt, wird "I" als zugehörige Geräte-Konformitäts Vorlagen-Zeichenfolge zugewiesen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Konformitäts Vorlagen für Audiogeräte**](audio-device-conformance-templates.md)
</dt> <dt>

[**Parameter für die Geräte Konformitäts Vorlage**](device-conformance-template-parameters.md)
</dt> <dt>

[**Empfohlene Kombinationen von Geräte Konformitäts Vorlagen**](recommended-device-conformance-template-combinations.md)
</dt> </dl>

 

 





