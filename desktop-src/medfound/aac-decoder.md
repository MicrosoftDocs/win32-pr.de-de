---
description: 'Der Microsoft Media Foundation AAC-Decoder ist eine Media Foundation-Transformation, die die folgenden AAC-Profile (Advanced Audio Coding) und High Efficiency AAC (HE-AAC) decodiert:'
ms.assetid: 036fb0ee-8165-41a3-b41a-2e9bf035a6a6
title: AAC-Decoder
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7554d6bc4a13fe1e4af4c51e75f1fe8a0bd38286
ms.sourcegitcommit: 3a0a8a8fdce560a81a27789a1c04172ed96147b1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/22/2021
ms.locfileid: "112436588"
---
# <a name="aac-decoder"></a>AAC-Decoder

Der Microsoft Media Foundation AAC-Decoder ist eine [Media Foundation-Transformation,](media-foundation-transforms.md) die die folgenden AAC-Profile (Advanced Audio Coding) und High Efficiency AAC -Profile (HE-AAC) decodiert:

-   MPEG-2 AAC Low Complexity (LC)-Profil (Multichannel).
-   MPEG-4 HE-AAC v1 (Multichannel) mit AAC-LC-Kern.
-   MPEG-4 HE-AAC v2 (Stereo) mit AAC-LC-Kern.

Der AAC-Decoder unterstützt sowohl unformatiert AAC-Streams ohne Header als auch AAC in einem Audiodatentransportstream (ADTS).

Ab Windows 8 unterstützt der AAC-Decoder auch das Decodieren von MPEG-4-Audiotransportstreams mit einer Multiplexebene (LATM) und Synchronisierungsschicht (LOAS). Sie kann auch einen LATM/LOAS-Stream in ADTS konvertieren.

## <a name="class-identifier"></a>Klassenbezeichner

Der Klassenbezeichner (CLSID) des AAC-Encoders ist **CLSID \_ CMSAACDecMFT,** definiert in der Headerdatei wmcodecdsp.h.

## <a name="media-types"></a>Medientypen

Der AAC-Decoder unterstützt die folgenden Medientypen.

### <a name="input-types"></a>Eingabetypen

Der AAC-Decoder unterstützt die folgenden Audiountertypen:



