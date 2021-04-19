---
description: MPEG-2-Demultiplexer-Medientypen
ms.assetid: 240d1753-df8c-45fe-b5a7-9faa96fc5b18
title: MPEG-2-Demultiplexer-Medientypen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b21eecff138b987c791ecd97056fb4cf417dd98d
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106355105"
---
# <a name="mpeg-2-demultiplexer-media-types"></a>MPEG-2-Demultiplexer-Medientypen

Der [MPEG-2-Demultiplexer-](mpeg-2-demultiplexer.md) Filter erkennt die folgenden Medientypen.

### <a name="input-types"></a>Eingabetypen

Der Haupttyp ist immer **mediaType \_ Stream**. Der Untertyp kann eine der folgenden sein.



| GUID                                             | Beschreibung                                                                                                                                                                                               |
|--------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **"Ksdataformat"- \_ Untertyp " \_ BDA" \_ \_** | Transportstream von einem Stream-Geräte Filter (Broadcast Driver Architecture). Der MPEG-2-Demultiplexer behandelt diesen Untertyp identisch mit **mediasubtype \_ - \_ Transport**.                                |
| **Mediasubtype \_ - \_ Programm**                 | Programmstream                                                                                                                                                                                            |
| **Mediasubtype \_ MPEG2- \_ Transport**               | Transport Datenstrom (TS) mit 188-Byte-Paketen                                                                                                                                                              |
| **Mediasubtype \_ MPEG2- \_ Transport \_ Stride**       | Transportstream mit "stricherten" Paketen. Dieser Untertyp gibt an, dass die TS-Pakete mit zusätzlichen Bytes aufgefüllt werden können. Weitere Informationen finden Sie unter [**MPEG2- \_ Transport \_ Stride**](mpeg2-transport-stride.md). |



 

Für strichlige Transport Pakete (**mediasubtype \_ MPEG2 \_ Transport \_ Stride**) muss jedes Medien Beispiel eine ganzzahlige Anzahl von Transport Paketen enthalten, wie in " [**MPEG2- \_ Transport \_ Stride**](mpeg2-transport-stride.md)" beschrieben. Für alle anderen Eingabetypen gibt es keine Einschränkungen für die Beispiel Grenzen. einzelne Pakete können Beispiel Grenzen umfassen.

### <a name="output-types"></a>Ausgabetypen

Der MPEG-2-Demultiplexer überprüft keine Ausgabetypen. der downstreamfilter ist für die Verarbeitung der Daten, die er vom Demultiplexer empfängt, verantwortlich. Die folgenden Typen werden jedoch häufig von downstreamfiltern als Ausgabe des demultiplexers akzeptiert.

### <a name="mpeg-2-sections"></a>MPEG-2-Abschnitte



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Haupttyp</td>
<td><strong>MEDIATYPE_MPEG2_SECTIONS</strong></td>
</tr>
<tr class="even">
<td>Subtype</td>
<td>Einer der folgenden Punkte trifft zu:<br/>
<ul>
<li><strong>MEDIASUBTYPE_ATSC_SI</strong>: Informationen zum ATSC-Dienst.</li>
<li><strong>MEDIASUBTYPE_DVB_SI</strong>: Informationen zum DVB-Dienst.</li>
<li><strong>MEDIASUBTYPE_ISDB_SI</strong>: Informationen zum ISDB-Dienst (Integrated Services Digital Broadcasting).</li>
<li><strong>MEDIASUBTYPE_MPEG2DATA</strong>: MPEG-2-Abschnitts Daten.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Formattyp</td>
<td>Keine</td>
</tr>
</tbody>
</table>



 

### <a name="mpeg-2-video"></a>MPEG-2-Video



|                  |                                          |
|------------------|------------------------------------------|
| Haupttyp       | **MediaType- \_ Video**                     |
| Subtype          | **Video zu mediasubtype \_ MPEG2 \_**           |
| Formattyp      | **MPEG2Video formatieren \_**                   |
| Format Struktur | [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) |



 

### <a name="mpeg-2-audio"></a>MPEG-2-Audiodatei



|                  |                                      |
|------------------|--------------------------------------|
| Haupttyp       | **MediaType \_ -Audiodatei**                 |
| Subtype          | **Mediasubtype \_ \_ -Audiodatei**       |
| Formattyp      | **Formatieren von \_ WaveFormatEx**             |
| Format Struktur | [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[MPEG-2-Medientypen](mpeg-2-media-types.md)
</dt> </dl>

 

 
