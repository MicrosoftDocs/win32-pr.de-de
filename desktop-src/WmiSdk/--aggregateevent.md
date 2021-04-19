---
description: Stellt ein Aggregat Ereignis aus mehreren einzelnen systeminternen oder extrinsischen Ereignissen dar.
ms.assetid: 99afa390-01fe-4a13-ba21-27587470f111
ms.tgt_platform: multiple
title: __AggregateEvent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __AggregateEvent
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: f93a962e57452ac555214e42f00af8ac8a4ea3db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349652"
---
# <a name="__aggregateevent-class"></a>\_\_Aggregateevent-Klasse

Die **\_ \_ aggregateevent** -System Klasse stellt ein Aggregat Ereignis aus mehreren einzelnen systeminternen oder extrinsischen Ereignissen dar. WMI generiert eine Instanz von **\_ \_ aggregateevent** anstelle eines [**\_ \_ Ereignisses**](--event.md) , wenn sich Consumer bei der [Group within](group-clause.md) -Klausel in der Ereignis Abfrage registrieren.

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

## <a name="syntax"></a>Syntax

``` syntax
class __AggregateEvent : __IndicationRelated
{
  uint32 NumberOfEvents;
  object Representative;
};
```

## <a name="members"></a>Member

Die **\_ \_ aggregateevent** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **\_ \_ aggregateevent** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**NumberOfEvents**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Anzahl der Ereignisse kombiniert, um dieses einzelne Zusammenfassungs Ereignis zu erhalten.

</dd> <dt>

**Representative**
</dt> <dd> <dl> <dt>

Datentyp: **Object**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Kopie eines der Ereignisse, die innerhalb des Aggregations Intervalls übermittelt werden. Wenn ein Consumer z. b. für Registrierungsschlüssel-Änderungs Ereignisse vom Registrierungs Ereignis Anbieter registriert ist, würde der **repräsentative** eine Instanz der **RegistryKeyChangeEvent** -Klasse enthalten.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **\_ \_ aggregateevent** -Klasse wird von " [**\_ \_ indicationrelated**](--indicationrelated.md)" abgeleitet, die keine Eigenschaften hat.

Ereignis Anbieter generieren niemals Aggregat Ereignisse. Die Group within-Klausel muss bei der Verarbeitung von Ereignis Abfragen ignoriert werden.

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

[Abfragen mit WQL](querying-with-wql.md)
</dt> </dl>

 

