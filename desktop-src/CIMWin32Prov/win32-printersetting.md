---
description: Die \_ WMI-Zuordnungsklasse Win32 PrinterSetting bezieht sich auf einen Drucker und dessen Konfigurationseinstellungen.
ms.assetid: 5d0f0724-0583-449b-a6da-336e7c8e526e
ms.tgt_platform: multiple
title: Win32_PrinterSetting-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrinterSetting
- Win32_PrinterSetting.Setting
- Win32_PrinterSetting.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: be39a9f614ab172c75e5ddc857254cdd91ea20d1352a33071cd6fa3627132d71
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119759380"
---
# <a name="win32_printersetting-class"></a>Win32 \_ PrinterSetting-Klasse

Die **WMI-Zuordnungsklasse Win32 \_ PrinterSetting** bezieht sich auf einen Drucker und dessen Konfigurationseinstellungen. [](../wmisdk/retrieving-a-class.md)

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.

## <a name="syntax"></a>Syntax

``` syntax
class Win32_PrinterSetting : Win32_DeviceSettings
{
  CIM_Setting       REF Setting;
  CIM_LogicalDevice REF Element;
};
```

## <a name="members"></a>Member

Die **Win32 \_ PrinterSetting-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ PrinterSetting-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Element**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ LogicalDevice**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Schlüssel**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM \| CIM \_ LogicalDevice")
</dt> </dl>

Ein [**CIM \_ LogicalDevice,**](cim-logicaldevice.md) das Eigenschaften des logischen Geräts darstellt, auf das die Einstellungen angewendet werden können.

Diese Eigenschaft wird von [**Win32 \_ DeviceSettings geerbt.**](win32-devicesettings.md)

</dd> <dt>

**Einstellung**
</dt> <dd> <dl> <dt>

Datentyp: **\_ CIM-Einstellung**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Schlüssel**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM \| \_ CIM-Einstellung")
</dt> </dl>

Eine [**\_ CIM-Einstellung,**](cim-setting.md) die Einstellungen darstellt, die auf das logische Gerät angewendet werden können.

Diese Eigenschaft wird von [**Win32 \_ DeviceSettings geerbt.**](win32-devicesettings.md)

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **Win32 \_ PrinterSetting-Klasse** wird von [**Win32 \_ DeviceSettings abgeleitet.**](win32-devicesettings.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                                |
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                        |
| MOF<br/>                      | <dl> <dt>Win32 \_ Printer.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl>       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ DeviceSettings**](win32-devicesettings.md)
</dt> <dt>

[Hardwareklassen des Computersystems](computer-system-hardware-classes.md)
</dt> </dl>

 

 
