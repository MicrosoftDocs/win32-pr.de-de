---
description: Die WMI-Klasse für die abstrakte Win32 SystemSetting-Zuordnung bezieht sich auf ein Computersystem und eine allgemeine \_ Einstellung auf diesem System.
ms.assetid: 796ee263-2526-43f8-bd3d-23442b6bd4ca
ms.tgt_platform: multiple
title: Win32_SystemSetting-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemSetting
- Win32_SystemSetting.Element
- Win32_SystemSetting.Setting
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 75c4ee9db2f48d02151c3874cc0ac5775f04e2d119ada972db09826dd1f791c5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119827790"
---
# <a name="win32_systemsetting-class"></a>Win32 \_ SystemSetting-Klasse

Die **WMI-Klasse \_ für die abstrakte Win32 SystemSetting-Zuordnung** bezieht sich auf ein Computersystem und eine allgemeine Einstellung auf diesem System. [](../wmisdk/retrieving-a-class.md)

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften und Methoden sind in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, UUID("{8502C501-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemSetting : CIM_ElementSetting
{
  Win32_ComputerSystem REF Element;
  CIM_Setting          REF Setting;
};
```

## <a name="members"></a>Member

Die **Win32 \_ SystemSetting-Klasse** verfügt über diese Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ SystemSetting-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Element**
</dt> <dd> <dl> <dt>

Datentyp: **Win32 \_ ComputerSystem**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ ComputerSystem")
</dt> </dl>

Verweis auf die -Instanz, die die Eigenschaften eines Computersystems darstellt, auf die diese Einstellung angewendet werden kann.

</dd> <dt>

**Einstellung**
</dt> <dd> <dl> <dt>

Datentyp: **\_ CIM-Einstellung**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Schlüssel,**](../wmisdk/key-qualifier.md) [**Überschreibung**](../wmisdk/standard-qualifiers.md) ("Einstellung"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM \| \_ CIM-Einstellung")
</dt> </dl>

Verweis auf die -Instanz, die die Eigenschaften der Einstellung darstellt, die auf das Computersystem angewendet werden können.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **Win32 \_ SystemSetting-Klasse** wird von [**CIM \_ ElementSetting abgeleitet.**](cim-elementsetting.md)

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_CIM-ElementSetting**](cim-elementsetting.md)
</dt> <dt>

[Betriebssystemklassen](./operating-system-classes.md)
</dt> </dl>

 

 
