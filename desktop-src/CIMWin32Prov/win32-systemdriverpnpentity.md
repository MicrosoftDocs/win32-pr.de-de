---
description: The Win32\_SystemDriverPNPEntity association WMI class relates a Plug and Play device on the computer system running Windows and the driver that supports the Plug and Play device.
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
ms.openlocfilehash: e4b0de9559d223db4c398387ca846be39b17566b3267c76399bdf4381cdd14e7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119751110"
---
# <a name="win32_systemdriverpnpentity-class"></a>Win32 \_ SystemDriverPNPEntity-Klasse

The **Win32\_SystemDriverPNPEntity** association [WMI class](../wmisdk/retrieving-a-class.md) relates a Plug and Play device on the computer system running Windows and the driver that supports the Plug and Play device.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.

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

Die **\_ Win32-SystemDriverPNPEntity-Klasse** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ SystemDriverPNPEntity-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Vorläufer**
</dt> <dd> <dl> <dt>

Datentyp: **Win32 \_ PNPEntity**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Schlüssel**](../wmisdk/key-qualifier.md), [**Außerkraftsetzung**](../wmisdk/standard-qualifiers.md) ("Vorgänger"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ PNPEntity")
</dt> </dl>

Stellt die Plug & Play Gerät dar, das vom Treiber gesteuert wird.

</dd> <dt>

**Abhängigen**
</dt> <dd> <dl> <dt>

Datentyp: **Win32 \_ SystemDriver**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Dependent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ SystemDriver")
</dt> </dl>

A [**Win32\_SystemDriver**](win32-systemdriver.md) that represents the driver that supports the Plug and Play device.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **Win32 \_ SystemDriverPNPEntity-Klasse** wird von [**\_ CIM-Abhängigkeit**](cim-dependency.md)abgeleitet.

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

[**\_CIM-Abhängigkeit**](cim-dependency.md)
</dt> <dt>

[Computersystemhardwareklassen](computer-system-hardware-classes.md)
</dt> </dl>

 

 
