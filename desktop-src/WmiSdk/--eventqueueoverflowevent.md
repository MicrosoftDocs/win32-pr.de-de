---
description: Meldet, wenn ein Ereignis aufgrund eines Überlaufs der Übermittlungs Warteschlange gelöscht wird.
ms.assetid: 7cb1ef3b-3b0a-4f72-96de-862022fd6db8
ms.tgt_platform: multiple
title: __EventQueueOverflowEvent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventQueueOverflowEvent
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 058b03b8a3311aad805f47a04d20e9f1fa8c2477
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362918"
---
# <a name="__eventqueueoverflowevent-class"></a>\_\_Eventqueueoverflowevent-Klasse

Die **\_ \_ eventqueueoverflowevent** -System Klasse meldet, wenn ein Ereignis aufgrund eines Überlaufs der Übermittlungs Warteschlange gelöscht wird.

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

## <a name="syntax"></a>Syntax

``` syntax
class __EventQueueOverflowEvent : __EventDroppedEvent
{
  uint32              CurrentQueueSize;
  object              Event;
  __EventConsumer REF IntendedConsumer;
  uint8               SECURITY_DESCRIPTOR[];
  uint64              TIME_CREATED;
};
```

## <a name="members"></a>Member

Die **\_ \_ eventqueueoverflowevent** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **\_ \_ eventqueueoverflowevent** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Currentqueuesize**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Aktuelle Warteschlangen Größe in Bytes. Diese Eigenschaft ist standardmäßig auf 10 MB für alle Warteschlangen zusammengefasst.

</dd> <dt>

**Event**
</dt> <dd> <dl> <dt>

Datentyp: **Object**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Interessantes Ereignis. Diese Eigenschaft wird von [**\_ \_ eventdroppedevent**](--eventdroppedevent.md)geerbt.

</dd> <dt>

**Intendidconsumer**
</dt> <dd> <dl> <dt>

Datentyp: **\_ \_ eventconsumer**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Verweis auf den gewünschten Consumer. Diese Eigenschaft wird von [**\_ \_ eventdroppedevent**](--eventdroppedevent.md)geerbt.

</dd> <dt>

**Sicherheits \_ Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Deskriptor, der vom Ereignis Anbieter verwendet wird, um zu bestimmen, welche Benutzer das Ereignis empfangen können. Diese Eigenschaft wird von einem [**\_ \_ Ereignis**](--event.md)geerbt.

</dd> <dt>

**\_Erstellungszeit**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eindeutiger Wert, der die Uhrzeit angibt, zu der das Ereignis generiert wurde. Dies ist ein 64-Bit-Wert, der die Anzahl der 100-Nanosecond-Intervalle nach dem 1. Januar 1601 darstellt. Die Informationen liegen im UTC-Format (koordinierte Weltzeit) vor. Diese Eigenschaft wird von einem [**\_ \_ Ereignis**](--event.md)geerbt.

Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Nur Benutzer mit Administratorrechten können dieses Ereignis empfangen. Die **\_ \_ eventqueueoverflowevent** -Klasse wird von [**\_ \_ eventdroppedevent**](--eventdroppedevent.md)abgeleitet.

Weitere Informationen finden Sie in der Eigenschaft " [**MaximumQueueSize**](--eventconsumer.md) " in der [**\_ \_ eventconsumer**](--eventconsumer.md) -Klasse und in der Eigenschaft " [**highprocessoldonevents**](/windows/desktop/CIMWin32Prov/win32-wmisetting) " in der **Win32- \_ wmisetting** -Klasse.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Alle WMI-Namespaces<br/>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_\_Eventdroppedevent**](/windows/desktop/WmiSdk/--eventdroppedevent)
</dt> <dt>

[WMI-System Klassen](wmi-system-classes.md)
</dt> </dl>

 

