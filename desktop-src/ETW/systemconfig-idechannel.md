---
description: Diese Klasse ist die Ereignistypklasse für IDE-Kanalereignisse. Die folgende Syntax wird durch einen MOF-Code vereinfacht.
ms.assetid: 2265a4a6-4377-4aa9-926a-def6e8eda998
title: SystemConfig_IDEChannel-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_IDEChannel
- SystemConfig_IDEChannel.TargetId
- SystemConfig_IDEChannel.DeviceType
- SystemConfig_IDEChannel.DeviceTimingMode
- SystemConfig_IDEChannel.LocationInformationLen
- SystemConfig_IDEChannel.LocationInformation
api_type:
- NA
api_location: ''
ms.openlocfilehash: 8cf764d266d98199e27b40c8690b36183aa82aa2cfb8ded006087ab55f3ddfca
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041600"
---
# <a name="systemconfig_idechannel-class"></a>SystemConfig \_ IDEChannel-Klasse

Diese Klasse ist die Ereignistypklasse für IDE-Kanalereignisse.

Die folgende Syntax wird durch einen MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[EventType(23), EventTypeName("IDEChannel")]
class SystemConfig_IDEChannel : SystemConfig
{
  uint32 TargetId;
  uint32 DeviceType;
  uint32 DeviceTimingMode;
  uint32 LocationInformationLen;
  string LocationInformation;
};
```

## <a name="members"></a>Member

Die **SystemConfig \_ IDEChannel-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **SystemConfig \_ IDEChannel-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**DeviceTimingMode**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(3), Format("x")
</dt> </dl>

Der Modus, in dem die IDE funktionieren könnte. Folgende Werte sind möglich:

-   PIO \_ MODE0 (0x1)
-   PIO \_ MODE1 (0x2)
-   PIO \_ MODE2 (0x4)
-   PIO \_ MODE3 (0x8)
-   PIO \_ MODE4 (0x10)
-   SWDMA \_ MODE0 (0x20)
-   SWDMA \_ MODE1 (0x40)
-   SWDMA \_ MODE2 (0x80)
-   FORMATDMA \_ MODE0 (0x100)
-   MODUS \_ 2 (0x200)
-   MODUS \_ 3 (0x400)
-   UDMA \_ MODE0 (0x800)
-   UDMA \_ MODE1 (0x1000)
-   UDMA \_ MODE2 (0x2000)
-   UDMA \_ MODE3 (0x4000)
-   UDMA \_ MODE4 (0x8000)
-   UDMA \_ MODE5 (0x10000)

</dd> <dt>

**DeviceType**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(2), Format("x")
</dt> </dl>

Der Gerätetyp. Folgende Werte sind möglich:

-   ATA (1)
-   ATAPI (2)

</dd> <dt>

**LocationInformation**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(5), StringTermination("NullTerminated"), Format("w")
</dt> </dl>

Der IDE-Kanal (z. B. Primärer Kanal, sekundärer Kanal und so weiter).

</dd> <dt>

**LocationInformationLen**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(4)
</dt> </dl>

Länge der **LocationInformation-Zeichenfolge.**

</dd> <dt>

**TargetId**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(1)
</dt> </dl>

Der Bezeichner des Datenträgers.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**SystemConfig**](systemconfig.md)
</dt> </dl>

 

 




