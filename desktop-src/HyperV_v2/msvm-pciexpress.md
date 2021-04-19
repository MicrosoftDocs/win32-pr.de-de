---
description: Stellt den Zustand des PCI Express-Ports dar.
ms.assetid: 15d670ee-940a-4737-b2cd-e89dd8a63a5c
title: Msvm_PciExpress-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_PciExpress
- Msvm_PciExpress.DeviceInstancePath
- Msvm_PciExpress.LocationPath
- Msvm_PciExpress.FunctionNumber
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7534d09c9c0f3825ca462c342747caa17c8de9c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362962"
---
# <a name="msvm_pciexpress-class"></a>MSVM \_ PCIExpress-Klasse

Stellt den Zustand des PCI Express-Ports dar.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_PciExpress : CIM_LogicalDevice
{
  string DeviceInstancePath;
  string LocationPath;
  uint16 FunctionNumber;
};
```

## <a name="members"></a>Member

Die **MSVM \_ PCIExpress** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSVM \_ PCIExpress** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Gerätepfad**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Zeichenfolge mit dem geräteinstanzpfad zur Identifizierung des virtuellen PCI Express-Geräts.

</dd> <dt>

**Functionnumber**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Funktions Nummer des virtuellen PCI Express-Geräts.

</dd> <dt>

**LocationPath**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Zeichenfolge mit dem Speicherort Pfad des Geräts, der das virtuelle PCI Express-Gerät identifiziert.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, Version 1703, \[ nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM \_ LogicalDevice**](cim-logicaldevice.md)
</dt> </dl>

 

 




