---
description: Der Dolby-Audioencoder ist eine Media Foundation Transform (MFT), die Mono- oder Stereoaudiodaten in Dolby Digital codiert, auch als Dolby AC-3 bezeichnet.
ms.assetid: CBC31132-046C-4CD7-9DBA-20A9C666FB43
title: Dolby Digital Audio Encoder
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84d14a434481a94021617f04e4cb9e10329ad20a
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122483096"
---
# <a name="dolby-digital-audio-encoder"></a>Dolby Digital Audio Encoder

Der Dolby-Audioencoder ist eine Media Foundation [Transform](media-foundation-transforms.md) (MFT), die Mono- oder Stereoaudiodaten in Dolby Digital codiert, auch als Dolby AC-3 bezeichnet. Der Encoder unterstützt keine Mehrkanaleingabe, z. B. die 5.1-Kanalkonfiguration.

> [!IMPORTANT]
> Bei Versionen von Windows vor Windows 8 ist die Microsoft-Implementierung der Dolby Digital-Technologie gemäß den Bedingungen des Dolby Digital-Lizenzierungsprogramms auf die Verwendung durch Microsoft-Anwendungen beschränkt.

 

Weitere Informationen zu Dolby Digital-Audio finden Sie im ATSC-Dokument *Digital Audio Compression Standard (AC-3, E-AC-3) Revision B*.

## <a name="class-identifier"></a>Klassenbezeichner

Der Klassenbezeichner (CLSID) des Dolby-Audioencoder ist **CLSID \_ CMSAssobyDigitalEncMFT,** definiert in der Headerdatei wmcodecdsp.h.

## <a name="output-types"></a>Ausgabetypen

Der Ausgabetyp muss zuerst vor dem Eingabetyp festgelegt werden. In der folgenden Tabelle sind die erforderlichen und optionalen Attribute für den Ausgabemedientyp aufgeführt.




| Attribut | BESCHREIBUNG | Bemerkungen | 
|-----------|-------------|---------|
| <a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a> | Haupttyp. | Erforderlich. Muss auf <strong>MFMediaType_Audio.</strong> | 
| <a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a> | Audiountertyp. | Erforderlich. Muss <strong>MFAudioFormat_Dolby_AC3.</strong> | 
| <a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a> | Beispiele pro Sekunde. | Erforderlich. Die folgenden Werte werden unterstützt:<ul><li>32000</li><li>44100</li><li>48000</li></ul> | 
| <a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a> | Anzahl von Kanälen. | Erforderlich. Muss entweder 1 (Mono) oder 2 (Stereo) sein. | 
| <a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a> | Gibt die Zuweisung von Audiokanälen zu Sprecherpositionen an. | Optional. Wenn festgelegt, muss der Wert 0x3 Stereokanal (linker und rechter Frontkanal) oder 0x4 Mono (Front-Center-Kanal) festgelegt werden. | 
| <a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a> | Bitrate des codierten AC-3-Streams in Bytes pro Sekunde. | Optional. Gültige Werte finden Sie unter Hinweise. Wenn dieses Attribut nicht festgelegt ist, verwendet der Encoder eine Standardbitrate, wie unter Hinweise beschrieben. | 




 

Wenn die optionalen Attribute nicht festgelegt sind, fügt der Encoder sie dem Medientyp hinzu, nachdem der Typ festgelegt wurde.

## <a name="input-types"></a>Eingabetypen

In der folgenden Tabelle sind die erforderlichen und optionalen Attribute für den Eingabemedientyp aufgeführt.




| Attribut | BESCHREIBUNG | Bemerkungen | 
|-----------|-------------|---------|
| <a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a> | Haupttyp. | Erforderlich. Muss auf <strong>MFMediaType_Audio.</strong> | 
| <a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a> | Audiountertyp. | Erforderlich. Muss <strong>MFAudioFormat_PCM</strong> oder <strong>MFAudioFormat_Float.</strong> | 
| <a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a> | Anzahl der Bits pro Audiobeispiel. | Erforderlich. Der Wert muss 16 sein, wenn der <strong>Untertyp</strong>MFAudioFormat_PCM ist, oder 32, wenn der Untertyp <strong>MFAudioFormat_Float.</strong> | 
| <a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a> | Beispiele pro Sekunde. | Erforderlich. Muss mit dem Ausgabetyp übereinstimmen. | 
| <a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a> | Anzahl von Kanälen. | Erforderlich. Muss mit dem Ausgabetyp übereinstimmen. | 
| <a href="mf-mt-audio-block-alignment-attribute.md">MF_MT_AUDIO_BLOCK_ALIGNMENT</a> | Blockausrichtung in Bytes. | Erforderlich. Berechnen Sie den Wert wie folgt:<ul><li><strong>MFAudioFormat_PCM</strong>: Anzahl der Kanäle × 2.</li><li><strong>MFAudioFormat_Float</strong>: Anzahl der Kanäle × 4.</li></ul> | 
| <a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a> | Bitrate des codierten AC3-Streams in Bytes pro Sekunde. | Erforderlich. Muss der Blockausrichtung × Stichproben pro Sekunde gleich sein. | 
| <a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a> | Gibt die Zuweisung von Audiokanälen zu Sprecherpositionen an. | Optional. Wenn festgelegt, muss der Wert mit dem Ausgabetyp übereinstimmen. | 
| <a href="mf-mt-audio-valid-bits-per-sample-attribute.md">MF_MT_AUDIO_VALID_BITS_PER_SAMPLE</a> | Anzahl der gültigen Bits von Audiodaten in jedem Audiobeispiel. | Optional. Wenn festgelegt, muss der Wert mit dem <a href="mf-mt-audio-bits-per-sample-attribute.md">Wert</a>MF_MT_AUDIO_BITS_PER_SAMPLE. | 




 

