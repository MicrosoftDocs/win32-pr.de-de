---
description: Diese Klasse ist die Ereignistypklasse für Stapelablaufverfolgungsereignisse.
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
ms.openlocfilehash: 672d8fc609c14a43ca2692b5cf8a46356a00cccb9c06371e515bc102706c3638
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069700"
---
# <a name="stackwalk_event-class"></a>\_StackWalk-Ereignisklasse

Diese Klasse ist die Ereignistypklasse für Stapelablaufverfolgungsereignisse.

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

Die **\_ StackWalk-Ereignisklasse** verfügt über folgende Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **\_ StackWalk-Ereignisklasse** verfügt über diese Eigenschaften.

<dl> <dt>

**EventTimeStamp**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(1)
</dt> </dl>

Ursprünglicher Ereigniszeitstempel aus dem Ereignisheader. Verwenden Sie diesen Zeitstempel, um den Stapel mit einem Ereignis abzugleichen.

</dd> <dt>

**Stack1**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(4), Zeiger
</dt> </dl>

Adresse des Aufrufs.

</dd> <dt>

**Stack192**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(195), Zeiger
</dt> </dl>

Adresse des Aufrufs.

</dd> <dt>

**StackProcess**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(2), format("x")
</dt> </dl>

Der Prozessbezeichner des ursprünglichen Ereignisses.

</dd> <dt>

**StackThread**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(3)
</dt> </dl>

Der Threadbezeichner des ursprünglichen Ereignisses.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Beachten Sie, dass die Klasse nicht alle **Stack*n***-Eigenschaften zeigt, die zwischen **Stack1** und **Stack192** vorhanden sind. Verwenden Sie die Größe des Ereignisses, um zu bestimmen, wie viele **Stack*n***-Eigenschaften gültige Adressen enthalten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>              |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/> |



 

 




