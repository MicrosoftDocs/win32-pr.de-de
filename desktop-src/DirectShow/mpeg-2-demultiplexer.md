---
description: Dieser Filter demultiplexes MPEG-2-Transport-und Programmstreams, die im Pushmodus übermittelt werden.
ms.assetid: 99bfc55d-6519-4e85-98ce-cad27bd71ffb
title: MPEG-2-Demultiplexer
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ea71727dc273bd0dc5d65ac49b28385b4898067
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106344326"
---
# <a name="mpeg-2-demultiplexer"></a>MPEG-2-Demultiplexer

Dieser Filter demultiplexes MPEG-2-Transport-und Programmstreams, die im Pushmodus übermittelt werden. Ab Windows XP unterstützt dieser Filter auch Programmstreams im Pull-Modus (Dateiwiedergabe). Verwenden Sie auf früheren Plattformen den [MPEG-2-Splitter](mpeg-2-splitter.md) Filter für Programmstreams im Pullmodus. Dieser Filter kann in jedem Filter Diagrammtyp verwendet werden, einschließlich eines digitalen Diagramm Diagramms.

> [!Note]  
> Der MPEG-2-Demultiplexer unterstützt keine Frame-exakte Suche.

 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Filter Schnittstellen</td>
<td>Alle Modi:<br/>
<ul>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>Ibasefilter</strong></a></li>
<li><strong>ISpecifyPropertyPages</strong></li>
</ul>
Nur Pushmodus:<br/>
<ul>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags"><strong>Iamfilterfehlflags</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-impeg2demultiplexer"><strong>IMpeg2Demultiplexer</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ireferenceclock"><strong>IReferenceClock</strong></a></li>
</ul></td>
</tr>
<tr class="even">
<td>Eingabe-PIN-Medientypen</td>
<td>Haupttyp: MEDIATYPE_STREAM<br/> Untertyp<br/>
<ul>
<li>KSDATAFORMAT_SUBTYPE_BDA_MPEG2_TRANSPORT</li>
<li>MEDIASUBTYPE_MPEG2_PROGRAM</li>
<li>MEDIASUBTYPE_MPEG2_TRANSPORT</li>
<li>MEDIASUBTYPE_MPEG2_TRANSPORT_STRIDE</li>
</ul>
Weitere Informationen finden Sie unter <a href="mpeg-2-demultiplexer-media-types.md"><strong>MPEG-2 Demultiplexer-Medientypen</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td>PIN-Eingabeschnittstellen</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>iqualitycontrol</strong></a></td>
</tr>
<tr class="even">
<td>Ausgabe-PIN-Medientypen</td>
<td>Elementare Audiodaten Ströme müssen einen Haupttyp von MEDIATYPE_Audio oder MEDIATYPE_Video haben.<br/> Weitere Informationen finden Sie unter <a href="mpeg-2-demultiplexer-media-types.md"><strong>MPEG-2 Demultiplexer-Medientypen</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td>PIN-Schnittstellen</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, nur <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>iqualitycontrol</strong></a>-Pushmodus: <a href="/windows/desktop/api/Strmif/nn-strmif-iampushsource"><strong>iampushsource</strong></a>, <a href="/previous-versions/windows/desktop/api/Bdaiface/nn-bdaiface-impeg2pidmap"><strong>IMPEG2PIDMap</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-impeg2streamidmap"><strong>IMPEG2StreamIdMap</strong></a><br/> Nur Pull-Modus: <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"> <strong>imediaseeking</strong></a><br/></td>
</tr>
<tr class="even">
<td>CLSID Filtern</td>
<td>CLSID_MPEG2Demultiplexer</td>
</tr>
<tr class="odd">
<td>CLSID der Eigenschaften Seite</td>
<td>Nur für Testzwecke verfügbar. Verwenden der <strong>ISpecifyPropertyPages</strong> -Schnittstelle für den Zugriff auf die Eigenschaften Seiten</td>
</tr>
<tr class="even">
<td>Ausführbare Datei</td>
<td>mpg2splt.ax</td>
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

Um elementare Audiodaten Ströme auszugeben, muss die Demux die Datenströme PCR und SCR empfangen. Auf der Eingabe Seite bedeutet dies, dass ein Transportstream die Tabellen Pat und PMT enthalten muss, die die PID für den PCR-Stream definieren. und Programm Datenströme müssen mindestens einen Pack-Header enthalten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>       |
| Ende des Supports (Server)<br/>    | Windows Server 2003 R2<br/>                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> <dt>

[Verwenden von MPEG-2 Demultiplexer](using-the-mpeg-2-demultiplexer.md)
</dt> </dl>

 

 




