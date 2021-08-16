---
description: Diese Eigenschaft ist mit System.Search.UrlToIndex identisch, mit der Ausnahme, dass sie den Zeitpunkt der letzten Änderung der URL enthält.
ms.assetid: 53ca765b-0795-49ab-9946-c3ef101ababd
title: System.Search.UrlToIndexWithModificationTime
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7869005084379db1bdf288c6237a420666634c349eee47ca7942af2bb271a39d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118464770"
---
# <a name="systemsearchurltoindexwithmodificationtime"></a>System.Search.UrlToIndexWithModificationTime

Diese Eigenschaft ist mit [**System.Search.UrlToIndex**](props-system-search-urltoindex.md) identisch, mit der Ausnahme, dass sie den Zeitpunkt der letzten Änderung der URL enthält. Dies ist eine Optimierung für den Indexer, sodass er nicht in den Protokollhandler zurückrufen muss, um nach diesen Informationen zu fragen, um zu bestimmen, ob der Inhalt erneut indiziert werden muss.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10, Version 1703, Windows 10, Version 1607, Windows 10, Version 1511, Windows 10, Version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista

```
propertyDescription
   name = System.Search.UrlToIndexWithModificationTime
   shellPKey = PKEY_Search_UrlToIndexWithModificationTime
   formatID = 0B63E343-9CCC-11D0-BCDB-00805FCCCE04
   propID = 12
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Multivalue Any
```

## <a name="remarks"></a>Hinweise

Diese [System.Search.UrlToIndexWithModificationTime-Eigenschaft]() entspricht der [System.Search.UrlToIndex-Eigenschaft,](/previous-versions/windows/desktop/legacy/bb760177(v=vs.85)) mit der Ausnahme, dass Sie auch den Zeitpunkt der letzten Änderung des Dokuments übergeben. Wenn der Zeitpunkt der letzten Änderung stimmt, geht der Indexer davon aus, dass das Dokument bereits indiziert ist, und löst die Benachrichtigung aus. Diese Eigenschaft ist ein Vektor mit zwei Elementen: einem **VT \_ LPWSTR-Wert,** der die URL enthält, und einem **VT \_ FILETIME-Wert,** der den Zeitpunkt der letzten Änderung enthält.

[System.Search.UrlToIndexWithModificationTime]() wurde in früheren Versionen des Windows ALS PID \_ GTHR \_ DIRLINK \_ WITH TIME \_ bezeichnet.

PKEY-Werte werden in Propkey.h definiert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System.Search.UrlToIndex](/previous-versions/windows/desktop/legacy/bb760177(v=vs.85))
</dt> <dt>

[propertyDescription](./propdesc-schema-propertydescription.md)
</dt> <dt>

[searchInfo](./propdesc-schema-searchinfo.md)
</dt> <dt>

[labelInfo](./propdesc-schema-labelinfo.md)
</dt> <dt>

[Typeinfo](./propdesc-schema-typeinfo.md)
</dt> <dt>

[displayInfo](./propdesc-schema-displayinfo.md)
</dt> <dt>

[Stringformat](./propdesc-schema-stringformat.md)
</dt> <dt>

[booleanFormat](./propdesc-schema-booleanformat.md)
</dt> <dt>

[Numberformat](./propdesc-schema-numberformat.md)
</dt> <dt>

[dateTimeFormat](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[enumeratedList](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[drawControl](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[editControl](./propdesc-schema-editcontrol.md)
</dt> <dt>

[Filtercontrol](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[queryControl](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