Der Encoder unterstützt keine Abtastratenkonvertierung oder Stereo-/Monokonvertierung.

## <a name="remarks"></a>Hinweise

Jeder Dolby AC-3-Audioframe enthält 1536 Audiobeispiele pro Kanal. Jeder Eingabepuffer für den Encoder kann jedoch eine beliebige Anzahl von PCM-Stichproben enthalten. Die Größe jedes Eingabepuffers muss ein Vielfaches der Blockausrichtung sein. Der Encoder speichert Eingabebeispiele zwischen, bis er für 1.536 Audiobeispiele pro Kanal ausreichend ist. An diesem Punkt gibt der Encoder einen AC-3-Frame aus.

Jeder Ausgabepuffer enthält einen unformatten AC-3-Frame. Die Dauer entspricht der Dauer von 1.536 PCM-Stichproben bei der aktuellen Samplingrate (32 msec) bei einer Abtastrate von 48 kHz, 34,83 msec bei 44,1 kHz und 48 msec bei 32 kHz. Die Größe der einzelnen Ausgabepuffer hängt von der Bitrate und der Abtastrate ab.

Um die Codierungsbitrate anzugeben, legen Sie das [MF \_ MT AUDIO \_ \_ AVG BYTES PER \_ \_ \_ SECOND-Attribut](mf-mt-audio-avg-bytes-per-second-attribute.md) im Ausgabetyp fest. Die folgende Tabelle zeigt die Beziehung zwischen der Codierungsbitrate und MF \_ MT \_ AUDIO \_ AVG BYTES PER \_ \_ \_ SECOND.



| Bitrate (KBit/s) | [MF \_ MT \_ AUDIO \_ AVG \_ BYTES \_ PER \_ SECOND](mf-mt-audio-avg-bytes-per-second-attribute.md) | Hinweise                                                 |
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



 

Die Standardcodierungsbitrate ist auf 256 KBit/s für Stereo und 192 KBit/s für Mono festgelegt. Die Standardeinstellungen werden in den Medientypen widergespiegelt, die von [**derENTransform::GetOutputAvailableType-Methode**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) des Encoders zurückgegeben werden.

### <a name="example-media-types"></a>Beispielmedientypen

Hier sehen Sie ein Beispiel für die Medientypen, die zum Codieren von 16-Bit-Ganzzahl-PCM mit Stereoaudio mit 48 kHz mit der Standardbitrate von 256 KBit/s erforderlich sind.

Ausgabemedientyp:

| Attribut                                                                           | Wert                         |
|-------------------------------------------------------------------------------------|-------------------------------|
| [MF \_ \_ MT-HAUPTTYP \_](mf-mt-major-type-attribute.md)                               | **MFMediaType \_ Audio**        |
| [MF \_ \_ MT-UNTERTYP](mf-mt-subtype-attribute.md)                                      | **MFAudioFormat \_ Dolby \_ AC3** |
| [MF \_ \_ MT-AUDIOBEISPIELE \_ \_ PRO \_ SEKUNDE](mf-mt-audio-samples-per-second-attribute.md) | 48000                         |
| [MF \_ MT \_ AUDIO \_ NUM \_ CHANNELS](mf-mt-audio-num-channels-attribute.md)              | 2                             |



 

Eingabemedientyp:

| attribute                                                                                | Wert                  |
|------------------------------------------------------------------------------------------|------------------------|
| [MF \_ \_ MT-HAUPTTYP \_](mf-mt-major-type-attribute.md)                                    | **MFMediaType \_ Audio** |
| [MF \_ \_ MT-UNTERTYP](mf-mt-subtype-attribute.md)                                           | **MFAudioFormat \_ PCM** |
| [MF \_ \_ MT-AUDIOBITS \_ \_ PRO \_ BEISPIEL](mf-mt-audio-bits-per-sample-attribute.md)            | 16                     |
| [MF \_ \_ MT-AUDIOBEISPIELE \_ \_ PRO \_ SEKUNDE](mf-mt-audio-samples-per-second-attribute.md)      | 48000                  |
| [MF \_ MT \_ AUDIO \_ NUM \_ CHANNELS](mf-mt-audio-num-channels-attribute.md)                   | 2                      |
| [MF \_ MT \_ AUDIO \_ BLOCK \_ ALIGNMENT](mf-mt-audio-block-alignment-attribute.md)             | 4                      |
| [MF \_ MT \_ AUDIO \_ AVG \_ BYTES \_ PER \_ SECOND](mf-mt-audio-avg-bytes-per-second-attribute.md) | 192000                 |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 \|Desktop-Apps UWP-Apps\]<br/>                                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                               |
| DLL<br/>                      | <dl> <dt>Msac3enc.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Codec-Objekte](codecobjects.md)
</dt> </dl>

 

 




