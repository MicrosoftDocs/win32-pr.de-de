---
description: Ist eine abstrakte Basisklasse, die als übergeordnete Klasse für alle systeminternen und extrinsischen Ereignisse fungiert.
ms.assetid: 4d2e4715-041c-49e9-b948-a148dfe85483
ms.tgt_platform: multiple
title: __Event-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __Event
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 39a032b3f082ed64ba7999d20366b89e8b3890c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357091"
---
# <a name="__event-class"></a>\_\_Ereignisklasse

**\_ \_ Bei der Ereignis** System Klasse handelt es sich um eine abstrakte Basisklasse, die als übergeordnete Klasse für alle systeminternen und extrinsischen Ereignisse fungiert. Alle neuen Ereignis Typen müssen letztendlich vom **\_ \_ Ereignis** abgeleitet werden. Systeminterne Ereignisse werden direkt von dieser Klasse abgeleitet. Benutzerdefinierte System externe-Ereignisse werden von einer Unterklasse dieser Klasse mit dem Namen " [**\_ \_ ExtrinsicEvent**](--extrinsicevent.md)" abgeleitet.

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

## <a name="syntax"></a>Syntax

``` syntax
[abstract]
class __Event : __IndicationRelated
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
};
```

## <a name="members"></a>Member

Die- **\_ \_ Ereignis** Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die- **\_ \_ Ereignis** Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Sicherheits \_ Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Deskriptor, den der Ereignis Anbieter verwendet, um zu bestimmen, welche Benutzer das Ereignis empfangen können. Weitere Informationen finden Sie unter [WMI-Sicherheits Konstanten](wmi-security-constants.md).

</dd> <dt>

**\_Erstellungszeit**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eindeutiger Wert, der die Uhrzeit angibt, zu der das Ereignis generiert wird. Dies ist ein 64-Bit-Wert, der die Anzahl der 100-Nanosecond-Intervalle nach dem 1. Januar 1601 darstellt. Die Informationen liegen im UTC-Format (koordinierte Weltzeit) vor.

Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **\_ \_ Ereignis** Klasse wird von " [**\_ \_ indicationrelated**](--indicationrelated.md)" abgeleitet, die keine Eigenschaften hat.

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

[Bestimmen des zu empfangenden Ereignis Typs](determining-the-type-of-event-to-receive.md)
</dt> <dt>

[**\_\_Classoperationevent**](--classoperationevent.md)
</dt> <dt>

[**\_\_Instanceoperationevent**](--instanceoperationevent.md)
</dt> <dt>

[**\_\_Namespaceoperationevent**](--namespaceoperationevent.md)
</dt> </dl>

 

