---
description: Der Dolby-Audiodecoder ist eine Media Foundation Transformation (MFT), die Mono-oder Stereo-Audiodaten in Dolby Digital codiert, auch als Dolby AC-3 bezeichnet.
ms.assetid: CBC31132-046C-4CD7-9DBA-20A9C666FB43
title: Dolby Digital-Audioencoder
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58d6c5b59bc09cd8c0fd56f22703ef8afdfe3921
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343022"
---
# <a name="dolby-digital-audio-encoder"></a>Dolby Digital-Audioencoder

Der Dolby-Audiodecoder ist eine [Media Foundation Transformation](media-foundation-transforms.md) (MFT), die Mono-oder Stereo-Audiodaten in Dolby Digital codiert, auch als Dolby AC-3 bezeichnet. Der Encoder unterstützt keine multikanaleingaben, z. b. die 5,1-Kanal Konfiguration.

> [!IMPORTANT]
> Bei Windows-Versionen vor Windows 8 ist die Microsoft-Implementierung der Dolby Digital-Technologie gemäß den Bedingungen des Dolby Digital Licensing Program, das von Microsoft-Anwendungen verwendet werden soll, eingeschränkt.

 

Weitere Informationen zu Dolby Digital-Audiodaten finden Sie unter Advanced Television System Committee (ATSC) Document *Digital audiocompression Standard (AC-3, E-AC-3) Revision B*.

## <a name="class-identifier"></a>Klassen Bezeichner

Der Klassen Bezeichner (CLSID) des Dolby-Audiodecoders ist **CLSID \_ cmsdolbydigitalencmft**, der in der Header Datei "wmcodecdsp. h" definiert ist.

## <a name="output-types"></a>Ausgabetypen

Der Ausgabetyp muss zuerst festgelegt werden, vor dem Eingabetyp. In der folgenden Tabelle sind die erforderlichen und optionalen Attribute für den Ausgabe Medientyp aufgeführt.



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
<td><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></td>
<td>Der Haupttyp.</td>
<td>Erforderlich. Muss <strong>MFMediaType_Audio</strong>werden.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></td>
<td>Audiountertyp.</td>
<td>Erforderlich. Muss <strong>MFAudioFormat_Dolby_AC3</strong>werden.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></td>
<td>Stichproben pro Sekunde.</td>
<td>Erforderlich. Die folgenden Werte werden unterstützt:
<ul>
<li>32000</li>
<li>44100</li>
<li>48000</li>
</ul></td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></td>
<td>Anzahl der Kanäle.</td>
<td>Erforderlich. Muss entweder 1 (Mono) oder 2 (Stereo) sein.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></td>
<td>Gibt die Zuweisung von Audiokanälen zu Redner Positionen an.</td>
<td>Dies ist optional. Wenn festgelegt, muss der Wert 0x3 für Stereo (Front Left und Right Channels) oder 0x4 für Mono (Front-Center-Kanal) lauten.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></td>
<td>Die Bitrate des codierten AC-3-Streams in Bytes pro Sekunde.</td>
<td>Dies ist optional. Gültige Werte finden Sie unter "Hinweise". Wenn dieses Attribut nicht festgelegt ist, verwendet der Encoder eine Standard Bitrate, wie unter Hinweise beschrieben.</td>
</tr>
</tbody>
</table>



 

Wenn die optionalen Attribute nicht festgelegt sind, fügt der Encoder Sie dem Medientyp hinzu, nachdem der Typ festgelegt wurde.

## <a name="input-types"></a>Eingabetypen

