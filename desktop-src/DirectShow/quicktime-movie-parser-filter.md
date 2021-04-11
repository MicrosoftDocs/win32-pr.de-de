---
description: QuickTime Movie Parser-Filter
ms.assetid: 9537dd7b-9aeb-4e73-a31d-86053874ef13
title: QuickTime Movie Parser-Filter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a046e143487a1455aeeb125910bbf4452b4f947
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104341949"
---
# <a name="quicktime-movie-parser-filter"></a>QuickTime Movie Parser-Filter

Diese Komponente wurde aus Windows Vista und höheren Betriebssystemen entfernt. Es ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.

Der Filter für den QuickTime-Movie-Parser teilt die Daten von Apple® QuickTime® in Audiodaten und Videostreams. Es unterstützt QuickTime 2,0 und früher. Die Eingabe-PIN stellt eine Verbindung mit einem Quell Filter her, z. b. dem asynchronen [Datei Quell](file-source--async--filter.md) Filter oder dem [URL-Quell](file-source--url--filter.md) Filter. Der Parser verwendet den [AVI Decompressor](avi-decompressor-filter.md) -oder [Qt Decompressor](qt-decompressor-filter.md) -Filter, um die QuickTime-Dateien zu dekomprimieren. Der Filter erstellt eine Ausgabe-PIN für den Videostream und eine Ausgabe-PIN für den Audiodatenstrom.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Filter Schnittstellen</td>
<td><a href="/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent"><strong>Iammediacontent</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"> <strong>ibasefilter</strong></a></td>
</tr>
<tr class="even">
<td>Eingabe-PIN-Medientypen</td>
<td>MEDIATYPE_Stream, MEDIASUBTYPE_QTMovie;</td>
</tr>
<tr class="odd">
<td>PIN-Eingabeschnittstellen</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>iqualitycontrol</strong></a></td>
</tr>
<tr class="even">
<td>Ausgabe-PIN-Medientypen</td>
<td><ul>
<li>MEDIATYPE_Video, MEDIASUBTYPE_NULL FORMAT_VideoInfo</li>
<li>MEDIATYPE_Audio, MEDIASUBTYPE_NULL FORMAT_WaveFormatEx</li>
</ul></td>
</tr>
<tr class="odd">
<td>PIN-Schnittstellen</td>
<td><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>Imediaposition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>imediaseeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>iqualitycontrol</strong></a></td>
</tr>
<tr class="even">
<td>CLSID Filtern</td>
<td>CLSID_QuickTimeParser</td>
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
<td>MERIT_NORMAL</td>
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

 

 



