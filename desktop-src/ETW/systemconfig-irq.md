---
description: Diese Klasse ist die Ereignistyp Klasse für Interrupt Request (UNQ)-Ereignisse. Die folgende Syntax wird durch den MOF-Code vereinfacht.
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
ms.openlocfilehash: e1dd674c34c06259bc343615c17d165be3f57d32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977592"
---
# <a name="systemconfig_irq-class"></a>SystemConfig- \_ Klasse "UNQ"

Diese Klasse ist die Ereignistyp Klasse für Interrupt Request (UNQ)-Ereignisse.

Die folgende Syntax wird durch den MOF-Code vereinfacht.

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

Die **SystemConfig-Klasse " \_ UNQ** " verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **SystemConfig-Klasse " \_ UNQ** " verfügt über diese Eigenschaften.

<dl> <dt>

**DeviceDescription**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (4), stringbeendigung ("nullterminiert"), Format ("w")
</dt> </dl>

Die Beschreibung des Geräts oder der Software, die die Anforderung sendet.

</dd> <dt>

**Devicedescriptionlen**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (3)
</dt> </dl>

Länge in Zeichen der Zeichenfolge in **devicedescription**.

</dd> <dt>

**Unqaffinität**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (1), Format ("x")
</dt> </dl>

UNQ-Affinitäts Maske. Die Affinitäts Maske identifiziert die spezifischen Prozessoren (oder Gruppen von Prozessoren), die die UNQ empfangen können.

</dd> <dt>

**Unqnum**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (2)
</dt> </dl>

Die Zeilennummer der Interrupt-Anforderung.

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

 

 




