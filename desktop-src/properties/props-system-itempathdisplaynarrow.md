---
description: Der benutzerfreundliche Anzeige Pfad zum Element.
ms.assetid: 5dd44e13-bc5c-4e32-b5eb-2c7c40e10dfb
title: System. itempathdisplaynarrow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87ef7b9d03a78a23e955c20f52e32062a8bcabd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217520"
---
# <a name="systemitempathdisplaynarrow"></a>System. itempathdisplaynarrow

Der benutzerfreundliche Anzeige Pfad zum Element.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10, Version 1703, Windows 10, Version 1607, Windows 10, Version 1511, Windows 10, Version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista

```
propertyDescription
   name = System.ItemPathDisplayNarrow
   shellPKey = PKEY_ItemPathDisplayNarrow
   formatID = 28636AA6-953D-11D2-B5D6-00C04FD918D0
   propID = 8
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a>Bemerkungen

Pkey-Werte werden in "propkey. h" definiert.

Um für eine schmale Anzeige Spalte zu optimieren, sollte das Format der Zeichenfolge so angepasst werden, dass der Name zuerst angezeigt wird.

Wenn es sich bei dem Element um eine Datei handelt, schließt der Eigenschafts Wert die Dateierweiterung aus, enthält jedoch lokalisierte Namen, sofern diese vorhanden sind. Wenn das Element eine Meldung ist, enthält der Wert " [System. itemnameprefix](./props-system-itemnameprefix.md)". Um einen Element Pfad zu analysieren, verwenden Sie " [System. itemurl](./props-system-itemurl.md) " oder " [System. Parser Path](./props-system-parsingpath.md)".

Beispielwerte:



| Pfad                                   | Itempathdisplayname                 |
|----------------------------------------|-------------------------------------|
| c: \\ "MyDir"- \\ Leiste \\hello.txt              | Hello (c: \\ "MyDir"- \\ Leiste)              |
| \\\\Server \\ Freigabe \\ "MyDir" \\goodnews.doc | goodnews ( \\ \\ Server \\ Freigabe \\ mydir) |
| \\\\Server \\ Freigabe \\ Ordner              | Ordner ( \\ \\ Server \\ Freigabe)          |
| c: \\ mydir \\ meinOrdner                    | MyFolder (c: \\ mydir)                |
| /Mailbox Account/Inbox/"Re: Hello!"    | Neu: Hallo! (/Mailbox Account/Inbox) |



 

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

 

 
