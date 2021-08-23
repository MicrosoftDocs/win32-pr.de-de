---
description: 'SystemConfig_V0_CPU-Klasse: Diese Klasse ist die Ereignistypklasse für CPU-Konfigurationsereignisse.'
ms.assetid: 9ca77676-ff0e-4c47-ae4e-f8192376d3ca
title: SystemConfig_V0_CPU-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_V0_CPU
- SystemConfig_V0_CPU.MHz
- SystemConfig_V0_CPU.NumberOfProcessors
- SystemConfig_V0_CPU.MemSize
- SystemConfig_V0_CPU.PageSize
- SystemConfig_V0_CPU.AllocationGranularity
- SystemConfig_V0_CPU.ComputerName
- SystemConfig_V0_CPU.DomainName
api_type:
- NA
api_location: ''
ms.openlocfilehash: d533eb06aca34ffdb5996bb0c08c7d40645042e7ccab7645cfd3a04adf0db2ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069660"
---
# <a name="systemconfig_v0_cpu-class"></a>SystemConfig \_ \_ V0-CPU-Klasse

Diese Klasse ist die Ereignistypklasse für CPU-Konfigurationsereignisse.

Die folgende Syntax wird durch einen MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[EventType(10), EventTypeName("CPU")]
class SystemConfig_V0_CPU : SystemConfig_V0
{
  uint32 MHz;
  uint32 NumberOfProcessors;
  uint32 MemSize;
  uint32 PageSize;
  uint32 AllocationGranularity;
  char16 ComputerName[];
  char16 DomainName[];
};
```

## <a name="members"></a>Member

Die **SystemConfig \_ \_ V0-CPU-Klasse** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **SystemConfig \_ \_ V0-CPU-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**AllocationGranularity**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (5)
</dt> </dl>

Granularität, mit der virtueller Arbeitsspeicher zugeordnet wird.

</dd> <dt>

**ComputerName**
</dt> <dd> <dl> <dt>

Datentyp: **char16-Array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (6), **Max** (256)
</dt> </dl>

Name des Computers

</dd> <dt>

**DomainName**
</dt> <dd> <dl> <dt>

Datentyp: **char16-Array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (7), **Max** (132)
</dt> </dl>

Name der Domäne, in der der Computer Mitglied ist.

</dd> <dt>

**MemSize**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (3)
</dt> </dl>

Gesamtmenge des für das Betriebssystem verfügbaren physischen Arbeitsspeichers.

</dd> <dt>

**Mhz**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (1)
</dt> </dl>

Maximale Geschwindigkeit des Prozessors in Megahertz.

</dd> <dt>

**NumberOfProcessors**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (2)
</dt> </dl>

Anzahl der Prozessoren auf dem Computer.

</dd> <dt>

**Pagesize**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (4)
</dt> </dl>

Größe einer Auslagerungsseite in Bytes.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**SystemConfig \_ V0**](systemconfig-v0.md)
</dt> </dl>

 

 




