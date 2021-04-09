---
description: Der Microsoft Media Foundation AAC-Encoder ist eine Media Foundation Transformation, mit der das von ISO/IEC 13818-7 (MPEG-2-Audioteil 7) definierte LC-Profil (Advanced audiocoding (AAC) Low Komplexitäts Profil codiert wird.
ms.assetid: d88a8c32-c71f-4ddb-af8c-e2fb54c2322c
title: AAC-Encoder
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec9730ffc17d7ac3d5e16d86ef5aa20a46b329cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862756"
---
# <a name="aac-encoder"></a>AAC-Encoder

Der Microsoft Media Foundation AAC-Encoder ist eine [Media Foundation Transformation](media-foundation-transforms.md) , mit der das von ISO/IEC 13818-7 (MPEG-2-Audioteil 7) definierte LC-Profil (Advanced audiocoding (AAC) Low Komplexitäts Profil codiert wird.

Der AAC-Encoder unterstützt keine Codierung zu anderen AAC-Profilen, wie z. b. Main, SSR oder LTP.

## <a name="class-identifier"></a>Klassen Bezeichner

Der Klassen Bezeichner (CLSID) des AAC-Encoders ist **CLSID \_ aacmscoder**, der in der Header Datei "wmcodecdsp. h" definiert ist.

## <a name="media-types"></a>Medientypen

Der AAC-Encoder unterstützt die folgenden Medientypen. Sie können die Typen zuerst in den Reihenfolge-Eingabetyp oder den Ausgabetyp zuerst festlegen.

### <a name="input-types"></a>Eingabetypen

Legen Sie die folgenden Attribute für den Eingabe Medientyp fest.



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
<td>Untertyp.</td>
<td>Muss <strong>MFAudioFormat_PCM</strong>werden.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-bits-per-sample-attribute.md"><strong>MF_MT_AUDIO_BITS_PER_SAMPLE</strong></a></td>
<td>Bits pro Stichprobe.</td>
<td>Muss 16 sein.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></td>
<td>Stichproben pro Sekunde.</td>
<td>Die folgenden Werte werden unterstützt:
<ul>
<li>44100 (44,1 kHz)</li>
<li>48000 (48 kHz)</li>
</ul></td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></td>
<td>Anzahl der Kanäle.</td>
<td>Muss 1 (Mono) oder 2 (Stereo) oder 6 (5,1) sein.
<blockquote>
[!Note]<br />
Unterstützung für 6 Audiokanäle wurde mit Windows 10 eingeführt und ist für frühere Versionen von Windows nicht verfügbar.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

Nachdem der Eingabetyp festgelegt wurde, leitet der Encoder die folgenden Werte ab und fügt Sie dem Medientyp hinzu:

-   [**MF \_ \_ -MT-audiodurchschn. \_ \_ Byte \_ pro \_ Sekunde**](mf-mt-audio-avg-bytes-per-second-attribute.md)
-   [**MF \_ \_ -MT- \_ Audioblock \_ Ausrichtung**](mf-mt-audio-block-alignment-attribute.md)
-   [**MF-mittlere mittlere \_ \_ \_ Bitrate**](mf-mt-avg-bitrate-attribute.md)

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
<td>Muss <strong>MFAudioFormat_AAC</strong>werden.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-bits-per-sample-attribute.md"><strong>MF_MT_AUDIO_BITS_PER_SAMPLE</strong></a></td>
<td>Bits pro Stichprobe.</td>
<td>Muss 16 sein.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></td>
<td>Stichproben pro Sekunde.</td>
<td>Muss mit dem Eingabetyp identisch sein.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></td>
<td>Anzahl der Kanäle.</td>
<td>Muss mit dem Eingabetyp identisch sein.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-avg-bytes-per-second-attribute.md"><strong>MF_MT_AUDIO_AVG_BYTES_PER_SECOND</strong></a></td>
<td>Die Bitrate des codierten AAC-Streams in Bytes pro Sekunde.</td>
<td>Die folgenden Werte werden unterstützt:
<ul>
<li>12000</li>
<li>16000</li>
<li>20000</li>
<li>24.000</li>
</ul>
Der Standardwert für Mono und Stereo ist 12000 (96 Kbit/s).<br/></td>
</tr>
<tr class="odd">
<td><a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a></td>
<td>Der AAC-Nutz Lasttyp.</td>
<td>Dies ist optional. Wenn festgelegt, muss der Wert 0 (null) sein, was bedeutet, dass der Stream nur raw_data_block Elemente enthält.<br/> Dies ist optional. Wenn das-Attribut nicht festgelegt ist, ist der Standardwert 0 (null) und gibt an, dass der Stream nur raw_data_block Elemente (RAW AAC) enthält. <br/> Wenn dieses Attribut in Windows 7 festgelegt ist, muss der Wert 0 (null) lauten.<br/> Ab Windows 8 kann der Wert 0 (RAW AAC) oder 1 (ADTs AAC) lauten. <br/></td>
</tr>
<tr class="even">
<td><a href="mf-mt-aac-audio-profile-level-indication.md">MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION</a></td>
<td>Das AAC-Audioprofil und die Ebene.</td>
<td>Dies ist optional. Die folgenden Werte werden unterstützt:
<ul>
<li>0x29 (Standard)</li>
<li>0x2A</li>
<li>0x2B</li>
<li>0x2c</li>
<li>0x2E</li>
<li>0x2F</li>
<li>0x30</li>
<li>0x31</li>
<li>0x32</li>
<li>0x33</li>
</ul></td>
</tr>
</tbody>
</table>

In der folgenden Tabelle sind die Werte aufgelistet, die für das MF_MT_AAC_PROFILE_LEVEL_INDICATION-Attribut verwendet werden können.

| MF_MT_AAC_PROFILE_LEVEL_INDICATION Wert | Profil                           |
|------------------------------------------|-----------------------------------|
| 0x29                                     | AAC-Profil L2                    | 
| 0x2A                                     | AAC-Profil L4                    | 
| 0x2B                                     | AAC-Profil L5                    | 
| 0x2c                                     | Hoch Effizienz v1-AAC-Profil L2 | 
| 0x2E                                     | Hoch Effizienz v1-AAC-Profil L4 | 
| 0x2F                                     | Hoch Effizienz v1-AAC-Profil L5 | 
| 0x30                                     | Hoch Effizienz v2-AAC-Profil L2 | 
| 0x31                                     | Hoch Effizienz v2-AAC-Profil L3 | 
| 0x32                                     | Hoch Effizienz v2 AAC-Profil L4 | 
| 0x33                                     | Hoch Effizienz v2-AAC-Profil L5 | 

 

Nachdem der Ausgabetyp festgelegt wurde, aktualisiert der AAC-Encoder den Typ durch Hinzufügen des [**\_ \_ Benutzer \_ Daten Attributs MF MT**](mf-mt-user-data-attribute.md) . Dieses Attribut enthält den Teil der [**heaacwaveinfo**](/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo) -Struktur, der nach der [**WaveFormatEx**](/previous-versions/dd757713(v=vs.85)) -Struktur angezeigt wird (d. h. nach dem **wfx** -Member). Danach folgen die audiospecificconfig ()-Daten gemäß ISO/IEC 14496-3.

Jedes Ausgabe Beispiel enthält einen komprimierten AAC-Frame ohne Header. Dieses Format entspricht dem RAW \_ Data \_ Block ()-Element, das von MPEG-2 definiert wird. Das [MF MT-Attribut des \_ AAC- \_ \_ Nutz Last \_ Typs](mf-mt-aac-payload-type.md) muss, sofern im Ausgabetyp vorhanden, auf NULL festgelegt werden, um diesen Nutz Lasttyp anzugeben.

Jedes Ausgabe Beispiel enthält einen komprimierten AAC-Frame, der 1024 PCM-Stichproben entspricht. Bei einer Samplingrate von 48 kHz beträgt die Dauer eines komprimierten Frames z. b. 21,33 ms.

Wenn der [MF-AAC-AAC- \_ \_ \_ Nutz \_ Lasttyp](mf-mt-aac-payload-type.md) 0 (null) ist (Standardwert), enthält jedes Ausgabe Beispiel ein unformatiertes \_ Daten \_ Block Element () gemäß ISO/IEC 13818-7.

## <a name="example-media-types"></a>Beispiel Medientypen

Im folgenden finden Sie ein Beispiel für die Medientypen, die zum Codieren zwischen 44,1-kHz-, 160-KBit/s-Stereo Audiodaten und RAW AAC

Eingabe Medientyp:



| Attribut                                                                                    | Wert                  |
|----------------------------------------------------------------------------------------------|------------------------|
| [**Haupt-Typ des MF- \_ MT \_ \_**](mf-mt-major-type-attribute.md)                                    | **MF MediaType \_ -Audiodatei** |
| [**MF- \_ MT- \_ Untertyp**](mf-mt-subtype-attribute.md)                                           | **MF Audioformat \_ PCM** |
| [**MF \_ \_ -MT- \_ audiobits \_ pro \_ Beispiel**](mf-mt-audio-bits-per-sample-attribute.md)            | 16                     |
| [**MF \_ \_ -MT- \_ Audiobeispiele \_ pro \_ Sekunde**](mf-mt-audio-samples-per-second-attribute.md)      | 44100                  |
| [**MF \_ \_ -MT- \_ audionum- \_ Kanäle**](mf-mt-audio-num-channels-attribute.md)                   | 2                      |
| [**MF \_ \_ -MT-audiodurchschn. \_ \_ Byte \_ pro \_ Sekunde**](mf-mt-audio-avg-bytes-per-second-attribute.md) | 176400 (optional)      |
| [**MF \_ \_ -MT- \_ Audioblock \_ Ausrichtung**](mf-mt-audio-block-alignment-attribute.md)             | 4 (optional)           |
| [**\_ \_ alle \_ Beispiele \_ unabhängig von MF**](mf-mt-all-samples-independent-attribute.md)         | 1 (optional)           |
| [**MF-mittlere mittlere \_ \_ \_ Bitrate**](mf-mt-avg-bitrate-attribute.md)                                  | 1411200 (optional)     |
| [**\_Beispiele für \_ die \_ große Größe \_ von MF MT**](mf-mt-fixed-size-samples-attribute.md)                   | 1 (optional)           |



 

Ausgabe Medientyp:



| Attribut                                                                                      | Wert                                                                                           |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [**Haupt-Typ des MF- \_ MT \_ \_**](mf-mt-major-type-attribute.md)                                      | **MF MediaType \_ -Audiodatei**                                                                          |
| [**MF- \_ MT- \_ Untertyp**](mf-mt-subtype-attribute.md)                                             | **MF Audioformat- \_ AAC**                                                                          |
| [**MF \_ \_ -MT- \_ audiobits \_ pro \_ Beispiel**](mf-mt-audio-bits-per-sample-attribute.md)              | 16                                                                                              |
| [**MF \_ \_ -MT- \_ Audiobeispiele \_ pro \_ Sekunde**](mf-mt-audio-samples-per-second-attribute.md)        | 44100                                                                                           |
| [**MF \_ \_ -MT- \_ audionum- \_ Kanäle**](mf-mt-audio-num-channels-attribute.md)                     | 2                                                                                               |
| [**MF \_ \_ -MT-audiodurchschn. \_ \_ Byte \_ pro \_ Sekunde**](mf-mt-audio-avg-bytes-per-second-attribute.md)   | 20000                                                                                           |
| [MF- \_ MT- \_ AAC- \_ Nutzlast \_](mf-mt-aac-payload-type.md)                                       | 0 (optional)                                                                                    |
| [Anzeige der MF \_ \_ \_ -AAC- \_ \_ audioprofilebene \_](mf-mt-aac-audio-profile-level-indication.md) | 0x29 (optional)                                                                                 |
| [**MF \_ \_ -MT- \_ Audioblock \_ Ausrichtung**](mf-mt-audio-block-alignment-attribute.md)               | 1 (optional)                                                                                    |
| [**\_ \_ alle \_ Beispiele \_ unabhängig von MF**](mf-mt-all-samples-independent-attribute.md)           | 0 (optional)                                                                                    |
| [**MF-mittlere mittlere \_ \_ \_ Bitrate**](mf-mt-avg-bitrate-attribute.md)                                    | 160000 (optional)                                                                               |
| [**\_ \_ Benutzer \_ Daten für MF-MT**](mf-mt-user-data-attribute.md)                                        | {0x00, 0x00, 0x29, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x12, 0x10} optionale |



 

## <a name="remarks"></a>Bemerkungen

In der aktuellen Implementierung muss jede Eingabe Stichprobe über eine gültige Zeit und Dauer verfügen. Um die Stichproben Zeit festzulegen, wenden Sie [**imfsample:: setsampletime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampletime)an. Um die Stichproben Dauer festzulegen, müssen Sie [**imfsample:: setsampleduration**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampleduration)aufrufen.

Wenn die Stichproben Zeit nicht festgelegt ist, gibt die [**IMF Transform::P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) -Methode von " **MF \_ E \_ No \_ Sample \_ timestamp**" zurück. Wenn die Stichproben Dauer nicht festgelegt ist, gibt die **ProcessInput** -Methode die " **MF \_ E \_ No \_ Sample \_ Duration**" zurück.

Die Stichproben Dauer kann wie folgt berechnet werden:


```C++
LONGLONG hnsSampleDuration = 
    ( nAudioSamplesPerChannel * (LONGLONG)10000000 )/nSamplesPerSec;
```



Dabei ist *naudiosamplesperchannel* die Anzahl von PCM-Audiobeispielen pro Kanal im Eingabepuffer, und *nsamplespersec* ist die Samplingrate in Stichproben pro Sekunde.

> [!Note]  
> Aufgrund eines Fehlers in der aktuellen Implementierung, wenn die Stichproben Dauer auf NULL festgelegt ist, wird der [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) -Befehl erfolgreich ausgeführt, aber ein nachfolgende Rückruf von [**imftransform::P rocess Output**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) löst eine Ausnahme aufgrund einer Division durch NULL aus. Um diesen Fehler zu vermeiden, legen Sie für jedes Eingabe Beispiel eine gültige Dauer ungleich NULL fest.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Mfaacenc.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Codec-Objekte](codecobjects.md)
</dt> <dt>

[**AAC-Decoder**](aac-decoder.md)
</dt> <dt>

[AAC-Medientypen](aac-media-types.md)
</dt> <dt>

[Audiomedientypen](audio-media-types.md)
</dt> <dt>

[MPEG-4-Unterstützung in Media Foundation](mpeg-4-support-in-media-foundation.md)
</dt> <dt>

[Unterstützte Medienformate in Media Foundation](supported-media-formats-in-media-foundation.md)
</dt> </dl>

 

