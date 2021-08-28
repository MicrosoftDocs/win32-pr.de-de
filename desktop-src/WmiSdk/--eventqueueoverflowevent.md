---
description: Meldet, wenn ein Ereignis als Folge eines Überlaufs der Übermittlungswarteschlange gelöscht wird.
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
ms.openlocfilehash: 6fd31df9f84883c8b677ea4fef0431ed762b4cec2155cb3d600893a40e3e1d9f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119612630"
---
# <a name="__eventqueueoverflowevent-class"></a>\_\_EventQueueOverflowEvent-Klasse

Die **\_ \_ Systemklasse EventQueueOverflowEvent** meldet, wenn ein Ereignis als Folge eines Überlaufs der Übermittlungswarteschlange gelöscht wird.

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.

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

Die **\_ \_ EventQueueOverflowEvent-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **\_ \_ EventQueueOverflowEvent-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**CurrentQueueSize**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Aktuelle Warteschlangengröße in Bytes. Diese Eigenschaft beträgt standardmäßig 10 MB für alle kombinierten Warteschlangen.

</dd> <dt>

**Event**
</dt> <dd> <dl> <dt>

Datentyp: **Objekt**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ereignis von Interesse. Diese Eigenschaft wird von [**\_ \_ EventDroppedEvent geerbt.**](--eventdroppedevent.md)

</dd> <dt>

**IntendedConsumer**
</dt> <dd> <dl> <dt>

Datentyp: **\_ \_ EventConsumer**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Verweis auf den beabsichtigten Consumer. Diese Eigenschaft wird von [**\_ \_ EventDroppedEvent geerbt.**](--eventdroppedevent.md)

</dd> <dt>

**\_SICHERHEITSDESKRIPTOR**
</dt> <dd> <dl> <dt>

Datentyp: **uint8 array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Deskriptor, der vom Ereignisanbieter verwendet wird, um zu bestimmen, welche Benutzer das Ereignis empfangen können. Diese Eigenschaft wird vom Ereignis [**\_ \_ geerbt.**](--event.md)

</dd> <dt>

**ZEIT \_ ERSTELLT**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eindeutiger Wert, der den Zeitpunkt angibt, zu dem das Ereignis generiert wurde. Dies ist ein 64-Bit-Wert, der die Anzahl von 100-Nanosekunden-Intervallen nach dem 1. Januar 1601 darstellt. Die Informationen haben das format koordinierte Weltzeit (UTC). Diese Eigenschaft wird vom Ereignis [**\_ \_ geerbt.**](--event.md)

Weitere Informationen zur Verwendung von **uint64-Werten** in Skripts finden Sie unter [Skripterstellung in WMI.](/windows/desktop/WmiSdk/creating-a-wmi-script)

</dd> </dl>

## <a name="remarks"></a>Hinweise

Nur Benutzer mit Administratorrechten können dieses Ereignis empfangen. Die **\_ \_ EventQueueOverflowEvent-Klasse** wird von [**\_ \_ EventDroppedEvent abgeleitet.**](--eventdroppedevent.md)

Weitere Informationen finden Sie unter [**der MaximumQueueSize-Eigenschaft**](--eventconsumer.md) in der [**\_ \_ EventConsumer-Klasse**](--eventconsumer.md) und der [**HighThresholdOnEvents-Eigenschaft**](/windows/desktop/CIMWin32Prov/win32-wmisetting) in der **Win32 \_ WMISetting-Klasse.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Alle WMI-Namespaces<br/>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_\_EventDroppedEvent**](/windows/desktop/WmiSdk/--eventdroppedevent)
</dt> <dt>

[WMI-Systemklassen](wmi-system-classes.md)
</dt> </dl>

 

