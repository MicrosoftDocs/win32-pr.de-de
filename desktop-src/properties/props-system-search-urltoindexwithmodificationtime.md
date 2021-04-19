---
description: Diese Eigenschaft ist identisch mit System. search. urlumindex, mit der Ausnahme, dass Sie den Zeitpunkt enthält, an dem die URL zuletzt geändert wurde.
ms.assetid: 53ca765b-0795-49ab-9946-c3ef101ababd
title: System. search. urldeindexwithmodificationtime
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fcc83b9796ae2375f10235a08ba0db313fb1958
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363684"
---
# <a name="systemsearchurltoindexwithmodificationtime"></a>System. search. urldeindexwithmodificationtime

Diese Eigenschaft ist identisch mit [**System. search. urlumindex**](props-system-search-urltoindex.md) , mit der Ausnahme, dass Sie den Zeitpunkt enthält, an dem die URL zuletzt geändert wurde. Dies ist eine Optimierung für den Indexer, sodass er keinen Rückruf an den Protokollhandler durchführt, um zu ermitteln, ob der Inhalt erneut indiziert werden muss.

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

## <a name="remarks"></a>Bemerkungen

Diese [System. search. urldeindexwithmodificationtime]() -Eigenschaft ist identisch mit der Eigenschaft [System. search. urldeindex](/previous-versions/windows/desktop/legacy/bb760177(v=vs.85)) , mit dem Unterschied, dass Sie auch den Zeitpunkt der letzten Änderung des Dokuments übergeben haben. Wenn die Uhrzeit der letzten Änderung übereinstimmt, geht der Indexer davon aus, dass das Dokument bereits indiziert wurde, und löst die Benachrichtigung aus. Diese Eigenschaft ist ein Vektor mit zwei Elementen, einem **VT \_ LPWSTR** -Wert, der die URL und einen **VT \_ FILETIME** -Wert enthält, der den Zeitpunkt der letzten Änderung enthält.

[System. search. urlshindexwithmodificationtime]() wurde \_ \_ \_ \_ in früheren Versionen des Windows-Betriebssystems in früheren Versionen des Windows-Betriebssystems PID gthr dirlink genannt.

Pkey-Werte werden in "propkey. h" definiert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System. search. urlum Index](/previous-versions/windows/desktop/legacy/bb760177(v=vs.85))
</dt> <dt>

[propertydescription](./propdesc-schema-propertydescription.md)
</dt> <dt>

[SearchInfo](./propdesc-schema-searchinfo.md)
</dt> <dt>

[Labelinfo](./propdesc-schema-labelinfo.md)
</dt> <dt>

[TypeInfo](./propdesc-schema-typeinfo.md)
</dt> <dt>

[Display Info](./propdesc-schema-displayinfo.md)
</dt> <dt>

[StringFormat](./propdesc-schema-stringformat.md)
</dt> <dt>

[BooleanFormat](./propdesc-schema-booleanformat.md)
</dt> <dt>

[NumberFormat](./propdesc-schema-numberformat.md)
</dt> <dt>

[dateTimeFormat](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[enumeratedlist](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[DrawControl](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[editcontrol](./propdesc-schema-editcontrol.md)
</dt> <dt>

[FilterControl](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[querycontrol](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
