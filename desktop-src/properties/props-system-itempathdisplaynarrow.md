---
description: Informieren Sie sich über die System.ItemPathDisplayNarrow-Eigenschaft, die den benutzerfreundlichen Anzeigepfad zum Element darstellt.
ms.assetid: 5dd44e13-bc5c-4e32-b5eb-2c7c40e10dfb
title: System.ItemPathDisplayNarrow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28385a889ea74b94ea990321dbb46173b078ff20222c22fe3599619faf9cb938
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118231473"
---
# <a name="systemitempathdisplaynarrow"></a>System.ItemPathDisplayNarrow

Der benutzerfreundliche Anzeigepfad zum Element.

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

## <a name="remarks"></a>Hinweise

PKEY-Werte werden in Propkey.h definiert.

Um für eine schmale Anzeigespalte zu optimieren, sollte das Format der Zeichenfolge so angepasst werden, dass der Name an erster Stelle steht.

Wenn es sich bei dem Element um eine Datei handelt, schließt der Eigenschaftswert die Dateierweiterung aus, enthält jedoch lokalisierte Namen, sofern vorhanden. Wenn es sich bei dem Element um eine Nachricht handelt, enthält der Wert [system.ItemNamePrefix.](./props-system-itemnameprefix.md) Um einen Elementpfad zu analysieren, verwenden Sie [System.ItemUrl](./props-system-itemurl.md) oder [System.ParsingPath](./props-system-parsingpath.md).

Beispielwerte:



| Pfad                                   | ItemPathDisplayName                 |
|----------------------------------------|-------------------------------------|
| c: \\ mydir \\ bar \\hello.txt              | hello (c: \\ mydir \\ bar)              |
| \\\\\\server share \\ mydir \\goodnews.doc | good servers ( \\ \\ server share \\ \\ mydir) |
| \\\\\\ \\ Serverfreigabeordner              | Ordner ( \\ \\ \\ Serverfreigabe)          |
| c: \\ MyDir \\ MyFolder                    | MyFolder (c: \\ mydir)                |
| /Mailbox Account/Inbox/'Re: Hello!'    | Re: Hello! (/Postfachkonto/Posteingang) |



 

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

 

 
