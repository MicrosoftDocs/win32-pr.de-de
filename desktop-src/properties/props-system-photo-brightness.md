---
description: Der Helligkeitswert des Bilds (in Spitze Einheiten) in der Regel im Bereich von-99,99 bis 99,99.
ms.assetid: 533f6934-dec8-455a-937c-d4e144be4335
title: System. Photo. Helligkeit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 131b7e2d51f402aa8da4d5e9b266fe1fc1b39b29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360228"
---
# <a name="systemphotobrightness"></a>System. Photo. Helligkeit

Der Helligkeitswert des Bilds (in Spitze Einheiten) in der Regel im Bereich von-99,99 bis 99,99.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10, Version 1703, Windows 10, Version 1607, Windows 10, Version 1511, Windows 10, Version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista

```
propertyDescription
   name = System.Photo.Brightness
   shellPKey = PKEY_Photo_Brightness
   formatID = 1A701BF6-478C-4361-83AB-3701BB053C58
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Double
      IsInnate = true
```

## <a name="remarks"></a>Bemerkungen

Pkey-Werte werden in "propkey. h" definiert.

Einen Vergleich von [System. Photo. Helligkeit]() -Zahlen und Foot-Lambert Messungen finden Sie in der EXIF 2,2-Spezifikation, Anhang C. Diese Eigenschaft wird aus [System. Photo. brightnessnumerator](./props-system-photo-brightnessnumerator.md) und [System. Photo. brightnessnenner](./props-system-photo-brightnessdenominator.md)berechnet. , Wenn der Zähler des aufgezeichneten Werts FFFFFFFF ist. H, "unknown", sollte angegeben werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Exchangeable Image File Format für digitale Kameras: EXIF Version 2,2](https://www.exif.org/Exif2-2.PDF)
</dt> <dt>

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

 

 
