---
description: Der benutzerfreundliche Anzeigename des übergeordneten Ordners eines Elements.
ms.assetid: 4049b6cb-41a1-4df6-89d1-a2022d3a285d
title: System.ItemFolderNameDisplay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7c8e8ca12af7c7665a2fd4b64f2911a1e6dbc99805cf4355ea1bb1ceec764c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119945170"
---
# <a name="systemitemfoldernamedisplay"></a>System.ItemFolderNameDisplay

Der benutzerfreundliche Anzeigename des übergeordneten Ordners eines Elements.

Dies wird von [System.ItemFolderPathDisplay abgeleitet.](./props-system-itemfolderpathdisplay.md) Wenn diese Eigenschaft VT \_ EMPTY ist, sollte diese Eigenschaft ebenfalls sein.

Wenn der Ordner ein Dateiordner ist, wird der Wert lokalisiert, wenn ein lokalisierter Name verfügbar ist.

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

## <a name="remarks"></a>Hinweise

PKEY-Werte werden in Propkey.h definiert.

Wenn [System.ItemFolderPathDisplay](./props-system-itemfolderpathdisplay.md) VT \_ EMPTY ist, sollte diese Eigenschaft ebenfalls leer sein. Andernfalls sollte sie von der Datenquelle von System.ItemFolderPathDisplay entsprechend abgeleitet werden.

Beispiele:



| Angegebener Pfad                             | Anzeigename des Ordners |
|----------------------------------------|---------------------|
| c: \\ \\ MyFiles-hello.txt \\           | Text                |
| \\\\server \\ share \\ mydir \\goodnews.doc | mydir               |
| \\\\\\ \\ Serverfreigabe-numbers.xls         | Freigeben               |
| c: \\ Ordner \\ MyFolder                  | Ordner             |
| /Postfachkonto/Posteingang/'Re: Hello!    | Posteingang               |



 

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

 

 
