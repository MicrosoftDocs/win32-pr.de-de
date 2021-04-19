---
description: Filter für Wave-Parser
ms.assetid: 53a9538d-7a79-40bb-9468-d710eb238925
title: Filter für Wave-Parser
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bb30465a25ab3a6eef190b5fbecd4a4878c2744
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369889"
---
# <a name="wave-parser-filter"></a>Filter für Wave-Parser

Der Wave-Parser-Filter analysiert Audiodaten im WAV-Format aus WAV-, au-oder AIF-Dateien. Der upstreamfilter muss der asynchrone [Datei Quell](file-source--async--filter.md) Filter, der [URL-Quell](file-source--url--filter.md) Filter oder ein kompatibler asynchroner Quell Filter eines Drittanbieters sein, der WAV-Audiodaten enthält. Der Ausgabestream ist Audiodaten, die Sie direkt mit einem audiorenderingfilter oder einem dazwischen liegenden audiotransformations Filter verbinden können.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Filter Schnittstellen</td>
<td><a href="/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent"><strong>Iammediacontent</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>ibasefilter</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipersistmediapropertybag"><strong>ipersistmediapropertybag</strong></a></td>
</tr>
<tr class="even">
<td>Eingabe-PIN-Medientypen</td>
<td>Haupttyp: MEDIATYPE_StreamThe folgenden Untertypen sind gültig:<br/>
<ul>
<li>MEDIASUBTYPE_AIFF</li>
<li>MEDIASUBTYPE_AU</li>
<li>MEDIASUBTYPE_WAVE</li>
</ul></td>
</tr>
<tr class="odd">
<td>PIN-Eingabeschnittstellen</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>iqualitycontrol</strong></a></td>
</tr>
<tr class="even">
<td>Ausgabe-PIN-Medientypen</td>
<td>Haupttyp: MEDIATYPE_AudioSubtype: MEDIASUBTYPE_PCM oder ein anderer Komprimierungstyp. (Siehe <a href="audio-subtypes.md"><strong>audiountertypen</strong></a>.)<br/> Formattyp: FORMAT_WaveFormatEx<br/></td>
</tr>
<tr class="odd">
<td>PIN-Schnittstellen</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"> <strong>imediaseeking</strong></a></td>
</tr>
<tr class="even">
<td>CLSID Filtern</td>
<td>{D51BD5A1-7548-11cf-A520-0080C77EF58A}</td>
</tr>
<tr class="odd">
<td>CLSID der Eigenschaften Seite</td>
<td>Keine Eigenschaften Seite.</td>
</tr>
<tr class="even">
<td>Ausführbare Datei</td>
<td>quartz.dll</td>
</tr>
<tr class="odd">
<td><a href="merit.md">Verdienst</a></td>
<td>MERIT_UNLIKELY</td>
</tr>
<tr class="even">
<td><a href="filter-categories.md">Filter Kategorie</a></td>
<td>CLSID_LegacyAmFilterCategory</td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Bemerkungen

Dieser Filter unterstützt die folgenden Dateitypen:

-   Wave (. wav)
-   AIFF und AIFF-C (. AIF)
-   Au (. au)

Allerdings gelten für das Audioformat die folgenden Einschränkungen:

-   Das Audioformat muss ein lineares 8-Bit-oder 16-Bit-PCM sein.
-   Bei AIFF-C-Dateien muss die Audiodatei in der Big-Endian-Byte Reihenfolge (Komprimierungstyp "None") dekomprimiert werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> </dl>

 

 




