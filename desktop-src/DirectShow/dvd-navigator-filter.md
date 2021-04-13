---
description: DVD-Navigator-Filter
ms.assetid: 3b2c01a2-d52c-4497-8fc9-d1113e8507e8
title: DVD-Navigator-Filter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53bb1c6f46e3dd846ffccda32fece2c2f04c8992
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481854"
---
# <a name="dvd-navigator-filter"></a>DVD-Navigator-Filter

Der Filter für den DVD-Navigator ist der Quell Filter für ein DVD-Video Wiedergabe Filter Diagramm. Dadurch werden alle erforderlichen Dateien in einem DVD-Video Volume geöffnet, die linearen DVD-Video. VOB-Dateien werden durchlaufen, und der resultierende MPEG-2-Programm Datenstrom wird analysiert, und der Stream wird in drei (Video-, Audio-, subbild-) Ausgabe Pins aufgeteilt.

Der DVD-navigatorfilter implementiert auch die [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) -und [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) -Schnittstellen, mit denen eine DVD-Wiedergabe Anwendung die DVD-Video Wiedergabe steuern kann.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Filter Schnittstellen</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>Ibasefilter</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2"><strong>IDvdControl2</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-idvdinfo2"><strong>IDvdInfo2</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter"><strong>IFileSourceFilter</strong></a>, <strong>ISpecifyPropertyPages</strong></td>
</tr>
<tr class="even">
<td>Eingabe-PIN-Medientypen</td>
<td>MEDIATYPE_Stream MEDIASUBTYPE_MPEG2_PROGRAM</td>
</tr>
<tr class="odd">
<td>PIN-Eingabeschnittstellen</td>
<td>Nicht zutreffend</td>
</tr>
<tr class="even">
<td>Ausgabe-PIN-Medientypen</td>
<td>Basis Typen:<br/>
<ul>
<li>Video: <strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong> <strong>MEDIASUBTYPE_MPEG2_VIDEO</strong></li>
<li>Audiodatei <strong></strong>: MEDIATYPE_DVD_ENCRYPTED_PACK <strong>MEDIASUBTYPE_DOLBY_AC3</strong></li>
<li>Subbild: <strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong> <strong>MEDIASUBTYPE_DVD_SUBPICTURE</strong></li>
</ul>
Erweiterte Typen:<br/> Video:<br/>
<ul>
<li><strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong> <strong>MEDIASUBTYPE_MPEG2_VIDEO</strong></li>
<li><strong>MEDIATYPE_Video</strong> <strong>MEDIASUBTYPE_MPEG2_VIDEO</strong></li>
<li><strong>MEDIATYPE_MPEG2_PES</strong> <strong>MEDIASUBTYPE_MPEG2_VIDEO</strong></li>
</ul>
Audio:<br/>
<ul>
<li><strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong> <strong>MEDIASUBTYPE_DOLBY_AC3</strong></li>
<li><strong>MEDIATYPE_Audio</strong> <strong>MEDIASUBTYPE_DOLBY_AC3</strong></li>
<li><strong>MEDIATYPE_MPEG2_PES</strong> <strong>MEDIASUBTYPE_DOLBY_AC3</strong></li>
</ul>
Untertitel<br/>
<ul>
<li><strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong> <strong>MEDIASUBTYPE_DVD_SUBPICTURE</strong></li>
<li><strong>MEDIATYPE_Video</strong> <strong>MEDIASUBTYPE_DVD_SUBPICTURE</strong></li>
<li><strong>MEDIATYPE_MPEG2_PES</strong> <strong>MEDIASUBTYPE_DVD_SUBPICTURE</strong></li>
</ul>
Um die erweiterten Typen zu aktivieren, geben Sie <a href="/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption"><strong>IDvdControl2:: SetOption</strong></a> ein, und legen Sie das <br/></td>
</tr>
<tr class="odd">
<td>PIN-Schnittstellen</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>iqualitycontrol</strong></a></td>
</tr>
<tr class="even">
<td>CLSID Filtern</td>
<td>CLSID_DVDNavigator</td>
</tr>
<tr class="odd">
<td>CLSID der Eigenschaften Seite</td>
<td>Keine Eigenschaften Seite.</td>
</tr>
<tr class="even">
<td>Ausführbare Datei</td>
<td>qdvd.dll</td>
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



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> <dt>

[DVD-Anwendungen](dvd-applications.md)
</dt> </dl>

 

 




