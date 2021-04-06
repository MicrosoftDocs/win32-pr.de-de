---
description: Eine abstrakte Basisklasse, die bei der Registrierung eines permanenten Ereignisconsumers verwendet wird.
ms.assetid: c1dc9a91-76f9-4527-ad69-0323a9aef28a
ms.tgt_platform: multiple
title: __EventConsumer-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventConsumer
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: b8478b76aebf293d562129d047330f33e52706b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960896"
---
# <a name="__eventconsumer-class"></a>\_\_Eventconsumer-Klasse

Die eventconsumer-System Klasse ist eine abstrakte Basisklasse, die bei der Registrierung eines permanenten **\_ \_ Ereignisconsumers** verwendet wird. Sie können eine neue **\_ \_ ereignisconsumerklasse von eventconsumer** ableiten.

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

## <a name="syntax"></a>Syntax

``` syntax
[abstract]
class __EventConsumer : __IndicationRelated
{
  uint8  CreatorSID[];
  string MachineName;
  uint32 MaximumQueueSize;
};
```

## <a name="members"></a>Member

Die **\_ \_ eventconsumer** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **\_ \_ eventconsumer** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**"Kreatorsid"**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Sicherheits-ID (SID), die den Benutzer, der einen Filter erstellt, eindeutig identifiziert. WMI speichert die SID des Benutzers, der eine Instanz von **\_ \_ eventconsumer** oder die Administrator-SID erstellt, je nach Betriebssystem. Weitere Informationen finden Sie unter [Binden eines Ereignis Filters mit einem logischen Consumer](binding-an-event-filter-with-a-logical-consumer.md) und über [wachen und reagieren auf Ereignisse mit Standard](monitoring-and-responding-to-events-with-standard-consumers.md)Consumern.

</dd> <dt>

**MachineName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name des Computers, an den Windows-Verwaltungsinstrumentation (WMI) Ereignisse sendet.

</dd> <dt>

**MaximumQueueSize**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Maximale Warteschlange für einen bestimmten Consumer in Bytes.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **\_ \_ eventconsumer** -Klasse wird von " [**\_ \_ indicationrelated**](--indicationrelated.md)" abgeleitet, die keine Eigenschaften hat.

Permanente Consumer definieren neue Consumerklassen, um eine Aktion zu beschreiben, die ausgeführt werden soll, und Daten, die verarbeitet werden sollen, wenn Consumer Ereignis Benachrichtigungen empfangen. Permanente Consumer haben besondere Sicherheitsbedenken. Weitere Informationen finden Sie unter [Sichern von WMI-Ereignissen](securing-wmi-events.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Alle WMI-Namespaces<br/>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_\_Indicationrelated**](/windows/desktop/WmiSdk/--indicationrelated)
</dt> <dt>

[WMI-System Klassen](wmi-system-classes.md)
</dt> <dt>

[Empfangen von Ereignissen zu allen Zeitpunkten](receiving-events-at-all-times.md)
</dt> <dt>

[Erstellen einer neuen permanenten ereignisconsumerklasse](creating-a-new-permanent-event-consumer-class.md)
</dt> <dt>

[Erstellen eines logischen Consumers](creating-a-logical-consumer.md)
</dt> <dt>

[Sichern von WMI-Ereignissen](securing-wmi-events.md)
</dt> </dl>

 

