---
description: 'Der Microsoft Media Foundation AAC-Decoder ist eine Media Foundation Transformation, die die folgenden "Advanced audiocoding (AAC)"-und "High Efficiency AAC"-Profile decodiert:'
ms.assetid: 036fb0ee-8165-41a3-b41a-2e9bf035a6a6
title: AAC-Decoder
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82dde090dee98cddce9658366bde593b5fc779d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348989"
---
# <a name="aac-decoder"></a>AAC-Decoder

Der Microsoft Media Foundation AAC-Decoder ist eine [Media Foundation Transformation](media-foundation-transforms.md) , die die folgenden "Advanced audiocoding (AAC)"-und "High Efficiency AAC"-Profile decodiert:

-   MPEG-2 AAC Low Komplexitäts Profil (LC) (Multichannel).
-   MPEG-4 HE-AAC v1 (Multichannel) mit AAC-LC Core.
-   MPEG-4 HE-AAC v2 (Stereo) mit AAC-LC Core.

Der AAC-Decoder unterstützt sowohl unformatierte AAC-Streams ohne Header und AAC in einem Audiodaten-Transportdaten Strom (ADTs).

Ab Windows 8 unterstützt der AAC-Decoder auch das Decodieren von MPEG-4-audiotransportstreams mit einer Multiplex Schicht (latm) und einer Synchronisierungs Schicht (LoAs). Außerdem kann ein latm/LoAs-Stream in ADTs konvertiert werden.

## <a name="media-types"></a>Medientypen

Der AAC-Decoder unterstützt die folgenden Medientypen.

### <a name="input-types"></a>Eingabetypen

Der AAC-Decoder unterstützt die folgenden audiountertypen:



| Subtype                     | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   | Header       |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|
| **MFAudioFormat_AAC**      | Unformatierte AAC-oder ADTs-AAC.<br/> Für diesen Untertyp gibt der Medientyp die Samplingrate und die Anzahl der Kanäle vor der Anwendung von SBR (Spectral Band Replication) und den Parametern der parametrischen Stereo (PS) an, falls vorhanden. Der Effekt des SBR-Tools besteht darin, die decodierte Samplingrate in Relation zur Core AAC-LC-Stichprobenrate zu verdoppeln. Der Effekt des PS-Tools besteht darin, Stereo von einem Mono-Channel-Kern-AAC-LC-Stream zu decodieren.<br/> Dieser Untertyp entspricht **MEDIASUBTYPE_MPEG_HEAAC**, die in wmcodecdsp. h definiert ist. Siehe [audiountertyp-GUIDs](audio-subtype-guids.md). <br/> Dieser Untertyp wird von der [MPEG-4-Datei Quelle](mpeg-4-file-source.md) und vom ADTs-Parser ausgegeben. <br/> | mfapi. h      |
| **MEDIASUBTYPE_RAW_AAC1** | RAW-AAC. <br/> Dieser Untertyp wird für AAC verwendet, der in einer AVI-Datei mit dem audioformattag gleich WAVE_FORMAT_RAW_AAC1 (0x00FF) enthalten ist. <br/> Für diesen Untertyp gibt der Medientyp die Stichprobenrate und die Anzahl der Kanäle nach Anwendung der SBR-und PS-Tools an (sofern vorhanden).<br/>                                                                                                                                                                                                                                                                                                                                                                                      | wmcodecdsp. h |



 

