---
description: Ist eine Basisklasse für alle systeminternen Ereignisse, die sich auf eine Klasse beziehen.
ms.assetid: 554bbabd-2639-40f5-8786-6df2188db0ec
ms.tgt_platform: multiple
title: __ClassOperationEvent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ClassOperationEvent
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 0c7a78219cec5c014e289dad4bf1cc29f0466a06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366516"
---
# <a name="__classoperationevent-class"></a>\_\_Classoperationevent-Klasse

Die **\_ \_ classoperationevent** -System Klasse ist eine Basisklasse für alle systeminternen Ereignisse, die sich auf eine Klasse beziehen.

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

## <a name="syntax"></a>Syntax

``` syntax
class __ClassOperationEvent : __Event
{
  uint8  SECURITY_DESCRIPTOR[];
  object TargetClass;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a>Member

Die **\_ \_ classoperationevent** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **\_ \_ classoperationevent** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

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

Die Klasse, auf die sich das Ereignis auswirkt. Bei Erstellungs Ereignissen handelt es sich hierbei um die neu erstellte Klasse. Bei Änderungs Ereignissen handelt es sich hierbei um die neue Version der geänderten-Klasse. Bei Lösch Ereignissen handelt es sich hierbei um die gelöschte-Klasse.

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

Die **\_ \_ classoperationevent** -Klasse wird von [**\_ \_ Event**](--event.md)abgeleitet.

Es werden keine Instanzen von **\_ \_ classoperationevent** erstellt; es werden nur Instanzen der Unterklassen erstellt. Die folgenden Klassen werden von **\_ \_ classoperationevent** abgeleitet:

[**\_\_Classcreationevent**](--classcreationevent.md)

[**\_\_Classmodificationevent**](--classmodificationevent.md)

[**\_\_Classdeletionevent**](--classdeletionevent.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Alle WMI-Namespaces<br/>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_\_Ereignis**](/windows/desktop/WmiSdk/--event)
</dt> <dt>

[WMI-System Klassen](wmi-system-classes.md)
</dt> <dt>

[Bestimmen des zu empfangenden Ereignis Typs](determining-the-type-of-event-to-receive.md)
</dt> </dl>

 

