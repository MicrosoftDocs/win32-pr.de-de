---
description: Die \_ WMI-Zuordnungsklasse Win32 SystemLoadOrderGroups verknüpft ein Computersystem und eine Lastreihenfolgegruppe.
ms.assetid: fb637300-0f70-465a-a72b-f0ab3f246790
ms.tgt_platform: multiple
title: Win32_SystemLoadOrderGroups-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemLoadOrderGroups
- Win32_SystemLoadOrderGroups.GroupComponent
- Win32_SystemLoadOrderGroups.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: bad87d62fddff6c4d76bb05a97fe0b7f97e713e70d0eba3ccfd36bb4aa31e813
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117833958"
---
# <a name="win32_systemloadordergroups-class"></a>Win32 \_ SystemLoadOrderGroups-Klasse

Die [WMI-Zuordnungsklasse](../wmisdk/retrieving-a-class.md) **Win32 \_ SystemLoadOrderGroups** verknüpft ein Computersystem und eine Lastreihenfolgegruppe.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften und Methoden werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge sortiert.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C503-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemLoadOrderGroups : CIM_SystemComponent
{
  Win32_ComputerSystem REF GroupComponent;
  Win32_LoadOrderGroup REF PartComponent;
};
```

## <a name="members"></a>Member

Die **Win32 \_ SystemLoadOrderGroups-Klasse** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ SystemLoadOrderGroups-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Datentyp: **Win32 \_ ComputerSystem**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ ComputerSystem")
</dt> </dl>

Verweis auf die -Instanz, die das Computersystem darstellt, in dem die Lastreihenfolgegruppe vorhanden ist.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Datentyp: **Win32 \_ LoadOrderGroup**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ LoadOrderGroup")
</dt> </dl>

Verweis auf die -Instanz, die die auf dem Computersystem vorhandene Lastreihenfolgegruppe darstellt.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **Win32 \_ SystemLoadOrderGroups-Klasse** wird von [**CIM \_ SystemComponent**](cim-systemcomponent.md)abgeleitet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CIM \_ SystemComponent**](cim-systemcomponent.md)
</dt> <dt>

[Betriebssystemklassen](./operating-system-classes.md)
</dt> </dl>

 

 
