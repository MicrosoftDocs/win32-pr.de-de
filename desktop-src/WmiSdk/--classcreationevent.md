---
description: Stellt ein Klassenerstellungsereignis dar, bei dem es sich um einen Typ systeminterner Ereignisse handelt, der generiert wird, wenn dem Namespace eine neue Klasse hinzugefügt wird.
ms.assetid: a946a8eb-498c-4104-b80f-e520b0e62e36
ms.tgt_platform: multiple
title: __ClassCreationEvent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ClassCreationEvent
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: e420d9dad948b9bd8ebd0c6670b850b3a2f9d5f578ca36a25a986081a1c454a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118110697"
---
# <a name="__classcreationevent-class"></a>\_\_ClassCreationEvent-Klasse

Die **\_ \_ ClassCreationEvent-Systemklasse** stellt ein Klassenerstellungsereignis [](determining-the-type-of-event-to-receive.md) dar, bei dem es sich um einen Typ systeminterner Ereignisse handelt, der generiert wird, wenn dem Namespace eine neue Klasse hinzugefügt wird.

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.

## <a name="syntax"></a>Syntax

``` syntax
class __ClassCreationEvent : __ClassOperationEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  object TargetClass;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a>Member

Die **\_ \_ ClassCreationEvent-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **\_ \_ ClassCreationEvent-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**\_SICHERHEITSDESKRIPTOR**
</dt> <dd> <dl> <dt>

Datentyp: **uint8 array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Deskriptor, der vom Ereignisanbieter verwendet wird, um zu bestimmen, welche Benutzer das Ereignis empfangen können. Diese Eigenschaft wird vom Ereignis [**\_ \_ geerbt.**](--event.md)

</dd> <dt>

**TargetClass**
</dt> <dd> <dl> <dt>

Datentyp: **Objekt**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Kopie der neu erstellten Klasse, die vom Klassenerstellungsereignis gemeldet wird. Diese Eigenschaft wird von [**\_ \_ ClassOperationEvent geerbt.**](--classoperationevent.md)

</dd> <dt>

**ZEIT \_ ERSTELLT**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eindeutiger Wert, der den Zeitpunkt angibt, zu dem das Ereignis generiert wurde. Dies ist ein 64-Bit-Wert, der die Anzahl von 100-Nanosekunden-Intervallen nach dem 1. Januar 1601 darstellt. Die Informationen sind im UTC-Format (Universal Time Coordinates) angegeben. Diese Eigenschaft wird vom Ereignis [**\_ \_ geerbt.**](--event.md)

Weitere Informationen zur Verwendung von **uint64-Werten** in Skripts finden Sie unter [Skripterstellung in WMI.](/windows/desktop/WmiSdk/creating-a-wmi-script)

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **\_ \_ ClassCreationEvent-Klasse** wird von [**\_ \_ ClassOperationEvent abgeleitet.**](--classoperationevent.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Alle WMI-Namespaces<br/>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_\_ClassOperationEvent**](/windows/desktop/WmiSdk/--classoperationevent)
</dt> <dt>

[WMI-Systemklassen](wmi-system-classes.md)
</dt> </dl>

 

