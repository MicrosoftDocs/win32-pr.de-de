---
description: Fungiert als übergeordnete Klasse für Registrierungs Klassen für verschiedene Typen von Anbietern.
ms.assetid: 1e5d95cb-0961-4be8-b80a-37b598c9ccfe
ms.tgt_platform: multiple
title: __ProviderRegistration-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ProviderRegistration
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 7359f3d5cdcfb2447b724fd6d369a1029d8fcd4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131772"
---
# <a name="__providerregistration-class"></a>\_\_Providerregistration-Klasse

Die abstrakte System Klasse **\_ \_ providerregistration** fungiert als übergeordnete Klasse für Registrierungs Klassen für verschiedene Typen von Anbietern.

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

## <a name="syntax"></a>Syntax

``` syntax
[abstract]
class __ProviderRegistration : __SystemClass
{
  __Provider REF provider;
};
```

## <a name="members"></a>Member

Die **\_ \_ providerregistration** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **\_ \_ providerregistration** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**ab**
</dt> <dd> <dl> <dt>

Datentyp: **\_ \_ Anbieter**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Verweis auf eine Instanz des [**\_ \_ Anbieters**](--provider.md) , die den Objekt Pfad zum Anbieter darstellt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **\_ \_ providerregistration** -Klasse wird von [**\_ \_ systemclass**](--systemclass.md)abgeleitet, die keine Eigenschaften hat.

Instanzen der **\_ \_ providerregistration** -System Klasse werden nie erstellt. Die Klassen, die Anbieter zum Erstellen von Instanzen für die Registrierung verwenden, werden entweder direkt oder indirekt von dieser Klasse abgeleitet. Diese Klassen sind:

[**\_\_Classproviderregistration**](--classproviderregistration.md)

[**\_\_Eventconsumerproviderregistration**](--eventconsumerproviderregistration.md)

[**\_\_Eventproviderregistration**](--eventproviderregistration.md)

[**\_\_Instanceproviderregistration**](--instanceproviderregistration.md)

[**\_\_Methodproviderregistration**](--methodproviderregistration.md)

[**\_\_Objectproviderregistration**](--objectproviderregistration.md)

[**\_\_Propertyproviderregistration**](--propertyproviderregistration.md)

Nur Administratoren können einen Anbieter registrieren oder löschen, indem Sie eine Instanz von [**\_ \_ Win32Provider**](--win32provider.md) erstellen und registrieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Alle WMI-Namespaces<br/>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_\_System Class**](/windows/desktop/WmiSdk/--systemclass)
</dt> <dt>

[WMI-System Klassen](wmi-system-classes.md)
</dt> <dt>

[Registrieren eines Anbieters](registering-a-provider.md)
</dt> </dl>

 

