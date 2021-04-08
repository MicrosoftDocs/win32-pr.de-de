---
description: AVI MUX-Filter
ms.assetid: 31d30c91-fc6a-45ec-a2e0-34e6a1e902a4
title: AVI MUX-Filter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3755a4d5f63e824ae08eb736a5999dcac3d7ab32
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103860476"
---
# <a name="avi-mux-filter"></a>AVI MUX-Filter

Der AVI MUX-Filter akzeptiert mehrere Eingabestreams und interverlässt Sie in das AVI-Format. Der Filter verwendet separate Eingabe Pins für jeden Eingabestream und eine Ausgabe-PIN für den AVI-Stream.

Video Erfassungs-oder Authoring Anwendungen können diesen Filter verwenden, um Dateien im AVI-Format auf dem Datenträger zu speichern. Der Filter ist in der Regel mit dem [Datei Schreiber](file-writer-filter.md) Filter verbunden, kann jedoch eine Verbindung mit jedem Filter herstellen, dessen eingabepin die IStream-und [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) -Schnittstellen unterstützt.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Filter Schnittstellen</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>Ibasefilter</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iconfigavimux"><strong>iconfigavimux</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iconfiginterleaving"><strong>iconfiginterleaving</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>imediaseeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipersistmediapropertybag"><strong>ipersistmediapropertybag</strong></a>, ISpecifyPropertyPages</td>
</tr>
<tr class="even">
<td>Eingabe-PIN-Medientypen</td>
<td>Jeder Haupttyp, der einem FourCC im alten Stil entspricht, oder MEDIATYPE_AUXLine21Data. (Weitere Informationen finden Sie unter <a href="fourccmap.md"><strong>fourccmap-Klasse</strong></a>.)
<ul>
<li>Wenn der Haupttyp MEDIATYPE_Audio ist, muss das Format FORMAT_WaveFormatEx sein.</li>
<li>Wenn der Haupttyp MEDIATYPE_Video ist, muss das Format FORMAT_VideoInfo oder FORMAT_DvInfo sein.</li>
<li>Wenn der Haupttyp MEDIATYPE_Interleaved ist, muss das Format FORMAT_DvInfo sein.</li>
</ul></td>
</tr>
<tr class="odd">
<td>PIN-Eingabeschnittstellen</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol"><strong>Iamstreamcontrol</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, IPropertyBag, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>iqualitycontrol</strong></a></td>
</tr>
<tr class="even">
<td>Ausgabe-PIN-Medientypen</td>
<td>MEDIATYPE_Stream MEDIASUBTYPE_Avi</td>
</tr>
<tr class="odd">
<td>PIN-Schnittstellen</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>iqualitycontrol</strong></a></td>
</tr>
<tr class="even">
<td>CLSID Filtern</td>
<td>CLSID_AviDest</td>
</tr>
<tr class="odd">
<td>CLSID der Eigenschaften Seite</td>
<td>CLSID_AviMuxProptyPage CLSID_AviMuxProptyPage1</td>
</tr>
<tr class="even">
<td>Ausführbare Datei</td>
<td>qcap.dll</td>
</tr>
<tr class="odd">
<td><a href="merit.md">Verdienst</a></td>
<td>MERIT_DO_NOT_USE</td>
</tr>
<tr class="even">
<td><a href="filter-categories.md">Filter Kategorie</a></td>
<td>CLSID_LegacyAmFilterCategory</td>
</tr>
</tbody>
</table>



 

### <a name="remarks"></a>Bemerkungen

Die folgenden Hinweise beschreiben verschiedene Aspekte der Funktionalität des AVI MUX-Filters.

Pins

Wenn der AVI MUX-Filter erstellt wird, verfügt er über eine Eingabe-PIN. Wenn jede Eingabe-PIN verbunden ist, erstellt der Filter eine neue Eingabe-PIN.

Streameigenschaften

Die Eingabe Pins unterstützen die IPropertyBag-Schnittstelle für das Festlegen von Eigenschaften für einzelne Streams. Derzeit ist die folgende Eigenschaft definiert:



| Eigenschaft | BESCHREIBUNG                                                           |
|----------|-----------------------------------------------------------------------|
| name     | Der Name des Datenstroms. Diese Eigenschaft wird als Block geschrieben `'strn'` . |



 

Wenn der Filter ausgeführt oder angehalten wird, gibt die IPropertyBag:: Write-Methode den falschen VFW- \_ \_ Status zurück \_ .

Frame Raten

Wenn der Upstream-Filter keine Framerate im **avgtimeperframe** -Member der [**videoinfoheader**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) -Struktur angibt, verwendet das AVI MUX die Zeitstempel des ersten Video Frames. Das AVI-Dateiformat unterstützt keine Variablen Rahmenraten.

Verworfene Frames

Der AVI MUX-Filter berechnet gelöschte Frames basierend auf den Medien Zeiten jedes Beispiels, falls verfügbar, oder andernfalls den Zeitstempeln des Beispiels. Er schreibt einen Index Eintrag mit der Länge 0 (null) für jeden gelöschten Frame.

Imediaseeking

Der AVI MUX-Filter implementiert die [**imediaseeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) -Schnittstelle wie folgt:

-   Die [**GetCurrentPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) -Methode gibt den aktuellen Fortschritt des Multiplexing zurück. Wenn Sie eine Datei (langsamer als die tatsächliche Zeit) transcodieren, ist dieser Wert präziser als der vom Filter Graph-Manager zurückgegebene Wert. Weitere Informationen finden Sie im Abschnitt "Hinweise" auf der Referenzseite zu GetCurrentPosition.
-   Die [**getduration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) -Methode fragt jeden Upstream-Filter ab und gibt die Dauer des längsten Streams zurück. Wenn bei einem dieser Filter der getduration-Befehl fehlschlägt (oder imediaseeking nicht unterstützt), gibt das AVI MUX einen Fehlercode zurück und füllt den *pduration* -Parameter mit der längsten gefundenen Dauer aus. Der Wert von " *pduration* " in diesem Fall ist jedoch nicht notwendigerweise die Länge des längsten Eingabestreams.
-   Der AVI MUX implementiert nicht die Methoden getstopposition, getpositions, getavailable, getrate oder getpreroll. Außerdem implementiert es keine Set- \* Methoden für die Suche.

Datei Format Erweiterungen für AVI 2,0

DirectShow unterstützt derzeit die folgenden AVI 2,0-Dateiformat Erweiterungen:

-   Erweiterte AVI-Dateigröße (mehr als 1 GB)
-   Hierarchische Indizierung

Weitere Informationen finden Sie unter Version 1,02 der "OpenDML-Dateiformat Erweiterungen", die vom OpenDML AVI M-JPEG-Dateiformat-Unterausschuss veröffentlicht werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> </dl>

 

 



