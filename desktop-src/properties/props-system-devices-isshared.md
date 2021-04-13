---
description: Wenn diese Eigenschaft den Wert true hat, ist das Gerät ein frei gegebenes Gerät.
ms.assetid: d1da0747-ad07-49e5-8082-5f39bf0a84d8
title: System. Devices. IsShared
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f41cf4f6ad2988a21e30c0c67101b2582699704
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350388"
---
# <a name="systemdevicesisshared"></a>System. Devices. IsShared

Wenn diese Eigenschaft den Wert true hat, ist das Gerät ein frei gegebenes Gerät.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8"></a>Windows 10, Version 1703, Windows 10, Version 1607, Windows 10, Version 1511, Windows 10, Version 1507, Windows 8.1, Windows 8

```
propertyDescription
   name = System.Devices.IsShared
   shellPKey = PKEY_Devices_IsShared
   formatID = 78C34FC8-104A-4ACA-9EA4-524D52996E57
   propID = 84
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Boolean
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            name = Shared
            value = #TRUE#
            text = Shared
            defineToken = ISSHAREDDEVICE_SHARED
         enum
            name = NotShared
            value = #FALSE#
            text = Not Shared
            defineToken = ISSHAREDDEVICE_NOTSHARED
```

## <a name="windows-7"></a>Windows 7

```
propertyDescription
   name = System.Devices.IsShared
   shellPKey = PKEY_Devices_IsSharedDevice
   formatID = 78C34FC8-104A-4ACA-9EA4-524D52996E57
   propID = 84
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Boolean
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            name = Shared
            value = #TRUE#
            text = Shared
            defineToken = ISSHAREDDEVICE_SHARED
         enum
            name = NotShared
            value = #FALSE#
            text = Not Shared
            defineToken = ISSHAREDDEVICE_NOTSHARED
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

 

 
