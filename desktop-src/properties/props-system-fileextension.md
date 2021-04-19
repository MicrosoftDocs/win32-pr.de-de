---
description: Identifiziert die Dateierweiterung des dateibasierten Elements, einschließlich des führenden Zeitraums.
ms.assetid: b72c695e-bdbd-471d-b902-9e30a62facd4
title: System. File Extension
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf8792a3965c394a1944985515df527e41e3a159
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360506"
---
# <a name="systemfileextension"></a>System. File Extension

Identifiziert die Dateierweiterung des dateibasierten Elements, einschließlich des führenden Zeitraums. Diese Eigenschaft wird von System. filename abgeleitet. Wenn System. filename entweder keine Dateierweiterung hat oder VT \_ leer ist, sollte der Wert für diese Eigenschaft "VT Empty" lauten \_ .

Zum Abrufen des Typs eines beliebigen Elements (einschließlich eines Elements, das keine Datei ist), verwenden Sie System. ItemType.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10, Version 1703, Windows 10, Version 1607, Windows 10, Version 1511, Windows 10, Version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista

```
propertyDescription
   name = System.FileExtension
   shellPKey = PKEY_FileExtension
   formatID = E4F10A3C-49E6-405D-8288-A23BD4EEAA6C
   propID = 100
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a>Bemerkungen

Pkey-Werte werden in "propkey. h" definiert.

Wenn [System. filename](./props-system-filename.md) den Wert VT \_ empty hat, sollte diese Eigenschaft auch leer sein. Andernfalls sollte diese Eigenschaft von der Datenquelle aus System. filename abgeleitet werden. Wenn "System. filename" keine Dateierweiterung enthält, muss " [System. FileExtension]() " "VT Empty" lauten \_ . Zum Abrufen des Typs eines beliebigen Elements (einschließlich eines Elements, das keine Datei ist), verwenden Sie [System. ItemType](./props-system-itemtype.md).

Beispiele für Pfad-und Datei Erweiterungs Eigenschaften. 

| Pfad                               | Dateierweiterung |
|------------------------------------|----------------|
| c: \\ \\ Eigene Dateien \\hello.txt     | .txt           |
| \\\\Server \\ Freigabe \\ "MyDir" \\news.doc | .doc           |
| \\\\Server \\ Freigabe \\numbers.xls     | .xls           |
| \\\\Server \\ Freigabe \\ Ordner          | VT \_ leer      |
| c: \\ Material \\ MyFolder                | VT \_ leer      |
| \[desktop\]                        | VT \_ leer      |



 

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

 

 
