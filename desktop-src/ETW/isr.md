---
description: Diese Klasse ist die Ereignistypklasse für ISR-Ereignisse (Interrupt Service Routine). Die folgende Syntax wird durch einen MOF-Code vereinfacht.
ms.assetid: 2c7ccace-3384-43f4-905e-e7eeeee6f87b
title: ISR-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISR
- ISR.InitialTime
- ISR.Routine
- ISR.ReturnValue
- ISR.Vector
- ISR.Reserved
api_type:
- NA
api_location: ''
ms.openlocfilehash: 621bf9c97aef9ea23fba6186a419f7c205d98fba608c2539702607986de0d258
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119901000"
---
# <a name="isr-class"></a>ISR-Klasse

Diese Klasse ist die Ereignistypklasse für ISR-Ereignisse (Interrupt Service Routine).

Die folgende Syntax wird durch einen MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[EventType{67}, EventTypeName{"ISR"}]
class ISR : PerfInfo
{
  object InitialTime;
  uint32 Routine;
  uint8  ReturnValue;
  uint8  Vector;
  uint16 Reserved;
};
```

## <a name="members"></a>Member

Die **ISR-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **ISR-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**InitialTime**
</dt> <dd> <dl> <dt>

Datentyp: **Objekt**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(1), Extension("WmiTime")
</dt> </dl>

ISR-Einstiegszeit.

</dd> <dt>

**Reserved**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(5), Zeiger
</dt> </dl>

Reserviert.

</dd> <dt>

**ReturnValue**
</dt> <dd> <dl> <dt>

Datentyp: **uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(3)
</dt> </dl>

Boolescher Wert, der angibt, ob der Interrupt beansprucht wurde (ist TRUE, wenn der Interrupt beansprucht wurde).

</dd> <dt>

**-Routine zurückgegebener Wert**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(2), Zeiger
</dt> </dl>

Adresse der ISR-Routine. Verwenden Sie die Adresse mit den Imageereignissen, um zu suchen, welches Image gestartet wurde.

</dd> <dt>

**Vektor**
</dt> <dd> <dl> <dt>

Datentyp: **uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(4)
</dt> </dl>

Vektor aus interrupt-Deskriptortabelle, der ISR-Routine zugewiesen ist.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

 




