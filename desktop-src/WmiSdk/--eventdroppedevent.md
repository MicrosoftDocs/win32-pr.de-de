---
description: Stellt das Auftreten eines Ereignisses dar, das gelöscht wird. Ein gelöschtes Ereignis ist ein Ereignis, das nicht an einen Ereignisverbraucher übermittelt wird.
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
ms.openlocfilehash: 695381a3471dcc744cae10622ee9e7935b2770941a770bd0e4e4e93e591a9220
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051088"
---
# <a name="__eventdroppedevent-class"></a>\_\_EventDroppedEvent-Klasse

Die **\_ \_ EventDroppedEvent-Systemklasse** stellt das Vorkommen eines Ereignisses dar, das gelöscht wird. Ein gelöschtes Ereignis ist ein Ereignis, das nicht an einen Ereignisverbraucher übermittelt wird.

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.

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

Die **\_ \_ EventDroppedEvent-Klasse** verfügt über folgende Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **\_ \_ EventDroppedEvent-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Event**
</dt> <dd> <dl> <dt>

Datentyp: **\_ \_ Ereignis**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Das Ereignis, das gelöscht wird.

</dd> <dt>

**IntendedConsumer**
</dt> <dd> <dl> <dt>

Datentyp: **\_ \_ EventConsumer**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Verweis auf eine Instanz von [**\_ \_ EventConsumer,**](--eventconsumer.md) die den permanenten Consumer darstellt, den Sie zum Empfangen eines Ereignisses identifizieren. Verschiedene permanente Consumer, die ein Ereignis abonnieren, können das Ereignis weiterhin empfangen.

</dd> <dt>

**\_SICHERHEITSBESCHREIBUNG**
</dt> <dd> <dl> <dt>

Datentyp: **uint8-Array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Deskriptor, den ein Ereignisanbieter verwendet, um die Benutzer zu bestimmen, die ein Ereignis empfangen können. Diese Eigenschaft wird von [**\_ \_ Ereignis**](--event.md)geerbt.

</dd> <dt>

**TIME \_ CREATED**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eindeutiger Wert, der den Zeitpunkt angibt, zu dem ein Ereignis generiert wird. Dies ist ein 64-Bit-Wert, der die Anzahl von 100-Nanosekunden-Intervallen nach dem 1. Januar 1601 darstellt. Die Informationen haben das format koordinierte Weltzeit (UTC). Diese Eigenschaft wird von [**\_ \_ Ereignis**](--event.md)geerbt.

Weitere Informationen zur Verwendung von **uint64-Werten** in Skripts finden Sie unter [Skripterstellung in WMI.](/windows/desktop/WmiSdk/creating-a-wmi-script)

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **\_ \_ EventDroppedEvent-Klasse** wird von [**\_ \_ SystemEvent**](--systemevent.md)abgeleitet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Alle WMI-Namespaces<br/>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_\_SystemEvent**](/windows/desktop/WmiSdk/--systemevent)
</dt> <dt>

[WMI-Systemklassen](wmi-system-classes.md)
</dt> </dl>

 

