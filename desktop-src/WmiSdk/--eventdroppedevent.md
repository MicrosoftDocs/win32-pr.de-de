---
description: Stellt das Vorkommen eines Ereignisses dar, das gelöscht wird. Ein gelöschter Ereignis ist ein Ereignis, das nicht an einen Ereignisconsumer übermittelt wird.
ms.assetid: fae267a9-e0ec-43fa-a3c3-d50345775a1d
ms.tgt_platform: multiple
title: __EventDroppedEvent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventDroppedEvent
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 4e9f68328a3c5c455c98e85a65d53156da6eeada
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363639"
---
# <a name="__eventdroppedevent-class"></a>\_\_Eventdroppedevent-Klasse

Die **\_ \_ eventdroppedevent** -System Klasse stellt das Vorkommen eines gelöschten Ereignisses dar. Ein gelöschter Ereignis ist ein Ereignis, das nicht an einen Ereignisconsumer übermittelt wird.

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

## <a name="syntax"></a>Syntax

``` syntax
class __EventDroppedEvent : __SystemEvent
{
  __Event             Event;
  __EventConsumer REF IntendedConsumer;
  uint8               SECURITY_DESCRIPTOR[];
  uint64              TIME_CREATED;
};
```

## <a name="members"></a>Member

Die **\_ \_ eventdroppedevent** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **\_ \_ eventdroppedevent** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Event**
</dt> <dd> <dl> <dt>

Datentyp: **\_ \_ Ereignis**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Das Ereignis, das gelöscht wird.

</dd> <dt>

**Intendidconsumer**
</dt> <dd> <dl> <dt>

Datentyp: **\_ \_ eventconsumer**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Verweis auf eine Instanz von [**\_ \_ eventconsumer**](--eventconsumer.md) , die den permanenten Consumer darstellt, den Sie für den Empfang eines Ereignisses identifizieren. Andere permanente Consumer, die ein Ereignis abonnieren, können weiterhin das Ereignis empfangen.

</dd> <dt>

**Sicherheits \_ Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Deskriptor, der von einem Ereignis Anbieter verwendet wird, um die Benutzer zu ermitteln, die ein Ereignis empfangen können. Diese Eigenschaft wird von einem [**\_ \_ Ereignis**](--event.md)geerbt.

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

Die **\_ \_ eventdroppedevent** -Klasse wird von System [**\_ \_ Event**](--systemevent.md)abgeleitet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Alle WMI-Namespaces<br/>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_\_System Event**](/windows/desktop/WmiSdk/--systemevent)
</dt> <dt>

[WMI-System Klassen](wmi-system-classes.md)
</dt> </dl>

 

