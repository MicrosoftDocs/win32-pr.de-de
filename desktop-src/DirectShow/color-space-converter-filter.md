---
description: Farb Raum Konverter-Filter
ms.assetid: a6765184-43ce-47b8-9eb1-e15af7e11c93
title: Farb Raum Konverter-Filter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f054ee03dd65cf619a697d4441b4d09279e7b912
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481182"
---
# <a name="color-space-converter-filter"></a>Farb Raum Konverter-Filter

Dieser Transformations Filter konvertiert von einem RGB-Farbtyp in einen anderen RGB-Typ, z. b. zwischen 24-Bit-und 8-Bit-RGB-Farbe. Da diese Art der Konvertierung in einem Video Dekompressor in der Regel effizienter gehandhabt wird, besteht der Haupt Verwendungsbereich des Farb Raum Konverters darin, dass die Streamquelle aus nicht komprimierten RGB-Frames besteht.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Filter Schnittstellen</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>Ibasefilter</strong></a></td>
</tr>
<tr class="even">
<td>Eingabe-PIN-Medientypen</td>
<td>MEDIATYPE_Video FORMAT_VideoInfo.<br/> Die folgenden Untertypen sind gültig:<br/>
<ul>
<li>MEDIASUBTYPE_RGB8</li>
<li>MEDIASUBTYPE_RGB555</li>
<li>MEDIASUBTYPE_RGB565</li>
<li>MEDIASUBTYPE_RGB24</li>
<li>MEDIASUBTYPE_RGB32</li>
</ul></td>
</tr>
<tr class="odd">
<td>PIN-Eingabeschnittstellen</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>iqualitycontrol</strong></a></td>
</tr>
<tr class="even">
<td>Ausgabe-PIN-Medientypen</td>
<td>MEDIATYPE_Video FORMAT_VideoInfo.<br/> Die folgenden Untertypen sind gültig:<br/>
<ul>
<li>MEDIASUBTYPE_RGB8</li>
<li>MEDIASUBTYPE_RGB555</li>
<li>MEDIASUBTYPE_RGB565</li>
<li>MEDIASUBTYPE_RGB24</li>
<li>MEDIASUBTYPE_RGB32</li>
</ul></td>
</tr>
<tr class="odd">
<td>PIN-Schnittstellen</td>
<td><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>Imediaposition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>imediaseeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>iqualitycontrol</strong></a></td>
</tr>
<tr class="even">
<td>CLSID Filtern</td>
<td>CLSID_Colour</td>
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



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> </dl>

 

 




