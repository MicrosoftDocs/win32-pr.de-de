---
description: Der benutzerfreundliche Anzeige Pfad zum Element.
ms.assetid: 27e4490b-7914-4b38-9799-e9d5dc407f13
title: System. itempathdisplay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddb76a4218e7e7580ec70cb57dd16c635ca024ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131573"
---
# <a name="systemitempathdisplay"></a>System. itempathdisplay

Der benutzerfreundliche Anzeige Pfad zum Element.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10, Version 1703, Windows 10, Version 1607, Windows 10, Version 1511, Windows 10, Version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista

```
propertyDescription
   name = System.ItemPathDisplay
   shellPKey = PKEY_ItemPathDisplay
   formatID = E3E0584C-B788-4A5A-BB20-7F5A44C9ACDD
   propID = 7
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a>Bemerkungen

Pkey-Werte werden in "propkey. h" definiert.

Wenn es sich bei dem Element um eine Datei oder einen Ordner handelt, enthält diese Eigenschaft in allen Fällen die Erweiterung und wird lokalisiert, wenn ein lokalisierter Name verfügbar ist. Bei anderen Elementen ist dies die benutzerfreundliche Entsprechung, wobei angenommen wird, dass das Element im hierarchischen Speicher vorhanden ist.

Im Gegensatz zu [System. itemurl](./props-system-itemurl.md)enthält dieser Eigenschafts Wert nicht das URL-Schema. Um einen Element Pfad zu analysieren, verwenden Sie "System. itemurl" oder " [System. Parser Path](./props-system-parsingpath.md)". Verwenden Sie zum Verweisen auf Shell-Namespace Elemente mithilfe von Shell-APIs System. Parser Path.

Beispielwerte:



| Pfad                                   | Itempathdisplay                        |
|----------------------------------------|----------------------------------------|
| c: \\ "MyDir"- \\ Leiste \\hello.txt              | c: \\ "MyDir"- \\ Leiste \\hello.txt              |
| \\\\Server \\ Freigabe \\ "MyDir" \\goodnews.doc | \\\\Server \\ Freigabe \\ "MyDir" \\goodnews.doc |
| \\\\Server \\ Freigabe \\numbers.xls         | \\\\Server \\ Freigabe \\numbers.xls         |
| c: \\ "MyDir" \\ meinOrdner                    | c: \\ "MyDir" \\ meinOrdner                    |
| /Mailbox Account/Inbox/"Re: Hello!"    | /Mailbox Account/Inbox/"Re: Hello!"    |



 

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

 

 
