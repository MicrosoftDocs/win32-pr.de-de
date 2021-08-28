---
description: Stellt den konfigurierten Zustand eines GPU-Partitionsgeräts dar.
ms.assetid: 33ec4ea2-4e79-4c84-8abe-da8308ad6702
title: Msvm_GpuPartitionSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GpuPartitionSettingData
- Msvm_GpuPartitionSettingData.MinPartitionVRAM
- Msvm_GpuPartitionSettingData.MaxPartitionVRAM
- Msvm_GpuPartitionSettingData.OptimalPartitionVRAM
- Msvm_GpuPartitionSettingData.MinPartitionEncode
- Msvm_GpuPartitionSettingData.MaxPartitionEncode
- Msvm_GpuPartitionSettingData.OptimalPartitionEncode
- Msvm_GpuPartitionSettingData.MinPartitionDecode
- Msvm_GpuPartitionSettingData.MaxPartitionDecode
- Msvm_GpuPartitionSettingData.OptimalPartitionDecode
- Msvm_GpuPartitionSettingData.MinPartitionCompute
- Msvm_GpuPartitionSettingData.MaxPartitionCompute
- Msvm_GpuPartitionSettingData.OptimalPartitionCompute
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 39fe0f5a794875c25cf844c39df2217fae04d1b791a5a5174358fa0ea70150ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014528"
---
# <a name="msvm_gpupartitionsettingdata-class"></a>Msvm \_ GpuPartitionSettingData-Klasse

Stellt den konfigurierten Zustand eines GPU-Partitionsgeräts dar.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_GpuPartitionSettingData : CIM_ResourceAllocationSettingData
{
  uint64 MinPartitionVRAM;
  uint64 MaxPartitionVRAM;
  uint64 OptimalPartitionVRAM;
  uint64 MinPartitionEncode;
  uint64 MaxPartitionEncode;
  uint64 OptimalPartitionEncode;
  uint64 MinPartitionDecode;
  uint64 MaxPartitionDecode;
  uint64 OptimalPartitionDecode;
  uint64 MinPartitionCompute;
  uint64 MaxPartitionCompute;
  uint64 OptimalPartitionCompute;
};
```

## <a name="members"></a>Member

Die **Msvm \_ GpuPartitionSettingData-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Msvm \_ GpuPartitionSettingData-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**MaxPartitionCompute**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Die maximale Anzahl von Compute-Engines, die in der GPU-Partition angezeigt werden.

</dd> <dt>

**MaxPartitionDecode**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Die maximale Anzahl von Decodierungs-Engines, die in der GPU-Partition angezeigt werden.

</dd> <dt>

**MaxPartitionEncode**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Die maximale Anzahl von Codierungs-Engines, die in der GPU-Partition angezeigt werden.

</dd> <dt>

**MaxPartitionVRAM**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Die maximale VRAM-Menge, die in der GPU-Partition angezeigt wird.

</dd> <dt>

**MinPartitionCompute**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Die Mindestmenge der Compute-Engines, die in der GPU-Partition angezeigt werden.

</dd> <dt>

**MinPartitionDecode**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Die Mindestanzahl von Decodierungs-Engines, die in der GPU-Partition angezeigt werden.

</dd> <dt>

**MinPartitionEncode**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Die Mindestanzahl von Codierungs-Engines, die in der GPU-Partition angezeigt werden.

</dd> <dt>

**MinPartitionVRAM**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Die Mindestmenge an VRAM, die in der GPU-Partition angezeigt wird.

</dd> <dt>

**OptimalPartitionCompute**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Die optimale Menge an Compute-Engines, die in der GPU-Partition angezeigt werden.

</dd> <dt>

**OptimalPartitionDecode**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Die optimale Menge an Decodierungs-Engines, die in der GPU-Partition angezeigt werden.

</dd> <dt>

**OptimalPartitionEncode**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Die optimale Menge an Codierungs-Engines, die in der GPU-Partition angezeigt werden.

</dd> <dt>

**OptimalPartitionVRAM**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Die optimale Menge an VRAM, die in der GPU-Partition angezeigt wird.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, version 1703 desktop apps only (Nur \[ Desktop-Apps der Version 1703)\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md)
</dt> </dl>

 

 