Legen Sie zum Konfigurieren des AAC-Decoders die folgenden Attribute für den Eingabe Medientyp fest.



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
<td>Weitere Informationen finden Sie in der vorherigen Beschreibung.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-aac-audio-profile-level-indication.md">MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION</a></td>
<td>Audioprofil und-Ebene. <br/></td>
<td>Dies ist optional. Gilt nur für <strong>MFAudioFormat_AAC</strong>. <br/> Der Wert dieses Attributs ist das Feld <strong>audioprofilelevelindikation</strong> gemäß ISO/IEC 14496-3. <br/> Wenn unbekannt, legen Sie auf 0 (null) oder auf 0xFE ( &quot; kein Audioprofil angegeben &quot; ) fest.<br/></td>
</tr>
<tr class="even">
<td><a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a></td>
<td>Der Nutzlasttyp.<br/></td>
<td>Gilt nur für <strong>MFAudioFormat_AAC</strong>. Der Decoder unterstützt die folgenden Nutz Last Typen: <br/>
<ul>
<li>0: RAW-AAC. Der Stream enthält nur raw_data_block ()-Elemente, wie in MPEG-2 definiert.</li>
<li>1: ADTS. Der Stream enthält eine adts_sequence (), wie in MPEG-2 definiert. Es ist nur ein raw_data_block () pro adts_frame () zulässig.</li>
<li>3: audiotransportstream mit einer Synchronisierungs Schicht (LoAs) und einer Multiplex Schicht (latm). Von den drei Typen von LoAs wird nur <strong>audiosyncstream</strong> unterstützt. Die Multiplex Schicht ist <strong>audiomuxelement</strong>, das auf ein Audioprogramm und eine Ebene beschränkt ist.</li>
</ul>
<a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a> ist optional. Wenn dieses Attribut nicht angegeben wird, wird der Standardwert 0 verwendet, der angibt, dass der Stream nur raw_data_block Elemente enthält.<br/></td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-bits-per-sample-attribute.md"><strong>MF_MT_AUDIO_BITS_PER_SAMPLE</strong></a></td>
<td>Gewünschte Bittiefe der decodierten PCM-Audiodaten.</td>

</tr>
<tr class="even">
<td><a href="mf-mt-audio-channel-mask-attribute.md"><strong>MF_MT_AUDIO_CHANNEL_MASK</strong></a></td>
<td>Gibt die Zuweisung von Audiokanälen zu Redner Positionen an.</td>
<td>Dies ist optional. Weitere Informationen finden Sie unter <a href="#format-constraints">Format Einschränkungen</a>.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></td>
<td>Anzahl der Kanäle, einschließlich des LFE-Kanals (Low Frequency), falls vorhanden.<br/></td>
<td>Die Interpretation dieses Werts hängt vom Medien Untertyp ab, wie zuvor beschrieben.<br/></td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></td>
<td>Abtastrate in Samplings pro Sekunde.<br/></td>
<td>Die Interpretation dieses Werts hängt vom Medien Untertyp ab, wie zuvor beschrieben.<br/></td>
</tr>
<tr class="odd">
<td><a href="mf-mt-user-data-attribute.md"><strong>MF_MT_USER_DATA</strong></a></td>
<td>Zusätzliche Formatierungsinformationen.</td>
<td>Der Wert dieses Attributs hängt vom Untertyp ab.<br/>
<ul>
<li><strong>MFAudioFormat_AAC</strong>: enthält den Teil der <a href="/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo"><strong>heaacwaveinfo</strong></a> -Struktur, der nach der <strong>WaveFormatEx</strong> -Struktur angezeigt wird (d. h. nach dem <strong>wfx</strong> -Member). Danach folgen die audiospecificconfig ()-Daten gemäß ISO/IEC 14496-3.</li>
<li><strong>MEDIASUBTYPE_RAW_AAC1</strong>: enthält die audiospecificconfig ()-Daten. Diese Daten müssen angezeigt werden. Andernfalls lehnt der Decoder den Medientyp ab.</li>
</ul>
Die Länge der audiospecificconfig ()-Daten beträgt 2 Bytes für AAC-LC oder den-AAC mit impliziter Signalisierung von SBR/PS. Es sind mehr als 2 Bytes für den-AAC mit expliziten Signalisierung von SBR/PS verfügbar.<br/> Der in audiospecificconfig () definierte Wert von <strong>audioobjecttype</strong> muss 2 sein, was AAC-LC angibt. Der Wert von <strong>extensionaudioobjecttype</strong> muss für SBR oder 29 für PS den Wert 5 aufweisen. <br/></td>
</tr>
</tbody>
</table>



 

### <a name="output-types"></a>Ausgabetypen

