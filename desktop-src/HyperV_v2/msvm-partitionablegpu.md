---
description: Stellt eine Partitionier Bare GPU dar. Jede GPU kann in eine Reihe von GPU-Partitionen aufgeteilt werden, die einem virtuellen Computer als vgpu zugewiesen werden können.
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
ms.openlocfilehash: 7f82904608a8e2ee4dfa13942066d57d35d511f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868495"
---
# <a name="msvm_partitionablegpu-class"></a>MSVM \_ partitionablegpu-Klasse

Stellt eine Partitionier Bare GPU dar. Jede GPU kann in eine Reihe von GPU-Partitionen aufgeteilt werden, die einem virtuellen Computer als vgpu zugewiesen werden können.

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

Die **MSVM \_ partitionablegpu** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSVM \_ partitionablegpu** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Availablecompute**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die verfügbare Menge an computeengines, die in der GPU-Partition angezeigt werden.

</dd> <dt>

**Availabledecode**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die verfügbare Anzahl von decodieren-Engines, die in der GPU-Partition angezeigt werden.

</dd> <dt>

**Availablecodieren**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die verfügbare Anzahl der codierungsmodule, die in der GPU-Partition angezeigt werden.

</dd> <dt>

**Availablevram**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die verfügbare VRAM-Größe, die in der GPU-Partition angezeigt wird.

</dd> <dt>

**Maxpartitioncompute**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die maximale Menge an computeengines, die in der GPU-Partition angezeigt werden.

</dd> <dt>

**Maxpartitiondecode**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die maximale Anzahl von decodieren-Engines, die in der GPU-Partition angezeigt werden.

</dd> <dt>

**Maxpartitioncocode**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die maximale Anzahl der codierungsmodule, die in der GPU-Partition angezeigt werden.

</dd> <dt>

**Maxpartitionvram**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die maximale VRAM-Größe, die in der GPU-Partition angezeigt wird.

</dd> <dt>

**Minpartitioncompute**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die minimale Menge an computeengines, die in der GPU-Partition angezeigt werden.

</dd> <dt>

**Minpartitiondecode**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die minimale Anzahl von decodieren-Engines, die in der GPU-Partition angezeigt werden.

</dd> <dt>

**Minpartitioncocode**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der minimale Betrag der Codierungs-Engines, der in der GPU-Partition angezeigt wird.

</dd> <dt>

**Minpartitionvram**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die minimale VRAM-Größe, die in der GPU-Partition angezeigt wird.

</dd> <dt>

**Optimalpartitioncompute**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die optimale Menge an computeengines, die in der GPU-Partition angezeigt werden.

</dd> <dt>

**Optimalpartitiondecode**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die optimale Menge an Decodieren von Modulen, die in der GPU-Partition angezeigt werden.

</dd> <dt>

**Optimalpartitioncocode**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die optimale Menge der codierungsmodule, die in der GPU-Partition angezeigt werden.

</dd> <dt>

**Optimalpartitionvram**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die optimale VRAM-Größe, die in der GPU-Partition angezeigt wird.

</dd> <dt>

**PartitionCount**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Die Menge der GPU-Partitionen, in die die physische GPU aufgeteilt ist.

</dd> <dt>

**Totalcompute**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Gesamtmenge der computemodule, die in der GPU-Partition angezeigt werden.

</dd> <dt>

**Totaldecode**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Gesamtmenge der decodierungsmodule, die in der GPU-Partition angezeigt werden.

</dd> <dt>

**Totalcodieren**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Gesamtmenge der codierungsmodule, die in der GPU-Partition angezeigt werden.

</dd> <dt>

**Totalvram**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Gesamtmenge des VRAM, der in der GPU-Partition angezeigt wird.

</dd> <dt>

**Validpartitioncounts**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16** Array
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Ein Array gültiger GPU-Partitions Optionen, in die die physische GPU aufgeteilt werden kann.

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

[**CIM- \_ Computersystem**](cim-computersystem.md)
</dt> </dl>

 

 




