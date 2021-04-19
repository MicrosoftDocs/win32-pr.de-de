---
description: Wird von einem Container-IFilter für jede untergeordnete URL innerhalb des Containers ausgegeben. Die untergeordneten Elemente werden schließlich vom Indexer durchlaufen, wenn Sie sich innerhalb des Bereichs befinden.
ms.assetid: e864b3fa-6d43-40fe-9556-474953098947
title: System. search. urlum Index
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d4832279237cb7a3659b37d6502bd853caff113
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106348666"
---
# <a name="systemsearchurltoindex"></a>System. search. urlum Index

Wird von einem Container- [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) für jede untergeordnete URL innerhalb des Containers ausgegeben. Die untergeordneten Elemente werden schließlich vom Indexer durchlaufen, wenn Sie sich innerhalb des Bereichs befinden.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10, Version 1703, Windows 10, Version 1607, Windows 10, Version 1511, Windows 10, Version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista

```
propertyDescription
   name = System.Search.UrlToIndex
   shellPKey = PKEY_Search_UrlToIndex
   formatID = 0B63E343-9CCC-11D0-BCDB-00805FCCCE04
   propID = 2
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = String
```

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft enthält eine URL und wird von einem Protokollhandler für jede untergeordnete URL oder dieses directtoy unter der aktuellen URL ausgegeben. Der Indexer ruft den Protokollhandler zurück und fordert das Indizieren dieses Dokuments an. [System. search. urldeindex](/previous-versions/windows/desktop/legacy/bb760177(v=vs.85)) wurde \_ \_ in früheren Versionen des Windows-Betriebssystems in früheren Versionen des Windows-Betriebssystems PID gthr dirlink genannt.

Pkey-Werte werden in "propkey. h" definiert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System. search. urldeindexwithmodificationtime](./props-system-search-urltoindexwithmodificationtime.md)
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

 

 
