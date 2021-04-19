---
description: Stellt ein Klassen Änderungs Ereignis dar, bei dem es sich um einen Typ eines systeminternen Ereignisses handelt, das generiert wird, wenn eine Klasse im Namespace geändert wird.
ms.assetid: 77e8e025-d584-495d-98f8-71e7fb2c9698
ms.tgt_platform: multiple
title: __ClassModificationEvent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ClassModificationEvent
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 3634b632fa9ab66f0da3e48bf77fab5875daf12c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358953"
---
# <a name="__classmodificationevent-class"></a>\_\_Classmodificationevent-Klasse

Die **\_ \_ classmodificationevent** -System Klasse stellt ein Klassen Änderungs Ereignis dar, bei dem es sich um einen Typ eines systeminternen [Ereignisses](determining-the-type-of-event-to-receive.md) handelt, das generiert wird, wenn eine Klasse im-Namespace geändert wird.

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

## <a name="syntax"></a>Syntax

``` syntax
class __ClassModificationEvent : __ClassOperationEvent
{
  object PreviousClass;
  uint8  SECURITY_DESCRIPTOR[];
  object TargetClass;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a>Member

Die **\_ \_ classmodificationevent** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **\_ \_ classmodificationevent** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Previousclass**
</dt> <dd> <dl> <dt>

Datentyp: **Object**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Kopie der ursprünglichen Version der-Klasse.

</dd> <dt>

**Sicherheits \_ Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Deskriptor, der vom Ereignis Anbieter verwendet wird, um zu bestimmen, welche Benutzer das Ereignis empfangen können. Diese Eigenschaft wird von einem [**\_ \_ Ereignis**](--event.md)geerbt.

</dd> <dt>

**Targetclass**
</dt> <dd> <dl> <dt>

Datentyp: **Object**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Kopie der neu geänderten Klasse, die vom Klassen Änderungs Ereignis gemeldet wird. Diese Eigenschaft wird von [**\_ \_ classoperationevent**](--classoperationevent.md)geerbt.

</dd> <dt>

**\_Erstellungszeit**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eindeutiger Wert, der die Uhrzeit angibt, zu der das Ereignis generiert wurde. Dies ist ein 64-Bit-Wert, der die Anzahl der 100-Nanosecond-Intervalle nach dem 1. Januar 1601 darstellt. Die Informationen liegen im UTC-Format (koordiniert Universal Times) vor. Diese Eigenschaft wird von einem [**\_ \_ Ereignis**](--event.md)geerbt.

Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **\_ \_ classmodificationevent** -Klasse wird von [**\_ \_ classoperationevent**](--classoperationevent.md)abgeleitet.

Das Ereignis meldet sowohl die neue als auch die alte Version der Klassendefinition.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Alle WMI-Namespaces<br/>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_\_Classoperationevent**](/windows/desktop/WmiSdk/--classoperationevent)
</dt> <dt>

[WMI-System Klassen](wmi-system-classes.md)
</dt> </dl>

 

