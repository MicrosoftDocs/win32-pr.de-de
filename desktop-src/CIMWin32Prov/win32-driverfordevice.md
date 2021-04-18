---
description: Die \_ WMI-Klasse "Win32 driverfordevice Association" verknüpft eine Drucker Instanz mit einer Druckertreiber Instanz.
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
ms.openlocfilehash: b5fb384eed80c6a614af448477c50be3204d3080
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106341149"
---
# <a name="win32_driverfordevice-class"></a>Win32- \_ Klasse "driverfordevice"

Die [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) " **Win32 \_ driverfordevice** Association" verknüpft eine Drucker Instanz mit einer Druckertreiber Instanz.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

## <a name="syntax"></a>Syntax

``` syntax
class Win32_DriverForDevice : CIM_Dependency
{
  Win32_Printer       REF Antecedent;
  Win32_PrinterDriver REF Dependent;
};
```

## <a name="members"></a>Member

Die Win32-Klasse " **\_ driverfordevice** " enthält diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die Win32-Klasse " **\_ driverfordevice** " verfügt über diese Eigenschaften.

<dl> <dt>

**Vorgänger**
</dt> <dd> <dl> <dt>

Datentyp: **Win32- \_ Drucker**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Verweis auf die [**Win32- \_ Drucker**](win32-printer.md) Instanz, die den Drucker darstellt.

Diese Eigenschaft wird von der [**CIM- \_ Abhängigkeit**](cim-dependency.md)geerbt.

</dd> <dt>

**Dependent**
</dt> <dd> <dl> <dt>

Datentyp: **Win32 \_ PrinterDriver**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Verweis auf die [**Win32- \_ PrinterDriver**](win32-printerdriver.md) -Instanz, die den Druckertreiber für den Drucker darstellt.

Diese Eigenschaft wird von der [**CIM- \_ Abhängigkeit**](cim-dependency.md)geerbt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die Win32-Klasse " **\_ driverfordevice** " wird von [**CIM- \_ Abhängigkeit**](cim-dependency.md)abgeleitet.

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

[Computer System-Hardware Klassen](computer-system-hardware-classes.md)
</dt> </dl>

 

