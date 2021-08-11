---
description: In diesem Thema sind die Medienformate aufgeführt, für die Microsoft Media Foundation systemeigene Unterstützung bietet.
ms.assetid: 69c12a28-4b58-4979-b4d8-ae37efa847fe
title: Unterstützte Medienformate in Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ecbc5024ab70e9e0bdd07d6213ad9779c21e2b7f34f10f3e2d3fe538a784734
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118238189"
---
# <a name="supported-media-formats-in-media-foundation"></a>Unterstützte Medienformate in Media Foundation

In diesem Thema sind die Medienformate aufgeführt, für die Microsoft Media Foundation systemeigene Unterstützung bietet. Drittanbieter können zusätzliche Formate unterstützen, indem sie benutzerdefinierte Plug-Ins schreiben.

## <a name="file-containers"></a>Dateicontainer



| Format                                           | Dateierweiterungen          | Medienquelle                                 | Mediensenke                                   | Erforderlich                                                              |
|--------------------------------------------------|--------------------------|----------------------------------------------|----------------------------------------------|-----------------------------------------------------------------------|
| 3GP                                              | .3g2, .3gp, .3gp2, .3gpp | [MPEG-4-Dateiquelle](mpeg-4-file-source.md) | 3GP-Dateisenke                                | Windows 7                                                             |
| Advanced Streaming Format (ASF)                  | .asf, .wma, .wmv         | [ASF-Medienquelle](asf-media-source.md)     | [ASF-Mediensenke](asf-media-sinks.md)        | Windows Vista                                                         |
| Audio Data Transport Stream (ADTS).              | .aac, .adts              | ADTS-Dateiquelle                             | Keine                                         | Windows 7                                                             |
| AVI                                              | AVI                     | AVI-Dateiquelle                              | Keine                                         | Windows 7                                                             |
| MP3                                              | .mp3                     | [**MP3-Dateiquelle**](mp3-file-source.md)   | MP3-Dateisenke                                | Dateiquelle: Windows Vista<br/> Dateisenke: Windows 7<br/> |
| MPEG-4                                           | .m4a, .m4v, .mov, .mp4   | [MPEG-4-Dateiquelle](mpeg-4-file-source.md) | [**MPEG-4-Dateisenke**](mpeg-4-file-sink.md) | Windows 7                                                             |
| Synchronized Accessible Media Interchange (SAMI) | .sami, .smi              | [SAMI-Medienquelle](sami-media-source.md)   | Keine                                         | Windows Vista                                                         |
| Welle                                             | WAV                     | AVI-Dateiquelle                              | Keine                                         | Windows 7                                                             |



 

## <a name="audio-codecs"></a>Audiocodecs



| Format                                              | Decoder                                                                                                                                                          | Encoder                                                                                                                                                          | Erforderlich      |
|-----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------|
| μ-Law Coding                                        | Audiokomprimierungs-Manager (ACM) μ-Law-Codec                                                                                                                      | Keine                                                                                                                                                             | Windows Vista |
| Adaptive Differential Pulse Code Pulses (ADPCM) | ACM-ADPCM-Codec                                                                                                                                                  | Keine                                                                                                                                                             | Windows Vista |
| Erweiterte Audiocodierung (Advanced Audio Coding, AAC)                         | [**AAC-Decoder**](aac-decoder.md)                                                                                                                               | [**AAC-Encoder**](aac-encoder.md)                                                                                                                               | Windows 7     |
| MP3                                                 | [**Windows Medien-MP3-Decoder**](windows-media-mp3-decoder.md)                                                                                                   | Keine                                                                                                                                                             | Windows Vista |
| GSM 6.10                                            | ACM GSM 6.10-Codec                                                                                                                                               | Keine                                                                                                                                                             | Windows Vista |
| Windows Media Audio (WMA)                           | [**Windows Medienaudiodecoder**](windowsmediaaudiodecoder.md)<br/> [**Windows Medienaudio-Sprachdecoder**](windowsmediaaudiovoicedecoder.md)<br/> | [**Windows Medienaudioencoder**](windowsmediaaudioencoder.md)<br/> [**Windows Media Audio Voice Encoder**](windowsmediaaudiovoiceencoder.md)<br/> | Windows Vista |



 

> [!Note]  
> Media Foundation stellt Wrapper für mehrere ACM-Codecs bereit, die in der vorherigen Tabelle aufgeführt sind. Allerdings unterstützt Media Foundation keine beliebigen ACM-Codecs.

 

## <a name="video-codecs"></a>Videocodecs



| Format                                                                                                         | Decoder                                                                                                                                                                  | Encoder                                                                                                                             | Erforderlich      |
|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|---------------|
| DV-Video                                                                                                       | [**DV-Videodecoder**](dv-video-decoder.md)                                                                                                                             | Keine                                                                                                                                | Windows 7     |
| H.264                                                                                                          | [**H.264-Videodecoder**](h-264-video-decoder.md)                                                                                                                       | [**H.264 Video Encoder**](h-264-video-encoder.md)                                                                                  | Windows 7     |
| H.263<br/> (H.264-Baselineprofil, das mit dem Kurzen Videoheadermodus MPEG-4 Pt2 kompatibel ist)<br/> | [**MPEG-4 Part 2 Video Decoder**](mpeg4part2videodecoder.md)                                                                                                            | Keine                                                                                                                                | Windows 8     |
| Mjpeg                                                                                                          | MJPEG-Decoder                                                                                                                                                            | Keine                                                                                                                                | Windows 7     |
| MPEG-4 Teil 2                                                                                                  | [**MPEG-4 Part 2 Video Decoder**](mpeg4part2videodecoder.md)                                                                                                            | Keine                                                                                                                                | Windows 7     |
| MPEG-4 v1/v2/v3                                                                                                | [**Windows Mpeg-4 V3-Mediendecoder**](./windowsmediampeg4v3decoder.md)<br/> [**Windows Media MPEG4 V1/V2-Decoder**](windowsmediampeg4decoder.md)<br/>         | Keine                                                                                                                                | Windows Vista |
| Windows Media Video (WMV)                                                                                      | [**Windows Media Video 9-Decoder**](windowsmediavideo9decoder.md)<br/> [**Windows Media Video 9-Bildschirmdecoder**](windowsmediavideo9screendecoder.md)<br/> | Windows Media Video 9 Encoder<br/> Windows Media Video 9 Screen Encoder<br/> Windows Media Video 7/8 Encoder<br/> | Windows Vista |



 

> [!Note]  
> In der Spalte "Erforderlich" ist das mindestens erforderliche Betriebssystem aufgeführt, um diese Codecs in einer Media Foundation verwenden zu können. Einige dieser Codecs wurden vor der Windows Vista als [DirectX Media Objects](../directshow/directx-media-objects.md) (DMOs) eingeführt. Wenn ein Codec DMO unterstützt, kann er mit [DirectShow](../directshow/directshow.md) oder dem Windows [Media Format SDK verwendet werden.](../wmformat/windows-media-format-11-sdk.md)

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Codec-Objekte](codecobjects.md)
</dt> <dt>

[Media Foundation-Programmierhandbuch](media-foundation-programming-guide.md)
</dt> <dt>

[Medienquellen und -senken](media-sources-and-sinks.md)
</dt> </dl>

 

 
