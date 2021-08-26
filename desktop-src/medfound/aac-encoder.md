---
description: Der Microsoft Media Foundation AAC-Encoder ist eine Media Foundation Transform, die das Profil Advanced Audio Coding (AAC) Low Complexity (LC) codiert, wie in ISO/IEC 13818-7 (MPEG-2 Audio Part 7) definiert.
ms.assetid: d88a8c32-c71f-4ddb-af8c-e2fb54c2322c
title: AAC-Encoder
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 674ad291e1cf6b56f7ffef640fade683265b62a7
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465637"
---
# <a name="aac-encoder"></a>AAC-Encoder

Der Microsoft Media Foundation AAC-Encoder ist eine [Media Foundation Transform,](media-foundation-transforms.md) die das Profil Advanced Audio Coding (AAC) Low Complexity (LC) codiert, wie in ISO/IEC 13818-7 (MPEG-2 Audio Part 7) definiert.

Der AAC-Encoder unterstützt keine Codierung für andere AAC-Profile wie Main, SSR oder LTP.

## <a name="class-identifier"></a>Klassenbezeichner

Der Klassenbezeichner (CLSID) des AAC-Encoders ist **CLSID \_ AACMFTEncoder,** definiert in der Headerdatei wmcodecdsp.h.

## <a name="media-types"></a>Medientypen

Der AAC-Encoder unterstützt die folgenden Medientypen. Sie können die Typen entweder zuerst in der Reihenfolge eingabetyp oder als Ausgabetyp festlegen.

### <a name="input-types"></a>Eingabetypen

Legen Sie die folgenden Attribute für den Eingabemedientyp fest.




| Attribut | BESCHREIBUNG | Bemerkungen | 
|-----------|-------------|---------|
| <a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a> | Haupttyp. | Muss <strong>MFMediaType_Audio</strong>sein. | 
| <a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a> | Untertyp. | Muss <strong>MFAudioFormat_PCM</strong>sein. | 
| <a href="mf-mt-audio-bits-per-sample-attribute.md"><strong>MF_MT_AUDIO_BITS_PER_SAMPLE</strong></a> | Bits pro Stichprobe. | Muss 16 sein. | 
| <a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a> | Stichproben pro Sekunde. | Die folgenden Werte werden unterstützt:<ul><li>44100 (44,1 KHz)</li><li>48000 (48 KHz)</li></ul> | 
| <a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a> | Anzahl der Kanäle. | Muss 1 (Mono) oder 2 (Stereo) oder 6 (5,1) sein.<blockquote>[!Note]<br />Die Unterstützung für sechs Audiokanäle wurde mit Windows 10 eingeführt und ist für frühere Versionen von Windows nicht verfügbar.</blockquote><br /> | 




 

Nachdem der Eingabetyp festgelegt wurde, leitet der Encoder die folgenden Werte ab und fügt sie dem Medientyp hinzu:

-   [**MF \_ MT \_ AUDIO \_ AVG \_ BYTES \_ PER \_ SECOND**](mf-mt-audio-avg-bytes-per-second-attribute.md)
-   [**MF \_ MT \_ AUDIO \_ BLOCK \_ ALIGNMENT**](mf-mt-audio-block-alignment-attribute.md)
-   [**MF \_ MT \_ AVG \_ BITRATE**](mf-mt-avg-bitrate-attribute.md)

### <a name="output-types"></a>Ausgabetypen

Legen Sie die folgenden Attribute für den Ausgabemedientyp fest.




| Attribut | BESCHREIBUNG | Bemerkungen | 
|-----------|-------------|---------|
| <a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a> | Haupttyp. | Muss <strong>MFMediaType_Audio</strong>sein. | 
| <a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a> | Audiountertyp. | Muss <strong>MFAudioFormat_AAC</strong>sein. | 
| <a href="mf-mt-audio-bits-per-sample-attribute.md"><strong>MF_MT_AUDIO_BITS_PER_SAMPLE</strong></a> | Bits pro Stichprobe. | Muss 16 sein. | 
| <a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a> | Stichproben pro Sekunde. | Muss mit dem Eingabetyp übereinstimmen. | 
| <a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a> | Anzahl der Kanäle. | Muss mit dem Eingabetyp übereinstimmen. | 
| <a href="mf-mt-audio-avg-bytes-per-second-attribute.md"><strong>MF_MT_AUDIO_AVG_BYTES_PER_SECOND</strong></a> | Bitrate des codierten AAC-Streams in Bytes pro Sekunde. | Die folgenden Werte werden unterstützt:<ul><li>12000</li><li>16000</li><li>20000</li><li>24.000</li></ul>Der Standardwert für Mono und Stereo ist 12.000 (96 KBit/s).<br /> | 
| <a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a> | Der AAC-Nutzlasttyp. | Optional. Wenn diese Einstellung festgelegt ist, muss der Wert 0 (null) sein, was angibt, dass der Stream nur raw_data_block Elemente enthält.<br /> Optional. Wenn das Attribut nicht festgelegt ist, ist der Standardwert 0 (null), was angibt, dass der Stream nur raw_data_block Elemente enthält (unformatierte AAC). <br /> Wenn dieses Attribut in Windows 7 festgelegt ist, muss der Wert 0 (null) sein.<br /> Ab Windows 8 kann der Wert 0 (unformatierte AAC) oder 1 (ADTS AAC) sein. <br /> | 
| <a href="mf-mt-aac-audio-profile-level-indication.md">MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION</a> | Das AAC-Audioprofil und die AAC-Audioebene. | Optional. Die folgenden Werte werden unterstützt:<ul><li>0x29 (Standard)</li><li>0x2A</li><li>0x2B</li><li>0x2C</li><li>0x2E</li><li>0x2F</li><li>0x30</li><li>0x31</li><li>0x32</li><li>0x33</li></ul> | 


