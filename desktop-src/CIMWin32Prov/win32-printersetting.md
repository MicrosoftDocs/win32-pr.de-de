---
description: Die \_ WMI-Klasse der Win32-printersetting-Zuordnung bezieht einen Drucker und seine Konfigurationseinstellungen ein.
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
ms.openlocfilehash: 90a77678e61b755550ebb1818c34ccdc3159a88c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214160"
---
# <a name="win32_printersetting-class"></a>Win32- \_ Klasse "printersetting"

Die [WMI-Klasse](../wmisdk/retrieving-a-class.md) der **Win32- \_ printersetting** -Zuordnung bezieht einen Drucker und seine Konfigurationseinstellungen ein.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

## <a name="syntax"></a>Syntax

``` syntax
class Win32_PrinterSetting : Win32_DeviceSettings
{
  CIM_Setting       REF Setting;
  CIM_LogicalDevice REF Element;
};
```

## <a name="members"></a>Member

Die Win32-Klasse " **\_ printersetting** " verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die Win32-Klasse " **\_ printersetting** " verfügt über diese Eigenschaften.

<dl> <dt>

**Element**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ LogicalDevice**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("CIM \| CIM \_ LogicalDevice")
</dt> </dl>

Ein [**CIM \_ LogicalDevice**](cim-logicaldevice.md) , das die Eigenschaften des logischen Geräts darstellt, auf das die Einstellungen angewendet werden können.

Diese Eigenschaft wird von [**Win32- \_**](win32-devicesettings.md)Geräte-Debug-Elementen geerbt.

</dd> <dt>

**Einstellung**
</dt> <dd> <dl> <dt>

Datentyp: **CIM- \_ Einstellung**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("CIM \| CIM- \_ Einstellung")
</dt> </dl>

Eine [**CIM- \_ Einstellung**](cim-setting.md) , die Einstellungen darstellt, die auf das logische Gerät angewendet werden können.

Diese Eigenschaft wird von [**Win32- \_**](win32-devicesettings.md)Geräte-Debug-Elementen geerbt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die Win32-Klasse " **\_ printersetting** " wird von [**Win32- \_ devicesettings**](win32-devicesettings.md)abgeleitet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                                |
| Namespace<br/>                | Root \\ CIMV2<br/>                                                                        |
| MOF<br/>                      | <dl> <dt>Win32 \_ Printer. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl>       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32-Geräte-Manager \_**](win32-devicesettings.md)
</dt> <dt>

[Computer System-Hardware Klassen](computer-system-hardware-classes.md)
</dt> </dl>

 

 
