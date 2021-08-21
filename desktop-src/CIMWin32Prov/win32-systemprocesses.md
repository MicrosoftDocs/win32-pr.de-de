---
description: Die \_ WMI-Klasse für die Win32-Systemprocesses-Zuordnung bezieht sich auf ein Computersystem und einen Prozess, der auf diesem System ausgeführt wird.
ms.assetid: 0d8c3ec6-265e-4486-8e94-f5acd2845cf5
ms.tgt_platform: multiple
title: Win32_SystemProcesses-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemProcesses
- Win32_SystemProcesses.GroupComponent
- Win32_SystemProcesses.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6ef5b856fe263133a6d1ea3064e83af8d7fead83e84dfaec7e50b82510920f9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119079644"
---
# <a name="win32_systemprocesses-class"></a>Win32 \_ SystemProcesses-Klasse

Die **WMI-Klasse \_ für die Win32-Systemprocesses-Zuordnung** bezieht sich auf ein Computersystem und einen Prozess, der auf diesem System ausgeführt wird. [](../wmisdk/retrieving-a-class.md)

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften und Methoden sind in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4F3-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemProcesses : CIM_SystemComponent
{
  Win32_ComputerSystem REF GroupComponent;
  Win32_Process        REF PartComponent;
};
```

## <a name="members"></a>Member

Die **Win32 \_ SystemProcesses-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ SystemProcesses-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Datentyp: **Win32 \_ ComputerSystem**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**schlüssel**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ ComputerSystem")
</dt> </dl>

Verweis auf die -Instanz, die das Computersystem darstellt, auf dem der Prozess ausgeführt wird.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Datentyp: **\_ Win32-Prozess**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**schlüssel**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ Process")
</dt> </dl>

Verweis auf die -Instanz, die den prozess darstellt, der auf dem Computersystem ausgeführt wird.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **Win32 \_ SystemProcesses-Klasse** wird von [**CIM \_ SystemComponent abgeleitet.**](cim-systemcomponent.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM \_ SystemComponent**](cim-systemcomponent.md)
</dt> <dt>

[Betriebssystemklassen](./operating-system-classes.md)
</dt> </dl>

 

 
