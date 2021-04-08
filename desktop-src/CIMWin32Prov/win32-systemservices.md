---
description: Die \_ WMI-Klasse der Win32-Systemdienst Zuordnung bezieht sich auf ein Computersystem und ein Dienstprogramm, das im System vorhanden ist.
ms.assetid: b372e696-e1e0-4b1e-9fb8-83af8a75c405
ms.tgt_platform: multiple
title: Win32_SystemServices-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemServices
- Win32_SystemServices.GroupComponent
- Win32_SystemServices.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d8e61469729f3753256bc7fcf5598265b5c1b7dc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748392"
---
# <a name="win32_systemservices-class"></a>Win32- \_ systemdiensteklasse

Die [WMI-Klasse](../wmisdk/retrieving-a-class.md) der Win32-System **\_ Dienst** Zuordnung bezieht sich auf ein Computersystem und ein Dienstprogramm, das im System vorhanden ist.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4F6-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemServices : CIM_SystemComponent
{
  Win32_ComputerSystem REF GroupComponent;
  Win32_Service        REF PartComponent;
};
```

## <a name="members"></a>Member

Die **Win32- \_ systemdiensteklasse** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32- \_ systemdiensteklasse** verfügt über diese Eigenschaften.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Datentyp: **Win32 \_ Computersystem**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ Computersystem")
</dt> </dl>

Verweis auf die-Instanz, die die Eigenschaften des Computer Systems darstellt, auf dem der Dienst vorhanden ist.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Datentyp: **Win32- \_ Dienst**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32- \_ Dienst")
</dt> </dl>

Verweis auf die-Instanz, die den Dienst darstellt, der auf dem Computersystem vorhanden ist.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **Win32- \_ systemdiensteklasse** wird von [**CIM \_ SystemComponent**](cim-systemcomponent.md)abgeleitet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>Cimwin32. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM- \_ SystemComponent**](cim-systemcomponent.md)
</dt> <dt>

[Betriebssystemklassen](./operating-system-classes.md)
</dt> </dl>

 

 
