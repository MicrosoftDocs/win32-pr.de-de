---
description: Stellt eine partitionierbare GPU dar. Jede GPU kann in mehrere GPU-Partitionen aufgeteilt werden, die einem virtuellen Computer als vGPU zugewiesen werden können.
ms.assetid: a32dfc03-6967-4fa3-ae32-bf074137740b
title: Msvm_PartitionableGpu-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_PartitionableGpu
- Msvm_PartitionableGpu.ValidPartitionCounts
- Msvm_PartitionableGpu.PartitionCount
- Msvm_PartitionableGpu.TotalVRAM
- Msvm_PartitionableGpu.AvailableVRAM
- Msvm_PartitionableGpu.MinPartitionVRAM
- Msvm_PartitionableGpu.MaxPartitionVRAM
- Msvm_PartitionableGpu.OptimalPartitionVRAM
- Msvm_PartitionableGpu.TotalEncode
- Msvm_PartitionableGpu.AvailableEncode
- Msvm_PartitionableGpu.MinPartitionEncode
- Msvm_PartitionableGpu.MaxPartitionEncode
- Msvm_PartitionableGpu.OptimalPartitionEncode
- Msvm_PartitionableGpu.TotalDecode
- Msvm_PartitionableGpu.AvailableDecode
- Msvm_PartitionableGpu.MinPartitionDecode
- Msvm_PartitionableGpu.MaxPartitionDecode
- Msvm_PartitionableGpu.OptimalPartitionDecode
- Msvm_PartitionableGpu.TotalCompute
- Msvm_PartitionableGpu.AvailableCompute
- Msvm_PartitionableGpu.MinPartitionCompute
- Msvm_PartitionableGpu.MaxPartitionCompute
- Msvm_PartitionableGpu.OptimalPartitionCompute
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 15ce369a0186ae6309f90a5b37a77a35cce90ae6997e3c8cbc7e968a0a0d0de0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119148293"
---
# <a name="msvm_partitionablegpu-class"></a>Msvm \_ PartitionableGpu-Klasse

Stellt eine partitionierbare GPU dar. Jede GPU kann in mehrere GPU-Partitionen aufgeteilt werden, die einem virtuellen Computer als vGPU zugewiesen werden können.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_PartitionableGpu : CIM_ComputerSystem
{
  uint16 ValidPartitionCounts[];
  uint16 PartitionCount;
  uint64 TotalVRAM;
  uint64 AvailableVRAM;
  uint64 MinPartitionVRAM;
  uint64 MaxPartitionVRAM;
  uint64 OptimalPartitionVRAM;
  uint64 TotalEncode;
  uint64 AvailableEncode;
  uint64 MinPartitionEncode;
  uint64 MaxPartitionEncode;
  uint64 OptimalPartitionEncode;
  uint64 TotalDecode;
  uint64 AvailableDecode;
  uint64 MinPartitionDecode;
  uint64 MaxPartitionDecode;
  uint64 OptimalPartitionDecode;
  uint64 TotalCompute;
  uint64 AvailableCompute;
  uint64 MinPartitionCompute;
  uint64 MaxPartitionCompute;
  uint64 OptimalPartitionCompute;
};
```

## <a name="members"></a>Member

Die **Msvm \_ PartitionableGpu-Klasse** verfügt über folgende Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Msvm \_ PartitionableGpu-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**AvailableCompute**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die verfügbare Anzahl von Compute-Engines, die in der GPU-Partition angezeigt werden.

</dd> <dt>

**AvailableDecode**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die verfügbare Menge an Decodierungs-Engines, die in der GPU-Partition angezeigt werden.

</dd> <dt>

**AvailableEncode**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die verfügbare Menge an Codierungs-Engines, die in der GPU-Partition angezeigt werden.

</dd> <dt>

**AvailableVRAM**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die verfügbare Menge an VRAM, die in der GPU-Partition angezeigt wird.

</dd> <dt>

**MaxPartitionCompute**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die maximale Anzahl von Compute-Engines, die in der GPU-Partition angezeigt werden.

</dd> <dt>

**MaxPartitionDecode**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die maximale Anzahl von Decodierungs-Engines, die in der GPU-Partition angezeigt werden.

</dd> <dt>

**MaxPartitionEncode**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die maximale Menge an Codierungs-Engines, die in der GPU-Partition angezeigt werden.

</dd> <dt>

**MaxPartitionVRAM**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die maximale Menge an VRAM, die in der GPU-Partition angezeigt wird.

</dd> <dt>

**MinPartitionCompute**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Mindestmenge von Compute-Engines, die in der GPU-Partition angezeigt werden.

</dd> <dt>

**MinPartitionDecode**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Mindestmenge an Decodierungs-Engines, die in der GPU-Partition angezeigt werden.

</dd> <dt>

**MinPartitionEncode**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Minumummenge der Codierungs-Engines, die in der GPU-Partition angezeigt werden.

</dd> <dt>

**MinPartitionVRAM**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Mindestmenge von VRAM, die in der GPU-Partition angezeigt wird.

</dd> <dt>

**OptimalPartitionCompute**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die optimale Anzahl von Compute-Engines, die in der GPU-Partition angezeigt werden.

</dd> <dt>

**OptimalPartitionDecode**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die optimale Menge an Decodierungs-Engines, die in der GPU-Partition angezeigt werden.

</dd> <dt>

**OptimalPartitionEncode**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die optimale Menge an Codierungs-Engines, die in der GPU-Partition angezeigt werden.

</dd> <dt>

**OptimalPartitionVRAM**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die optimale Menge an VRAM, die in der GPU-Partition angezeigt wird.

</dd> <dt>

**PartitionCount**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Die Menge der GPU-Partitionen, in die die physische GPU aufgeteilt wird.

</dd> <dt>

**TotalCompute**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Gesamtmenge der Compute-Engines, die in der GPU-Partition angezeigt werden.

</dd> <dt>

**TotalDecode**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Gesamtmenge der Decodierungs-Engines, die in der GPU-Partition angezeigt werden.

</dd> <dt>

**TotalEncode**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Gesamtmenge der Codierungs-Engines, die in der GPU-Partition angezeigt werden.

</dd> <dt>

**TotalVRAM**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Gesamtmenge von VRAM, die in der GPU-Partition angezeigt wird.

</dd> <dt>

**ValidPartitionCounts**
</dt> <dd> <dl> <dt>

Datentyp: **uint16-Array**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Ein Array gültiger GPU-Partitionsoptionen, in die die physische GPU aufgeteilt werden kann.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10 Desktop-Apps, Version 1703 \[\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**\_CIM-ComputerSystem**](cim-computersystem.md)
</dt> </dl>

 

 




