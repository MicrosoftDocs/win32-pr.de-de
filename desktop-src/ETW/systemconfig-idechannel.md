---
description: Diese Klasse ist die Ereignistyp Klasse für IDE-Kanal Ereignisse. Die folgende Syntax wird durch den MOF-Code vereinfacht.
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
ms.openlocfilehash: 60cdfcec8f62e6fb96dcedc895d874f01a209430
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526381"
---
# <a name="systemconfig_idechannel-class"></a>SystemConfig- \_ idechannel-Klasse

Diese Klasse ist die Ereignistyp Klasse für IDE-Kanal Ereignisse.

Die folgende Syntax wird durch den MOF-Code vereinfacht.

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

Die **\_ idechannel** -Klasse von SystemConfig verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **\_ idechannel** -Klasse von SystemConfig verfügt über diese Eigenschaften.

<dl> <dt>

**Devicetimingmode**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (3), Format ("x")
</dt> </dl>

Der Modus, in dem die IDE funktionieren könnte. Folgende Werte sind möglich:

-   Pio \_ MODE0 (0x1)
-   Pio \_ MODE1 (0x2)
-   Pio \_ Mode2 (0x4)
-   Pio \_ MODE3 (0x8)
-   Pio \_ MODE4 (0x10)
-   Swap- \_ MODE0 (0x20)
-   MODE1-Datei \_ (0x40)
-   Swap- \_ Mode2 (0x80)
-   Mwdma \_ MODE0 (0x100)
-   Mwdma \_ Mode2 (0x200)
-   Mwdma \_ MODE3 (0x400)
-   UDMA \_ MODE0 (0x800)
-   UDMA \_ MODE1 (0x1000)
-   UDMA \_ Mode2 (0x2000)
-   UDMA \_ MODE3 (0x4000)
-   UDMA \_ MODE4 (0X8000)
-   UDMA \_ MODE5 (0x10000)

</dd> <dt>

**DeviceType**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (2), Format ("x")
</dt> </dl>

Der Gerätetyp. Folgende Werte sind möglich:

-   ATA (1)
-   ATAPI (2)

</dd> <dt>

**Locationinformation**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (5), stringbeendigung ("nullterminiert"), Format ("w")
</dt> </dl>

Der IDE-Kanal (z. b. primärer Kanal, sekundärer Kanal usw.).

</dd> <dt>

**Locationinformationlen**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (4)
</dt> </dl>

Länge der **locationinformation** -Zeichenfolge.

</dd> <dt>

**TargetId**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (1)
</dt> </dl>

Der Bezeichner des Datenträgers.

</dd> </dl>

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**SystemConfig**](systemconfig.md)
</dt> </dl>

 

 




