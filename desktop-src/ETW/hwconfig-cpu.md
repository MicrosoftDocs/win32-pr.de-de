---
description: Die hwconfig- \_ CPU-Klasse ist die Ereignistyp Klasse für CPU-Konfigurations Ereignisse. Die folgende Syntax wird durch den MOF-Code vereinfacht.
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
ms.openlocfilehash: 493952e25080d4a64e018477ca1b45033c8747af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978273"
---
# <a name="hwconfig_cpu-class"></a>Hwconfig- \_ CPU-Klasse

Die **hwconfig- \_ CPU** -Klasse ist die Ereignistyp Klasse für CPU-Konfigurations Ereignisse.

Die folgende Syntax wird durch den MOF-Code vereinfacht.

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

Die **hwconfig- \_ CPU** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **hwconfig- \_ CPU** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

"Zuweisung"-Granularität
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (5)
</dt> </dl>

Die Granularität, mit der der virtuelle Arbeitsspeicher zugewiesen wird.

</dd> <dt>

Computername
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (6), stringbeendigung ("nullterminiert"), Format ("w")
</dt> </dl>

Name des Computers

</dd> <dt>

Memsize
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (3)
</dt> </dl>

Gesamtmenge des für das Betriebssystem verfügbaren physischen Speichers.

</dd> <dt>

Suhr
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (1)
</dt> </dl>

Maximale Geschwindigkeit des Prozessors in Megahertz.

</dd> <dt>

NumberOfProcessors
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (2)
</dt> </dl>

Anzahl der Prozessoren auf dem Computer.

</dd> <dt>

PageSize
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (4)
</dt> </dl>

Größe einer Auslagerungs Seite (in Bytes).

</dd> </dl>

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Hwconfig**](hwconfig.md)
</dt> </dl>

 

 




