---
description: Verbleibende Akku Lebensdauer in Prozent.
ms.assetid: b6f4f5d6-7f12-4104-95ad-b163445d198b
title: System.Devices.Batterylife
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe8f24f5ecaa78231fdc463b718046adc42fc681
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368928"
---
# <a name="systemdevicesbatterylife"></a>System.Devices.Batterylife

Verbleibende Akku Lebensdauer in Prozent.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a>Windows 10, Version 1703, Windows 10, Version 1607, Windows 10, Version 1511, Windows 10, Version 1507, Windows 8.1, Windows 8, Windows 7

```
propertyDescription
   name = System.Devices.BatteryLife
   shellPKey = PKEY_Devices_BatteryLife
   formatID = 49CD1F76-5626-4B17-A4E8-18B4AA1A2213
   propID = 10
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Byte
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enumRange
            name = CriticallyLow
            minValue = 0
            setValue = 5
            text = Critically low battery
            defineToken = BATTERYLIFE_CRITICALLY_LOW
         enumRange
            name = Low
            minValue = 11
            setValue = 18
            text = Low battery
            defineToken = BATTERYLIFE_LOW
         enumRange
            name = Average
            minValue = 26
            setValue = 60
            text = Average battery
            defineToken = BATTERYLIFE_AVERAGE
         enumRange
            name = Full
            minValue = 90
            setValue = 95
            text = Full battery
            defineToken = BATTERYLIFE_FULL
         enumRange
            name = UnknownStatus
            minValue = 101
            setValue = 101
            text = Unknown battery status
            defineToken = BATTERYLIFE_UNKNOWN_STATUS
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

 

 
