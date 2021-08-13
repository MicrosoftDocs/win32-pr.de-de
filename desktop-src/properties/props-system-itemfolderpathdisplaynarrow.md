---
description: Erfahren Sie mehr über die System.ItemFolderPathDisplayNarrow-Eigenschaft, die den benutzerfreundlichen Anzeigepfad des übergeordneten Ordners eines Elements darstellt.
ms.assetid: f60b7465-bca4-4c7b-9caf-9cda1bf6eeeb
title: System.ItemFolderPathDisplayNarrow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb87cadc4f4f132870ea51af1bba55c992c09d3eb5a90f446a3d92810b5941d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118726483"
---
# <a name="systemitemfolderpathdisplaynarrow"></a>System.ItemFolderPathDisplayNarrow

Der benutzerfreundliche Anzeigepfad des übergeordneten Ordners eines Elements.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10, Version 1703, Windows 10, Version 1607, Windows 10, Version 1511, Windows 10, Version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista

```
propertyDescription
   name = System.ItemFolderPathDisplayNarrow
   shellPKey = PKEY_ItemFolderPathDisplayNarrow
   formatID = DABD30ED-0043-4789-A7F8-D013A4736622
   propID = 100
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a>Hinweise

PKEY-Werte werden in Propkey.h definiert.

Das Format der Zeichenfolge sollte so angepasst werden, dass der Ordnername an erster Stelle steht, um eine Schmalansichtsspalte zu optimieren. Wenn der Ordner ein Dateiordner ist, enthält der Wert alle lokalisierten Namen. Wenn [System.ItemFolderPathDisplay](./props-system-itemfolderpathdisplay.md) VT \_ EMPTY ist, sollte diese Eigenschaft ebenfalls leer sein. Andernfalls sollte sie von der Datenquelle von System.ItemFolderPathDisplay entsprechend abgeleitet werden.

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

 

 
