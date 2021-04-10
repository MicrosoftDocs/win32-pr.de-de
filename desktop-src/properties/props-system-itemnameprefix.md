---
description: 'Das Präfix eines Elements, das für e-Mail-Nachrichten verwendet wird, bei denen der Betreff mit dem Präfix &\# 0034 Re: &\# 0034;.'
ms.assetid: 3c257edc-b7f7-498d-8347-0be4fca41023
title: System. itemnameprefix
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cf669dd867c8cf60046f226e33dae18f46060cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959130"
---
# <a name="systemitemnameprefix"></a>System. itemnameprefix

Das Präfix eines Elements, das für e-Mail-Nachrichten verwendet wird, wobei der Betreff mit dem Präfix "Re:" beginnt.

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

## <a name="remarks"></a>Bemerkungen

Pkey-Werte werden in "propkey. h" definiert.

Wenn es sich bei dem Element um eine Datei handelt, ist der Wert dieser Eigenschaft VT \_ empty. Wenn es sich bei dem Element um eine Nachricht handelt, ist der Wert dieser Eigenschaft die Weiterleitungs-oder Antwort Präfixe (einschließlich des Trenn Zeichens, aber ohne Leerzeichen), oder VT \_ empty, wenn kein Präfix vorhanden ist.

Beispielwerte:



| System. itemnameprefix | System. ItemName  | System.ItemNameDisplay |
|-----------------------|------------------|------------------------|
| VT \_ leer             | "Toller Tag"      | "Toller Tag"            |
| "Re:"                 | "Toller Tag"      | "Re: tolle Tage"        |
| "F":               | "Monatliches Budget" | "F: Monatliches Budget"  |
| VT \_ leer             | accounts.xls     | accounts.xls           |



 

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

 

 
