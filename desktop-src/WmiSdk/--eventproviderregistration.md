---
description: Wird verwendet, um Ereignisanbieter bei der Windows Management Instrumentation (WMI) zu registrieren.
ms.assetid: d87f61a8-5549-4f33-ba67-31b5d72b5282
ms.tgt_platform: multiple
title: __EventProviderRegistration-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventProviderRegistration
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: ce973f05aec0a1c859598c558ef8c2cc637a8faec22fd1d7f2ad2aaf383bd201
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118557944"
---
# <a name="__eventproviderregistration-class"></a>\_\_EventProviderRegistration-Klasse

Die **\_ \_ EventProviderRegistration-Systemklasse** wird verwendet, um Ereignisanbieter bei der Windows Management Instrumentation (WMI) zu registrieren.

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.

## <a name="syntax"></a>Syntax

``` syntax
class __EventProviderRegistration : __ProviderRegistration
{
  string         EventQueryList[];
  __Provider REF provider;
};
```

## <a name="members"></a>Member

Die **\_ \_ EventProviderRegistration-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **\_ \_ EventProviderRegistration-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**EventQueryList**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Mindestens eine Windows WQL-Abfragen (Management Instrumentation Query Language), die die vom Ereignisanbieter unterstützten Ereignisse beschreiben.

</dd> <dt>

**Anbieter**
</dt> <dd> <dl> <dt>

Datentyp: **\_ \_ Anbieter**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Objektpfad zum Ereignisanbieter. Diese Eigenschaft wird von [**\_ \_ ProviderRegistration geerbt.**](--providerregistration.md)

</dd> </dl>

## <a name="remarks"></a>Hinweise

Nur Administratoren können einen Ereignisanbieter registrieren oder löschen, indem sie eine Instanz von [**\_ \_ Win32Provider**](--win32provider.md) und [**\_ \_ EventProviderRegistration erstellen.**](--eventconsumerproviderregistration.md) Die **\_ \_ EventProviderRegistration-Klasse** wird von [**\_ \_ ProviderRegistration abgeleitet.**](--providerregistration.md)

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

[Registrieren eines Ereignisanbieters](registering-an-event-provider.md)
</dt> <dt>

[Schreiben eines Ereignisanbieters](writing-an-event-provider.md)
</dt> </dl>

 

