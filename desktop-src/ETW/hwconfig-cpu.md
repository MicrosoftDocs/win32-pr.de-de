---
description: Die \_ HWConfig-CPU-Klasse ist die Ereignistypklasse für CPU-Konfigurationsereignisse. Die folgende Syntax wird durch einen MOF-Code vereinfacht.
ms.assetid: a94714c6-009c-4300-a0a0-b7b3ce94f91e
title: HWConfig_CPU-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HWConfig_CPU
- HWConfig_CPU.MHz
- HWConfig_CPU.NumberOfProcessors
- HWConfig_CPU.MemSize
- HWConfig_CPU.PageSize
- HWConfig_CPU.AllocationGranularity
- HWConfig_CPU.ComputerName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 9987095c8c2a1e9b9abbb54eb66816277428e2296c98395d36340297cc541bfa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119070190"
---
# <a name="hwconfig_cpu-class"></a>\_HWConfig-CPU-Klasse

Die **\_ HWConfig-CPU-Klasse** ist die Ereignistypklasse für CPU-Konfigurationsereignisse.

Die folgende Syntax wird durch einen MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[EventType(10), EventTypeName("CPU")]
class HWConfig_CPU : HWConfig
{
  uint32 MHz;
  uint32 NumberOfProcessors;
  uint32 MemSize;
  uint32 PageSize;
  uint32 AllocationGranularity;
  string ComputerName;
};
```

## <a name="members"></a>Member

Die **\_ HWConfig-CPU-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **\_ HWConfig-CPU-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

AllocationGranularity
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(5)
</dt> </dl>

Granularität, mit der virtueller Arbeitsspeicher zugeordnet wird.

</dd> <dt>

Computername
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(6), StringTermination("NullTerminated"), Format("w")
</dt> </dl>

Name des Computers

</dd> <dt>

MemSize
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(3)
</dt> </dl>

Gesamtmenge des für das Betriebssystem verfügbaren physischen Arbeitsspeichers.

</dd> <dt>

Mhz
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(1)
</dt> </dl>

Maximale Geschwindigkeit des Prozessors in Megahertz.

</dd> <dt>

NumberOfProcessors
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(2)
</dt> </dl>

Anzahl der Prozessoren auf dem Computer.

</dd> <dt>

PageSize
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(4)
</dt> </dl>

Größe einer Auslagerungsseite in Bytes.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**HWConfig**](hwconfig.md)
</dt> </dl>

 

 




