---
description: Gibt den Grad der Gesamtanpassung des Bildgewinns an. Berechnet aus PKEY \_ Photo \_ GainControlNumerator und PKEY \_ Photo \_ GainControlDenominator.
ms.assetid: 5076e03b-2c8a-4ef4-93d6-271a4bd697a6
title: System.Photo.GainControl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65faba3fe41d63d12b5918e229543670f122ac36e2dbcbfd80c96947a3a408a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118228991"
---
# <a name="systemphotogaincontrol"></a>System.Photo.GainControl

Gibt den Grad der Gesamtanpassung des Bildgewinns an. Berechnet aus PKEY \_ Photo \_ GainControlNumerator und PKEY \_ Photo \_ GainControlDenominator.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a>Windows 10, Version 1703, Windows 10, Version 1607, Windows 10, Version 1511, Windows 10, Version 1507, Windows 8.1, Windows 8, Windows 7

```
propertyDescription
   name = System.Photo.GainControl
   shellPKey = PKEY_Photo_GainControl
   formatID = FA304789-00C7-4D80-904A-1E4DCC7265AA
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Double
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            name = None
            value = 0.0
            text = None
            defineToken = PHOTO_GAINCONTROL_NONE
         enum
            name = LowGainUp
            value = 1.0
            text = Low gain up
            defineToken = PHOTO_GAINCONTROL_LOWGAINUP
         enum
            name = HighGainUp
            value = 2.0
            text = High gain up
            defineToken = PHOTO_GAINCONTROL_HIGHGAINUP
         enum
            name = LowGainDown
            value = 3.0
            text = Low gain down
            defineToken = PHOTO_GAINCONTROL_LOWGAINDOWN
         enum
            name = HighGainDown
            value = 4.0
            text = High gain down
            defineToken = PHOTO_GAINCONTROL_HIGHGAINDOWN
```

## <a name="windows-vista"></a>Windows Vista

```
propertyDescription
   name = System.Photo.GainControl
   shellPKey = PKEY_Photo_GainControl
   formatID = FA304789-00C7-4D80-904A-1E4DCC7265AA
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Double
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            value = 0.0
            text = None
            defineName = PHOTO_GAINCONTROL_NONE
         enum
            value = 1.0
            text = Low gain up
            defineName = PHOTO_GAINCONTROL_LOWGAINUP
         enum
            value = 2.0
            text = High gain up
            defineName = PHOTO_GAINCONTROL_HIGHGAINUP
         enum
            value = 3.0
            text = Low gain down
            defineName = PHOTO_GAINCONTROL_LOWGAINDOWN
         enum
            value = 4.0
            text = High gain down
            defineName = PHOTO_GAINCONTROL_HIGHGAINDOWN
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

 

 
