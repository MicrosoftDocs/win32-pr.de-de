---
description: Diese Klasse ist die Ereignistypklasse für INTERRUPT-Anforderungsereignisse (IRQ). Die folgende Syntax wird durch einen MOF-Code vereinfacht.
ms.assetid: 9d4692e8-f19f-478c-a003-396722e426c3
title: SystemConfig_IRQ-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_IRQ
- SystemConfig_IRQ.IRQAffinity
- SystemConfig_IRQ.IRQNum
- SystemConfig_IRQ.DeviceDescriptionLen
- SystemConfig_IRQ.DeviceDescription
api_type:
- NA
api_location: ''
ms.openlocfilehash: 3da720de11aa7dbbd759131a521e44e546b7cad6d2525565c81d0aa6920dd0ac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078290"
---
# <a name="systemconfig_irq-class"></a>SystemConfig \_ IRQ-Klasse

Diese Klasse ist die Ereignistypklasse für INTERRUPT-Anforderungsereignisse (IRQ).

Die folgende Syntax wird durch einen MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[EventType(21), EventTypeName("IRQ")]
class SystemConfig_IRQ : SystemConfig
{
  uint64 IRQAffinity;
  uint32 IRQNum;
  uint32 DeviceDescriptionLen;
  string DeviceDescription;
};
```

## <a name="members"></a>Member

Die **SystemConfig \_ IRQ-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **SystemConfig \_ IRQ-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**DeviceDescription**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(4), StringTermination("NullTerminated"), Format("w")
</dt> </dl>

Beschreibung des Geräts oder der Software, von dem die Anforderung gestellt wird.

</dd> <dt>

**DeviceDescriptionLen**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(3)
</dt> </dl>

Länge der Zeichenfolge in **DeviceDescription** in Zeichen.

</dd> <dt>

**IRQAffinity**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(1), Format("x")
</dt> </dl>

IRQ-Affinitätsmaske. Die Affinitätsmaske identifiziert die spezifischen Prozessoren (oder Prozessorgruppen), die den IRQ empfangen können.

</dd> <dt>

**IRQNum**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(2)
</dt> </dl>

Nummer der Interruptanforderungszeile.

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

 

 




