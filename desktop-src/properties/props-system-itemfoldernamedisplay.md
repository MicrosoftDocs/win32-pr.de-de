---
description: Der benutzerfreundliche Anzeige Name des übergeordneten Ordners eines Elements.
ms.assetid: 4049b6cb-41a1-4df6-89d1-a2022d3a285d
title: System. itemfoldernamedisplay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d637412b02345b52fee2e1c13e8f499314af4c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216996"
---
# <a name="systemitemfoldernamedisplay"></a>System. itemfoldernamedisplay

Der benutzerfreundliche Anzeige Name des übergeordneten Ordners eines Elements.

Dies wird von [System. itemfolderpathdisplay](./props-system-itemfolderpathdisplay.md)abgeleitet. Wenn diese Eigenschaft den Wert VT \_ empty hat, sollte diese Eigenschaft ebenfalls sein.

Wenn es sich bei dem Ordner um einen Datei Ordner handelt, wird der Wert lokalisiert, wenn ein lokalisierter Name verfügbar ist.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10, Version 1703, Windows 10, Version 1607, Windows 10, Version 1511, Windows 10, Version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista

```
propertyDescription
   name = System.ItemFolderNameDisplay
   shellPKey = PKEY_ItemFolderNameDisplay
   formatID = B725F130-47EF-101A-A5F1-02608C9EEBAC
   propID = 2
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a>Bemerkungen

Pkey-Werte werden in "propkey. h" definiert.

Wenn [System. itemfolderpathdisplay](./props-system-itemfolderpathdisplay.md) den Wert VT \_ empty hat, sollte diese Eigenschaft auch leer sein. Andernfalls sollte Sie von der Datenquelle aus System. itemfolderpathdisplay ordnungsgemäß abgeleitet werden.

Beispiele:



| Gegebener Pfad                             | Anzeige Name des Ordners |
|----------------------------------------|---------------------|
| c: \\ myfiles- \\ Text \\hello.txt           | Text                |
| \\\\Server \\ Freigabe \\ "MyDir" \\goodnews.doc | "MyDir"               |
| \\\\Server \\ Freigabe \\numbers.xls         | Freigeben               |
| c: \\ Ordner \\ MyFolder                  | Ordner             |
| /Mailbox Account/Inbox/"Re: Hello!"    | Posteingang               |



 

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

 

 