In der folgenden Tabelle sind die erforderlichen und optionalen Attribute für den Eingabe Medientyp aufgeführt.



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
<td><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></td>
<td>Der Haupttyp.</td>
<td>Erforderlich. Muss <strong>MFMediaType_Audio</strong>werden.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></td>
<td>Audiountertyp.</td>
<td>Erforderlich. Muss <strong>MFAudioFormat_PCM</strong> oder <strong>MFAudioFormat_Float</strong>sein.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a></td>
<td>Anzahl von Bits pro audiostich Probe.</td>
<td>Erforderlich. Der Wert muss 16 sein, wenn der Untertyp <strong>MFAudioFormat_PCM</strong>ist, oder 32, wenn der Untertyp <strong>MFAudioFormat_Float</strong>ist.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></td>
<td>Stichproben pro Sekunde.</td>
<td>Erforderlich. Muss mit dem Ausgabetyp identisch sein.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></td>
<td>Anzahl der Kanäle.</td>
<td>Erforderlich. Muss mit dem Ausgabetyp identisch sein.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-block-alignment-attribute.md">MF_MT_AUDIO_BLOCK_ALIGNMENT</a></td>
<td>Block Ausrichtung (in Bytes).</td>
<td>Erforderlich. Berechnen Sie den Wert wie folgt:
<ul>
<li><strong>MFAudioFormat_PCM</strong>: Anzahl der Kanäle × 2.</li>
<li><strong>MFAudioFormat_Float</strong>: Anzahl der Kanäle × 4.</li>
</ul></td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></td>
<td>Die Bitrate des codierten AC3-Streams in Bytes pro Sekunde.</td>
<td>Erforderlich. Muss die Block Ausrichtung × Samples pro Sekunde gleich sein.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></td>
<td>Gibt die Zuweisung von Audiokanälen zu Redner Positionen an.</td>
<td>Dies ist optional. Wenn festgelegt, muss der Wert mit dem Ausgabetyp identisch sein.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-valid-bits-per-sample-attribute.md">MF_MT_AUDIO_VALID_BITS_PER_SAMPLE</a></td>
<td>Anzahl gültiger Bits von Audiodaten in jedem Audiobeispiel.</td>
<td>Dies ist optional. Wenn dieser Wert festgelegt ist, muss der Wert mit <a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a>identisch sein.</td>
</tr>
</tbody>
</table>



 

Der Encoder unterstützt keine Stichproben Raten Konvertierung oder Stereo/Mono-Konvertierung.

## <a name="remarks"></a>Bemerkungen

Jeder Dolby AC-3-audioframe enthält 1536 Audiobeispiele pro Kanal. Jeder Eingabepuffer für den Encoder kann jedoch eine beliebige Anzahl von PCM-Stichproben enthalten. Die Größe jedes Eingabe Puffers muss ein Vielfaches der Block Ausrichtung sein. Der Encoder speichert Eingabe Beispiele zwischen, bis er für 1536-Audiobeispiele pro Kanal genug ist. an diesem Punkt gibt der Encoder einen AC-3-Frame aus.

Jeder Ausgabepuffer enthält einen unformatierten AC-3-Frame. Die Dauer entspricht der Dauer von 1536 PCM-Stichproben mit der aktuellen Samplingrate (32 MS) um 48 kHz Sample Rate, 34,83 ms bei 44,1 kHz und 48 ms bei 32 kHz). Die Größe jedes Ausgabepuffers hängt von der Bitrate und der Stichprobenrate ab.

Um die Codierungs Bitrate anzugeben, legen Sie das Attribut [MF \_ MT \_ -audiodurchschn \_ \_ Bytes \_ pro \_ Sekunde](mf-mt-audio-avg-bytes-per-second-attribute.md) im Ausgabetyp fest. In der folgenden Tabelle wird die Beziehung zwischen der Codierungs Bitrate und den von MF \_ \_ -MT- \_ \_ Bytes pro Sekunde verfügbaren Bytes angezeigt \_ \_ .



