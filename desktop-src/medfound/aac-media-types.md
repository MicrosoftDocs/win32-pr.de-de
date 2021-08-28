---
description: In diesem Thema wird beschrieben, wie Sie das Format eines AAC-Streams (Advanced Audio Coding) in Media Foundation.
ms.assetid: 82218bc5-6660-4253-b50c-b6d9f30be3d5
title: AAC-Medientypen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae70661478ad0d2267c951c80fc4a63d98c15267
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479886"
---
# <a name="aac-media-types"></a>AAC-Medientypen

In diesem Thema wird beschrieben, wie Sie das Format eines AAC-Streams (Advanced Audio Coding) in Media Foundation.

Für AAC-Audio sind zwei Untertypen definiert:



| Subtype                     | BESCHREIBUNG          | Header       |
|-----------------------------|----------------------|--------------|
| **MFAudioFormat \_ AAC**      | Unformatiert AAC oder ADTS AAC. | mfapi.h      |
| **MEDIASUBTYPE \_ RAW \_ AAC1** | AAC-Rohdaten.             | wmcodecdsp.h |



 

<dl> <dt>

<span id="MFAudioFormat_AAC"></span><span id="mfaudioformat_aac"></span><span id="MFAUDIOFORMAT_AAC"></span>MFAudioFormat \_ AAC
</dt> <dd>

Für diesen Untertyp gibt der Medientyp die Abtastrate und die Anzahl der Kanäle vor der Anwendung von SBR-Tools (Mergereplikation) und parametrischen Stereotools (PS) an, sofern vorhanden. Das SBR-Tool hat den Effekt, dass die decodierte Abtastrate relativ zur AAC-LC-Kernabtastrate verdoppelt wird. Der Effekt des PS-Tools besteht in der Decodierung von Stereo aus einem AAC-LC-Stream mit Monokanalkern.

Dieser Untertyp entspricht **MEDIASUBTYPE \_ MPEG \_ HEAAC,** definiert in wmcodecdsp.h. Weitere Informationen [finden Sie unter Audio Subtype GUIDs](audio-subtype-guids.md).

</dd> <dt>

<span id="MEDIASUBTYPE_RAW_AAC1"></span><span id="mediasubtype_raw_aac1"></span>MEDIASUBTYPE \_ RAW \_ AAC1
</dt> <dd>

Dieser Untertyp wird für AAC in einer AVI-Datei verwendet, deren Audioformattag gleich WAVE \_ FORMAT \_ RAW \_ AAC1 (0x00FF.

Für diesen Untertyp gibt der Medientyp die Abtastrate und die Anzahl von Kanälen an, nachdem die SBR- und PS-Tools angewendet wurden(sofern vorhanden).

</dd> </dl>

Die folgenden Medientypattribute gelten für AAC-Audio.




| attribute | BESCHREIBUNG | 
|-----------|-------------|
| <a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a> | Haupttyp. Muss <strong>MFMediaType_Audio.</strong> | 
| <a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a> | Audiountertyp. Weitere Informationen finden Sie in der vorherigen Beschreibung. | 
| <a href="mf-mt-aac-audio-profile-level-indication.md">MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION</a> | Audioprofil und -ebene. <br /> Der Wert dieses Attributs ist das <strong>Feld audioProfileLevelIndication,</strong> wie in ISO/IEC 14496-3 definiert.<br /> Wenn unbekannt, legen Sie auf 0 (null) oder 0xFE ("kein Audioprofil angegeben") fest.<br /> | 
| <a href="mf-mt-audio-avg-bytes-per-second-attribute.md"><strong>MF_MT_AUDIO_AVG_BYTES_PER_SECOND</strong></a> | Bitrate des codierten AAC-Streams in Bytes pro Sekunde. | 
| <a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a> | Der Nutzlasttyp.<br /> Gilt nur für <strong>MFAudioFormat_AAC</strong>.<br /><a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a> ist optional. Wenn dieses Attribut nicht angegeben wird, wird der Standardwert 0 verwendet, der angibt, dass der Stream nur raw_data_block enthält.<br /> | 
| <a href="mf-mt-audio-bits-per-sample-attribute.md"><strong>MF_MT_AUDIO_BITS_PER_SAMPLE</strong></a> | Bittiefe des decodierten PCM-Audios. | 
| <a href="mf-mt-audio-channel-mask-attribute.md"><strong>MF_MT_AUDIO_CHANNEL_MASK</strong></a> | Zuweisung von Audiokanälen zu Sprecherpositionen. | 
| <a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a> | Anzahl der Kanäle, einschließlich des Kanals mit niedriger Frequenz (Low Frequency, LFE), sofern vorhanden.<br /> Die Interpretation dieses Werts hängt vom Medienuntertyp ab, wie zuvor beschrieben.<br /> | 
| <a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a> | Stichprobenrate in Stichproben pro Sekunde.<br /> Die Interpretation dieses Werts hängt vom Medienuntertyp ab, wie zuvor beschrieben.<br /> | 
| <a href="mf-mt-user-data-attribute.md"><strong>MF_MT_USER_DATA</strong></a> | Der Wert dieses Attributs hängt vom Untertyp ab:<br /><ul><li><strong>MFAudioFormat_AAC</strong>: Enthält den Teil der <a href="/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo"><strong>HEAACWAVEINFO-Struktur,</strong></a> der nach der <strong>WAVEFORMATEX-Struktur</strong> (d. h. nach dem <strong>wfx-Element) angezeigt</strong> wird. Darauf folgen die AudioSpecificConfig()-Daten gemäß ISO/IEC 14496-3.</li><li><strong>MEDIASUBTYPE_RAW_AAC1</strong>: Enthält die AudioSpecificConfig()-Daten.</li></ul> | 




 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Audiomedientypen](audio-media-types.md)
</dt> <dt>

[Medientypattribute](media-type-attributes.md)
</dt> <dt>

[MPEG-4-Unterstützung in Media Foundation](mpeg-4-support-in-media-foundation.md)
</dt> <dt>

[**VERERBungstyp**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> </dl>

 

