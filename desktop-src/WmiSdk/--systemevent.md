---
description: Stellt ein Systemereignis dar.
ms.assetid: 84099483-03e4-4c21-b680-f0975b18c1f6
ms.tgt_platform: multiple
title: __SystemEvent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemEvent
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 445b84e8b692283693c0849c43f603678cdbabde8fc6c313c4da973e3921a4e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118110167"
---
# <a name="__systemevent-class"></a>\_\_SystemEvent-Klasse

Die **\_ \_ Systemklasse SystemEvent** stellt ein Systemereignis dar.

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.

## <a name="syntax"></a>Syntax

``` syntax
class __SystemEvent : __ExtrinsicEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
};
```

## <a name="members"></a>Member

Die **\_ \_ SystemEvent-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **\_ \_ SystemEvent-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**\_SICHERHEITSDESKRIPTOR**
</dt> <dd> <dl> <dt>

Datentyp: **uint8 array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Deskriptor, der vom Ereignisanbieter verwendet wird, um zu bestimmen, welche Benutzer das Ereignis empfangen können. Diese Eigenschaft wird vom Ereignis [**\_ \_ geerbt.**](--event.md)

> [!Note]  
> Eine  NULL Access Control Liste (ACL) im [**SECURITY \_ DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) gewährt jedem die ganze Zeit unbegrenzten Zugriff. Weitere Informationen finden Sie unter [Erstellen eines Sicherheitsdeskriptors für ein neues Objekt.](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--)

 

</dd> <dt>

**ZEIT \_ ERSTELLT**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eindeutiger Wert, der den Zeitpunkt angibt, zu dem das Ereignis generiert wurde. Dies ist ein 64-Bit-Wert, der die Anzahl von 100-Nanosekunden-Intervallen nach dem 1. Januar 1601 darstellt. Die Informationen sind im UTC-Format (Coordinated Universal Times) angegeben. Diese Eigenschaft wird vom Ereignis [**\_ \_ geerbt.**](--event.md)

Weitere Informationen zur Verwendung von **uint64-Werten** in Skripts finden Sie unter [Skripterstellung in WMI.](/windows/desktop/WmiSdk/creating-a-wmi-script)

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **\_ \_ SystemEvent-Klasse** wird von der [**\_ \_ ExtrinsicEvent-Klasse**](--extrinsicevent.md) abgeleitet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Alle WMI-Namespaces<br/>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_\_ExtrinsicEvent**](/windows/desktop/WmiSdk/--extrinsicevent)
</dt> <dt>

[WMI-Systemklassen](wmi-system-classes.md)
</dt> </dl>

 

