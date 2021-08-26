---
description: Filter für den Dateistreamrenderer
ms.assetid: e26462bb-e67f-4522-bec2-88378c4ff442
title: Filter für den Dateistreamrenderer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3da8651d61559a9b22b722f91563426cb067f7a3
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470565"
---
# <a name="file-stream-renderer-filter"></a>Filter für den Dateistreamrenderer

Der Filter für den Dateistreamrenderer rendert Dateinamen, die vom [Multidateiparserfilter](multi-file-parser-filter.md) analysiert werden. Weitere Informationen finden Sie in der Dokumentation für diesen Filter.

Die Verwendung dieses Filters ist veraltet. Um mehrere Dateien innerhalb desselben Filterdiagramms zu rendern, sollte die Anwendung einfach **renderFile** oder **AddSourceFilter** mehrmals aufrufen.




| | | Filtern von Schnittstellen | <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a> | | Eingabepinmedientypen | <ul><li>Haupttyp: MEDIATYPE_File</li><li>Untertyp: GUID_NULL</li><li>Formattyp: MEDIATYPE_File</li></ul> | | Eingabepinschnittstellen | <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | | Ausgabepinmedientypen | Keine | | Ausgabepinschnittstellen | <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-istreambuilder"><strong>IStreamBuilder</strong></a> | | Filtern von CLSID-| CLSID_FileRend | | Ausführbare | Quartz.dll | | <a href="merit.md">|</a> MERIT_UNLIKELY | | <a href="filter-categories.md">| "Filterkategorie"</a> CLSID_LegacyAmFilterCategory | 




 

## <a name="remarks"></a>Hinweise

Die CLSID des Filters ist in Uuids.h nicht definiert. Verwenden Sie dieses Makro in Ihrer eigenen Headerdatei:


```C++
// {D51BD5A5-7548-11cf-A520-0080C77EF58A}
DEFINE_GUID(CLSID_FileRend,
0xd51bd5A5, 0x7548, 0x11cf, 0xa5, 0x20, 0x0, 0x80, 0xc7, 0x7e, 0xf5, 0x8a);
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> </dl>

 

 



