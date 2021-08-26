---
description: Die WMI-Klasse für die Win32-SystemBIOS-Zuordnung bezieht sich auf ein Computersystem (einschließlich Starteigenschaften, Zeitzonen, Startkonfigurationen oder Administratorkennwörter) und ein \_ System-BIOS (Dienste, Sprachen und Systemverwaltungseigenschaften).
ms.assetid: 92747b1b-ef28-40ab-868a-6755aee8c723
ms.tgt_platform: multiple
title: Win32_SystemBIOS-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemBIOS
- Win32_SystemBIOS.PartComponent
- Win32_SystemBIOS.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c9180b78add8b2646ae39a6f910296d53499e513f4fa05a4bbaaee42e240de5f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119971505"
---
# <a name="win32_systembios-class"></a>Win32 \_ SystemBIOS-Klasse

Die [WMI-Klasse](../wmisdk/retrieving-a-class.md) für die **Win32-SystemBIOS-Zuordnung \_** bezieht sich auf ein Computersystem (einschließlich Starteigenschaften, Zeitzonen, Startkonfigurationen oder Administratorkennwörter) und ein System-BIOS (Dienste, Sprachen und Systemverwaltungseigenschaften).

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4EE-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemBIOS : CIM_SystemComponent
{
  Win32_BIOS           REF PartComponent;
  Win32_ComputerSystem REF GroupComponent;
};
```

## <a name="members"></a>Member

Die **\_ Win32-SystemBIOS-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **\_ Win32-SystemBIOS-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Datentyp: **Win32 \_ ComputerSystem**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**schlüssel**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ ComputerSystem")
</dt> </dl>

Das [**\_ Win32-Computersystem,**](win32-computersystemprocessor.md) das das BIOS der Zuordnung enthält.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Datentyp: **Win32 \_ BIOS**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**schlüssel**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ BIOS")
</dt> </dl>

Ein [**\_ Win32-BIOS,**](win32-bios.md) das im Computersystem dieser Zuordnung enthalten ist.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **Win32 \_ SystemBIOS-Klasse** wird von [**CIM \_ SystemComponent abgeleitet.**](cim-systemcomponent.md)

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

[Hardwareklassen des Computersystems](computer-system-hardware-classes.md)
</dt> </dl>

 

 
