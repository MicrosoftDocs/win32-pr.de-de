---
description: Unterstützte Formate in DirectShow
ms.assetid: cd8af779-2fb5-4724-a838-5d0c8244f0d3
title: Unterstützte Formate in DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5a6c9a0c85a3ccdfd3db092ba2efce00a191493
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359192"
---
# <a name="supported-formats-in-directshow"></a>Unterstützte Formate in DirectShow

DirectShow ist eine offene Architektur, was bedeutet, dass Sie jedes beliebige Format unterstützen kann, solange Filter zum Analysieren und decodieren vorhanden sind. Die von Microsoft bereitgestellten Filter, entweder als verteilbare Komponenten über DirectShow oder als Windows-Betriebssystemkomponenten, bieten Standardunterstützung für die folgenden Datei-und Komprimierungs Formate.

Dateitypen:



| Dateityp                                                                                        | Weitere Informationen                                                                                                                  |
|--------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| Advanced Systems Format (ASF), einschließlich Windows Media Audio (WMA) und Windows Media Video (WMV) | [WM-ASF-Lesefilter](about-the-wm-asf-reader-filter.md)<br/> [WM-ASF-Writer-Filter](wm-asf-writer-filter.md)<br/> |
| AIFF                                                                                             | [Filter für Wave-Parser](wave-parser-filter.md)                                                                                      |
| AU                                                                                               | [Filter für Wave-Parser](wave-parser-filter.md)                                                                                      |
| Audio-Video Interleaved (AVI)                                                                    | [AVI MUX-Filter](avi-mux-filter.md)<br/> [AVI-Splitter Filter](avi-splitter-filter.md)<br/>                         |
| MIDI                                                                                             | [MIDI-Parser-Filter](midi-parser-filter.md)<br/> [**MIDI-rendererfilter**](midi-renderer-filter.md)<br/>           |
| SND                                                                                              |                                                                                                                                   |
| WAV                                                                                              | [Filter für Wave-Parser](wave-parser-filter.md)                                                                                      |



 

Komprimierungs Formate:



| Format                                        | Weitere Informationen                                                                                                                                                                                                                                |
|-----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AAC                                           | [**Microsoft MPEG-1/DD/AAC-Audiodecoder**](microsoft-mpeg-1-dd-audio-decoder.md)                                                                                                                                                              |
| Cinepak                                       |                                                                                                                                                                                                                                                 |
| Digitales Video (DV)                            | [DV-Video-Decoderfilter](dv-video-decoder-filter.md)<br/> [DV-Video Encoder-Filter](dv-video-encoder-filter.md)<br/>                                                                                                             |
| H.264                                         | [**Microsoft MPEG-2-Video Decoder**](microsoft-mpeg-2-video-decoder.md)                                                                                                                                                                        |
| ISO MPEG-4-Videoversion 1,0                  |                                                                                                                                                                                                                                                 |
| Microsoft MPEG-4, Version 3                    |                                                                                                                                                                                                                                                 |
| MJPEG                                         | [MJPEG-Daemon-Filter](mjpeg-compressor-filter.md)<br/> [MJPEG-Debug-Filter](mjpeg-decompressor-filter.md)<br/>                                                                                                         |
| MPEG-Audioschicht-3 (MP3) (nur für die Komprimierung) |                                                                                                                                                                                                                                                 |
| MPEG-1 Layer I-und Layer II-Audiodatei             | [**Microsoft MPEG-1/DD/AAC-Audiodecoder**](microsoft-mpeg-1-dd-audio-decoder.md)<br/> [MPEG-1-audiodecoderfilter](mpeg-1-audio-decoder-filter.md)<br/>                                                                         |
| MPEG-1-Video                                  | [MPEG-1-Video-Decoderfilter](mpeg-1-video-decoder-filter.md)<br/> [**Microsoft MPEG-2-Video Decoder**](microsoft-mpeg-2-video-decoder.md)<br/>                                                                                   |
| MPEG-2-Audiodatei                                  | [**Microsoft MPEG-2-Audioencoder**](microsoft-mpeg-2-audio-encoder.md)<br/> [**Microsoft MPEG-2-Encoder**](microsoft-mpeg-2-encoder.md)<br/>                                                                                     |
| MPEG-2-Video                                  | [**Microsoft MPEG-2-Encoder**](microsoft-mpeg-2-encoder.md)<br/> [**Microsoft MPEG-2-Video Decoder**](microsoft-mpeg-2-video-decoder.md)<br/> [**Microsoft MPEG-2-Video Encoder**](microsoft-mpeg-2-video-encoder.md)<br/> |



 

Informationen zur Verfügbarkeit von bestimmten Drittanbieter-Codecs für die Weiterverteilung mit DirectShow-Anwendungen erhalten Sie vom Codec-Hersteller.

 

 




