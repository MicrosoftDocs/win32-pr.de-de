---
description: Die \_ \_ MethodInvocationEvent-Systemklasse ist definiert, aber nicht implementiert.
ms.assetid: ea736e44-a6bc-41e5-abc5-9e21a5504f44
ms.tgt_platform: multiple
title: __MethodInvocationEvent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __MethodInvocationEvent
- All
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 4cd30e1865ab807f095dbe8a94fa59424131a087360e565207cdeb2d1977ca90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118821135"
---
# <a name="__methodinvocationevent-class"></a>\_\_MethodInvocationEvent-Klasse

Die **\_ \_ MethodInvocationEvent-Systemklasse** ist definiert, aber nicht implementiert.

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.

## <a name="syntax"></a>Syntax

``` syntax
class __MethodInvocationEvent : __InstanceOperationEvent
{
  string       Method;
  __Parameters Parameters;
  boolean      PreCall;
  uint8        SECURITY_DESCRIPTOR[];
  object       TargetInstance;
  uint64       TIME_CREATED;
};
```

## <a name="members"></a>Member

Die **\_ \_ MethodInvocationEvent-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **\_ \_ MethodInvocationEvent-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Methode**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Methode, die aufgerufen wird, um das Ereignis auszulösen.

</dd> <dt>

**Parameter**
</dt> <dd> <dl> <dt>

Datentyp: **\_ \_ Parameter**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Verweis auf eine -Instanz, die die Eingabe- und Ausgabeparameter des Methodenaufrufs darstellt.

</dd> <dt>

**PreCall**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

True **gibt an,** dass das -Ereignis ausgelöst wird, bevor die -Methode aufgerufen wird.

</dd> <dt>

**\_SICHERHEITSDESKRIPTOR**
</dt> <dd> <dl> <dt>

Datentyp: **uint8 array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Deskriptor, der vom Ereignisanbieter verwendet wird, um zu bestimmen, welche Benutzer das Ereignis empfangen können. Diese Eigenschaft wird vom Ereignis [**\_ \_ geerbt.**](--event.md) Weitere Informationen finden Sie unter [Sicherheitsdeskriptoren.](/windows/desktop/SecAuthZ/security-descriptors)

</dd> <dt>

**TargetInstance**
</dt> <dd> <dl> <dt>

Datentyp: **Objekt**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Instanz, für die die Methode aufgerufen wird. Diese Eigenschaft wird von [**\_ \_ InstanceOperationEvent geerbt.**](--instanceoperationevent.md)

</dd> <dt>

**ZEIT \_ ERSTELLT**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eindeutiger Wert, der den Zeitpunkt angibt, zu dem ein Ereignis generiert wird. Dies ist ein 64-Bit-Wert, der die Anzahl von 100-Nanosekunden-Intervallen nach dem 1. Januar 1601 darstellt. Die Informationen haben das format koordinierte Weltzeit (UTC). Diese Eigenschaft wird vom Ereignis [**\_ \_ geerbt.**](--event.md)

Weitere Informationen zur Verwendung von **uint64-Werten** in Skripts finden Sie unter [Skripterstellung in WMI.](/windows/desktop/WmiSdk/creating-a-wmi-script)

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **\_ \_ MethodInvocationEvent-Klasse** wird von [**\_ \_ InstanceOperationEvent abgeleitet.**](--instanceoperationevent.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Alle WMI-Namespaces<br/>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_\_InstanceOperationEvent**](/windows/desktop/WmiSdk/--instanceoperationevent)
</dt> <dt>

[WMI-Systemklassen](wmi-system-classes.md)
</dt> </dl>

 

