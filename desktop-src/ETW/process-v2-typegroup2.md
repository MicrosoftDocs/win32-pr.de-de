---
description: Diese Klasse ist die Ereignistypklasse für Prozesszählerereignisse. Die folgende Syntax wird durch einen MOF-Code vereinfacht.
ms.assetid: 7f1fa1c4-a2ff-4a1c-ac9d-e922a13c99a1
title: Process_V2_TypeGroup2-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Process_V2_TypeGroup2
- Process_V2_TypeGroup2.ProcessId
- Process_V2_TypeGroup2.PageFaultCount
- Process_V2_TypeGroup2.HandleCount
- Process_V2_TypeGroup2.Reserved
- Process_V2_TypeGroup2.PeakVirtualSize
- Process_V2_TypeGroup2.PeakWorkingSetSize
- Process_V2_TypeGroup2.PeakPagefileUsage
- Process_V2_TypeGroup2.QuotaPeakPagedPoolUsage
- Process_V2_TypeGroup2.QuotaPeakNonPagedPoolUsage
- Process_V2_TypeGroup2.VirtualSize
- Process_V2_TypeGroup2.WorkingSetSize
- Process_V2_TypeGroup2.PagefileUsage
- Process_V2_TypeGroup2.QuotaPagedPoolUsage
- Process_V2_TypeGroup2.QuotaNonPagedPoolUsage
- Process_V2_TypeGroup2.PrivatePageCount
api_type:
- NA
api_location: ''
ms.openlocfilehash: 51c24e12ed423b6240daeefee0b69a40f9b14b86813ca83cb09f74f807e24429
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069950"
---
# <a name="process_v2_typegroup2-class"></a>Process \_ V2 \_ TypeGroup2-Klasse

Diese Klasse ist die Ereignistypklasse für Prozesszählerereignisse.

Die folgende Syntax wird durch einen MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[EventType{32, 33}, EventTypeName{"PerfCtr", PerfCtrRundown"}]
class Process_V2_TypeGroup2 : Process_V2
{
  uint32 ProcessId;
  uint32 PageFaultCount;
  uint32 HandleCount;
  uint32 Reserved;
  object PeakVirtualSize;
  object PeakWorkingSetSize;
  object PeakPagefileUsage;
  object QuotaPeakPagedPoolUsage;
  object QuotaPeakNonPagedPoolUsage;
  object VirtualSize;
  object WorkingSetSize;
  object PagefileUsage;
  object QuotaPagedPoolUsage;
  object QuotaNonPagedPoolUsage;
  object PrivatePageCount;
};
```

## <a name="members"></a>Member

Die **Klasse Process \_ V2 \_ TypeGroup2** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Klasse Process \_ V2 \_ TypeGroup2** verfügt über diese Eigenschaften.

<dl> <dt>

**HandleCount**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(3)
</dt> </dl>

Anzahl der verwendeten Handles.

</dd> <dt>

**PageFaultCount**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(2)
</dt> </dl>

Anzahl der Seitenfehler.

</dd> <dt>

**PagefileUsage**
</dt> <dd> <dl> <dt>

Datentyp: **Objekt**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(12), Extension("SizeT")
</dt> </dl>

Aktuelle Nutzung von Seitendatei.

</dd> <dt>

**PeakPagefileUsage**
</dt> <dd> <dl> <dt>

Datentyp: **Objekt**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(7), Extension("SizeT")
</dt> </dl>

Die größte verwendete Seitendateigröße.

</dd> <dt>

**PeakVirtualSize**
</dt> <dd> <dl> <dt>

Datentyp: **Objekt**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(5), Extension("SizeT")
</dt> </dl>

Die größte verwendete virtuelle Seitengröße.

</dd> <dt>

**PeakWorkingSetSize**
</dt> <dd> <dl> <dt>

Datentyp: **Objekt**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(6), Extension("SizeT")
</dt> </dl>

Die größte verwendete Arbeitssatzgröße.

</dd> <dt>

**PrivatePageCount**
</dt> <dd> <dl> <dt>

Datentyp: **Objekt**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(15), Extension("SizeT")
</dt> </dl>

Aktuelle Anzahl privater physischer Seiten.

</dd> <dt>

ProcessId
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(1), Format("x")
</dt> </dl>

Globaler Prozessbezeichner, den Sie zum Identifizieren eines Prozesses verwenden können. Der Wert ist ab dem Zeitpunkt gültig, zu dem ein Prozess erstellt wird, bis er beendet wird.

</dd> <dt>

**QuotaNonPagedPoolUsage**
</dt> <dd> <dl> <dt>

Datentyp: **Objekt**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(14), Extension("SizeT")
</dt> </dl>

Aktuelle speicherbasierte Speicherauslastung ohne Aus pagen.

</dd> <dt>

**QuotaPagedPoolUsage**
</dt> <dd> <dl> <dt>

Datentyp: **Objekt**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(13), Extension("SizeT")
</dt> </dl>

Aktuelle Auspagespeicherauslastung mit Committed.

</dd> <dt>

**QuotaPeakNonPagedPoolUsage**
</dt> <dd> <dl> <dt>

Datentyp: **Objekt**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(9), Extension("SizeT")
</dt> </dl>

Größter verwendeter nicht aus seiteringsseitiger Arbeitsspeicher mit einem Committed.

</dd> <dt>

**QuotaPeakPagedPoolUsage**
</dt> <dd> <dl> <dt>

Datentyp: **Objekt**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(8), Extension("SizeT")
</dt> </dl>

Der größte aus paged-Speicher, für den ein Committed verwendet wurde.

</dd> <dt>

**Reserved**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(4)
</dt> </dl>

Reserviert.

</dd> <dt>

**VirtualSize**
</dt> <dd> <dl> <dt>

Datentyp: **Objekt**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(10), Extension("SizeT")
</dt> </dl>

Aktuelle Größe der virtuellen Seite.

</dd> <dt>

**WorkingSetSize**
</dt> <dd> <dl> <dt>

Datentyp: **Objekt**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(11), Extension("SizeT")
</dt> </dl>

Aktuelle Arbeitssatzgröße.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Ereignisse werden protokolliert, wenn der Prozess beendet wird. Das -Ereignis gibt an, wie ein Prozess die Speicherauslastung verarbeitet hat.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Prozess \_ V2**](process-v2.md)
</dt> </dl>

 

 




