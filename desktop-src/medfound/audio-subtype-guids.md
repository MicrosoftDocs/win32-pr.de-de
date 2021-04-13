---
description: Audiountertyp-GUIDs
ms.assetid: c38a1194-e2d8-42ca-8581-4054171f6f44
title: Audiountertyp-GUIDs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c04192f19f530c288b9aef7b5718b8329ea108bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484131"
---
# <a name="audio-subtype-guids"></a>Audiountertyp-GUIDs

Die folgenden audiountertyp-GUIDs sind definiert. Um den Untertyp anzugeben, legen Sie das Attribut " [**MF \_ MT \_ SubType**](mf-mt-subtype-attribute.md) " für den Medientyp fest. Sofern nicht angegeben, werden diese Konstanten in der Header Datei "mfapi. h" definiert.

Wenn diese Untertypen verwendet werden, legen Sie das [MF \_ MT- \_ \_ Haupttyp](mf-mt-major-type-attribute.md) Attribut auf **mfmediatype \_ -Audiodaten** fest.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>GUID</th>
<th>Beschreibung</th>
<th>Formattag (FourCC)</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>MEDIASUBTYPE_RAW_AAC1</strong></td>
<td>"Advanced audiocoding" (AAC).<br/> Dieser Untertyp wird für AAC verwendet, der in einer AVI-Datei mit einem audioformattag gleich 0x00FF enthalten ist. <br/> Weitere Informationen finden Sie unter <a href="aac-decoder.md"><strong>AAC-Decoder</strong></a>.<br/> Definiert in "wmcodecdsp. h"<br/></td>
<td>WAVE_FORMAT_RAW_AAC1 (0x00FF)</td>
</tr>
<tr class="even">
<td><strong>MFAudioFormat_AAC</strong></td>
<td>"Advanced audiocoding" (AAC).<br/>
<blockquote>
[!Note]<br />
Entspricht MEDIASUBTYPE_MPEG_HEAAC, die in wmcodecdsp. h definiert ist.
</blockquote>
<br/> Der Stream kann unformatierte AAC-Daten oder AAC-Daten in einem Datenstrom (Stream Data Transport Stream, ADTs) enthalten.<br/> Weitere Informationen finden Sie unter<br/>
<ul>
<li><a href="aac-decoder.md"><strong>AAC-Decoder</strong></a></li>
<li><a href="mpeg-4-file-source.md">MPEG-4-Datei Quelle</a></li>
</ul></td>
<td>WAVE_FORMAT_MPEG_HEAAC (0x1610)</td>
</tr>
<tr class="odd">
<td><strong>MFAudioFormat_ADTS</strong></td>
<td>Nicht verwendet.</td>
<td>WAVE_FORMAT_MPEG_ADTS_AAC (0x1600)</td>
</tr>
<tr class="even">
<td><strong>MFAudioFormat_ALAC</strong></td>
<td>Apple-Audiocodec ohne Verlust<br/> Unterstützt in Windows 10 und höher.<br/></td>
<td>WAVE_FORMAT_ALAC (0x6c61)</td>
</tr>
<tr class="odd">
<td><strong>MFAudioFormat_AMR_NB</strong></td>
<td>Adaptative mehrstufige Audiodaten<br/> Wird in Windows 8.1 und höher unterstützt.<br/></td>
<td>WAVE_FORMAT_AMR_NB</td>
</tr>
<tr class="even">
<td><strong>MFAudioFormat_AMR_WB</strong></td>
<td>Adaptative mehrstufige Wideband-Audiodaten<br/> Wird in Windows 8.1 und höher unterstützt.<br/></td>
<td>WAVE_FORMAT_AMR_WB</td>
</tr>
<tr class="odd">
<td><strong>MFAudioFormat_AMR_WP</strong></td>
<td>Wird in Windows 8.1 und höher unterstützt.<br/></td>
<td>WAVE_FORMAT_AMR_WP</td>
</tr>
<tr class="even">
<td><strong>MFAudioFormat_Dolby_AC3</strong></td>
<td>Dolby Digital (AC-3).<br/> Gleicher GUID-Wert wie <strong>MEDIASUBTYPE_DOLBY_AC3</strong>, der in "ksuuids. h" definiert ist.<br/></td>
<td>Keine.</td>
</tr>
<tr class="odd">
<td><strong>MFAudioFormat_Dolby_AC3_SPDIF</strong></td>
<td>Dolby AC-3-Audiodatei über Sony/Philips Digital Interface (S/PDIF).<br/> Dieser GUID-Wert ist identisch mit den folgenden Untertypen:<br/>
<ul>
<li><strong>KSDATAFORMAT_SUBTYPE_IEC61937_DOLBY_DIGITAL</strong>in "ksmedia. h" definiert.</li>
<li><strong>MEDIASUBTYPE_DOLBY_AC3_SPDIF</strong>in "UUIDs. h" definiert.</li>
</ul></td>
<td>WAVE_FORMAT_DOLBY_AC3_SPDIF (0x0092)</td>
</tr>
<tr class="even">
<td><strong>MFAudioFormat_Dolby_DDPlus</strong></td>
<td>Dolby Digital Plus.<br/> Gleicher GUID-Wert wie <strong>MEDIASUBTYPE_DOLBY_DDPLUS</strong>, der in wmcodecdsp. h definiert ist.<br/></td>
<td>Keine</td>
</tr>
<tr class="odd">
<td><strong>MFAudioFormat_DRM</strong></td>
<td>Verschlüsselte Audiodaten, die mit einem sicheren Audiopfad verwendet werden.</td>
<td>WAVE_FORMAT_DRM (0x0009)</td>
</tr>
<tr class="even">
<td><strong>MFAudioFormat_DTS</strong></td>
<td>Digital Theater Systems (DTS)-Audiodatei.</td>
<td>WAVE_FORMAT_DTS (0x0008)</td>
</tr>
<tr class="odd">
<td><strong>MFAudioFormat_FLAC</strong></td>
<td>Kostenloser Audiocodec ohne Verlust<br/> Unterstützt in Windows 10 und höher.<br/></td>
<td>WAVE_FORMAT_FLAC (0xF 1AC)</td>
</tr>
<tr class="even">
<td><strong>MFAudioFormat_Float</strong></td>
<td>Unkomprimierte IEEE-Gleit Komma-Audiodaten.</td>
<td>WAVE_FORMAT_IEEE_FLOAT (0x0003)</td>
</tr>
<tr class="odd">
<td><strong>MFAudioFormat_Float_SpatialObjects</strong></td>
<td>Unkomprimierte IEEE-Gleit Komma-Audiodaten.</td>
<td>Keine</td>
</tr>
<tr class="even">
<td><strong>MFAudioFormat_MP3</strong></td>
<td>MPEG-Audioschicht-3 (MP3).</td>
<td>WAVE_FORMAT_MPEGLAYER3 (0x0055)</td>
</tr>
<tr class="odd">
<td><strong>MFAudioFormat_MPEG</strong></td>
<td>MPEG-1-audionutzlast.</td>
<td>WAVE_FORMAT_MPEG (0x0050)</td>
</tr>
<tr class="even">
<td><strong>MFAudioFormat_MSP1</strong></td>
<td>Windows Media Audio 9 Voice-Codec.</td>
<td>WAVE_FORMAT_WMAVOICE9 (0x000a)</td>
</tr>
<tr class="odd">
<td><strong>MFAudioFormat_Opus</strong></td>
<td>Opus<br/> Unterstützt in Windows 10 und höher.<br/></td>
<td>WAVE_FORMAT_OPUS (0x704f)</td>
</tr>
<tr class="even">
<td><strong>MFAudioFormat_PCM</strong></td>
<td>Nicht komprimierte PCM-Audiodaten.</td>
<td>WAVE_FORMAT_PCM (1)</td>
</tr>
<tr class="odd">
<td><strong>MFAudioFormat_QCELP</strong></td>
<td>QCELP (Qualcomm-Code begeisterte lineare Vorhersage).</td>
<td>Keine</td>
</tr>
<tr class="even">
<td><strong>MFAudioFormat_WMASPDIF</strong></td>
<td>Windows Media Audio 9 Professional-Codec über S/PDIF.</td>
<td>WAVE_FORMAT_WMASPDIF (0x0164)</td>
</tr>
<tr class="odd">
<td><strong>MFAudioFormat_WMAudio_Lossless</strong></td>
<td>Windows Media Audio 9 Verlust lose Codec oder Windows Media Audio 9,1-Codec.</td>
<td>WAVE_FORMAT_WMAUDIO_LOSSLESS (0x0163)</td>
</tr>
<tr class="even">
<td><strong>MFAudioFormat_WMAudioV8</strong></td>
<td>Windows Media Audio 8-Codec, Windows Media Audio 9-Codec oder Windows Media Audio 9,1-Codec.</td>
<td>WAVE_FORMAT_WMAUDIO2 (0x0161)</td>
</tr>
<tr class="odd">
<td><strong>MFAudioFormat_WMAudioV9</strong></td>
<td>Windows Media Audio 9 Professional Codec oder Windows Media Audio 9,1 Professional-Codec.</td>
<td>WAVE_FORMAT_WMAUDIO3 (0x0162)</td>
</tr>
</tbody>
</table>



 

Die in der dritten Spalte der Tabelle aufgeführten Formatierungs Tags werden in der **WaveFormatEx** -Struktur verwendet und in der Header Datei mmreg. h definiert.

Bei Angabe eines audioformattags können Sie eine GUID für einen audiountertyp wie folgt erstellen:

1.  Beginnen Sie mit dem Wert " **MF \_ Audioformat**", der in "mfaph. i" definiert ist.
2.  Ersetzen Sie das erste **DWORD** dieser GUID durch das Formattag.

Sie können das " [**\_ mediaType- \_ GUID**](/windows/desktop/api/mfapi/nf-mfapi-define_mediatype_guid) "-Makro definieren, um eine neue GUID-Konstante zu definieren, die diesem Muster folgt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Audiomedientypen](audio-media-types.md)
</dt> <dt>

[**IMF MediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Medientyp-GUIDs](media-type-guids.md)
</dt> <dt>

[Medientypen](media-types.md)
</dt> </dl>

 

 




