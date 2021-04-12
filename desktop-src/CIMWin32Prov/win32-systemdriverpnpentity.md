---
description: Die \_ WMI-Klasse "Win32 systemdriverpnptity" verknüpft ein Plug & Play-Gerät auf dem Computersystem, auf dem Windows ausgeführt wird, sowie den Treiber, der das Plug & Play Gerät unterstützt.
ms.assetid: 2696c8e5-3bc3-42e3-807b-a387607c7c09
ms.tgt_platform: multiple
title: Win32_SystemDriverPNPEntity-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriverPNPEntity
- Win32_SystemDriverPNPEntity.Antecedent
- Win32_SystemDriverPNPEntity.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8b5a7eedfbd7a545e37cb9cda38c19cf61308761
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523683"
---
# <a name="win32_systemdriverpnpentity-class"></a>Win32 \_ systemdriverpnptity-Klasse

Die [WMI-Klasse](../wmisdk/retrieving-a-class.md) " **Win32 \_ systemdriverpnptity** " verknüpft ein Plug & Play-Gerät auf dem Computersystem, auf dem Windows ausgeführt wird, sowie den Treiber, der das Plug & Play Gerät unterstützt.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{0800F074-CB98-11d2-B35D-00104BC97924}"), AMENDMENT]
class Win32_SystemDriverPNPEntity : CIM_Dependency
{
  Win32_PNPEntity    REF Antecedent;
  Win32_SystemDriver REF Dependent;
};
```

## <a name="members"></a>Member

Die **Win32 \_ systemdriverpnptity** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ systemdriverpnptity** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Vorgänger**
</dt> <dd> <dl> <dt>

Datentyp: **Win32 \_ pnptity**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("Vorgänger"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ pnptity")
</dt> </dl>

Stellt das vom Treiber gesteuerte Plug & Play Gerät dar.

</dd> <dt>

**Dependent**
</dt> <dd> <dl> <dt>

Datentyp: **Win32 \_ System Driver**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("Dependent"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ System Driver")
</dt> </dl>

Ein [**Win32- \_ System Treiber**](win32-systemdriver.md) , der den Treiber darstellt, der das Plug & Play Gerät unterstützt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **Win32- \_ systemdriverpnptity** -Klasse wird von der [**CIM- \_ Abhängigkeit**](cim-dependency.md)abgeleitet.

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

[**CIM- \_ Abhängigkeit**](cim-dependency.md)
</dt> <dt>

[Computer System-Hardware Klassen](computer-system-hardware-classes.md)
</dt> </dl>

 

 
