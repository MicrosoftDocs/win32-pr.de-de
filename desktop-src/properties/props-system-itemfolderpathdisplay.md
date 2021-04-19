---
description: Der benutzerfreundliche Anzeige Pfad für den übergeordneten Ordner eines Elements.
ms.assetid: 16f67edc-ca8a-4c2e-9d9b-be8600446e51
title: System. itemfolderpathdisplay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c4ae4c9178356d36c644f1bc886d63331155e88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106359012"
---
# <a name="systemitemfolderpathdisplay"></a>System. itemfolderpathdisplay

Der benutzerfreundliche Anzeige Pfad für den übergeordneten Ordner eines Elements.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10, Version 1703, Windows 10, Version 1607, Windows 10, Version 1511, Windows 10, Version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista

```
propertyDescription
   name = System.ItemFolderPathDisplay
   shellPKey = PKEY_ItemFolderPathDisplay
   formatID = E3E0584C-B788-4A5A-BB20-7F5A44C9ACDD
   propID = 6
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a>Bemerkungen

Pkey-Werte werden in "propkey. h" definiert.

Wenn [System. itempathdisplay](./props-system-itempathdisplay.md) den Wert VT \_ empty hat, sollte diese Eigenschaft auch leer sein. Andernfalls sollte Sie von der Datenquelle aus System. itempathdisplay ordnungsgemäß abgeleitet werden.

Beispielwerte:



| Pfad                                   | Itemfolderpathdisplay    |
|----------------------------------------|--------------------------|
| c: \\ \\ Eigene Dateien \\hello.txt         | c: \\ \\ persönliche Dateien      |
| \\\\Server \\ Freigabe \\ "MyDir" \\goodnews.doc | \\\\Server \\ Freigabe \\ "MyDir" |
| \\\\Server \\ Freigabe \\numbers.xls         | \\\\Server \\ Freigabe        |
| c: \\ Nahrungsmittel \\ MyFolder                     | c: \\ Nahrungsmittel                 |
| /Mailbox Account/Inbox/"Re: Hello!"    | /Mailbox Konto/Eingangsbox   |



 

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

 

 
