---
description: Unterstützte Formate in DirectShow
ms.assetid: cd8af779-2fb5-4724-a838-5d0c8244f0d3
title: Unterstützte Formate in DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10e42079f29ce89ba66fcd0c03a6520769a91538eb1a9b8901115b6895420d65
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119633230"
---
# <a name="supported-formats-in-directshow"></a>Unterstützte Formate in DirectShow

DirectShow ist eine offene Architektur, was bedeutet, dass sie jedes Format unterstützen kann, solange Filter zum Analysieren und Decodieren verfügbar sind. Die von Microsoft bereitgestellten Filter , entweder als verteilbare Elemente über DirectShow oder als Windows-Betriebssystemkomponenten, bieten Standardunterstützung für die folgenden Datei- und Komprimierungsformate.

Dateitypen:



| Dateityp                                                                                        | Weitere Informationen                                                                                                                  |
|--------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| Advanced Systems Format (ASF), einschließlich Windows Media Audio (WMA) und Windows Media Video (WMV) | [WM ASF-Readerfilter](about-the-wm-asf-reader-filter.md)<br/> [WM ASF Writer-Filter](wm-asf-writer-filter.md)<br/> |
| Aiff                                                                                             | [WAVE-Parserfilter](wave-parser-filter.md)                                                                                      |
| AU                                                                                               | [WAVE-Parserfilter](wave-parser-filter.md)                                                                                      |
| Audio-Video Interleaved (AVI)                                                                    | [AVI Mux-Filter](avi-mux-filter.md)<br/> [AVI-Splitterfilter](avi-splitter-filter.md)<br/>                         |
| MIDI                                                                                             | [PARSER-Filter](midi-parser-filter.md)<br/> [**RENDERING-Rendererfilter**](midi-renderer-filter.md)<br/>           |
| Snd                                                                                              |                                                                                                                                   |
| WAV                                                                                              | [WAVE-Parserfilter](wave-parser-filter.md)                                                                                      |



 

Komprimierungsformate:



| Format                                        | Weitere Informationen                                                                                                                                                                                                                                |
|-----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AAC                                           | [**Microsoft MPEG-1/DD/AAC-Audiodecoder**](microsoft-mpeg-1-dd-audio-decoder.md)                                                                                                                                                              |
| Cineppe                                       |                                                                                                                                                                                                                                                 |
| Digitales Video (DV)                            | [DV-Videodecoderfilter](dv-video-decoder-filter.md)<br/> [DV-Videoencoderfilter](dv-video-encoder-filter.md)<br/>                                                                                                             |
| H.264                                         | [**Microsoft MPEG-2-Videodecoder**](microsoft-mpeg-2-video-decoder.md)                                                                                                                                                                        |
| ISO MPEG-4 Videoversion 1.0                  |                                                                                                                                                                                                                                                 |
| Microsoft MPEG-4 Version 3                    |                                                                                                                                                                                                                                                 |
| Mjpeg                                         | [MJPEG-Filter "Filter für Filter"](mjpeg-compressor-filter.md)<br/> [MJPEG-Dekomprimierungsfilter](mjpeg-decompressor-filter.md)<br/>                                                                                                         |
| MPEG Audio Layer-3 (MP3) (nur Dekomprimierung) |                                                                                                                                                                                                                                                 |
| MPEG-1-Layer-I- und Layer-II-Audio             | [**Microsoft MPEG-1/DD/AAC-Audiodecoder**](microsoft-mpeg-1-dd-audio-decoder.md)<br/> [MPEG-1-Audiodecoderfilter](mpeg-1-audio-decoder-filter.md)<br/>                                                                         |
| MPEG-1-Video                                  | [MPEG-1-Videodecoderfilter](mpeg-1-video-decoder-filter.md)<br/> [**Microsoft MPEG-2-Videodecoder**](microsoft-mpeg-2-video-decoder.md)<br/>                                                                                   |
| MPEG-2-Audio                                  | [**Microsoft MPEG-2-Audioencoder**](microsoft-mpeg-2-audio-encoder.md)<br/> [**Microsoft MPEG-2 Encoder**](microsoft-mpeg-2-encoder.md)<br/>                                                                                     |
| MPEG-2-Video                                  | [**Microsoft MPEG-2 Encoder**](microsoft-mpeg-2-encoder.md)<br/> [**Microsoft MPEG-2-Videodecoder**](microsoft-mpeg-2-video-decoder.md)<br/> [**Microsoft MPEG-2 Video Encoder**](microsoft-mpeg-2-video-encoder.md)<br/> |



 

Informationen zur Verfügbarkeit bestimmter Drittanbietercodecs für die Weiterverteilung mit DirectShow-Anwendungen erhalten Sie vom Codechersteller.

 

 




