---
description: In diesem Thema sind die Medienformate aufgeführt, für die Microsoft Media Foundation systemeigene Unterstützung bietet.
ms.assetid: 69c12a28-4b58-4979-b4d8-ae37efa847fe
title: Unterstützte Medienformate in Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00e8f698179d37fc6bde8d5d1dab25214727cd38
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106363893"
---
# <a name="supported-media-formats-in-media-foundation"></a>Unterstützte Medienformate in Media Foundation

In diesem Thema sind die Medienformate aufgeführt, für die Microsoft Media Foundation systemeigene Unterstützung bietet. Drittanbieter können zusätzliche Formate unterstützen, indem Sie benutzerdefinierte Plug-ins schreiben.

## <a name="file-containers"></a>Datei Container



| Format                                           | Dateierweiterungen          | Medienquelle                                 | Medien Senke                                   | Erforderlich                                                              |
|--------------------------------------------------|--------------------------|----------------------------------------------|----------------------------------------------|-----------------------------------------------------------------------|
| 3GP                                              | .3g2,. 3GP,. 3gp2,. 3GPP | [MPEG-4-Datei Quelle](mpeg-4-file-source.md) | 3GP-Datei-Senke                                | Windows 7                                                             |
| Advanced Streaming Format (ASF)                  | . ASF,. WMA,. WMV         | [ASF-Medienquelle](asf-media-source.md)     | [ASF-Medien Senke](asf-media-sinks.md)        | Windows Vista                                                         |
| Der audiodatentransport-Stream (ADTs).              | . AAC,. ADTs              | ADTS-Datei Quelle                             | Keine                                         | Windows 7                                                             |
| AVI                                              | AVI                     | AVI-Datei Quelle                              | Keine                                         | Windows 7                                                             |
| MP3                                              | .mp3                     | [**MP3-Datei Quelle**](mp3-file-source.md)   | MP3-Datei Senke                                | Datei Quelle: Windows Vista<br/> Datei Senke: Windows 7<br/> |
| MPEG-4                                           | . m4a,. m4v,. MOV,. MP4   | [MPEG-4-Datei Quelle](mpeg-4-file-source.md) | [**MPEG-4-Datei-Senke**](mpeg-4-file-sink.md) | Windows 7                                                             |
| Synchronisierter, barrierefreier Medienaustausch (Sami) | . Sami,. SMI              | [Sami-Medienquelle](sami-media-source.md)   | Keine                                         | Windows Vista                                                         |
| Welle                                             | WAV                     | AVI-Datei Quelle                              | Keine                                         | Windows 7                                                             |



 

## <a name="audio-codecs"></a>Audiocodecs



| Format                                              | Decoder                                                                                                                                                          | Encoder                                                                                                                                                          | Erforderlich      |
|-----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------|
| Codierungs Gesetze                                        | "Audiokomprimierungs-Manager" (ACM),-Gesetz-Codec                                                                                                                      | Keine                                                                                                                                                             | Windows Vista |
| Adaptive Differential Pulse Code-Modulation (ADPCM) | ACM ADPCM-CODEC                                                                                                                                                  | Keine                                                                                                                                                             | Windows Vista |
| "Advanced audiocoding" (AAC)                         | [**AAC-Decoder**](aac-decoder.md)                                                                                                                               | [**AAC-Encoder**](aac-encoder.md)                                                                                                                               | Windows 7     |
| MP3                                                 | [**Windows Media MP3-Decoder**](windows-media-mp3-decoder.md)                                                                                                   | Keine                                                                                                                                                             | Windows Vista |
| GSM 6.10                                            | ACM GSM 6,10 Codec                                                                                                                                               | Keine                                                                                                                                                             | Windows Vista |
| Windows Media Audio (WMA)                           | [**Windows Media Audio Decoder**](windowsmediaaudiodecoder.md)<br/> [**Windows Media Audio sprach Decoder**](windowsmediaaudiovoicedecoder.md)<br/> | [**Windows Media Audio Encoder**](windowsmediaaudioencoder.md)<br/> [**Windows Media Audio sprach Encoder**](windowsmediaaudiovoiceencoder.md)<br/> | Windows Vista |



 

> [!Note]  
> Media Foundation stellt Wrapper für mehrere ACM-Codecs bereit, die in der vorherigen Tabelle aufgeführt sind. Allerdings unterstützt Media Foundation keine beliebigen ACM-Codecs.

 

## <a name="video-codecs"></a>Videocodecs



| Format                                                                                                         | Decoder                                                                                                                                                                  | Encoder                                                                                                                             | Erforderlich      |
|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|---------------|
| DV-Video                                                                                                       | [**DV-Video Decoder**](dv-video-decoder.md)                                                                                                                             | Keine                                                                                                                                | Windows 7     |
| H.264                                                                                                          | [**H. 264-Video Decoder**](h-264-video-decoder.md)                                                                                                                       | [**H. 264-Video Encoder**](h-264-video-encoder.md)                                                                                  | Windows 7     |
| H.263<br/> (H. 264-baselineprofil, das mit MPEG-4 PT2 Kurzvideo-Header Modus kompatibel ist)<br/> | [**MPEG-4 Part 2-Video Decoder**](mpeg4part2videodecoder.md)                                                                                                            | Keine                                                                                                                                | Windows 8     |
| MJPEG                                                                                                          | MJPEG-Decoder                                                                                                                                                            | Keine                                                                                                                                | Windows 7     |
| MPEG-4 Teil 2                                                                                                  | [**MPEG-4 Part 2-Video Decoder**](mpeg4part2videodecoder.md)                                                                                                            | Keine                                                                                                                                | Windows 7     |
| MPEG-4 v1/v2/v3                                                                                                | [**Windows Media MPEG-4 V3-Decoder**](./windowsmediampeg4v3decoder.md)<br/> [**Windows Media MPEG4 V1/V2-Decoder**](windowsmediampeg4decoder.md)<br/>         | Keine                                                                                                                                | Windows Vista |
| Windows Media Video (WMV)                                                                                      | [**Windows Media Video 9-Decoder**](windowsmediavideo9decoder.md)<br/> [**Windows Media Video 9-Bildschirm Decoder**](windowsmediavideo9screendecoder.md)<br/> | Windows Media Video 9-Encoder<br/> Windows Media Video 9-Bildschirm Encoder<br/> Windows Media Video 7/8-Encoder<br/> | Windows Vista |



 

> [!Note]  
> In der Spalte "erfordert" ist das Betriebssystem, das mindestens erforderlich ist, um diese Codecs in einer Media Foundation Anwendung zu verwenden, aufgeführt. Einige dieser Codecs wurden vor Windows Vista als [DirectX Media Objects](../directshow/directx-media-objects.md) (DMOs) eingeführt. Wenn ein Codec DMO-Funktionalität unterstützt, kann er mit [DirectShow](../directshow/directshow.md) oder dem [Windows Media Format SDK](../wmformat/windows-media-format-11-sdk.md)verwendet werden.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Codec-Objekte](codecobjects.md)
</dt> <dt>

[Media Foundation-Programmier Handbuch](media-foundation-programming-guide.md)
</dt> <dt>

[Medienquellen und senken](media-sources-and-sinks.md)
</dt> </dl>

 

 
