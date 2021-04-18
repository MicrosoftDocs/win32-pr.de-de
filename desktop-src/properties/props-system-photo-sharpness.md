---
description: Gibt die Richtung der Schärfe Verarbeitung an, die von der Kamera angewendet wurde, als das Foto entnommen wurde.
ms.assetid: ee3dca97-a094-4de8-aacd-729abcef4965
title: System. Photo. Schärding
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61b6b1b3dc90df576b90b8de6d912a176872bfee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106351644"
---
# <a name="systemphotosharpness"></a>System. Photo. Schärding

Gibt die Richtung der Schärfe Verarbeitung an, die von der Kamera angewendet wurde, als das Foto entnommen wurde.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a>Windows 10, Version 1703, Windows 10, Version 1607, Windows 10, Version 1511, Windows 10, Version 1507, Windows 8.1, Windows 8, Windows 7

```
propertyDescription
   name = System.Photo.Sharpness
   shellPKey = PKEY_Photo_Sharpness
   formatID = FC6976DB-8349-4970-AE97-B3C5316A08F0
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = UInt32
      EnumeratedList
         UseValueForDefault = True
         enum
            name = Normal
            value = 0
            text = Normal
            defineToken = PHOTO_SHARPNESS_NORMAL
         enum
            name = Soft
            value = 1
            text = Soft
            defineToken = PHOTO_SHARPNESS_SOFT
         enum
            name = Hard
            value = 2
            text = Hard
            defineToken = PHOTO_SHARPNESS_HARD
```

## <a name="windows-vista"></a>Windows Vista

```
propertyDescription
   name = System.Photo.Sharpness
   shellPKey = PKEY_Photo_Sharpness
   formatID = FC6976DB-8349-4970-AE97-B3C5316A08F0
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = UInt32
      EnumeratedList
         UseValueForDefault = True
         enum
            value = 0
            text = Normal
            defineName = PHOTO_SHARPNESS_NORMAL
         enum
            value = 1
            text = Soft
            defineName = PHOTO_SHARPNESS_SOFT
         enum
            value = 2
            text = Hard
            defineName = PHOTO_SHARPNESS_HARD
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

 

 