| Bitrate (Kbit/s) | [MF \_ \_ -MT-audiodurchschn. \_ \_ Byte \_ pro \_ Sekunde](mf-mt-audio-avg-bytes-per-second-attribute.md) | Bemerkungen                                                 |
|-----------------|------------------------------------------------------------------------------------------|---------------------------------------------------------|
| 64              | 8.000                                                                                     | Nur Mono.                                              |
| 80              | 10000                                                                                    | Nur Mono.                                              |
| 96              | 12000                                                                                    | Nur Mono.                                              |
| 112             | 14000                                                                                    | Nur Mono.                                              |
| 128             | 16000                                                                                    | Mono oder Stereo.                                         |
| 160             | 20000                                                                                    | Mono oder Stereo.                                         |
| 192             | 24.000                                                                                    | Mono oder Stereo. Dies ist die Standardeinstellung für Mono.   |
| 224             | 28000                                                                                    | Mono oder Stereo.                                         |
| 256             | 32000                                                                                    | Mono oder Stereo. Dies ist die Standardeinstellung für Stereo. |
| 320             | 40.000                                                                                    | Nur Stereo.                                            |
| 384             | 48000                                                                                    | Nur Stereo.                                            |
| 448             | 56000                                                                                    | Nur Stereo.                                            |



 

Die standardmäßige Codierungs Bitrate ist für Stereo und 192 Kbit/s für Mono auf 256 KBit/s festgelegt. Die Standardeinstellungen werden in den von der [**imftransform:: getoutputavailabletype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) -Methode des Encoders zurückgegebenen Medientypen widergespiegelt.

### <a name="example-media-types"></a>Beispiel Medientypen

Im folgenden finden Sie ein Beispiel für die Medientypen, die zum Codieren von ganzzahligen 16-Bit-PCM, 48-kHz-Stereo Audiodaten mit der Standard Bitrate von 256 KBit/s erforderlich sind.

Ausgabe Medientyp:

| Attribut                                                                           | Wert                         |
|-------------------------------------------------------------------------------------|-------------------------------|
| [Haupt-Typ des MF- \_ MT \_ \_](mf-mt-major-type-attribute.md)                               | **MF MediaType \_ -Audiodatei**        |
| [MF- \_ MT- \_ Untertyp](mf-mt-subtype-attribute.md)                                      | **MF Audioformat \_ Dolby \_ AC3** |
| [MF \_ \_ -MT- \_ Audiobeispiele \_ pro \_ Sekunde](mf-mt-audio-samples-per-second-attribute.md) | 48000                         |
| [MF \_ \_ -MT- \_ audionum- \_ Kanäle](mf-mt-audio-num-channels-attribute.md)              | 2                             |



 

Eingabe Medientyp:

| Attribut                                                                                | Wert                  |
|------------------------------------------------------------------------------------------|------------------------|
| [Haupt-Typ des MF- \_ MT \_ \_](mf-mt-major-type-attribute.md)                                    | **MF MediaType \_ -Audiodatei** |
| [MF- \_ MT- \_ Untertyp](mf-mt-subtype-attribute.md)                                           | **MF Audioformat \_ PCM** |
| [MF \_ \_ -MT- \_ audiobits \_ pro \_ Beispiel](mf-mt-audio-bits-per-sample-attribute.md)            | 16                     |
| [MF \_ \_ -MT- \_ Audiobeispiele \_ pro \_ Sekunde](mf-mt-audio-samples-per-second-attribute.md)      | 48000                  |
| [MF \_ \_ -MT- \_ audionum- \_ Kanäle](mf-mt-audio-num-channels-attribute.md)                   | 2                      |
| [MF \_ \_ -MT- \_ Audioblock \_ Ausrichtung](mf-mt-audio-block-alignment-attribute.md)             | 4                      |
| [MF \_ \_ -MT-audiodurchschn. \_ \_ Byte \_ pro \_ Sekunde](mf-mt-audio-avg-bytes-per-second-attribute.md) | 192000                 |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8 \[ -Desktop-Apps \| UWP-apps\]<br/>                                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                               |
| DLL<br/>                      | <dl> <dt>Msac3enc.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Codec-Objekte](codecobjects.md)
</dt> </dl>

 

 




