---
description: 'SystemConfig_V0_Power-Klasse: Diese Klasse ist die Ereignistypklasse für Energiekonfigurationsereignisse. Die folgende Syntax wird aus MOF-Code vereinfacht.'
ms.assetid: b3391435-dac0-4c48-b788-eb4d4a7aa635
title: SystemConfig_V0_Power-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_V0_Power
- SystemConfig_V0_Power.s1
- SystemConfig_V0_Power.s2
- SystemConfig_V0_Power.s3
- SystemConfig_V0_Power.s4
- SystemConfig_V0_Power.s5
- SystemConfig_V0_Power.Pad1
- SystemConfig_V0_Power.Pad2
- SystemConfig_V0_Power.Pad3
api_type:
- NA
api_location: ''
ms.openlocfilehash: ab268e719374906e149dc9c1b733487f986e8308
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105938"
---
# <a name="systemconfig_v0_power-class"></a>SystemConfig \_ V0 \_ Power-Klasse

Diese Klasse ist die Ereignistypklasse für Energiekonfigurationsereignisse.

Die folgende Syntax wird aus MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[EventType(16), EventTypeName("Power")]
class SystemConfig_V0_Power : SystemConfig_V0
{
  boolean s1;
  boolean s2;
  boolean s3;
  boolean s4;
  boolean s5;
  uint8   Pad1;
  uint8   Pad2;
  uint8   Pad3;
};
```

## <a name="members"></a>Member

Die **SystemConfig \_ V0 \_ Power-Klasse** verfügt über folgende Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **SystemConfig \_ V0 \_ Power-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

Pad1
</dt> <dd> <dl> <dt>

Datentyp: **uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(6)
</dt> </dl>

Reserviert.

</dd> <dt>

Pad2
</dt> <dd> <dl> <dt>

Datentyp: **uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(7)
</dt> </dl>

Reserviert.

</dd> <dt>

Pad3
</dt> <dd> <dl> <dt>

Datentyp: **uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(8)
</dt> </dl>

Reserviert.

</dd> <dt>

s1
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(1)
</dt> </dl>

True gibt an, dass das System den Standbyzustand S1 unterstützt.

</dd> <dt>

s2
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(2)
</dt> </dl>

True gibt an, dass das System den Ruhezustand S2 unterstützt.

</dd> <dt>

s3
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(3)
</dt> </dl>

True gibt an, dass das System den Ruhezustand S3 unterstützt.

</dd> <dt>

s4
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(4)
</dt> </dl>

True gibt an, dass das System den Ruhezustand S4 unterstützt.

</dd> <dt>

s5
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(5)
</dt> </dl>

True gibt an, dass das System den Ruhezustand S5 unterstützt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2003-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**SystemConfig \_ V0**](systemconfig-v0.md)
</dt> </dl>

 

 




