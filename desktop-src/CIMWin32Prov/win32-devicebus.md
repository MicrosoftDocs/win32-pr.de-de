---
description: Die WMI-Klasse für die Win32 \_ DeviceBus-Zuordnung verknüpft einen Systembus und ein logisches Gerät, das den Bus verwendet. Diese Klasse wird verwendet, um zu ermitteln, welche Geräte sich in welchem Bus befinden.
ms.assetid: 2d7d83a5-c058-40c0-aab3-7700f4067a16
ms.tgt_platform: multiple
title: Win32_DeviceBus-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DeviceBus
- Win32_DeviceBus.Dependent
- Win32_DeviceBus.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: fc8c6c8cb1d83d31539fa405d09d60db2de68089d82213d08ee9ba8f0491a731
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119439160"
---
# <a name="win32_devicebus-class"></a>Win32 \_ DeviceBus-Klasse

Die [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) für **die Win32 \_ DeviceBus-Zuordnung** verknüpft einen Systembus und ein logisches Gerät, das den Bus verwendet. Diese Klasse wird verwendet, um zu ermitteln, welche Geräte sich in welchem Bus befinden.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C50F-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_DeviceBus : CIM_Dependency
{
  CIM_LogicalDevice REF Dependent;
  Win32_Bus         REF Antecedent;
};
```

## <a name="members"></a>Member

Die **Win32 \_ DeviceBus-Klasse** verfügt über folgende Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ DeviceBus-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Vorläufer**
</dt> <dd> <dl> <dt>

Datentyp: **Win32 \_ Bus**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Vorgänger"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ Bus")
</dt> </dl>

Ein [**\_ Win32-Bus,**](win32-bus.md) der die Eigenschaften des Systembus beschreibt, der vom logischen Gerät verwendet wird.

</dd> <dt>

**Abhängigen**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ LogicalDevice**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \| CIM \_ LogicalDevice")
</dt> </dl>

Ein [**CIM \_ LogicalDevice,**](cim-logicaldevice.md) der die Eigenschaften des logischen Geräts beschreibt, das den Systembus verwendet.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **Win32 \_ DeviceBus-Klasse** wird von [**\_ CIM-Abhängigkeit**](cim-dependency.md)abgeleitet.

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

 

