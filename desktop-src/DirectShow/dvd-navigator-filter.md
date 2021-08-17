---
description: DVD Navigator-Filter
ms.assetid: 3b2c01a2-d52c-4497-8fc9-d1113e8507e8
title: DVD Navigator-Filter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a395001daeac5f90be85bea972d1d4f118198ee4343960cb4eed0d958e1677aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016008"
---
# <a name="dvd-navigator-filter"></a>DVD Navigator-Filter

Der FILTER DVD Navigator ist der Quellfilter für ein DVD-Video Wiedergabefilterdiagramm. Es öffnet alle erforderlichen Dateien in einem DVD-Video-Volume, navigiert durch die linearen DVD-Video.vob-Dateien und analysiert den resultierenden MPEG-2-Programmstream und teilt den Stream in drei Ausgabepins (Video, Audio, Unterbild) auf.

Der FILTER DVD Navigator implementiert auch die [**Schnittstellen IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) und [**IDvdInfo2,**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) die es einer DVD-Wiedergabeanwendung ermöglichen, DVD-Video zu steuern.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Filterschnittstellen</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2"><strong>IDvdControl2</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-idvdinfo2"><strong>IDvdInfo2</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter"><strong>IFileSourceFilter</strong></a>, <strong>ISpecifyPropertyPages</strong></td>
</tr>
<tr class="even">
<td>Eingabepin-Medientypen</td>
<td>MEDIATYPE_Stream, MEDIASUBTYPE_MPEG2_PROGRAM</td>
</tr>
<tr class="odd">
<td>Eingabepinschnittstellen</td>
<td>Nicht zutreffend</td>
</tr>
<tr class="even">
<td>Ausgabepin-Medientypen</td>
<td>Basistypen:<br/>
<ul>
<li>Video: <strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_MPEG2_VIDEO</strong></li>
<li>Audio: <strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_DOLBY_AC3</strong></li>
<li>Unterbild: <strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_DVD_SUBPICTURE</strong></li>
</ul>
Erweiterte Typen:<br/> Video:<br/>
<ul>
<li><strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_MPEG2_VIDEO</strong></li>
<li><strong>MEDIATYPE_Video</strong>, <strong>MEDIASUBTYPE_MPEG2_VIDEO</strong></li>
<li><strong>MEDIATYPE_MPEG2_PES</strong>, <strong>MEDIASUBTYPE_MPEG2_VIDEO</strong></li>
</ul>
Audio:<br/>
<ul>
<li><strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_DOLBY_AC3</strong></li>
<li><strong>MEDIATYPE_Audio</strong>, <strong>MEDIASUBTYPE_DOLBY_AC3</strong></li>
<li><strong>MEDIATYPE_MPEG2_PES</strong>, <strong>MEDIASUBTYPE_DOLBY_AC3</strong></li>
</ul>
Subpicture:<br/>
<ul>
<li><strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_DVD_SUBPICTURE</strong></li>
<li><strong>MEDIATYPE_Video</strong>, <strong>MEDIASUBTYPE_DVD_SUBPICTURE</strong></li>
<li><strong>MEDIATYPE_MPEG2_PES</strong>, <strong>MEDIASUBTYPE_DVD_SUBPICTURE</strong></li>
</ul>
Um die erweiterten Typen zu aktivieren, rufen Sie <a href="/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption"><strong>IDvdControl2::SetOption</strong></a> auf, und legen Sie fest. <br/></td>
</tr>
<tr class="odd">
<td>Ausgabe-PIN-Schnittstellen</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>Filtern der CLSID</td>
<td>CLSID_DVDNavigator</td>
</tr>
<tr class="odd">
<td>Eigenschaftenseite CLSID</td>
<td>Keine Eigenschaftenseite.</td>
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
<td><a href="filter-categories.md">Filterkategorie</a></td>
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

 

 




