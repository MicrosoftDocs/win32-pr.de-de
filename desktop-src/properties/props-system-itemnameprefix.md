---
description: Das Präfix eines Elements, das für E-Mail-Nachrichten verwendet wird, bei denen der Betreff mit dem Präfix &\# 0034 beginnt. Re:&\# 0034;.
ms.assetid: 3c257edc-b7f7-498d-8347-0be4fca41023
title: System.ItemNamePrefix
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd7830f63c3e9e0f6026099c95d11820a1d8592928cece72ebe72d76936d8467
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119598460"
---
# <a name="systemitemnameprefix"></a>System.ItemNamePrefix

Das Präfix eines Elements, das für E-Mail-Nachrichten verwendet wird, bei denen der Betreff mit dem Präfix "Re:" beginnt.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10, Version 1703, Windows 10, Version 1607, Windows 10, Version 1511, Windows 10, Version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista

```
propertyDescription
   name = System.ItemNamePrefix
   shellPKey = PKEY_ItemNamePrefix
   formatID = D7313FF1-A77A-401C-8C99-3DBDD68ADD36
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a>Hinweise

PKEY-Werte werden in Propkey.h definiert.

Wenn das Element eine Datei ist, ist der Wert dieser Eigenschaft VT \_ EMPTY. Wenn das Element eine Nachricht ist, ist der Wert dieser Eigenschaft die Weiterleitungs- oder Antwortpräfixe (einschließlich des Trennzeichens, aber kein Leerzeichen) oder VT \_ EMPTY, wenn kein Präfix vorhanden ist.

Beispielwerte:



| System.ItemNamePrefix | System.ItemName  | System.ItemNameDisplay |
|-----------------------|------------------|------------------------|
| VT \_ EMPTY             | "Toller Tag"      | "Toller Tag"            |
| "Re:"                 | "Toller Tag"      | "Re: Great day"        |
| "Fwd: "               | "Monatliches Budget" | "Fwd: Monatliches Budget"  |
| VT \_ EMPTY             | accounts.xls     | accounts.xls           |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

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

 

 
