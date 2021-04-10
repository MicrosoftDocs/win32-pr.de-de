---
description: Der benutzerfreundliche Typname des Elements.
ms.assetid: 5d4c86da-6317-4a34-88d6-caf794aaa165
title: System. itemtypetext
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 699a953392054cb2344c5f3b3d652e64a9a2c1f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215779"
---
# <a name="systemitemtypetext"></a>System. itemtypetext

Der benutzerfreundliche Typname des Elements. Dieser Wert sollte nicht Programm gesteuert analysiert werden.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10, Version 1703, Windows 10, Version 1607, Windows 10, Version 1511, Windows 10, Version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista

```
propertyDescription
   name = System.ItemTypeText
   shellPKey = PKEY_ItemTypeText
   formatID = B725F130-47EF-101A-A5F1-02608C9EEBAC
   propID = 4
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a>Bemerkungen

Pkey-Werte werden in "propkey. h" definiert.

Wenn [System. ItemType](./props-system-itemtype.md) \_ den Wert VT Empty hat, ist der Wert dieser Eigenschaft ebenfalls VT \_ empty. Wenn es sich bei dem Element um eine Datei handelt, ist der Wert dieser Eigenschaft mit dem Wert identisch, wenn Sie den System. ItemType-Wert der Datei an [**psformatfordisplay**](/windows/win32/api/propsys/nf-propsys-psformatfordisplay)übergeben haben.

Diese Eigenschaft sollte nicht mit [System. Kind](./props-system-kind.md)verwechselt werden. Dies ist ein allgemeiner, benutzerfreundlicher Name der Art. Für eine doc-Dokument Datei werden z. b. die verschiedenen Eigenschaften wie hier gezeigt angezeigt:



| Eigenschaft                                               | Wert                   |
|--------------------------------------------------------|-------------------------|
| [System. Kind](./props-system-kind.md)                 | Dokument                |
| [System. ItemType](./props-system-itemtype.md)         | .doc                    |
| [System. itemtypetext]() | Microsoft Word-Dokument |



 

Beispielwerte:



| Pfad                                   | Itemtypetext            |
|----------------------------------------|-------------------------|
| c: \\ "MyDir"- \\ Leiste \\hello.txt              | Textdatei               |
| \\\\Server \\ Freigabe \\ "MyDir" \\goodnews.doc | Microsoft Word-Dokument |
| \\\\Server \\ Freigabe \\ Ordner              | Datei Ordner             |
| c: \\ mydir \\ meinOrdner                    | Datei Ordner             |
| /Mailbox Account/Inbox/"Re: Hello!"    | Outlook-e-Mail  |



 

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

 

 
