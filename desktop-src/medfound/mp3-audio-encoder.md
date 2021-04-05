---
description: Der Microsoft Media Foundation.
ms.assetid: 4C397139-6553-4707-B737-7C31C5D423BA
title: MP3-Audioencoder
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ea2b22d2fe8cd51f9a2990970493e0415f34d3c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041907"
---
# <a name="mp3-audio-encoder"></a>MP3-Audioencoder

Der Microsoft Media Foundation MP3-Audioencoder ist eine [Media Foundation Transformation](media-foundation-transforms.md) (MFT), die MPEG-1 Layer 3-Audiodaten (MP3) codiert.

## <a name="class-identifier"></a>Klassen Bezeichner

Der Klassen Bezeichner (CLSID) des MP3-Encoders ist die **CLSID- \_ MP3ACMCodecWrapper**, die in der Header Datei "wmcodecdsp. h" definiert ist.

## <a name="media-types"></a>Medientypen

Der MP3-Encoder unterstützt die folgenden Medientypen. Der Ausgabetyp muss vor dem Eingabetyp festgelegt werden.

### <a name="output-types"></a>Ausgabetypen

Legen Sie die folgenden Attribute für den Ausgabe Medientyp fest.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Attribut</th>
<th>BESCHREIBUNG</th>
<th>Bemerkungen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></td>
<td>Der Haupttyp.</td>
<td>Muss <strong>MFMediaType_Audio</strong>werden.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></td>
<td>Audiountertyp.</td>
<td>Muss <strong>MFAudioFormat_MP3</strong>werden.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-avg-bytes-per-second-attribute.md"><strong>MF_MT_AUDIO_AVG_BYTES_PER_SECOND</strong></a></td>
<td>Die Bitrate des codierten MP3-Streams in Bytes pro Sekunde.</td>
<td>Der Encoder unterstützt alle durch den Standard definierten Bitraten (32, 40, 48, 56, 64, 80, 96, 112, 128, 160, 192, 224, 256 oder 320 Kbit/s).<br/> Die Standard Bitraten sind 128 Kbit/s für Mono und 320 Kbit/s für Stereo.<br/> Verwenden Sie dieses Attribut, um die codierte Bitrate anzugeben.<br/></td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></td>
<td>Anzahl der Kanäle.</td>
<td>Die folgenden Werte werden unterstützt:
<ul>
<li>1 (Mono)</li>
<li>2 (Stereo)</li>
</ul></td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></td>
<td>Stichproben pro Sekunde.</td>
<td>Die folgenden Werte werden unterstützt:
<ul>
<li>48000 (48 kHz)</li>
<li>44100 (44,1 kHz)</li>
<li>32000 (32 kHz)</li>
</ul></td>
</tr>
<tr class="even">
<td><a href="mf-mt-user-data-attribute.md">MF_MT_USER_DATA</a></td>
<td>Zusätzliche Codec-Daten.</td>
<td>Dieses Attribut enthält die 12 Bytes der <a href="/windows/desktop/api/mmreg/ns-mmreg-mpeglayer3waveformat"><strong>MPEGLAYER3WAVEFORMAT</strong></a> -Struktur, die dem <strong>wfx</strong> -Member dieser Struktur folgen.</td>
</tr>
</tbody>
</table>



 

Alternativ können Sie eine [**MPEGLAYER3WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-mpeglayer3waveformat) -Struktur ausfüllen und [**mfinitmediatypefromwaveformatex**](/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromwaveformatex) aufrufen, um die Struktur in einen Media Foundation Medientyp zu konvertieren.

### <a name="input-types"></a>Eingabetypen

Legen Sie die folgenden Attribute für den Eingabe Medientyp fest.



| Attribut                                                                               | BESCHREIBUNG         | Bemerkungen                         |
|-----------------------------------------------------------------------------------------|---------------------|---------------------------------|
| [**Haupt-Typ des MF- \_ MT \_ \_**](mf-mt-major-type-attribute.md)                               | Der Haupttyp.         | Muss **MF MediaType \_ -Audiodaten** sein. |
| [**MF- \_ MT- \_ Untertyp**](mf-mt-subtype-attribute.md)                                      | Untertyp.            | Muss **MF Audioformat \_ PCM** sein. |
| [**MF \_ \_ -MT- \_ audiobits \_ pro \_ Beispiel**](mf-mt-audio-bits-per-sample-attribute.md)       | Bits pro Stichprobe.    | Muss 16 sein.                     |
| [**MF \_ \_ -MT- \_ Audiobeispiele \_ pro \_ Sekunde**](mf-mt-audio-samples-per-second-attribute.md) | Stichproben pro Sekunde. | Muss mit dem Ausgabetyp identisch sein.     |
| [**MF \_ \_ -MT- \_ audionum- \_ Kanäle**](mf-mt-audio-num-channels-attribute.md)              | Anzahl der Kanäle. | Muss mit dem Ausgabetyp identisch sein.     |



 

Der Encoder unterstützt nur 16-Bit-ganz Zahl-PCM-Eingaben. Es werden keine 32-Bit-Gleit Komma Eingaben unterstützt.

### <a name="media-formats"></a>Medienformate

Der MPEG-1-und MPEG-2-Standard definiert 252 Layer 3-Audioformate. Der MP3-Encoder unterstützt den Standard mit einigen Ausnahmen sowie einige zusätzliche Formate, wie unten beschrieben. Layer 3 ist definiert als:



| Anforderung | Wert |
|----------------------------------|---------------------------------------------------------------|
| Channels                         | Mono oder Stereo                                                |
| MPEG-1-Stichproben Raten in kHz       | 44,1, 48, 32                                                  |
| MPEG-1-codierte Bitraten in Kbit/s | 32, 40, 48, 56, 64, 80, 96, 112, 128, 160, 192, 224, 256, 320 |
| MPEG-2-Stichproben Raten in kHz       | 8, 11,025, 12, 16, 22,05, 24                                  |
| MPEG-2-codierte Bitraten in Kbit/s | 8, 16, 24, 32, 40, 48, 56, 64, 80, 96, 112, 144, 160          |



 

Der MP3-Encoder unterstützt auch die folgenden Formate.



| Samplingrate | Bitrate     | Kanalnummer |
|-------------|--------------|----------------|
| 8.000        | 18000, 20000 | 2              |
| 11025       | 18000, 20000 | 1 oder 2         |
| 12000       | 18000, 20000 | 1 oder 2         |
| 16000       | 18000, 20000 | 1              |
| 32000       | 144000       | 1 oder 2         |
| 44100       | 144000       | 1 oder 2         |
| 48000       | 144000       | 1 oder 2         |



 

Der MP3-Encoder unterstützt die folgenden Formate nicht, die vom Standard definiert werden.



| Samplingrate | Bitraten                                    | Kanalnummer |
|-------------|----------------------------------------------|----------------|
| 12000       | 80000, 96000, 112000, 128000, 144000, 160000 | 1 oder 2         |
| 11025       | 80000, 96000, 112000, 128000, 144000, 160000 | 1 oder 2         |
| 8.000        | 80000, 96000, 112000, 128000, 144000, 160000 | 1 oder 2         |
| 8.000        | 8000, 11025, 12000, 16000, 22050, 24000      | 2              |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Codec-Objekte](codecobjects.md)
</dt> </dl>

 

 
