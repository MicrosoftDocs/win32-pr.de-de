---
description: Diese Klasse ist die Ereignistypklasse für Threadstartereignisse. Die folgende Syntax wird durch einen MOF-Code vereinfacht.
ms.assetid: 412de56f-4f54-46e8-ab60-d47371247e79
title: Thread_V1_TypeGroup1-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Thread_V1_TypeGroup1
- Thread_V1_TypeGroup1.ProcessId
- Thread_V1_TypeGroup1.TThreadId
- Thread_V1_TypeGroup1.StackBase
- Thread_V1_TypeGroup1.StackLimit
- Thread_V1_TypeGroup1.UserStackBase
- Thread_V1_TypeGroup1.UserStackLimit
- Thread_V1_TypeGroup1.StartAddr
- Thread_V1_TypeGroup1.Win32StartAddr
- Thread_V1_TypeGroup1.WaitMode
api_type:
- NA
api_location: ''
ms.openlocfilehash: 90d8f4afe9d78cc774dea3159a728ccc6d4db52314e692594d026f7e4fe2161c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069440"
---
# <a name="thread_v1_typegroup1-class"></a>Thread \_ V1 \_ TypeGroup1-Klasse

Diese Klasse ist die Ereignistypklasse für Threadstartereignisse.

Die folgende Syntax wird durch einen MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[EventType{1, 3}, EventTypeName{"Start", "DCStart"}]
class Thread_V1_TypeGroup1 : Thread_V1
{
  uint32 ProcessId;
  uint32 TThreadId;
  uint32 StackBase;
  uint32 StackLimit;
  uint32 UserStackBase;
  uint32 UserStackLimit;
  uint32 StartAddr;
  uint32 Win32StartAddr;
  sint8  WaitMode;
};
```

## <a name="members"></a>Member

Die **\_ Thread V1 \_ TypeGroup1-Klasse** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Thread \_ V1 \_ TypeGroup1-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

ProcessId
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(1)
</dt> </dl>

Prozessbezeichner des am Ereignis beteiligten Threads.

**Windows Server 2003:** Enthält den Format("x")-Qualifizierer.

</dd> <dt>

StackBase
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(3), Zeiger
</dt> </dl>

Basisadresse des Threadstapels.

</dd> <dt>

StackLimit
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(4), Zeiger
</dt> </dl>

Der Grenzwert des Stapels des Threads.

</dd> <dt>

StartAddr
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(7), Zeiger
</dt> </dl>

Speicheradresse, an der die Ablaufverfolgung gestartet wird.

</dd> <dt>

TThreadId
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(2)
</dt> </dl>

Threadbezeichner des Threads, der am Ereignis beteiligt ist.

**Windows Server 2003:** Enthält den Format("x")-Qualifizierer.

</dd> <dt>

UserStackBase
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(5), Zeiger
</dt> </dl>

Basisadresse des Benutzermodusstapels des Threads.

</dd> <dt>

UserStackLimit
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(6), Zeiger
</dt> </dl>

Der Grenzwert des Benutzermodusstapels des Threads.

</dd> <dt>

WaitMode
</dt> <dd> <dl> <dt>

Datentyp: **sint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(9), Format("c")
</dt> </dl>

Wird nicht verwendet.

</dd> <dt>

Win32StartAddr
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(8), Zeiger
</dt> </dl>

Startadresse der Funktion, die von diesem Thread ausgeführt werden soll.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Thread \_ V1**](thread-v1.md)
</dt> </dl>

 

 




