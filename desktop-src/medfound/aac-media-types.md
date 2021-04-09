---
description: In diesem Thema wird beschrieben, wie das Format eines AAC-Streams (Advanced audiocoding) in Media Foundation angegeben wird.
ms.assetid: 82218bc5-6660-4253-b50c-b6d9f30be3d5
title: AAC-Medientypen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab95423b26a0e2a327b599011e88a05ab2ab58c5
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "103961097"
---
# <a name="aac-media-types"></a>AAC-Medientypen

In diesem Thema wird beschrieben, wie das Format eines AAC-Streams (Advanced audiocoding) in Media Foundation angegeben wird.

Zwei Untertypen werden für das AAC-Audioformat definiert:



| Subtype                     | BESCHREIBUNG          | Header       |
|-----------------------------|----------------------|--------------|
| **MF Audioformat- \_ AAC**      | Unformatierte AAC-oder ADTs-AAC. | mfapi. h      |
| **Mediasubtype \_ RAW \_ AAC1** | RAW-AAC.             | wmcodecdsp. h |



 

<dl> <dt>

<span id="MFAudioFormat_AAC"></span><span id="mfaudioformat_aac"></span><span id="MFAUDIOFORMAT_AAC"></span>MF Audioformat- \_ AAC
</dt> <dd>

Für diesen Untertyp gibt der Medientyp die Samplingrate und die Anzahl der Kanäle vor der Anwendung von SBR (Spectral Band Replication) und den Parametern der parametrischen Stereo (PS) an, falls vorhanden. Der Effekt des SBR-Tools besteht darin, die decodierte Samplingrate in Relation zur Core AAC-LC-Stichprobenrate zu verdoppeln. Der Effekt des PS-Tools besteht darin, Stereo von einem Mono-Channel-Kern-AAC-LC-Stream zu decodieren.

Dieser Untertyp entspricht dem **mediasubtype \_ MPEG \_ heaac**, der in wmcodecdsp. h definiert ist. Siehe [audiountertyp-GUIDs](audio-subtype-guids.md).

</dd> <dt>

<span id="MEDIASUBTYPE_RAW_AAC1"></span><span id="mediasubtype_raw_aac1"></span>Mediasubtype \_ RAW \_ AAC1
</dt> <dd>

Dieser Untertyp wird für AAC verwendet, der in einer AVI-Datei mit dem audioformattag gleich dem Wave- \_ Format \_ RAW \_ AAC1 (0x00FF) enthalten ist.

Für diesen Untertyp gibt der Medientyp die Stichprobenrate und die Anzahl der Kanäle nach Anwendung der SBR-und PS-Tools an (sofern vorhanden).

</dd> </dl>

Die folgenden Medientyp Attribute gelten für AAC-Audiodaten.



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
<td><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></td>
<td>Der Haupttyp. Muss <strong>MFMediaType_Audio</strong>werden.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></td>
<td>Audiountertyp. Weitere Informationen finden Sie in der vorherigen Beschreibung.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-aac-audio-profile-level-indication.md">MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION</a></td>
<td>Audioprofil und-Ebene. <br/> Der Wert dieses Attributs ist das Feld <strong>audioprofilelevelindikation</strong> gemäß ISO/IEC 14496-3.<br/> Wenn unbekannt, legen Sie auf 0 (null) oder auf 0xFE ( &quot; kein Audioprofil angegeben &quot; ) fest.<br/></td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-avg-bytes-per-second-attribute.md"><strong>MF_MT_AUDIO_AVG_BYTES_PER_SECOND</strong></a></td>
<td>Die Bitrate des codierten AAC-Streams in Bytes pro Sekunde.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a></td>
<td>Der Nutzlasttyp.<br/> Gilt nur für <strong>MFAudioFormat_AAC</strong>.<br/> <a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a> ist optional. Wenn dieses Attribut nicht angegeben wird, wird der Standardwert 0 verwendet, der angibt, dass der Stream nur raw_data_block Elemente enthält.<br/></td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-bits-per-sample-attribute.md"><strong>MF_MT_AUDIO_BITS_PER_SAMPLE</strong></a></td>
<td>Bittiefe der decodierten PCM-Audiodaten.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-channel-mask-attribute.md"><strong>MF_MT_AUDIO_CHANNEL_MASK</strong></a></td>
<td>Zuweisung von Audiokanälen zu Redner Positionen.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></td>
<td>Anzahl der Kanäle, einschließlich des LFE-Kanals (Low Frequency), falls vorhanden.<br/> Die Interpretation dieses Werts hängt vom Medien Untertyp ab, wie zuvor beschrieben.<br/></td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></td>
<td>Abtastrate in Samplings pro Sekunde.<br/> Die Interpretation dieses Werts hängt vom Medien Untertyp ab, wie zuvor beschrieben.<br/></td>
</tr>
<tr class="even">
<td><a href="mf-mt-user-data-attribute.md"><strong>MF_MT_USER_DATA</strong></a></td>
<td>Der Wert dieses Attributs ist von dem Untertyp abhängig:<br/>
<ul>
<li><strong>MFAudioFormat_AAC</strong>: enthält den Teil der <a href="/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo"><strong>heaacwaveinfo</strong></a> -Struktur, der nach der <strong>WaveFormatEx</strong> -Struktur angezeigt wird (d. h. nach dem <strong>wfx</strong> -Member). Danach folgen die audiospecificconfig ()-Daten gemäß ISO/IEC 14496-3.</li>
<li><strong>MEDIASUBTYPE_RAW_AAC1</strong>: enthält die audiospecificconfig ()-Daten.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Audiomedientypen](audio-media-types.md)
</dt> <dt>

[Medientyp Attribute](media-type-attributes.md)
</dt> <dt>

[MPEG-4-Unterstützung in Media Foundation](mpeg-4-support-in-media-foundation.md)
</dt> <dt>

[**IMF MediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> </dl>

 