Der Decoder unterstützt die folgenden Ausgabetypen:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Subtype</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>MFAudioFormat_Float</strong></td>
<td>IEEE-Gleit Komma-Audiodaten.</td>
</tr>
<tr class="even">
<td><strong>MFAudioFormat_PCM</strong></td>
<td>16-Bit-PCM-Audiodaten.</td>
</tr>
<tr class="odd">
<td><strong>MFAudioFormat_AAC</strong></td>
<td>Erfordert Windows 8. <br/> Dieser Ausgabetyp kann verwendet werden, um einen AAC-Datenstrom im LoAs/latm-Format in das ADTs-Format zu konvertieren. <br/> Um einen LoAs/latm-Stream in einen ADTs-Stream zu konvertieren, legen Sie den Eingabetyp auf <strong>MFAudioFormat_AAC</strong> mit Payload Type 3 (LoAs) fest. Legen Sie dann den Ausgabetyp auf <strong>MFAudioFormat_AAC</strong> mit Payload Type 1 (ADTs) fest. Der Decoder formatiert die Konstante neu, ohne dass der Bitstream decodiert wird. <br/>
<blockquote>
[!Note]<br />
Der Decoder registriert <strong>MFAudioFormat_AAC</strong> nicht als Ausgabetyp. Wenn die Anwendung den Eingabetyp jedoch wie beschrieben festlegt, gibt die <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype"><strong>imftransform:: getoutputavailabletype</strong></a> -Methode <strong>MFAudioFormat_AAC</strong> in der Liste der verfügbaren Ausgabetypen zurück.
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

Wenn der Eingabedaten Strom mehr als zwei Kanäle enthält, stellt der AAC-Decoder zwei Optionen für das Ausgabeformat bereit:

-   Dieselbe Kanal Konfiguration wie der Eingabetyp.
-   Stereo-Fold.

## <a name="format-constraints"></a>Format Einschränkungen

Die decodierte audiosamplingrate muss nach dem Anwenden von SBR (sofern vorhanden) einen der folgenden Punkte aufweisen:

-   8 kHz
-   11,025 kHz
-   12 kHz
-   16 kHz
-   22,05 kHz
-   24 kHz
-   32 kHz
-   44,1 kHz
-   48 kHz

Stichproben Raten oberhalb von 48 kHz werden nicht unterstützt.

Der Decoder unterstützt bis zu 6 Audiokanäle. Für jede Sprecher Konfiguration erwartet der Decoder, dass die AAC-syntaktischen Elemente in einer bestimmten Reihenfolge angezeigt werden. In der folgenden Tabelle sind die unterstützten Lautsprecherkonfigurationen aufgeführt. In der dritten Spalte der Tabelle sind die erwarteten syntaktischen Elemente und deren Reihenfolge mit der folgenden Notation aufgeführt:

-   <SCE1>: Das single_channel_element (SCE), das mit dem Front-Center-Redner verknüpft ist.
-   <SCE2>: Der SCE, der dem Back-Center-Redner zugeordnet ist.
-   <CPE1>: Die der Vorderseite zugeordneten channel_pair_element (CPE).
-   <CPE2>: Das CPE, das den zurück-oder Seiten-Referenten zugeordnet ist
-   <LFE>: Der lfe_channel_element (LFE).

Weitere Informationen zu diesen syntaktischen Elementen finden Sie unter ISO/IEC 13818-7.



| Konfiguration       | Kanalmaske                                                                                                                                                              | AAC-syntaktische Elemente                          |
|---------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| Mono                | **SPEAKER_FRONT_CENTER**                                                                                                                                                | <SCE1>                                    |
| Stereo oder Dual Mono | **SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT**                                                                                                                     | <CPE1>                                    |
| 2/1                 | **SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_BACK_CENTER**                                                                                        | <CPE1><SCE1>                        |
| 2/2                 | **SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_BACK_LEFT** \| **SPEAKER_BACK_RIGHT**                                                              | <CPE1><CPE2>                        |
| 3/0                 | **SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER**                                                                                       | <SCE1><CPE1>                        |
| 3/1                 | **SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER** \| **SPEAKER_BACK_CENTER**                                                          | <SCE1><CPE1><SCE2>            |
| 3/2                 | **SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER** \| **SPEAKER_BACK_LEFT** \| **SPEAKER_BACK_RIGHT**                                | <SCE1><CPE1><CPE2>            |
| 3/2 + LFE           | **SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER** \| **SPEAKER_LOW_FREQUENCY** \| **SPEAKER_BACK_LEFT** \| **SPEAKER_BACK_RIGHT** | <SCE1><CPE1><CPE2><LFE> |



 