In der folgenden Tabelle sind die Werte aufgeführt, die für das attribut MF_MT_AAC_PROFILE_LEVEL_INDICATION verwendet werden können.

| MF_MT_AAC_PROFILE_LEVEL_INDICATION Wert | Profil                           |
|------------------------------------------|-----------------------------------|
| 0x29                                     | AAC-Profil L2                    | 
| 0x2A                                     | AAC-Profil L4                    | 
| 0x2B                                     | AAC-Profil L5                    | 
| 0x2C                                     | High Efficiency v1 AAC Profile L2 | 
| 0x2E                                     | High Efficiency v1 AAC Profile L4 | 
| 0x2F                                     | High Efficiency v1 AAC Profile L5 | 
| 0x30                                     | High Efficiency v2 AAC Profile L2 | 
| 0x31                                     | High Efficiency v2 AAC Profile L3 | 
| 0x32                                     | High Efficiency v2 AAC Profile L4 | 
| 0x33                                     | High Efficiency v2 AAC Profile L5 | 

 

Nachdem der Ausgabetyp festgelegt wurde, aktualisiert der AAC-Encoder den Typ, indem er das [**MF \_ MT USER \_ \_ DATA-Attribut**](mf-mt-user-data-attribute.md) hinzufügt. Dieses Attribut enthält den Teil der [**HEAACWAVEINFO-Struktur,**](/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo) der nach der [**WAVEFORMATEX-Struktur**](/previous-versions/dd757713(v=vs.85)) (d. h. nach dem **wfx-Member)** angezeigt wird. Darauf folgen die AudioSpecificConfig()-Daten gemäß ISO/IEC 14496-3.

Jedes Ausgabebeispiel enthält einen komprimierten AAC-Frame ohne Header. Dieses Format entspricht dem \_ \_ block()-Rohdatenelement, das von MPEG-2 definiert wird. Wenn das [MF \_ MT \_ AAC PAYLOAD \_ \_ TYPE-Attribut](mf-mt-aac-payload-type.md) im Ausgabetyp vorhanden ist, muss es auf 0 (null) festgelegt werden, um diesen Nutzlasttyp anzugeben.

Jedes Ausgabebeispiel enthält einen komprimierten AAC-Frame, der 1024 PCM-Beispielen entspricht. Bei einer Samplingrate von 48 KHz beträgt die Dauer eines komprimierten Frames beispielsweise 21,33 Ms.

Wenn [MF \_ MT \_ AAC PAYLOAD \_ \_ TYPE](mf-mt-aac-payload-type.md) 0 (Standardwert) ist, enthält jedes Ausgabebeispiel ein \_ \_ Block()-Rohdatenelement gemäß ISO/IEC 13818-7.

## <a name="example-media-types"></a>Beispielmedientypen

Hier ist ein Beispiel für die Medientypen, die zum Codieren von Stereoaudiodaten mit 44,1 kHz und 160 KBit/s in unformatierte AAC erforderlich sind.

Eingabemedientyp:



| Attribut                                                                                    | Wert                  |
|----------------------------------------------------------------------------------------------|------------------------|
| [**MF \_ \_ MT-HAUPTTYP \_**](mf-mt-major-type-attribute.md)                                    | **MFMediaType \_ Audio** |
| [**MF \_ \_ MT-UNTERTYP**](mf-mt-subtype-attribute.md)                                           | **MFAudioFormat \_ PCM** |
| [**MF \_ \_ MT-AUDIOBITS \_ \_ PRO \_ BEISPIEL**](mf-mt-audio-bits-per-sample-attribute.md)            | 16                     |
| [**MF \_ \_ MT-AUDIOBEISPIELE \_ \_ PRO \_ SEKUNDE**](mf-mt-audio-samples-per-second-attribute.md)      | 44100                  |
| [**MF \_ MT \_ AUDIO \_ NUM \_ CHANNELS**](mf-mt-audio-num-channels-attribute.md)                   | 2                      |
| [**MF \_ MT \_ AUDIO \_ AVG \_ BYTES \_ PER \_ SECOND**](mf-mt-audio-avg-bytes-per-second-attribute.md) | 176400 (optional)      |
| [**MF \_ MT \_ AUDIO \_ BLOCK \_ ALIGNMENT**](mf-mt-audio-block-alignment-attribute.md)             | 4 (optional)           |
| [**MF \_ \_ MT– ALLE \_ BEISPIELE \_ UNABHÄNGIG**](mf-mt-all-samples-independent-attribute.md)         | 1 (optional)           |
| [**MF \_ MT \_ AVG \_ BITRATE**](mf-mt-avg-bitrate-attribute.md)                                  | 1411200 (optional)     |
| [**\_MF \_ MT-BEISPIELE FESTER \_ GRÖßE \_**](mf-mt-fixed-size-samples-attribute.md)                   | 1 (optional)           |



 

