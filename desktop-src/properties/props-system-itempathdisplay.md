---
description: Erfahren Sie mehr über die System.ItemPathDisplay-Eigenschaft, die den benutzerfreundlichen Anzeigepfad zum Element darstellt.
ms.assetid: 27e4490b-7914-4b38-9799-e9d5dc407f13
title: System.ItemPathDisplay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88a58d48740c6f7a2f9db0e496a951105c176ca7eba3dd205c2971188af7fd55
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118231663"
---
# <a name="systemitempathdisplay"></a>System.ItemPathDisplay

Der benutzerfreundliche Anzeigepfad zum Element.

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

## <a name="remarks"></a>Hinweise

PKEY-Werte werden in Propkey.h definiert.

Wenn es sich bei dem Element um eine Datei oder einen Ordner handelt, enthält diese Eigenschaft in allen Fällen die Erweiterung und wird lokalisiert, wenn ein lokalisierter Name verfügbar ist. Bei anderen Elementen ist dies die benutzerfreundliche Entsprechung, vorausgesetzt, das Element ist im hierarchischen Speicher vorhanden.

Im [Gegensatz zu System.ItemUrl](./props-system-itemurl.md)enthält dieser Eigenschaftswert nicht das URL-Schema. Um einen Elementpfad zu analysieren, verwenden Sie System.ItemUrl oder [System.ParsingPath](./props-system-parsingpath.md). Verwenden Sie System.ParsingPath, um mithilfe von Shell-APIs auf Shellnamespaceelemente zu verweisen.

Beispielwerte:



| Pfad                                   | ItemPathDisplay                        |
|----------------------------------------|----------------------------------------|
| c: \\ mydir \\ bar \\hello.txt              | c: \\ mydir \\ bar \\hello.txt              |
| \\\\server \\ share \\ mydir \\goodnews.doc | \\\\server \\ share \\ mydir \\goodnews.doc |
| \\\\Serverfreigabe \\ \\numbers.xls         | \\\\Serverfreigabe \\ \\numbers.xls         |
| c: \\ mydir \\ MyFolder                    | c: \\ mydir \\ MyFolder                    |
| /Postfachkonto/Posteingang/'Re: Hello!'    | /Postfachkonto/Posteingang/'Re: Hello!'    |



 

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

 

 
