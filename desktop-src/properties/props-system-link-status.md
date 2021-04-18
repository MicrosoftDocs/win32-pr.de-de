---
description: Gibt an, ob der Linkpfad in System. Link. targetparamesingpath überprüft wird.
ms.assetid: 38c73501-6376-41bb-8ad0-8f94ad42dfc9
title: System. Link. Status
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df9b4a6b398ba022f9f62a0860262028ced49a55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347553"
---
# <a name="systemlinkstatus"></a>System. Link. Status

Gibt an, ob der Linkpfad in [System. Link. targetparamesingpath](./props-system-link-targetparsingpath.md) überprüft wird. Diese Werte werden definiert.

-   Nicht **aufgelöst (Standard** )
-   Gelöst
-   Unterbrochen

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a>Windows 10, Version 1703, Windows 10, Version 1607, Windows 10, Version 1511, Windows 10, Version 1507, Windows 8.1, Windows 8, Windows 7

```
propertyDescription
   name = System.Link.Status
   shellPKey = PKEY_Link_Status
   formatID = B9B4B3FC-2B51-4A42-B5D8-324146AFCF25
   propID = 3
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Int32
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            name = Resolved
            value = 1
            text = Resolved
            defineToken = LINK_STATUS_RESOLVED
         enum
            name = Broken
            value = 2
            text = Broken
            defineToken = LINK_STATUS_BROKEN
```

## <a name="windows-vista"></a>Windows Vista

```
propertyDescription
   name = System.Link.Status
   shellPKey = PKEY_Link_Status
   formatID = B9B4B3FC-2B51-4A42-B5D8-324146AFCF25
   propID = 3
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Int32
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            value = 1
            text = Resolved
            defineName = LINK_STATUS_RESOLVED
         enum
            value = 2
            text = Broken
            defineName = LINK_STATUS_BROKEN
```

## <a name="remarks"></a>Bemerkungen

Pkey-Werte werden in "propkey. h" definiert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

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

 

 
