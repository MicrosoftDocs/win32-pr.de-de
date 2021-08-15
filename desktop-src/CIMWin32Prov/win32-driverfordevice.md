---
description: Die \_ WMI-Zuordnungsklasse Win32 DriverForDevice verknüpft eine Druckerinstanz mit einer Druckertreiberinstanz.
ms.assetid: 56ff74b2-31ba-4d8e-b389-9f962932aa03
ms.tgt_platform: multiple
title: Win32_DriverForDevice-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DriverForDevice
- Win32_DriverForDevice.Antecedent
- Win32_DriverForDevice.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: f55025c84b8ab7e7114f5a1746d84f8fbdb6b0a7dfe952abfe84efb980430881
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119546320"
---
# <a name="win32_driverfordevice-class"></a>Win32 \_ DriverForDevice-Klasse

Die [WMI-Zuordnungsklasse](/windows/desktop/WmiSdk/retrieving-a-class) **Win32 \_ DriverForDevice** verknüpft eine Druckerinstanz mit einer Druckertreiberinstanz.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.

## <a name="syntax"></a>Syntax

``` syntax
class Win32_DriverForDevice : CIM_Dependency
{
  Win32_Printer       REF Antecedent;
  Win32_PrinterDriver REF Dependent;
};
```

## <a name="members"></a>Member

Die **Win32 \_ DriverForDevice-Klasse** verfügt über folgende Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ DriverForDevice-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Vorläufer**
</dt> <dd> <dl> <dt>

Datentyp: **\_ Win32-Drucker**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Verweis auf die [**Win32-Druckerinstanz, \_**](win32-printer.md) die den Drucker darstellt.

Diese Eigenschaft wird von [**\_ CIM-Abhängigkeit**](cim-dependency.md)geerbt.

</dd> <dt>

**Abhängigen**
</dt> <dd> <dl> <dt>

Datentyp: **Win32 \_ PrinterDriver**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Verweis auf die [**Win32 \_ PrinterDriver-Instanz,**](win32-printerdriver.md) die den Druckertreiber für den Drucker darstellt.

Diese Eigenschaft wird von [**\_ CIM-Abhängigkeit**](cim-dependency.md)geerbt.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **Win32 \_ DriverForDevice-Klasse** wird von [**\_ CIM-Abhängigkeit**](cim-dependency.md)abgeleitet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                                |
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                        |
| MOF<br/>                      | <dl> <dt>Win32 \_ Printer.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl>       |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Computersystemhardwareklassen](computer-system-hardware-classes.md)
</dt> </dl>

 

