---
description: Diese Zeichenfolge sollte auf die phonetische Version des Anzeigenamens festgelegt werden, wie in System.ItemNameDisplay in CJK-Gebietsschemas (CHS Pinyin, JPN Hiragana, KOR Hangul usw.) definiert.
ms.assetid: eb491644-bf59-4439-9e9b-bcafde619d66
title: System.ItemNameSortOverride
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64c555007ae7bd2a0c7ca5f16e6e3ad26449942b2c7031b81a03317d0d6212a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117865883"
---
# <a name="systemitemnamesortoverride"></a>System.ItemNameSortOverride

Diese Zeichenfolge sollte auf die phonetische Version des Anzeigenamens festgelegt werden, wie in System.ItemNameDisplay in CJK-Gebietsschemas (CHS Pinyin, JPN Hiragana, KOR Hangul usw.) definiert. Das erste Zeichen dieses Felds wird auch zum Gruppieren von Namen nach FirstLetter verwendet. Für die meisten Nicht-CJK-Sprachen muss dieses Feld nicht festgelegt werden (in diesem Fall wird System.ItemNameDisplay verwendet). Wenn es jedoch wünschenswert ist, den Gruppierungsbuchstaben zu überschreiben (z. B. um führende Artikel wie "a" und "the") zu entfernen, kann hier eine alternative Zeichenfolge angegeben werden.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8"></a>Windows 10, Version 1703, Windows 10, Version 1607, Windows 10, Version 1511, Windows 10, Version 1507, Windows 8.1, Windows 8

```
propertyDescription
   name = System.ItemNameSortOverride
   shellPKey = PKEY_ItemNameSortOverride
   formatID = B725F130-47EF-101A-A5F1-02608C9EEBAC
   propID = 23
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a>Hinweise

PKEY-Werte werden in Propkey.h definiert.

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

 

 
