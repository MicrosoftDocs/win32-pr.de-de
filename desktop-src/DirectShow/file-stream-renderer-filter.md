---
description: Filter für Datei Datenstrom-Renderer
ms.assetid: e26462bb-e67f-4522-bec2-88378c4ff442
title: Filter für Datei Datenstrom-Renderer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a64c8d8a0c87dab3aa811c8246be24ded8ee04dc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522315"
---
# <a name="file-stream-renderer-filter"></a>Filter für Datei Datenstrom-Renderer

Der Dateistream-rendererfilter rendert Dateinamen, die vom [MultiFile-](multi-file-parser-filter.md) Parserfilter analysiert werden. Weitere Informationen finden Sie in der Dokumentation für diesen Filter.

Die Verwendung dieses Filters ist veraltet. Wenn Sie mehrere Dateien innerhalb desselben Filter Diagramms **Renderen** möchten, sollte die Anwendung immer mehrmals RenderFile oder **addsourcefilter** aufrufen.



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
<td><ul>
<li>Haupttyp: MEDIATYPE_File</li>
<li>Untertyp: GUID_NULL</li>
<li>Formattyp: MEDIATYPE_File</li>
</ul></td>
</tr>
<tr class="odd">
<td>PIN-Eingabeschnittstellen</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>iqualitycontrol</strong></a></td>
</tr>
<tr class="even">
<td>Ausgabe-PIN-Medientypen</td>
<td>Keine</td>
</tr>
<tr class="odd">
<td>PIN-Schnittstellen</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>iqualitycontrol</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-istreambuilder"><strong>istreambuilder</strong></a></td>
</tr>
<tr class="even">
<td>CLSID Filtern</td>
<td>CLSID_FileRend</td>
</tr>
<tr class="odd">
<td>Ausführbare Datei</td>
<td>Quartz.dll</td>
</tr>
<tr class="even">
<td><a href="merit.md">Verdienst</a></td>
<td>MERIT_UNLIKELY</td>
</tr>
<tr class="odd">
<td><a href="filter-categories.md">Filter Kategorie</a></td>
<td>CLSID_LegacyAmFilterCategory</td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Bemerkungen

Die CLSID des Filters ist nicht in "UUIDs. h" definiert. Verwenden Sie dieses Makro in ihrer eigenen Header Datei:


```C++
// {D51BD5A5-7548-11cf-A520-0080C77EF58A}
DEFINE_GUID(CLSID_FileRend,
0xd51bd5A5, 0x7548, 0x11cf, 0xa5, 0x20, 0x0, 0x80, 0xc7, 0x7e, 0xf5, 0x8a);
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> </dl>

 

 