| Subtype                     | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   | Header       |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|
| **MFAudioFormat_AAC**      | Unformatiert AAC oder ADTS AAC.<br/> Für diesen Untertyp gibt der Medientyp die Abtastrate und die Anzahl der Kanäle vor der Anwendung von SBR-Tools (Mergereplikation) und parametrischen Stereotools (PS) an, sofern vorhanden. Das SBR-Tool hat den Effekt, dass die decodierte Abtastrate relativ zur AAC-LC-Kernabtastrate verdoppelt wird. Der Effekt des PS-Tools besteht in der Decodierung von Stereo aus einem AAC-LC-Stream mit Monokanalkern.<br/> Dieser Untertyp entspricht **MEDIASUBTYPE_MPEG_HEAAC**, definiert in wmcodecdsp.h. Weitere Informationen [finden Sie unter Audio Subtype GUIDs](audio-subtype-guids.md). <br/> Die [MPEG-4-Dateiquelle](mpeg-4-file-source.md) und der ADTS-Parser geben diesen Untertyp aus. <br/> | mfapi.h      |
| **MEDIASUBTYPE_RAW_AAC1** | AAC-Rohdaten. <br/> Dieser Untertyp wird für AAC in einer AVI-Datei verwendet, deren Audioformattag gleich WAVE_FORMAT_RAW_AAC1 (0x00FF. <br/> Für diesen Untertyp gibt der Medientyp die Abtastrate und die Anzahl von Kanälen an, nachdem die SBR- und PS-Tools angewendet wurden(sofern vorhanden).<br/>                                                                                                                                                                                                                                                                                                                                                                                      | wmcodecdsp.h |



 

Legen Sie zum Konfigurieren des AAC-Decoders die folgenden Attribute für den Eingabemedientyp fest.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>attribute</th>
<th>BESCHREIBUNG</th>
<th>Bemerkungen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></td>
<td>Haupttyp.</td>
<td>Muss <strong>MFMediaType_Audio.</strong></td>
</tr>
<tr class="even">
<td><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></td>
<td>Audiountertyp.</td>
<td>Weitere Informationen finden Sie in der vorherigen Beschreibung.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-aac-audio-profile-level-indication.md">MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION</a></td>
<td>Audioprofil und -ebene. <br/></td>
<td>Dies ist optional. Gilt nur für <strong>MFAudioFormat_AAC</strong>. <br/> Der Wert dieses Attributs ist das <strong>Feld audioProfileLevelIndication,</strong> wie in ISO/IEC 14496-3 definiert. <br/> Wenn unbekannt, legen Sie auf 0 oder 0xFE fest &quot; (kein Audioprofil &quot; angegeben).<br/></td>
</tr>
<tr class="even">
<td><a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a></td>
<td>Der Nutzlasttyp.<br/></td>
<td>Gilt nur für <strong>MFAudioFormat_AAC</strong>. Der Decoder unterstützt die folgenden Nutzlasttypen: <br/>
<ul>
<li>0: AAC-Rohdaten. Der Stream enthält raw_data_block()-Elemente, wie durch MPEG-2 definiert.</li>
<li>1: ADTS. Der Stream enthält eine adts_sequence(), wie durch MPEG-2 definiert. Pro adts_frame() ist nur raw_data_block() zulässig.</li>
<li>3: Audiotransportstream mit einer Synchronisierungsschicht (SYNCHRONIZATION Layer, LOAS) und einer Multiplexebene (LATM). Von den drei LOAS-Typen wird <strong>nur AudioSyncStream</strong> unterstützt. Die Multiplexebene ist <strong>"AudioMuxElement",</strong>die auf ein Audioprogramm und eine Ebene beschränkt ist.</li>
</ul>
<a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a> ist optional. Wenn dieses Attribut nicht angegeben wird, wird der Standardwert 0 verwendet, der angibt, dass der Stream nur raw_data_block enthält.<br/></td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-bits-per-sample-attribute.md"><strong>MF_MT_AUDIO_BITS_PER_SAMPLE</strong></a></td>
<td>Gewünschte Bittiefe des decodierten PCM-Audios.</td>

</tr>
<tr class="even">
<td><a href="mf-mt-audio-channel-mask-attribute.md"><strong>MF_MT_AUDIO_CHANNEL_MASK</strong></a></td>
<td>Gibt die Zuweisung von Audiokanälen zu Sprecherpositionen an.</td>
<td>Dies ist optional. Weitere Informationen finden Sie unter <a href="#format-constraints">Formateinschränkungen.</a></td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></td>
<td>Anzahl der Kanäle, einschließlich des Kanals mit niedriger Frequenz (Low Frequency, LFE), sofern vorhanden.<br/></td>
<td>Die Interpretation dieses Werts hängt vom Medienuntertyp ab, wie zuvor beschrieben.<br/></td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></td>
<td>Stichprobenrate in Stichproben pro Sekunde.<br/></td>
<td>Die Interpretation dieses Werts hängt vom Medienuntertyp ab, wie zuvor beschrieben.<br/></td>
</tr>
<tr class="odd">
<td><a href="mf-mt-user-data-attribute.md"><strong>MF_MT_USER_DATA</strong></a></td>
<td>Zusätzliche Formatinformationen.</td>
<td>Der Wert dieses Attributs hängt vom Untertyp ab.<br/>
<ul>
<li><strong>MFAudioFormat_AAC</strong>: Enthält den Teil der <a href="/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo"><strong>HEAACWAVEINFO-Struktur,</strong></a> der nach der <strong>WAVEFORMATEX-Struktur</strong> (d. h. nach dem <strong>wfx-Element) angezeigt</strong> wird. Darauf folgen die AudioSpecificConfig()-Daten gemäß ISO/IEC 14496-3.</li>
<li><strong>MEDIASUBTYPE_RAW_AAC1</strong>: Enthält die AudioSpecificConfig()-Daten. Diese Daten müssen angezeigt werden. Andernfalls lehnt der Decoder den Medientyp ab.</li>
</ul>
Die Länge der AudioSpecificConfig()-Daten beträgt 2 Byte für AAC-LC oder HE-AAC mit impliziter Signalisierung von SBR/PS. Es sind mehr als 2 Bytes für HE-AAC mit expliziter Signalisierung von SBR/PS.<br/> Der Wert von <strong>audioObjectType,</strong> wie in AudioSpecificConfig() definiert, muss 2 sein, was AAC-LC angibt. Der Wert von <strong>extensionAudioObjectType</strong> muss 5 für SBR oder 29 für PS sein. <br/></td>
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
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>MFAudioFormat_Float</strong></td>
<td>IEEE-Gleitkommaaudio.</td>
</tr>
<tr class="even">
<td><strong>MFAudioFormat_PCM</strong></td>
<td>16-Bit-PCM-Audio.</td>
</tr>
<tr class="odd">
<td><strong>MFAudioFormat_AAC</strong></td>
<td>Erfordert Windows 8. <br/> Dieser Ausgabetyp kann verwendet werden, um einen AAC-Stream im LOAS/LATM-Format in das ADTS-Format zu konvertieren. <br/> Um einen LOAS/LATM-Stream in einen ADTS-Stream <strong></strong> zu konvertieren, legen Sie den Eingabetyp auf MFAudioFormat_AAC Nutzlasttyp 3 (LOAS) fest. Legen Sie dann den Ausgabetyp auf <strong>MFAudioFormat_AAC</strong> Nutzlasttyp 1 (ADTS) fest. Der Decoder wird den Conainter neu umdekontieren, ohne den Bitstream zu decodieren. <br/>
<blockquote>
[!Note]<br />
Der Decoder registriert <strong>MFAudioFormat_AAC</strong> nicht als Ausgabetyp. Wenn die Anwendung den Eingabetyp jedoch wie beschrieben festlegt, gibt die <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype"><strong>METHODE DERTRANSFORM::GetOutputAvailableType</strong></a> <strong>MFAudioFormat_AAC</strong> in der Liste der verfügbaren Ausgabetypen zurück.
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

Wenn der Eingabestream mehr als zwei Kanäle enthält, bietet der AAC-Decoder zwei Optionen für das Ausgabeformat:

-   Die gleiche Kanalkonfiguration wie der Eingabetyp.
-   Stereo-Fold-Down.

## <a name="format-constraints"></a>Formateinschränkungen

Die Samplingrate für decodierte Audiodaten muss eine der folgenden Sein, nachdem SBR angewendet wurde (sofern vorhanden):

-   8 kHz
-   11,025 kHz
-   12 kHz
-   16 kHz
-   22,05 kHz
-   24 kHz
-   32 kHz
-   44,1 kHz
-   48 kHz

Samplingraten über 48 kHz werden nicht unterstützt.

Der Decoder unterstützt bis zu 6 Audiokanäle. Für jede Sprecherkonfiguration erwartet der Decoder, dass die syntaktischen AAC-Elemente in einer bestimmten Reihenfolge angezeigt werden. In der folgenden Tabelle sind die unterstützten Sprecherkonfigurationen aufgeführt. In der dritten Spalte der Tabelle werden die erwarteten syntaktischen Elemente und ihre Reihenfolge mithilfe der folgenden Notation aufgelistet:

-   <SCE1>: Die dem Front-Center-Lautsprecher zugeordnete single_channel_element (SCE).
-   <SCE2>: Die dem Back-Center-Lautsprecher zugeordnete SCE.
-   <CPE1>: Die channel_pair_element (CPE), die den Vorderlautsprechern zugeordnet ist.
-   <CPE2>: Die CPE, die den hinteren (oder seitlichen) Lautsprechern zugeordnet ist.
-   <LFE>: Die lfe_channel_element (LFE).

Weitere Informationen zu diesen syntaktischen Elementen finden Sie unter ISO/IEC 13818-7.



| Konfiguration       | Kanalmaske                                                                                                                                                              | Syntaktische AAC-Elemente                          |
|---------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| Mono                | **SPEAKER_FRONT_CENTER**                                                                                                                                                | <SCE1>                                    |
| Stereo oder Dual Mono | **SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT**                                                                                                                     | <CPE1>                                    |
| 2/1                 | **SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_BACK_CENTER**                                                                                        | <CPE1><SCE1>                        |
| 2/2                 | **SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_BACK_LEFT** \| **SPEAKER_BACK_RIGHT**                                                              | <CPE1><CPE2>                        |
| 3/0                 | **SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER**                                                                                       | <SCE1><CPE1>                        |
| 3/1                 | **SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER** \| **SPEAKER_BACK_CENTER**                                                          | <SCE1><CPE1><SCE2>            |
| 3/2                 | **SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER** \| **SPEAKER_BACK_LEFT** \| **SPEAKER_BACK_RIGHT**                                | <SCE1><CPE1><CPE2>            |
| 3/2 + LFE           | **SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER** \| **SPEAKER_LOW_FREQUENCY** \| **SPEAKER_BACK_LEFT** \| **SPEAKER_BACK_RIGHT** | <SCE1><CPE1><CPE2><LFE> |



 

Für unformatierte AAC muss jedes Eingabebeispiel genau einen vollständigen komprimierten AAC-Frame enthalten.

Für ADTS kann jedes Eingabebeispiel mehrere Audioframes sowie Teilframes enthalten, d. h., Frames können Sich über Beispielgrenzen erstrecken. Auf jeden ADTS-Header muss ein AAC-Frame folgen.

Der AAC-Decoder unterstützt keine der folgenden Möglichkeiten:

-   Hauptprofil, Sample-Rate SRS-Profil (Scalable) oder LTP-Profil (Long Term Prediction).
-   Audiodatenaustauschformat (ADIF).
-   LATM/CSV-Transportstreams.
-   Kopplungskanalelemente (CCEs). Der Decoder überspringt Audioframes mit CCEs.
-   AAC-LC mit einer Framegröße von 960 Stichproben. Nur 1024-Sample-Frames werden unterstützt.

## <a name="transform-attributes"></a>Transformieren von Attributen

Der AAC-Decoder implementiert die [**DECODERTransform::GetAttributes-Methode.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) Anwendungen können diese Methode verwenden, um die folgenden Attribute abzurufen oder festzulegen.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>attribute</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/DirectShow/avdecaudiodualmono-property"><strong>CODECAPI_AVDecAudioDualMono</strong></a></td>
<td>Gibt an, ob 2-Kanal-Audio als Stereo oder Dual Mono codiert wird. Als schreibgeschützt behandeln.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/DirectShow/avdecaudiodualmonorepromode-property"><strong>CODECAPI_AVDecAudioDualMonoReproMode</strong></a></td>
<td>Gibt an, wie der Decoder duale Mono-Audiodaten reproduziert. Der Standardwert ist <strong>eAVDecAudioDualMonoReproMode_LEFT_MONO:</strong>Ausgabe ch1 links und rechts. <br/> Anwendungen können diese Eigenschaft festlegen, um das Standardverhalten zu ändern.<br/></td>
</tr>
<tr class="odd">
<td><a href="mft-support-dynamic-format-change-attribute.md"><strong>MFT_SUPPORT_DYNAMIC_FORMAT_CHANGE</strong></a></td>
<td>Der AAC-Decoder verarbeitet keine dynamischen Formatänderungen und muss geleert oder entladen werden, bevor ein neuer Eingabemedientyp festgelegt wird. Behandeln Sie dieses Attribut als schreibgeschützt. <br/>
<blockquote>
[!Note]<br />
Der AAC-Decoder meldet fälschlicherweise den Wert <strong>TRUE</strong> für dieses Attribut.
</blockquote>
<br/> <br/> In Windows 7 meldet der Decoder fälschlicherweise den Wert <strong>TRUE</strong> für dieses Attribut. In Windows 8 meldet der Decoder <strong>FALSE</strong>. Dies ist der richtige Wert.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="example-media-types"></a>Beispielmedientypen

Hier sehen Sie ein Beispiel für den Eingabemedientyp, der für einen 6-Kanal-AAC-LC-Stream mit 48 kHz und einer unformatierten AAC-Nutzlast benötigt wird:



| attribute                                                                                      | Wert                                                                                |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [**MF_MT_MAJOR_TYPE**](mf-mt-major-type-attribute.md)                                      | **MFMediaType_Audio**                                                               |
| [**MF_MT_SUBTYPE**](mf-mt-subtype-attribute.md)                                             | **MFAudioFormat_AAC**                                                               |
| [**MF_MT_AUDIO_SAMPLES_PER_SECOND**](mf-mt-audio-samples-per-second-attribute.md)        | 48000                                                                                |
| [**MF_MT_AUDIO_NUM_CHANNELS**](mf-mt-audio-num-channels-attribute.md)                     | 6                                                                                    |
| [MF_MT_AAC_PAYLOAD_TYPE](mf-mt-aac-payload-type.md)                                       | 0                                                                                    |
| [**MF_MT_USER_DATA**](mf-mt-user-data-attribute.md)                                        | {0x00, 0x00, 0x2a, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x11, 0xb0} |
| [MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION](mf-mt-aac-audio-profile-level-indication.md) | 0x2a (optional)                                                                      |



 

Die ersten 12 Bytes von [**MF_MT_USER_DATA**](mf-mt-user-data-attribute.md) entsprechen den folgenden [**HEAACWAVEINFO-Strukturmembern:**](/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo)

-   **wPayloadType** = 0 (unformatierte AAC)
-   **wAudioProfileLevelIndication** = 0x2a (AAC-Profil, Ebene 4)
-   **wStructType** = 0

Die letzten beiden Bytes von [**MF_MT_USER_DATA**](mf-mt-user-data-attribute.md) den Wert von AudioSpecificConfig() enthalten, wie von MPEG-4 definiert.

-   AudioSpecificConfig.audioObjectType = 2 (AAC LC) (5 Bits)
-   AudioSpecificConfig.samplingFrequencyIndex = 3 (4 Bits)
-   AudioSpecificConfig.channelConfiguration = 6 (4 Bits)
-   GASpecificConfig.frameLengthFlag = 0 (1 Bit)
-   GASpecificConfig.dependsOnCoreCoder = 0 (1 Bit)
-   GASpecificConfig.extensionFlag = 0 (1 Bit)

Verwenden Sie bei diesem Eingabetyp den folgenden Ausgabemedientyp, um 6-Kanal-PCM-Audio mit 32-Bit-Gleitkommadaten aus dem Decoder zu erhalten:



| attribute                                                                                    | Wert                    |
|----------------------------------------------------------------------------------------------|--------------------------|
| [**MF_MT_MAJOR_TYPE**](mf-mt-major-type-attribute.md)                                    | **MFMediaType_Audio**   |
| [**MF_MT_SUBTYPE**](mf-mt-subtype-attribute.md)                                           | **MFAudioFormat_Float** |
| [**MF_MT_AUDIO_BITS_PER_SAMPLE**](mf-mt-audio-bits-per-sample-attribute.md)            | 32                       |
| [**MF_MT_AUDIO_SAMPLES_PER_SECOND**](mf-mt-audio-samples-per-second-attribute.md)      | 48000                    |
| [**MF_MT_AUDIO_NUM_CHANNELS**](mf-mt-audio-num-channels-attribute.md)                   | 6                        |
| [**MF_MT_AUDIO_AVG_BYTES_PER_SECOND**](mf-mt-audio-avg-bytes-per-second-attribute.md) | 1152000 (optional)       |
| [**MF_MT_AUDIO_BLOCK_ALIGNMENT**](mf-mt-audio-block-alignment-attribute.md)             | 24 (optional)            |
| [**MF_MT_AUDIO_CHANNEL_MASK**](mf-mt-audio-channel-mask-attribute.md)                   | 0x3f (optional)          |



 

Wenn die Plattformupdateergänzung für Windows Vista installiert ist, ist der AAC-Audiodecoder unter Windows Vista verfügbar, aber unter Windows Vista nur über den [Quellleser zugänglich.](source-reader.md)

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows \[ 7-Desktop-Apps\]<br/>                                                                                                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ R2-Desktop-Apps\]<br/>                                                                                                                                     |
| DLL<br/>                      | <dl> <dt>Msmpeg2adec.dll unter Windows 7; </dt> <dt>MSAudDecMFT.dll auf Windows 8</dt> </dl> |



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
