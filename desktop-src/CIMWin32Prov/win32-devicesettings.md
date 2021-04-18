---
description: Die Win32 \_ -Klasse "devicesettings abstract, Association WMI" verknüpft ein logisches Gerät und eine Einstellung, die darauf angewendet werden kann.
ms.assetid: 4f6c4c26-8da9-4e2c-8b8c-cec658ac08d4
ms.tgt_platform: multiple
title: Win32_DeviceSettings-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DeviceSettings
- Win32_DeviceSettings.Setting
- Win32_DeviceSettings.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1cd9cae29cfa608c9f3c0c36ebfe3ca7f903c809
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214247"
---
# <a name="win32_devicesettings-class"></a>Win32- \_ Klasse "devicesettings"

Die Win32-Klasse " **\_ devicesettings** abstract, Association [WMI](/windows/desktop/WmiSdk/retrieving-a-class) " verknüpft ein logisches Gerät und eine Einstellung, die darauf angewendet werden kann.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, UUID("{8502C4FD-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_DeviceSettings : CIM_ElementSetting
{
  CIM_Setting       REF Setting;
  CIM_LogicalDevice REF Element;
};
```

## <a name="members"></a>Member

Die Win32-Klasse " **\_ devicesettings** " verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32-Klasse \_ devicesettings** verfügt über diese Eigenschaften.

<dl> <dt>

**Element**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ LogicalDevice**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Element"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \| CIM \_ LogicalDevice")
</dt> </dl>

Ein [**CIM \_ LogicalDevice**](cim-logicaldevice.md) , das die Eigenschaften des logischen Geräts darstellt, auf das die Einstellungen angewendet werden können.

</dd> <dt>

**Einstellung**
</dt> <dd> <dl> <dt>

Datentyp: **CIM- \_ Einstellung**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Setting"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \| CIM- \_ Einstellung")
</dt> </dl>

Eine [**CIM- \_ Einstellung**](cim-setting.md) , die Einstellungen darstellt, die auf das logische Gerät angewendet werden können.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **Win32-Klasse \_ devicesettings** wird von [**CIM \_ Element Setting**](cim-elementsetting.md)abgeleitet.

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

[**CIM- \_ Element Setting**](cim-elementsetting.md)
</dt> <dt>

[Computer System-Hardware Klassen](computer-system-hardware-classes.md)
</dt> </dl>

 

