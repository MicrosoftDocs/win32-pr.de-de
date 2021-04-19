---
description: Gibt an, ob das Element gelesen wurde.
ms.assetid: 2efa6dd9-8521-48c9-9aff-e2e8f0e2296d
title: System. isread
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 045dda6e840ff9d800b44573c4ba8537cdd2ebfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353142"
---
# <a name="systemisread"></a>System. isread

Gibt an, ob das Element gelesen wurde.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a>Windows 10, Version 1703, Windows 10, Version 1607, Windows 10, Version 1511, Windows 10, Version 1507, Windows 8.1, Windows 8, Windows 7

```
propertyDescription
   name = System.IsRead
   shellPKey = PKEY_IsRead
   formatID = E3E0584C-B788-4A5A-BB20-7F5A44C9ACDD
   propID = 10
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = Boolean
      EnumeratedList
         UseValueForDefault = True
         enum
            name = Read
            value = #TRUE#
            text = Read
            defineToken = ISREAD_READ
         enum
            name = NotRead
            value = #FALSE#
            text = Unread
            defineToken = ISREAD_NOTREAD
```

## <a name="windows-vista"></a>Windows Vista

```
propertyDescription
   name = System.IsRead
   shellPKey = PKEY_IsRead
   formatID = E3E0584C-B788-4A5A-BB20-7F5A44C9ACDD
   propID = 10
   SearchInfo
      IsColumn = true
   typeInfo
      type = Boolean
      EnumeratedList
         UseValueForDefault = True
         enum
            value = #TRUE#
            text = Read
            mnemonics = read
         enum
            value = #FALSE#
            text = Unread
            mnemonics = unread
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

 

 
