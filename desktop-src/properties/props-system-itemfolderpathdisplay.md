---
description: Erfahren Sie mehr über die System.ItemFolderPathDisplay-Eigenschaft, die den benutzerfreundlichen Anzeigepfad des übergeordneten Ordners eines Elements darstellt.
ms.assetid: 16f67edc-ca8a-4c2e-9d9b-be8600446e51
title: System.ItemFolderPathDisplay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8fd2288f12073fe8e36707bf49aca2bc5e000d0bbe25d95fba0736b4e77af44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119822340"
---
# <a name="systemitemfolderpathdisplay"></a>System.ItemFolderPathDisplay

Der benutzerfreundliche Anzeigepfad des übergeordneten Ordners eines Elements.

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

## <a name="remarks"></a>Hinweise

PKEY-Werte werden in Propkey.h definiert.

Wenn [System.ItemPathDisplay](./props-system-itempathdisplay.md) VT \_ EMPTY ist, sollte diese Eigenschaft ebenfalls leer sein. Andernfalls sollte sie von der Datenquelle von System.ItemPathDisplay entsprechend abgeleitet werden.

Beispielwerte:



| Pfad                                   | ItemFolderPathDisplay    |
|----------------------------------------|--------------------------|
| c: \\ Persönliche \\ Dateienhello.txt \\         | c: \\ Persönliche \\ Dateien      |
| \\\\server \\ share \\ mydir \\goodnews.doc | \\\\Serverfreigabe \\ \\ mydir |
| \\\\\\ \\ Serverfreigabe-numbers.xls         | \\\\\\Serverfreigabe        |
| c: \\ food \\ MyFolder                     | c: \\ Essen                 |
| /Postfachkonto/Posteingang/'Re: Hello!    | /Postfachkonto/Posteingang   |



 

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

 

 
