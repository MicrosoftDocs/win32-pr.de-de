---
description: Ein Bewertungssystem, das einen Bereich von ganzzahligen Werten zwischen 0 und 5 verwendet.
ms.assetid: 50353ba9-86dd-4172-91b4-1898c8fc5522
title: System.SimpleRating
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74e13d7f65fb335aea6362509c20845bd1324b6e99d48f14cd9746f0237661f4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119598140"
---
# <a name="systemsimplerating"></a>System.SimpleRating

Ein Bewertungssystem, das einen Bereich von ganzzahligen Werten zwischen 0 und 5 verwendet.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10, Version 1703, Windows 10, Version 1607, Windows 10, Version 1511, Windows 10, Version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista

```
propertyDescription
   name = System.SimpleRating
   shellPKey = PKEY_SimpleRating
   formatID = A09F084E-AD41-489F-8076-AA5BE3082BCA
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = UInt32
      IsInnate = true
```

## <a name="remarks"></a>Hinweise

PKEY-Werte werden in Propkey.h definiert.

Zur Kompatibilität mit dem Windows Vista Shell-Bewertungssystem sollte ihr Eigenschaftenhandler auch die [System.Rating-Eigenschaft](./props-system-rating.md) mit der Für diese Eigenschaft beschriebenen Zuordnung auffüllen.

Verwenden Sie die folgende Tabelle, um [von System.Rating in](./props-system-rating.md) [System.SimpleRating zu konvertieren.]()



| System.Rating | System.SimpleRating |
|---------------|---------------------|
| 0             | 0                   |
| 1-12          | 1                   |
| 13-37         | 2                   |
| 38-62         | 3                   |
| 63-87         | 4                   |
| 88-99         | 5                   |



 

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

 

 
