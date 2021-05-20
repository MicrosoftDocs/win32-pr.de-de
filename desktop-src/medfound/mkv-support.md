---
description: In diesem Abschnitt werden die Media Foundation Matroska Media Container-Dateien (MKV) beschrieben.
title: Matroska Media Container -Unterstützung (MKV)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdd860f58087bc8a0f3fe95d278bfa81edc412d0
ms.sourcegitcommit: 88049609e29f91a42442235885abf56f598b06b3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/19/2021
ms.locfileid: "110154215"
---
# <a name="matroska-media-container-mkv-support"></a>Matroska Media Container -Unterstützung (MKV)

In diesem Abschnitt werden die Media Foundation Matroska Media Container-Dateien (MKV) beschrieben.

Das MKV-Format kann mehrere Video- und Audiocodecs unterstützen, z. B. H.264- und AAC-Audio. Im Allgemeinen beschreiben Container, wie Video- und Audiodaten angelegt werden und welche ergänzenden Informationen verwendet werden, um diese A/V-Streams zu beschreiben. Container können auch Daten enthalten, die A/V-Streams ergänzen, z. B. Titel, Sprachen der Audiostreams, Untertitel- oder Untertiteltitel, Schriftarten für diese Untertitel, Bilder, Kapitelinformationen und Menüs. MKV ist ein äußerst flexibles Format, das viele dieser Containerfeatures unterstützt. Weitere Informationen zum MKV-Format finden Sie unter [https://matroska.org](https://matroska.org/)


## <a name="mkv-container-feature-support"></a>Unterstützung von MKV-Containerfeatures
MKV-Containerfeatures werden auf der von Media Foundation wie folgt unterstützt:
- Wenn eine oder mehrere Videospuren vorhanden sind, wird der erste Titel abgespielt.
- Wenn eine oder mehrere Audiospuren vorhanden sind, wird der erste Titel abgespielt.
- Untertiteltitel werden unterstützt, sind aber standardmäßig nicht ausgewählt (abgespielt).
- Wenn eine oder mehrere Schriftarten oder Bilder vorhanden sind, werden Untertitel und Bilder nicht gerendert, obwohl die Datei geladen und wiedergegeben wird.
- Menüinformationen werden nicht unterstützt und nicht angezeigt, aber die Datei wird geladen und abspielt.
- Wenn Dateien mit Kapiteln auf ergänzende Dateien verweisen, werden die ergänzenden Dateien nicht wieder verwendet.
- Miniaturansichten sind verfügbar, wenn Sie mithilfe des Dateibrowsers nach Dateien auf USB-Laufwerken suchen.

Dieser Satz von Features sollte die Wiedergabe der meisten MKV-Dateien ermöglichen, wenn sie unterstützte Codecs enthalten.
MKV-Dateien, die Video- und Audiospuren enthalten, die mit den im folgenden Abschnitt aufgeführten Codecs codiert sind, werden unterstützt.

## <a name="supported-mkv-codecs"></a>Unterstützte MKV-Codecs

### <a name="video-codec-support-for-mkv"></a>Videocodec-Unterstützung für MKV

Matroska-ID: V_MPEG4/ISO/AVC

- MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_H264
- Beschreibung: H.264-Video
- FourCC- oder WAV-Bezeichner: H264

Matroska-ID: V_MPEG2

- MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_MPEG2
- Beschreibung: MPEG-2-Video

Matroska-ID: V_MPEG1

- MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_MPG1
- Beschreibung: MPEG-1-Video
- FourCC- oder WAV-Bezeichner: MPG1

Matroska-ID: V_MPEG4/MS/V3

- MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_MP43
- Beschreibung: Microsoft MPEG 4 Codec Version 3
- FourCC- oder WAV-Bezeichner: MP43

Matroska-ID: V_MPEG4/ISO/ASP

- MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_MP4V
- Beschreibung: MPEG-4 Part 2 video (MPEG-4 Teil 2-Video)
- FourCC- oder WAV-Bezeichner: MP4V

Matroska-ID: V_MS/VFW/FOURCC

- Beschreibung: Wird mehreren Codecs im AVI-Format, die in der Konsole verfügbar sind, normalerweise unterstützt.

Matroska-ID: V_THEORA

- MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_Theora
- Beschreibung: Theora
- FourCC- oder WAV-Bezeichner: theo

Matroska-ID: V_MPEG4/ISO/SP

- MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_MP4V
- Beschreibung: MPEG4 ISO Simple Profile (DivX4)
- FourCC- oder WAV-Bezeichner: MP4V

Matroska-ID: V_MPEG4/ISO/AP

- MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_MP4V
- Beschreibung: MPEG4 ISO advanced simple profile (DivX5,IgenD, FFMPEG)
- FourCC- oder WAV-Bezeichner: MP4V


Matroska-ID: V_MPEGH/ISO/HEVC 

- MSFT-Media Foundation MF_MT_SUBTYPE: MFVideoFormat_HEVC
- Beschreibung: HEVC/H.265
- FourCC- oder WAV-Bezeichner: 

Matroska-ID: V_VP8

- MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_VP80
- Beschreibung: VP8-Codecformat
- FourCC- oder WAV-Bezeichner: VP80

Matroska-ID: V_VP9

- MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_VP90
- Beschreibung: VP9-Codecformat
- FourCC- oder WAV-Bezeichner: VP90

Matroska-ID: V_MJPEG

- MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_MJPG
- Beschreibung: Motion JPEG
- FourCC- oder WAV-Bezeichner: MJPG

Matroska-ID: V_AV1

- MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_AV1
- Beschreibung: AOMedia Video 1
- FourCC- oder WAV-Bezeichner: AV01

### <a name="audio-codec-support-for-mkv"></a>Audiocodec-Unterstützung für MKV

Matroska-ID: A_AAC

- MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_AAC
- Beschreibung: Erweiterte Audiocodierung (Advanced Audio Coding, AAC)
- FourCC- oder WAV-Bezeichner: WAVE_FORMAT_MPEG_HEAAC

Matroska-ID: A_AC3

- MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_Dolby_AC3
- Beschreibung: Dolby AC3
- FourCC- oder WAV-Bezeichner: WAVE_FORMAT_DOLBY_AC3_SPDIF

Matroska-ID: A_MPEG/L3

- MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_MP3
- Beschreibung: MPEG Audio Layer-3 (MP3)
- FourCC- oder WAV-Bezeichner: WAVE_FORMAT_MPEGLAYER3

Matroska-ID: A_MPEG/L1

- MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_MPEG
- Beschreibung: MPEG-1-Audionutzlast
- FourCC- oder WAV-Bezeichner: WAVE_FORMAT_MPEG

Matroska-ID: A_PCM/INT/BIG

- MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_PCM
- Beschreibung: Unkomprimierte PCM-Audiodaten
- FourCC- oder WAV-Bezeichner: WAVE_FORMAT_PCM

Matroska-ID: A_PCM/INT/LIT

- MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_PCM
- Beschreibung: Unkomprimierte PCM-Audiodaten
- FourCC- oder WAV-Bezeichner: WAVE_FORMAT_PCM

Matroska-ID: A_PCM/FLOAT/IEEE

- MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_Float
- Beschreibung: Unkomprimierte IEEE-Gleitkommaaudio
- FourCC- oder WAV-Bezeichner: WAVE_FORMAT_IEEE_FLOAT

Matroska-ID: A_ALAC

- MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_ALAC
- Beschreibung: Apple Lossless Audio Codec
- FourCC- oder WAV-Bezeichner: 

Matroska-ID: A_MPEG/L2

- MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_MPEG
- Beschreibung: MPEG Audio 1, 2 Layer II
- FourCC- oder WAV-Bezeichner: WAVE_FORMAT_MPEG

Matroska-ID: A_DTS

- MSFT Media Foundation MF_MT_SUBTYPE: MEDIASUBTYPE_DTS_HD
- Beschreibung: DigitalSchreibesystem
- FourCC- oder WAV-Bezeichner: WAVE_FORMAT_DTS

Matroska-ID: A_OPUS

- MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_Opus
- Beschreibung: Opus
- FourCC- oder WAV-Bezeichner: WAVE_FORMAT_OPUS

Matroska-ID: A_VORBIS

- MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_Vorbis
- Beschreibung: Vorbis
- FourCC- oder WAV-Bezeichner: 

Matroska-ID: A_FLAC

- MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_FLAC
- Beschreibung: Freier verlustfreier Audiocodec
- FourCC- oder WAV-Bezeichner: WAVE_FORMAT_FLAC

Matroska-ID: A_AAC/MAIN

- MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_AAC
- Beschreibung: Erweiterte Audiocodierung (Advanced Audio Coding, AAC)
- FourCC- oder WAV-Bezeichner: WAVE_FORMAT_MPEG_HEAAC

Matroska-ID: A_EAC3

- MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_Dolby_DDPlus
- Beschreibung: Erweiterte AC-3
- FourCC- oder WAV-Bezeichner: 

Matroska-ID: A_TRUEHD

- MSFT Media Foundation MF_MT_SUBTYPE: MEDIASUBTYPE_DOLBY_TRUEHD
- Beschreibung: Dolby TrueHD
- FourCC- oder WAV-Bezeichner: 

Matroska-ID: A_MS/ACM

- MSFT Media Foundation MF_MT_SUBTYPE: Wird mehreren in mmreg.h definierten WAVE_FORMAT Audiotypen zugeordnet.


### <a name="subtitles-codec-support-for-mkv"></a>Unterstützung des Untertitelcodecs für MKV

Matroska-ID: S_TEXT/ASCII

- MSFT Media Foundation MF_MT_SUBTYPE: MFSubtitleFormat_SRT
- Beschreibung: ASCII-Text

Matroska-ID: S_TEXT/UTF8

- MSFT Media Foundation MF_MT_SUBTYPE: MFSubtitleFormat_SRT
- Beschreibung: UTF-8-Nur-Text

Matroska-ID: S_TEXT/SSA

- MSFT Media Foundation MF_MT_SUBTYPE: MFSubtitleFormat_SSA
- Beschreibung: Untertitelformat

Matroska-ID: S_TEXT/ASS

- MSFT Media Foundation MF_MT_SUBTYPE: MFSubtitleFormat_SSA
- Beschreibung: Erweitertes Untertitelformat

Matroska-ID: S_VOBSUB

- MSFT Media Foundation MF_MT_SUBTYPE: MFSubtitleFormat_VobSub
- Beschreibung: VobSub-Untertitel

Matroska-ID: S_HDMV/PGS

- MSFT Media Foundation MF_MT_SUBTYPE: MFSubtitleFormat_PGS
- Beschreibung: HDMV Presentation Graphics Untertitel (PGS)


## <a name="technical-details-regarding-codecs"></a>Technische Details zu Codecs

Im Folgenden finden Sie technische Details zu Codecs.

- [Matroska-Codecspezifikationen](http://www.matroska.org/technical/specs/codecid/index.html)
- [AudioUntertyp-GUIDs](audio-subtype-guids.md)
- [Video-Untertyp-GUIDs](video-subtype-guids.md)


## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Unterstützte Medienformate in Media Foundation](supported-media-formats-in-media-foundation.md)
</dt> <dt>

[Media Foundation-Programmierhandbuch](media-foundation-programming-guide.md)
</dt> </dl>

 

 



