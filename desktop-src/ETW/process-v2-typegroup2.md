---
description: Diese Klasse ist die Ereignistyp Klasse für Prozess-Counter-Ereignisse. Die folgende Syntax wird durch den MOF-Code vereinfacht.
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
ms.openlocfilehash: 284b77da03b53f9c2662c8729a7bf6606c45630a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867707"
---
# <a name="process_v2_typegroup2-class"></a>Process \_ v2 \_ TypeGroup2-Klasse

Diese Klasse ist die Ereignistyp Klasse für Prozess-Counter-Ereignisse.

Die folgende Syntax wird durch den MOF-Code vereinfacht.

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

Die **Process \_ v2 \_ TypeGroup2** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Process \_ v2 \_ TypeGroup2** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**HandleCount**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (3)
</dt> </dl>

Anzahl der verwendeten Handles.

</dd> <dt>

**Pagefehlercount**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (2)
</dt> </dl>

Anzahl der Seiten Fehler.

</dd> <dt>

**PageFileUsage**
</dt> <dd> <dl> <dt>

Datentyp: **Object**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (12), Erweiterung ("sizet")
</dt> </dl>

Aktuelle Verwendung der Auslagerungs Datei.

</dd> <dt>

**"Peer Page File Usage"**
</dt> <dd> <dl> <dt>

Datentyp: **Object**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (7), Erweiterung ("sizet")
</dt> </dl>

Die größte verwendete Seiten Dateigröße.

</dd> <dt>

**Peakvirtualsize**
</dt> <dd> <dl> <dt>

Datentyp: **Object**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (5), Erweiterung ("sizet")
</dt> </dl>

Die größte verwendete Größe der virtuellen Seite.

</dd> <dt>

**PeakWorkingSetSize**
</dt> <dd> <dl> <dt>

Datentyp: **Object**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (6), Erweiterung ("sizet")
</dt> </dl>

Die größte verwendete Workingsetgröße.

</dd> <dt>

**PrivatePageCount**
</dt> <dd> <dl> <dt>

Datentyp: **Object**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (15), Extension ("sizet")
</dt> </dl>

Aktuelle private physische Seitenanzahl.

</dd> <dt>

ProcessId
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (1), Format ("x")
</dt> </dl>

Die globale Prozess-ID, mit der Sie einen Prozess identifizieren können. Der Wert ist gültig ab dem Zeitpunkt, zu dem ein Prozess erstellt wird, bis er beendet wird.

</dd> <dt>

**Quotanonpgedpoolusage**
</dt> <dd> <dl> <dt>

Datentyp: **Object**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (14), Erweiterung ("sizet")
</dt> </dl>

Aktuell zugesicherte, nicht auslagerbare Speicherauslastung.

</dd> <dt>

**Quotapgedpoolusage**
</dt> <dd> <dl> <dt>

Datentyp: **Object**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (13), Erweiterung ("sizet")
</dt> </dl>

Aktuelle zugesicherte auslagerter Speicherauslastung.

</dd> <dt>

**Quotapeaknonpgedpoolusage**
</dt> <dd> <dl> <dt>

Datentyp: **Object**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (9), Erweiterung ("sizet")
</dt> </dl>

Der größte nicht auslagerbare nicht auslagerbare Speicher wurde verwendet.

</dd> <dt>

**Quotapeakpgedpoolusage**
</dt> <dd> <dl> <dt>

Datentyp: **Object**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (8), Erweiterung ("sizet")
</dt> </dl>

Der größte verwendete auslagerter ausgehenster Speicher.

</dd> <dt>

**Reserved**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (4)
</dt> </dl>

Reserviert.

</dd> <dt>

**VirtualSize**
</dt> <dd> <dl> <dt>

Datentyp: **Object**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (10), Extension ("sizet")
</dt> </dl>

Aktuelle Größe der virtuellen Seite.

</dd> <dt>

**Workingsetsize**
</dt> <dd> <dl> <dt>

Datentyp: **Object**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (11), Erweiterung ("sizet")
</dt> </dl>

Aktuelle Workingsetgröße.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Ereignisse werden protokolliert, wenn der Prozess beendet wird. Das Ereignis gibt an, wie ein Prozess die Speicherauslastung verarbeitet hat.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Prozess \_ v2**](process-v2.md)
</dt> </dl>

 

 




