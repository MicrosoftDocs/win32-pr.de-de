---
description: Der von der Kamera verwendete Messungs Modus, der aus den Informationen zur austauschbaren Bilddatei (EXIF) stammt.
ms.assetid: 9dd031a8-f1fa-4753-a86b-18051c624a00
title: System. Photo. meteringmode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e90fff67abe04486504ecda67684f85cb5ac1a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368712"
---
# <a name="systemphotometeringmode"></a>System. Photo. meteringmode

Der von der Kamera verwendete Messungs Modus, der aus den Informationen zur austauschbaren Bilddatei (EXIF) stammt.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a>Windows 10, Version 1703, Windows 10, Version 1607, Windows 10, Version 1511, Windows 10, Version 1507, Windows 8.1, Windows 8, Windows 7

```
propertyDescription
   name = System.Photo.MeteringMode
   shellPKey = PKEY_Photo_MeteringMode
   formatID = 14B81DA1-0135-4D31-96D9-6CBFC9671A99
   propID = 37383
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = UInt16
      EnumeratedList
         UseValueForDefault = True
         enum
            name = Unknown
            value = 0
            text = Unknown
            defineToken = PHOTO_METERINGMODE_UNKNOWN
         enum
            name = Average
            value = 1
            text = Average
            defineToken = PHOTO_METERINGMODE_AVERAGE
         enum
            name = Center
            value = 2
            text = Center Weighted Average
            defineToken = PHOTO_METERINGMODE_CENTER
         enum
            name = Spot
            value = 3
            text = Spot
            defineToken = PHOTO_METERINGMODE_SPOT
         enum
            name = MultiSpot
            value = 4
            text = Multi Spot
            defineToken = PHOTO_METERINGMODE_MULTISPOT
         enum
            name = Pattern
            value = 5
            text = Pattern
            defineToken = PHOTO_METERINGMODE_PATTERN
         enum
            name = Partial
            value = 6
            text = Partial
            defineToken = PHOTO_METERINGMODE_PARTIAL
```

## <a name="windows-vista"></a>Windows Vista

```
propertyDescription
   name = System.Photo.MeteringMode
   shellPKey = PKEY_Photo_MeteringMode
   formatID = 14B81DA1-0135-4D31-96D9-6CBFC9671A99
   propID = 37383
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = UInt16
      EnumeratedList
         UseValueForDefault = True
         enum
            value = 0
            text = Unknown
            defineName = PHOTO_METERINGMODE_UNKNOWN
         enum
            value = 1
            text = Average
            defineName = PHOTO_METERINGMODE_AVERAGE
         enum
            value = 2
            text = Center Weighted Average
            defineName = PHOTO_METERINGMODE_CENTER
         enum
            value = 3
            text = Spot
            defineName = PHOTO_METERINGMODE_SPOT
         enum
            value = 4
            text = Multi Spot
            defineName = PHOTO_METERINGMODE_MULTISPOT
         enum
            value = 5
            text = Pattern
            defineName = PHOTO_METERINGMODE_PATTERN
         enum
            value = 6
            text = Partial
            defineName = PHOTO_METERINGMODE_PARTIAL
```

## <a name="remarks"></a>Bemerkungen

Pkey-Werte werden in "propkey. h" definiert.

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

 

 