Ausgabemedientyp:



| Attribut                                                                                      | Wert                                                                                           |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [**MF \_ \_ MT-HAUPTTYP \_**](mf-mt-major-type-attribute.md)                                      | **MFMediaType \_ Audio**                                                                          |
| [**MF \_ \_ MT-UNTERTYP**](mf-mt-subtype-attribute.md)                                             | **MFAudioFormat \_ AAC**                                                                          |
| [**MF \_ \_ MT-AUDIOBITS \_ \_ PRO \_ BEISPIEL**](mf-mt-audio-bits-per-sample-attribute.md)              | 16                                                                                              |
| [**MF \_ \_ MT-AUDIOBEISPIELE \_ \_ PRO \_ SEKUNDE**](mf-mt-audio-samples-per-second-attribute.md)        | 44100                                                                                           |
| [**MF \_ MT \_ AUDIO \_ NUM \_ CHANNELS**](mf-mt-audio-num-channels-attribute.md)                     | 2                                                                                               |
| [**MF \_ MT \_ AUDIO \_ AVG \_ BYTES \_ PER \_ SECOND**](mf-mt-audio-avg-bytes-per-second-attribute.md)   | 20000                                                                                           |
| [MF \_ MT \_ AAC \_ PAYLOAD \_ TYPE](mf-mt-aac-payload-type.md)                                       | 0 (optional)                                                                                    |
| [MF \_ MT \_ AAC \_ AUDIO \_ PROFILE \_ LEVEL \_ INDICATION](mf-mt-aac-audio-profile-level-indication.md) | 0x29 (optional)                                                                                 |
| [**MF \_ MT \_ AUDIO \_ BLOCK \_ ALIGNMENT**](mf-mt-audio-block-alignment-attribute.md)               | 1 (optional)                                                                                    |
| [**MF \_ \_ MT– ALLE \_ BEISPIELE \_ UNABHÄNGIG**](mf-mt-all-samples-independent-attribute.md)           | 0 (optional)                                                                                    |
| [**MF \_ MT \_ AVG \_ BITRATE**](mf-mt-avg-bitrate-attribute.md)                                    | 160000 (optional)                                                                               |
| [**MF \_ \_ MT-BENUTZERDATEN \_**](mf-mt-user-data-attribute.md)                                        | {0x00, 0x00, 0x29, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x12, 0x10} (optional) |



 

## <a name="remarks"></a>Hinweise

In der aktuellen Implementierung muss jedes Eingabebeispiel über eine gültige Zeit und Dauer verfügen. Rufen Sie ZUM Festlegen der Beispielzeit [**DEN AUFRUF VONSAMPLE::SetSampleTime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampletime)auf. Rufen Sie ZUM Festlegen der Beispieldauer [**DEN AUFRUF VONSAMPLE::SetSampleDuration auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampleduration)

Wenn die Beispielzeit nicht festgelegt ist, gibt die [**ROCTransform::P rocessInput-Methode**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) des Encoders **MF E NO SAMPLE \_ \_ \_ \_ TIMESTAMP** zurück. Wenn die Beispieldauer nicht festgelegt ist, gibt die **ProcessInput-Methode** **MF E NO SAMPLE \_ \_ \_ \_ DURATION** zurück.

Die Stichprobendauer kann wie folgt berechnet werden:


```C++
LONGLONG hnsSampleDuration = 
    ( nAudioSamplesPerChannel * (LONGLONG)10000000 )/nSamplesPerSec;
```



wobei *nAudioSamplesPerChannel* die Anzahl der PCM-Audiobeispiele pro Kanal im Eingabepuffer und *nSamplesPerSec* die Samplingrate in Stichproben pro Sekunde ist.

> [!Note]  
> Wenn die Beispieldauer aufgrund eines Fehlers in der aktuellen Implementierung auf 0 (null) festgelegt ist, wird der [**ProcessInput-Aufruf**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) erfolgreich ausgeführt, aber ein nachfolgender Aufruf von [**ZEROTransform::P rocessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) löst eine Division durch 0 (null) aus. Um diesen Fehler zu vermeiden, legen Sie eine gültige Dauer ungleich 0 (null) für jedes Eingabebeispiel fest.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Mfaacenc.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

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

 

