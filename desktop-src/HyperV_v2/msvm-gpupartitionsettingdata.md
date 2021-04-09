---
description: Stellt den konfigurierten Status eines GPU-Partitions Geräts dar.
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
ms.openlocfilehash: 7d8c9809b3a062654eaf0fb7a73b75b0188f7284
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959040"
---
# <a name="msvm_gpupartitionsettingdata-class"></a>MSVM \_ gpupartitionsettingdata-Klasse

Stellt den konfigurierten Status eines GPU-Partitions Geräts dar.

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

Die **MSVM-Klasse " \_ gpupartitionsettingdata** " enthält diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSVM \_ gpupartitionsettingdata** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Maxpartitioncompute**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Die maximale Menge an computeengines, die in der GPU-Partition angezeigt werden.

</dd> <dt>

**Maxpartitiondecode**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Die maximale Anzahl von decodieren-Engines, die in der GPU-Partition angezeigt werden.

</dd> <dt>

**Maxpartitioncocode**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Die maximale Anzahl der codierungsmodule, die in der GPU-Partition angezeigt werden.

</dd> <dt>

**Maxpartitionvram**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Die maximale VRAM-Größe, die in der GPU-Partition angezeigt wird.

</dd> <dt>

**Minpartitioncompute**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Die minimale Menge an computeengines, die in der GPU-Partition angezeigt werden.

</dd> <dt>

**Minpartitiondecode**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Die minimale Anzahl von decodieren-Engines, die in der GPU-Partition angezeigt werden.

</dd> <dt>

**Minpartitioncocode**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Die Mindestanzahl der codiermodule, die in der GPU-Partition angezeigt werden.

</dd> <dt>

**Minpartitionvram**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Die minimale VRAM-Größe, die in der GPU-Partition angezeigt wird.

</dd> <dt>

**Optimalpartitioncompute**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Die optimale Menge an computeengines, die in der GPU-Partition angezeigt werden.

</dd> <dt>

**Optimalpartitiondecode**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Die optimale Menge an Decodieren von Modulen, die in der GPU-Partition angezeigt werden.

</dd> <dt>

**Optimalpartitioncocode**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Die optimale Menge der codierungsmodule, die in der GPU-Partition angezeigt werden.

</dd> <dt>

**Optimalpartitionvram**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Die optimale VRAM-Größe, die in der GPU-Partition angezeigt wird.

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

[**CIM \_ resourcezubesettingdata**](cim-resourceallocationsettingdata.md)
</dt> </dl>

 

 




