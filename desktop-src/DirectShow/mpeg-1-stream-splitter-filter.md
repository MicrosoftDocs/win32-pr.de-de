---
description: MPEG-1-Datenstrom Splitter Filter
ms.assetid: abadf37f-2876-496d-90e7-77c3475a0064
title: MPEG-1-Datenstrom Splitter Filter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deec47e5ad8df16446c588beec2c5d1c2606b9b1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125221"
---
# <a name="mpeg-1-stream-splitter-filter"></a>MPEG-1-Datenstrom Splitter Filter

Dieser Filter teilt einen MPEG-1-Systemdaten Strom in seine komponentenaudiodaten und Videodaten Ströme auf.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Filter Schnittstellen</td>
<td><a href="/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent"><strong>Iammediacontent</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamselect"><strong>iamstreamselect</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>ibasefilter</strong></a></td>
</tr>
<tr class="even">
<td>Eingabe-PIN-Medientypen</td>
<td>Haupttyp: MEDIATYPE_Stream<br/> Untertypen<br/>
<ul>
<li>MEDIASUBTYPE_MPEG1System</li>
<li>MEDIASUBTYPE_MPEG1VideoCD</li>
<li>MEDIASUBTYPE_Audio</li>
<li>MEDIASUBTYPE_Video</li>
</ul>
Siehe <a href="mpeg-1-media-types.md"> <strong>MPEG-1-Medientypen</strong></a><br/></td>
</tr>
<tr class="odd">
<td>PIN-Eingabeschnittstellen</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>iqualitycontrol</strong></a></td>
</tr>
<tr class="even">
<td>Ausgabe-PIN-Medientypen</td>
<td>Haupttyp: MEDIATYPE_Audio oder MEDIATYPE_Video<br/> Untertyp: MEDIASUBTYPE_MPEG1Payload oder MEDIASUBTYPE_MPEG1Packet<br/> Siehe <a href="mpeg-1-media-types.md"> <strong>MPEG-1-Medientypen</strong></a><br/></td>
</tr>
<tr class="odd">
<td>PIN-Schnittstellen</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"> <strong>imediaseeking</strong></a></td>
</tr>
<tr class="even">
<td>CLSID Filtern</td>
<td>CLSID_MPEG1Splitter</td>
</tr>
<tr class="odd">
<td>CLSID der Eigenschaften Seite</td>
<td>Keine Eigenschaften Seite</td>
</tr>
<tr class="even">
<td>Ausführbare Datei</td>
<td>quartz.dll</td>
</tr>
<tr class="odd">
<td><a href="merit.md">Verdienst</a></td>
<td>MERIT_NORMAL</td>
</tr>
<tr class="even">
<td><a href="filter-categories.md">Filter Kategorie</a></td>
<td>CLSID_LegacyAmFilterCategory</td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Bemerkungen

Diese Datei unterstützt nur den Pull-Modus über [**iasynkreader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) . der Pushmodus wird nicht unterstützt.

Da der MPEG-1-Inhalt nicht indiziert ist, kann die Suche sehr ungefähre Werte aufweisen. Es ist in der Regel gut für einen MPEG-1-Systemdaten Strom mit fester Bitrate (in der Regel Hardware, die für Video-CD generiert wird).

Der Filter unterstützt die [**iammediacontent**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent) -Schnittstelle zum Abrufen von ID3-Metadaten.

Nicht alle MPEG-Beispiele haben Zeitstempel. Das Fehlen eines Zeitstempels in einem MPEG-Beispiel ist kein Fehler. Für Filter Entwickler bedeutet dies, dass Sie keinen Fehlercode aus der **Receive** -Methode der Eingabe-PIN zurückgeben sollten, wenn [**imediasample:: getTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-gettime) fehlschlägt. Wenn **Receive** einen anderen Wert als S OK zurückgibt \_ , bewirkt dies, dass der Splitter das Senden von Beispielen beendet.

Wenn die Datei einen Videostream enthält, unterstützt der MPEG-1-Datenstrom Splitter das Suchen nach Frame Nummer. Um Frame basierte Suche zu aktivieren, rufen Sie [**imediaseeking:: settimeformat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) im [Filter Graph-Manager](filter-graph-manager.md) mit dem Wert **Zeit \_ Format \_ Rahmen** auf.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> </dl>

 

 




