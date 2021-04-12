---
description: Diese Zeichenfolge sollte auf die phonetische Version des Anzeige namensfest gelegt werden, wie in "System. itemnamedisplay" in cjk-Gebiets Schemata (CHS Pinyin, JPN Hiragana, Kor Hangul usw.) definiert.
ms.assetid: eb491644-bf59-4439-9e9b-bcafde619d66
title: System. itemnamesoresverride
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d79f9bb07eb15eb5d25fbfa1e95d4c0f80b35611
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217212"
---
# <a name="systemitemnamesortoverride"></a>System. itemnamesoresverride

Diese Zeichenfolge sollte auf die phonetische Version des Anzeige namensfest gelegt werden, wie in "System. itemnamedisplay" in cjk-Gebiets Schemata (CHS Pinyin, JPN Hiragana, Kor Hangul usw.) definiert. Das erste Zeichen dieses Felds wird auch zum Gruppieren von Namen nach FirstLetter verwendet. Bei den meisten nicht-CJK-Sprachen muss dieses Feld nicht festgelegt werden (in diesem Fall wird System. itemnamedisplay verwendet). Wenn es jedoch wünschenswert ist, den Gruppierungs Buchstaben zu überschreiben (z. b. um führende Artikel wie z. b. "a" und "The" zu entfernen), kann hier eine Alternative Zeichenfolge angegeben werden.

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

## <a name="remarks"></a>Bemerkungen

Pkey-Werte werden in "propkey. h" definiert.

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

 

 