Für RAW AAC muss jedes Eingabe Beispiel genau einen vollständigen AAC-komprimierten Frame enthalten.

Bei ADTs kann jede Eingabe Stichprobe mehrere Audioframes und partielle Frames enthalten, bei denen es sich um Beispiel Grenzen mit Frames handelt. Jedem ADTs-Header muss ein AAC-Frame folgen.

Der AAC-Decoder unterstützt keines der folgenden Aktionen:

-   Hauptprofil, Sample-Rate skalierbares (SRS) Profil oder das LTP-Profil (Long Term Vorhersage).
-   Das Format für den audiodatenaustausch (ADIF).
-   Latm/Laos-Transportdaten Ströme.
-   Kopplung von Kanal Elementen (CCES). Der Decoder überspringt Audioframes mit CCES.
-   AAC-LC mit der Frame Größe 960-Sample. Nur 1024-Sample Frames werden unterstützt.

## <a name="transform-attributes"></a>Transformations Attribute

Der AAC-Decoder implementiert die [**IMF Transform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) -Methode. Anwendungen können diese Methode verwenden, um die folgenden Attribute zu erhalten oder festzulegen.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Attribut</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/DirectShow/avdecaudiodualmono-property"><strong>CODECAPI_AVDecAudioDualMono</strong></a></td>
<td>Gibt an, ob die zwei-Kanal-Audiodaten als Stereo oder Dual Mono codiert werden. Als schreibgeschützt behandeln.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/DirectShow/avdecaudiodualmonorepromode-property"><strong>CODECAPI_AVDecAudioDualMonoReproMode</strong></a></td>
<td>Gibt an, wie der Decoder Dual Mono-Audiodaten wiederherstellt. Der Standardwert ist <strong>eAVDecAudioDualMonoReproMode_LEFT_MONO</strong>: Output CH1 auf der linken und rechten sprechenden Seite. <br/> Anwendungen können diese Eigenschaft festlegen, um das Standardverhalten zu ändern.<br/></td>
</tr>
<tr class="odd">
<td><a href="mft-support-dynamic-format-change-attribute.md"><strong>MFT_SUPPORT_DYNAMIC_FORMAT_CHANGE</strong></a></td>
<td>Der AAC-Decoder verarbeitet keine dynamischen Formatänderungen und muss geleert oder entladen werden, bevor ein neuer Eingabe Medientyp festgelegt wird. Behandeln Sie dieses Attribut als schreibgeschützt. <br/>
<blockquote>
[!Note]<br />
Der AAC-Decoder meldet fälschlicherweise den Wert <strong>true</strong> für dieses Attribut.
</blockquote>
<br/> <br/> In Windows 7 meldet der Decoder fälschlicherweise den Wert <strong>true</strong> für dieses Attribut. In Windows 8 meldet der Decoder <strong>false</strong>, was der korrekte Wert ist.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="example-media-types"></a>Beispiel Medientypen

Im folgenden finden Sie ein Beispiel für den Eingabe Medientyp, der für einen 6-Kanal-AAC-LC-Stream mit 48-kHz benötigt wird



| Attribut                                                                                      | Wert                                                                                |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [**MF_MT_MAJOR_TYPE**](mf-mt-major-type-attribute.md)                                      | **MFMediaType_Audio**                                                               |
| [**MF_MT_SUBTYPE**](mf-mt-subtype-attribute.md)                                             | **MFAudioFormat_AAC**                                                               |
| [**MF_MT_AUDIO_SAMPLES_PER_SECOND**](mf-mt-audio-samples-per-second-attribute.md)        | 48000                                                                                |
| [**MF_MT_AUDIO_NUM_CHANNELS**](mf-mt-audio-num-channels-attribute.md)                     | 6                                                                                    |
| [MF_MT_AAC_PAYLOAD_TYPE](mf-mt-aac-payload-type.md)                                       | 0                                                                                    |
| [**MF_MT_USER_DATA**](mf-mt-user-data-attribute.md)                                        | {0x00, 0x00, 0x2A, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x11, 0xb0} |
| [MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION](mf-mt-aac-audio-profile-level-indication.md) | 0x2A (optional)                                                                      |



 

