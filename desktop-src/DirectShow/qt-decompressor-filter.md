---
description: QT-Dekomprimierungsfilter
ms.assetid: d013075f-deab-40ef-8438-4fb09820da3e
title: QT-Dekomprimierungsfilter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ae916b358feda7d8c98352a067c534f78814ecf008843a5719644012bfd8b4f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747770"
---
# <a name="qt-decompressor-filter"></a>QT-Dekomprimierungsfilter

Diese Komponente wurde aus den Betriebssystemen Windows Vista und höher entfernt. Es ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.

Der QT-Dekomprimierungsfilter dekomprimiert das Apple® QuickTime® 2.0-Video. Dieses Format wird in der Regel in älteren QuickTime-Dateien verwendet.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Filterschnittstellen</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></td>
</tr>
<tr class="even">
<td>Eingabepin-Medientypen</td>
<td>MEDIATYPE_Video, FORMAT_VideoInfo<br/> Die folgenden Untertypen sind gültig:<br/>
<ul>
<li>MEDIASUBTYPE_QTRpza</li>
<li>MEDIASUBTYPE_QTSmc</li>
<li>MEDIASUBTYPE_QTRle</li>
<li>MEDIASUBTYPE_QTJpeg</li>
</ul></td>
</tr>
<tr class="odd">
<td>Eingabepinschnittstellen</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>Ausgabepin-Medientypen</td>
<td>MEDIATYPE_Video, MEDIASUBTYPE_NULL, FORMAT_VideoInfo</td>
</tr>
<tr class="odd">
<td>Ausgabe-PIN-Schnittstellen</td>
<td><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>Filtern der CLSID</td>
<td>CLSID_QTDec</td>
</tr>
<tr class="odd">
<td>Eigenschaftenseite CLSID</td>
<td>Keine Eigenschaftenseite.</td>
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
<td><a href="filter-categories.md">Filterkategorie</a></td>
<td>CLSID_LegacyAmFilterCategory</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> </dl>

 

 




