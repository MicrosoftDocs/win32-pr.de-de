---
description: Registriert Ereignisverbraucheranbieter bei WMI.
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
ms.openlocfilehash: bc3acec16b92c375f07836318be0e77c335862aec826c80bb77815865a337a72
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118557934"
---
# <a name="__eventconsumerproviderregistration-class"></a>\_\_EventConsumerProviderRegistration-Klasse

Die **\_ \_ Systemklasse EventConsumerProviderRegistration** registriert Ereignisconsumeranbieter bei WMI.

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.

## <a name="syntax"></a>Syntax

``` syntax
class __EventConsumerProviderRegistration : __ProviderRegistration
{
  string         ConsumerClassNames[];
  __Provider REF provider;
};
```

## <a name="members"></a>Member

Die **\_ \_ EventConsumerProviderRegistration-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **\_ \_ EventConsumerProviderRegistration-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**ConsumerClassNames**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Array von Namen der logischen Consumerklassen, die der Ereignisverbraucheranbieter unterstützt.

</dd> <dt>

**Anbieter**
</dt> <dd> <dl> <dt>

Datentyp: **\_ \_ Anbieter**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Objektpfad zum Anbieter. Diese Eigenschaft wird von [**\_ \_ ProviderRegistration geerbt.**](--providerregistration.md)

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **\_ \_ EventConsumerProviderRegistration-Klasse** wird von [**\_ \_ ProviderRegistration abgeleitet.**](--providerregistration.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Alle WMI-Namespaces<br/>  |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**\_\_ProviderRegistration**](/windows/desktop/WmiSdk/--providerregistration)
</dt> <dt>

[WMI-Systemklassen](wmi-system-classes.md)
</dt> <dt>

[Registrieren eines Ereignisverbraucheranbieters](registering-an-event-consumer-provider.md)
</dt> <dt>

[Schreiben eines Ereignisverbraucheranbieters](writing-an-event-consumer-provider.md)
</dt> </dl>

 

