---
description: Die WMI-Klasse für die Win32-SystemGeräte-Zuordnung bezieht sich auf ein Computersystem und ein logisches Gerät, \_ das auf diesem System installiert ist.
ms.assetid: 84dfcb75-3b44-4b27-8eee-779be522eb1f
ms.tgt_platform: multiple
title: Win32_SystemDevices-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDevices
- Win32_SystemDevices.GroupComponent
- Win32_SystemDevices.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 698b827e2dd3f9097f2348c83cbb52120186b0694a836fd2468396c542e535c4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119971470"
---
# <a name="win32_systemdevices-class"></a>Win32 \_ SystemDevices-Klasse

Die [WMI-Klasse](../wmisdk/retrieving-a-class.md) für die **\_ Win32-SystemGeräte-Zuordnung** bezieht sich auf ein Computersystem und ein logisches Gerät, das auf diesem System installiert ist.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften und Methoden sind in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4F4-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemDevices : CIM_SystemDevice
{
  Win32_ComputerSystem REF GroupComponent;
  CIM_LogicalDevice    REF PartComponent;
};
```

## <a name="members"></a>Member

Die **Win32 \_ SystemDevices-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ SystemDevices-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Datentyp: **Win32 \_ ComputerSystem**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**schlüssel**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ ComputerSystem")
</dt> </dl>

Verweis auf die -Instanz, die die Eigenschaften des Computersystems darstellt, in dem das logische Gerät vorhanden ist.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ LogicalDevice**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**schlüssel**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM \| CIM \_ LogicalDevice")
</dt> </dl>

Verweis auf die -Instanz, die die Eigenschaften eines logischen Geräts darstellt, das auf dem Computersystem vorhanden ist.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **Win32 \_ SystemDevices-Klasse** wird von [**CIM \_ SystemDevice abgeleitet.**](cim-systemdevice.md)

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

[**\_CIM-SystemGeräte**](cim-systemdevice.md)
</dt> <dt>

[Betriebssystemklassen](./operating-system-classes.md)
</dt> </dl>

 

 
