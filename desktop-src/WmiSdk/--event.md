---
description: Eine abstrakte Basisklasse, die als übergeordnete Klasse für alle systeminternen und extrinsischen Ereignisse dient.
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
ms.openlocfilehash: a74abb8a02676ba97ffb7a41df6ee4a3bd7f428d5288e376f85d61927fbb0e06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118821091"
---
# <a name="__event-class"></a>\_\_Ereignisklasse

Die **\_ \_ Ereignissystemklasse** ist eine abstrakte Basisklasse, die als übergeordnete Klasse für alle systeminternen und extrinsischen Ereignisse dient. Alle neuen Ereignistypen müssen letztendlich von **\_ \_ Ereignis** abgeleitet werden. Systeminterne Ereignisse werden direkt von dieser Klasse abgeleitet. Benutzerdefinierte extrinsische Ereignisse leiten sich von einer Unterklasse dieser Klasse namens [**\_ \_ ExtrinsicEvent**](--extrinsicevent.md)ab.

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.

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

Die **\_ \_ Event-Klasse** verfügt über folgende Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **\_ \_ Event-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**\_SICHERHEITSBESCHREIBUNG**
</dt> <dd> <dl> <dt>

Datentyp: **uint8-Array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Deskriptor, den der Ereignisanbieter verwendet, um zu bestimmen, welche Benutzer das Ereignis empfangen können. Weitere Informationen finden Sie unter [WMI-Sicherheitskonstanten.](wmi-security-constants.md)

</dd> <dt>

**TIME \_ CREATED**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eindeutiger Wert, der den Zeitpunkt angibt, zu dem das Ereignis generiert wird. Dies ist ein 64-Bit-Wert, der die Anzahl von 100-Nanosekunden-Intervallen nach dem 1. Januar 1601 darstellt. Die Informationen haben das format koordinierte Weltzeit (UTC).

Weitere Informationen zur Verwendung von **uint64-Werten** in Skripts finden Sie unter [Skripterstellung in WMI.](/windows/desktop/WmiSdk/creating-a-wmi-script)

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **\_ \_ Event-Klasse** wird von [**\_ \_ IndicationRelated**](--indicationrelated.md)abgeleitet, das keine Eigenschaften aufweist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Alle WMI-Namespaces<br/>  |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**\_\_IndicationRelated**](/windows/desktop/WmiSdk/--indicationrelated)
</dt> <dt>

[WMI-Systemklassen](wmi-system-classes.md)
</dt> <dt>

[Bestimmen des Typs des zu empfangenden Ereignisses](determining-the-type-of-event-to-receive.md)
</dt> <dt>

[**\_\_ClassOperationEvent**](--classoperationevent.md)
</dt> <dt>

[**\_\_InstanceOperationEvent**](--instanceoperationevent.md)
</dt> <dt>

[**\_\_NamespaceOperationEvent**](--namespaceoperationevent.md)
</dt> </dl>

 

