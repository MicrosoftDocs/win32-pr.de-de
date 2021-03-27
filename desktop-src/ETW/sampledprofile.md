---
description: Diese Klasse ist die Ereignistyp Klasse für samplingprofilereignisse. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: 75ea1e5e-2554-40bb-aa9d-c6d4942c5801
title: Sampledprofile-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SampledProfile
- SampledProfile.InstructionPointer
- SampledProfile.ThreadId
- SampledProfile.Count
api_type:
- NA
api_location: ''
ms.openlocfilehash: 3d7a69eef1a2a7988569ffcd930b73a559e18d90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980553"
---
# <a name="sampledprofile-class"></a>Sampledprofile-Klasse

Diese Klasse ist die Ereignistyp Klasse für samplingprofilereignisse.

Die folgende Syntax wird durch den MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[EventType{46}, EventTypeName{"SampleProfile"}]
class SampledProfile : PerfInfo
{
  uint32 InstructionPointer;
  uint32 ThreadId;
  uint32 Count;
};
```

## <a name="members"></a>Member

Die **sampledprofile** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **sampledprofile** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Count**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (3)
</dt> </dl>

Nicht verwendet.

</dd> <dt>

**Instructionpointer**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (1), Zeiger
</dt> </dl>

Adresse des Abbilds, das zum Zeitpunkt des Prozessors für den Prozessor ausgeführt wurde.

</dd> <dt>

**ThreadID**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (2)
</dt> </dl>

Thread Bezeichner des Threads, der zum Zeitpunkt der Stichprobenentnahme des Prozessors ausgeführt wurde.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Ereignisse stellen ein erfassten Ausführungsprofil bereit. Das Ereignis zeichnet auf, was auf dem Prozessor ausgeführt wurde. Sie können die Image-Ereignisse verwenden, um das binäre Modul zu identifizieren, das diese Anweisung enthält. Sie können diese Informationen dann verwenden, um ein Ausführungsprofil für die Dauer der Ablauf Verfolgung zu erstellen.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

 




