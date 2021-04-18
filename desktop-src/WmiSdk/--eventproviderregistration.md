---
description: Wird zum Registrieren von Ereignis Anbietern bei Windows-Verwaltungsinstrumentation (WMI) verwendet.
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
ms.openlocfilehash: caaad1b4ab03cfc1b43e4239b9144d3ceeade82f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347682"
---
# <a name="__eventproviderregistration-class"></a>\_\_Eventproviderregistration-Klasse

Die **\_ \_ eventproviderregistration** -System Klasse wird zum Registrieren von Ereignis Anbietern bei Windows-Verwaltungsinstrumentation (WMI) verwendet.

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

## <a name="syntax"></a>Syntax

``` syntax
class __EventProviderRegistration : __ProviderRegistration
{
  string         EventQueryList[];
  __Provider REF provider;
};
```

## <a name="members"></a>Member

Die **\_ \_ eventproviderregistration** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **\_ \_ eventproviderregistration** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**EventQueryList**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Eine oder mehrere WQL-Abfragen (Windows-Verwaltungsinstrumentation Query Language), die die Ereignisse beschreiben, die vom Ereignis Anbieter unterstützt werden.

</dd> <dt>

**ab**
</dt> <dd> <dl> <dt>

Datentyp: **\_ \_ Anbieter**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Objekt Pfad zum Ereignis Anbieter. Diese Eigenschaft wird von [**\_ \_ providerregistration**](--providerregistration.md)geerbt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Nur Administratoren können einen Ereignis Anbieter registrieren oder löschen, indem Sie eine Instanz von [**\_ \_ Win32Provider**](--win32provider.md) und [**\_ \_ eventproviderregistration**](--eventconsumerproviderregistration.md)erstellen. Die **\_ \_ eventproviderregistration** -Klasse wird von [**\_ \_ providerregistration**](--providerregistration.md)abgeleitet.

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

[Registrieren eines Ereignis Anbieters](registering-an-event-provider.md)
</dt> <dt>

[Schreiben eines Ereignis Anbieters](writing-an-event-provider.md)
</dt> </dl>

 

