---
description: Wenn diese Eigenschaft den Wert true hat, wird das Gerät mit einem Netzwerk verbunden.
ms.assetid: 4d0aa672-1ff8-4fb1-82d2-76553c2b0209
title: System. Devices. isnetworkconnected
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c016b97dc3e966407582e0447ddeae1c4ffb86d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756373"
---
# <a name="systemdevicesisnetworkconnected"></a>System. Devices. isnetworkconnected

Wenn diese Eigenschaft den Wert true hat, wird das Gerät mit einem Netzwerk verbunden.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8"></a>Windows 10, Version 1703, Windows 10, Version 1607, Windows 10, Version 1511, Windows 10, Version 1507, Windows 8.1, Windows 8

```
propertyDescription
   name = System.Devices.IsNetworkConnected
   shellPKey = PKEY_Devices_IsNetworkConnected
   formatID = 78C34FC8-104A-4ACA-9EA4-524D52996E57
   propID = 85
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Boolean
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            name = NetworkConnected
            value = #TRUE#
            text = Network Connected
            defineToken = ISNETWORKDEVICE_NETWORKDEVICE
         enum
            name = NotNetworkConnected
            value = #FALSE#
            text = Not Network Connected
            defineToken = ISNETWORKDEVICE_NOTNETWORKDEVICE
```

## <a name="windows-7"></a>Windows 7

```
propertyDescription
   name = System.Devices.IsNetworkConnected
   shellPKey = PKEY_Devices_IsNetworkDevice
   formatID = 78C34FC8-104A-4ACA-9EA4-524D52996E57
   propID = 85
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Boolean
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            name = NetworkConnected
            value = #TRUE#
            text = Network Connected
            defineToken = ISNETWORKDEVICE_NETWORKDEVICE
         enum
            name = NotNetworkConnected
            value = #FALSE#
            text = Not Network Connected
            defineToken = ISNETWORKDEVICE_NOTNETWORKDEVICE
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

 

 
