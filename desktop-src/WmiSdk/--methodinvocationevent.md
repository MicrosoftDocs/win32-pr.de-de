---
description: Die \_ \_ methodinvocationevent-System Klasse ist definiert, aber nicht implementiert.
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
ms.openlocfilehash: bc7e8d70d027caf31a90d49abc490c2de2d52fb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217136"
---
# <a name="__methodinvocationevent-class"></a>\_\_Methodinvocationevent-Klasse

Die **\_ \_ methodinvocationevent** -System Klasse ist definiert, aber nicht implementiert.

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

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

Die **\_ \_ methodinvocationevent** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **\_ \_ methodinvocationevent** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Methode**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Methode, die aufgerufen wird, um das Ereignis zu initiieren.

</dd> <dt>

**Parameter**
</dt> <dd> <dl> <dt>

Datentyp: **\_ \_ Parameter**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Verweis auf eine-Instanz, die die Eingabe-und Ausgabeparameter des Methoden Aufrufes darstellt.

</dd> <dt>

**Precallup**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

**True** gibt an, dass das-Ereignis ausgelöst wird, bevor die-Methode aufgerufen wird.

</dd> <dt>

**Sicherheits \_ Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Deskriptor, der vom Ereignis Anbieter verwendet wird, um zu bestimmen, welche Benutzer das Ereignis empfangen können. Diese Eigenschaft wird von einem [**\_ \_ Ereignis**](--event.md)geerbt. Weitere Informationen finden Sie unter [Sicherheits Deskriptoren](/windows/desktop/SecAuthZ/security-descriptors).

</dd> <dt>

**TargetInstance**
</dt> <dd> <dl> <dt>

Datentyp: **Object**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Instanz, für die die Methode aufgerufen wird. Diese Eigenschaft wird von [**\_ \_ instanceoperationevent**](--instanceoperationevent.md)geerbt.

</dd> <dt>

**\_Erstellungszeit**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eindeutiger Wert, der die Uhrzeit angibt, zu der ein Ereignis generiert wird. Dies ist ein 64-Bit-Wert, der die Anzahl der 100-Nanosecond-Intervalle nach dem 1. Januar 1601 darstellt. Die Informationen liegen im UTC-Format (koordinierte Weltzeit) vor. Diese Eigenschaft wird von einem [**\_ \_ Ereignis**](--event.md)geerbt.

Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **\_ \_ methodinvocationevent** -Klasse wird von [**\_ \_ instanceoperationevent**](--instanceoperationevent.md)abgeleitet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Alle WMI-Namespaces<br/>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_\_Instanceoperationevent**](/windows/desktop/WmiSdk/--instanceoperationevent)
</dt> <dt>

[WMI-System Klassen](wmi-system-classes.md)
</dt> </dl>

 

