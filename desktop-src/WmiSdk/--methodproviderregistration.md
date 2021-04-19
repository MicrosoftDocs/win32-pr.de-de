---
description: Registriert Methoden Anbieter bei WMI.
ms.assetid: c5a8ccd3-487e-42a3-bb31-d27da9a711c4
ms.tgt_platform: multiple
title: __MethodProviderRegistration-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __MethodProviderRegistration
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: dd59a88c9c0ff7b4b6726b58ce69f879eb3893ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363709"
---
# <a name="__methodproviderregistration-class"></a>\_\_Methodproviderregistration-Klasse

Die **\_ \_ methodproviderregistration** -System Klasse registriert Methoden Anbieter bei WMI.

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

## <a name="syntax"></a>Syntax

``` syntax
class __MethodProviderRegistration : __ProviderRegistration
{
  __Provider REF provider;
};
```

## <a name="members"></a>Member

Die **\_ \_ methodproviderregistration** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **\_ \_ methodproviderregistration** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**ab**
</dt> <dd> <dl> <dt>

Datentyp: **\_ \_ Anbieter**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Verweis auf eine Instanz des [**\_ \_ Anbieters**](--provider.md) , die den Objekt Pfad des Methoden Anbieters darstellt. Diese Eigenschaft wird von [**\_ \_ providerregistration**](--providerregistration.md)geerbt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **\_ \_ methodproviderregistration** -Klasse wird von [**\_ \_ providerregistration**](--providerregistration.md)abgeleitet. Nur Administratoren können einen Methoden Anbieter registrieren oder löschen, indem Sie eine Instanz von [**\_ \_ Win32Provider**](--win32provider.md) und **\_ \_ methodproviderregistration** erstellen.

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

[Registrieren eines Methoden Anbieters](registering-a-method-provider.md)
</dt> </dl>

 

