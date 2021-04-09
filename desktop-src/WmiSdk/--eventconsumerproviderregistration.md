---
description: Registriert Ereignisconsumeranbieter bei WMI.
ms.assetid: 31ff43dc-dc70-4ba0-866f-37445912f837
ms.tgt_platform: multiple
title: __EventConsumerProviderRegistration-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventConsumerProviderRegistration
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 38552519221018735c3c7543d9a1f3f2d4b680e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867356"
---
# <a name="__eventconsumerproviderregistration-class"></a>\_\_Eventconsumerproviderregistration-Klasse

Die **\_ \_ eventconsumerproviderregistration-System Klasse registriert Ereignisconsumeranbieter** bei WMI.

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

## <a name="syntax"></a>Syntax

``` syntax
class __EventConsumerProviderRegistration : __ProviderRegistration
{
  string         ConsumerClassNames[];
  __Provider REF provider;
};
```

## <a name="members"></a>Member

Die **\_ \_ eventconsumerproviderregistration** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **\_ \_ eventconsumerproviderregistration** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Consumerclassnames**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Array von Namen der logischen Consumerklassen, die vom Ereignisconsumeranbieter unterstützt werden.

</dd> <dt>

**ab**
</dt> <dd> <dl> <dt>

Datentyp: **\_ \_ Anbieter**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Objekt Pfad zum Anbieter. Diese Eigenschaft wird von [**\_ \_ providerregistration**](--providerregistration.md)geerbt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **\_ \_ eventconsumerproviderregistration** -Klasse wird von [**\_ \_ providerregistration**](--providerregistration.md)abgeleitet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Alle WMI-Namespaces<br/>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_\_Providerregistration**](/windows/desktop/WmiSdk/--providerregistration)
</dt> <dt>

[WMI-System Klassen](wmi-system-classes.md)
</dt> <dt>

[Registrieren eines Ereignisconsumeranbieters](registering-an-event-consumer-provider.md)
</dt> <dt>

[Schreiben eines Ereignisconsumeranbieters](writing-an-event-consumer-provider.md)
</dt> </dl>

 

