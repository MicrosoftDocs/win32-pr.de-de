---
description: Diese Klasse ist die Ereignistyp Klasse für Stapel Ablauf Verfolgungs Ereignisse.
ms.assetid: 05117bd6-a39c-42f3-8aed-c6f758f946c6
title: StackWalk_Event-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StackWalk_Event
- StackWalk_Event.EventTimeStamp
- StackWalk_Event.StackProcess
- StackWalk_Event.StackThread
- StackWalk_Event.Stack1
- StackWalk_Event.Stack192
api_type:
- NA
api_location: ''
ms.openlocfilehash: 746a7f2a9b5f6bb6316bf0d0e20e5645cea15a7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980081"
---
# <a name="stackwalk_event-class"></a>Stackwalk ( \_ Ereignisklasse)

Diese Klasse ist die Ereignistyp Klasse für Stapel Ablauf Verfolgungs Ereignisse.

Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.

## <a name="syntax"></a>Syntax

``` syntax
[EventType{32}, EventTypeName{"Stack"}]
class StackWalk_Event : StackWalk
{
  uint64 EventTimeStamp;
  uint32 StackProcess;
  uint32 StackThread;
  uint32 Stack1;
  uint32 Stack192;
};
```

## <a name="members"></a>Member

Die **Stackwalk- \_ Ereignis** Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Stackwalk- \_ Ereignis** Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Eventtimestamp**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (1)
</dt> </dl>

Ursprünglicher ereigniszeitstempel aus dem Ereignis Header. Verwenden Sie diesen Zeitstempel, um den Stapel mit einem Ereignis zu vergleichen.

</dd> <dt>

**Stack1**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (4), Zeiger
</dt> </dl>

Adresse des Aufrufes.

</dd> <dt>

**Stack192**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (195), Zeiger
</dt> </dl>

Adresse des Aufrufes.

</dd> <dt>

**Stackprocess**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (2), Format ("x")
</dt> </dl>

Der Prozess Bezeichner des ursprünglichen Ereignisses.

</dd> <dt>

**Stackthread**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (3)
</dt> </dl>

Der Thread Bezeichner des ursprünglichen Ereignisses.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Beachten Sie, dass die-Klasse nicht alle **Stapel * n***-Eigenschaften anzeigt, die zwischen **Stack1** und **Stack192** vorhanden sind. Verwenden Sie die Größe des Ereignisses, um zu bestimmen, wie viele **Stapel * n***-Eigenschaften gültige Adressen enthalten.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/> |



 

 




