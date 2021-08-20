---
description: Die WMI-Klasse für die Win32 SerialPortSetting-Zuordnung bezieht sich auf einen \_ seriellen Anschluss und dessen Konfigurationseinstellungen.
ms.assetid: 57856207-abe5-4d93-9a34-acfe30ccd80c
ms.tgt_platform: multiple
title: Win32_SerialPortSetting-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SerialPortSetting
- Win32_SerialPortSetting.Setting
- Win32_SerialPortSetting.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a40d11600a0da627ec887327b44fd860def774feff624936c302297d162d6372
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118007753"
---
# <a name="win32_serialportsetting-class"></a>Win32 \_ SerialPortSetting-Klasse

Die **WMI-Klasse für die Win32 \_ SerialPortSetting-Zuordnung** bezieht sich auf einen seriellen Anschluss und dessen Konfigurationseinstellungen. [](../wmisdk/retrieving-a-class.md)

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4FE-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SerialPortSetting : Win32_DeviceSettings
{
  Win32_SerialPortConfiguration REF Setting;
  Win32_SerialPort              REF Element;
};
```

## <a name="members"></a>Member

Die **Win32 \_ SerialPortSetting-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ SerialPortSetting-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Element**
</dt> <dd> <dl> <dt>

Datentyp: **Win32 \_ SerialPort**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Außerkraftsetzung**](../wmisdk/standard-qualifiers.md) ("Element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ SerialPort")
</dt> </dl>

Ein [**Win32 \_ SerialPort,**](win32-serialport.md) der die Eigenschaften eines seriellen Anschlusses auf dem Computersystem enthält.

</dd> <dt>

**Einstellung**
</dt> <dd> <dl> <dt>

Datentyp: **Win32 \_ SerialPortConfiguration**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Außerkraftsetzung**](../wmisdk/standard-qualifiers.md) [**("Einstellung"), MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ SerialPortConfiguration")
</dt> </dl>

Eine [**Win32 \_ SerialPortConfiguration,**](win32-serialportconfiguration.md) die die Konfigurationseinstellung für den seriellen Anschluss enthält.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **Win32 \_ SerialPortSetting-Klasse** wird von [**Win32 \_ DeviceSettings abgeleitet.**](win32-devicesettings.md)

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

[**Win32 \_ DeviceSettings**](win32-devicesettings.md)
</dt> <dt>

[Hardwareklassen des Computersystems](computer-system-hardware-classes.md)
</dt> </dl>

 

 
