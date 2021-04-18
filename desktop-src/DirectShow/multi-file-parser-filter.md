---
description: Multifile-Parserfilter
ms.assetid: 8ef06f49-fda4-49e2-9b07-70453a2e897c
title: Multifile-Parserfilter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44fc83a56bb12c307b85be875a3a2e7e73b744d9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106338873"
---
# <a name="multi-file-parser-filter"></a>Multifile-Parserfilter

Der MultiFile-Parserfilter analysiert ein einfaches Dateiformat, das ermöglicht, mehrere Dateinamen anzugeben, als ob es sich um eine Datei handelt. Diese Dateien weisen das Format auf, das im folgenden Beispiel gezeigt wird:


```C++
;MULTI
https://server/share/video.mpg
https://server/share/captions.smi
```



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
<li>Haupttyp: MEDIATYPE_Stream</li>
<li>Untertyp: CLSID_MultFile</li>
<li>Formattyp: GUID_NULL</li>
</ul></td>
</tr>
<tr class="odd">
<td>PIN-Eingabeschnittstellen</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>iqualitycontrol</strong></a></td>
</tr>
<tr class="even">
<td>Ausgabe-PIN-Medientypen</td>
<td><ul>
<li>Haupttyp: MEDIATYPE_File</li>
<li>Untertyp: GUID_NULL</li>
<li>Formattyp: MEDIATYPE_File</li>
</ul></td>
</tr>
<tr class="odd">
<td>PIN-Schnittstellen</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>iqualitycontrol</strong></a></td>
</tr>
<tr class="even">
<td>CLSID Filtern</td>
<td>CLSID_MultFile</td>
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

Der Filter erstellt eine Ausgabe-PIN für jede Datei, die in der Quelldatei aufgeführt ist. Der Ausgabetyp ist "MediaType \_ file", und der Format Block für den Ausgabetyp ist eine breit Zeichen-Zeichenfolge, die den Dateinamen enthält. Jede Pin stellt eine Verbindung mit einer Instanz des [Datei Datenstrom](file-stream-renderer-filter.md) -rendererfilters her. Der Filter für den Datei Datenstrom-Renderer erstellt eine Ausgabe-PIN, die die [**istreambuilder**](/windows/desktop/api/Strmif/nn-strmif-istreambuilder) -Schnittstelle verfügbar macht. Die Ausgabe-PIN rendert die angegebene Datei. Zwischen dem MultiFile-Parser und dem Datei Datenstrom-Renderer werden keine Mediendaten übertragen.

Die CLSID des Filters ist nicht in "UUIDs. h" definiert. Verwenden Sie dieses Makro in ihrer eigenen Header Datei:


```C++
// {D51BD5A3-7548-11cf-A520-0080C77EF58A}
DEFINE_GUID(CLSID_MultFile,
0xd51bd5a3, 0x7548, 0x11cf, 0xa5, 0x20, 0x0, 0x80, 0xc7, 0x7e, 0xf5, 0x8a);
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> </dl>

 

 