Die ersten 12 Bytes [**MF_MT_USER_DATA**](mf-mt-user-data-attribute.md) entsprechen den folgenden [**heaacwavin FO**](/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo) -Strukturmembern:

-   **wpayloadtype** = 0 (unformatierte AAC-Datei)
-   **waudioprofilelevelindikation** = 0x2A (AAC-Profil, Ebene 4)
-   **wstructtype** = 0

Die letzten zwei Bytes [**MF_MT_USER_DATA**](mf-mt-user-data-attribute.md) enthalten den Wert von audiospecificconfig (), wie in MPEG-4 definiert.

-   Audiospecificconfig. audioobjecttype = 2 (AAC LC) (5 Bits)
-   Audiospecificconfig. samplingfrequencyindex = 3 (4 Bits)
-   Audiospecificconfig. channelconfiguration = 6 (4 Bits)
-   "Gaspeer" config. framelengthflag = 0 (1 Bit)
-   "Gaspeer" config. dependsoncorecoder = 0 (1 Bit)
-   Gaspeer-Konfigurationsdatei. extensionflag = 0 (1 Bit)

Verwenden Sie für diesen Eingabetyp den folgenden Ausgabe Medientyp, um eine 6-Kanal-, 32-Bit-Gleit Komma-PCM-Audiodatei vom Decoder zu erhalten:



| Attribut                                                                                    | Wert                    |
|----------------------------------------------------------------------------------------------|--------------------------|
| [**MF_MT_MAJOR_TYPE**](mf-mt-major-type-attribute.md)                                    | **MFMediaType_Audio**   |
| [**MF_MT_SUBTYPE**](mf-mt-subtype-attribute.md)                                           | **MFAudioFormat_Float** |
| [**MF_MT_AUDIO_BITS_PER_SAMPLE**](mf-mt-audio-bits-per-sample-attribute.md)            | 32                       |
| [**MF_MT_AUDIO_SAMPLES_PER_SECOND**](mf-mt-audio-samples-per-second-attribute.md)      | 48000                    |
| [**MF_MT_AUDIO_NUM_CHANNELS**](mf-mt-audio-num-channels-attribute.md)                   | 6                        |
| [**MF_MT_AUDIO_AVG_BYTES_PER_SECOND**](mf-mt-audio-avg-bytes-per-second-attribute.md) | 1152000 (optional)       |
| [**MF_MT_AUDIO_BLOCK_ALIGNMENT**](mf-mt-audio-block-alignment-attribute.md)             | 24 (optional)            |
| [**MF_MT_AUDIO_CHANNEL_MASK**](mf-mt-audio-channel-mask-attribute.md)                   | 0x3f (optional)          |



 

Wenn die Ergänzung zum Platt Form Update für Windows Vista installiert ist, ist der AAC-Audiodecoder unter Windows Vista verfügbar, aber nur unter Windows Vista mit dem [Quell Leser](source-reader.md)verfügbar.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                                                                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                                                                                                                                     |
| DLL<br/>                      | <dl> <dt>Msmpeg2adec.dll unter Windows 7; </dt> <dt>MSAudDecMFT.dll unter Windows 8</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Codec-Objekte](codecobjects.md)
</dt> <dt>

[AAC-Medientypen](aac-media-types.md)
</dt> <dt>

[Audiomedientypen](audio-media-types.md)
</dt> <dt>

[**Microsoft MPEG-1/DD/AAC-Audiodecoder**](/windows/desktop/DirectShow/microsoft-mpeg-1-dd-audio-decoder)
</dt> <dt>

[MPEG-4-Unterstützung in Media Foundation](mpeg-4-support-in-media-foundation.md)
</dt> <dt>

[Unterstützte Medienformate in Media Foundation](supported-media-formats-in-media-foundation.md)
</dt> </dl>
