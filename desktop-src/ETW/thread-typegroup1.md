---
description: Diese Klasse ist die Ereignistyp Klasse für Ereignisse zum Starten und Beenden von Threads. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: d9e3e33a-0e59-4753-a8d8-5320cbae9d95
title: Thread_TypeGroup1-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Thread_TypeGroup1
- Thread_TypeGroup1.ProcessId
- Thread_TypeGroup1.TThreadId
- Thread_TypeGroup1.StackBase
- Thread_TypeGroup1.StackLimit
- Thread_TypeGroup1.UserStackBase
- Thread_TypeGroup1.UserStackLimit
- Thread_TypeGroup1.Affinity
- Thread_TypeGroup1.Win32StartAddr
- Thread_TypeGroup1.TebBase
- Thread_TypeGroup1.SubProcessTag
- Thread_TypeGroup1.BasePriority
- Thread_TypeGroup1.PagePriority
- Thread_TypeGroup1.IoPriority
- Thread_TypeGroup1.ThreadFlags
api_type:
- NA
api_location: ''
ms.openlocfilehash: 75352efbe044f5fee837c496c394fe28e2dbbbfb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130705"
---
# <a name="thread_typegroup1-class"></a>Thread \_ TypeGroup1-Klasse

Diese Klasse ist die Ereignistyp Klasse für Ereignisse zum Starten und Beenden von Threads.

Die folgende Syntax wird durch den MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[EventType{1, 2, 3, 4}, EventTypeName{"Start", "End", "DCStart", "DCEnd"}]
class Thread_TypeGroup1 : Thread
{
  uint32 ProcessId;
  uint32 TThreadId;
  uint32 StackBase;
  uint32 StackLimit;
  uint32 UserStackBase;
  uint32 UserStackLimit;
  uint32 Affinity;
  uint32 Win32StartAddr;
  uint32 TebBase;
  uint32 SubProcessTag;
  uint8  BasePriority;
  uint8  PagePriority;
  uint8  IoPriority;
  uint8  ThreadFlags;
};
```

## <a name="members"></a>Member

Die **Thread \_ TypeGroup1** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Thread \_ TypeGroup1** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

Affinität
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (7), Zeiger
</dt> </dl>

Der Satz von Prozessoren, auf denen der Thread ausgeführt werden darf.

</dd> <dt>

BasePriority
</dt> <dd> <dl> <dt>

Datentyp: **Uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (11)
</dt> </dl>

Die Zeit Planungs Modul Priorität des Threads (siehe die [**SetThreadPriority**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadpriority) -Funktion).

</dd> <dt>

Iopriority
</dt> <dd> <dl> <dt>

Datentyp: **Uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (13)
</dt> </dl>

Ein e/a-Prioritäts Hinweis zum Planen von IOS, der vom Thread generiert wird

</dd> <dt>

Pagepriority
</dt> <dd> <dl> <dt>

Datentyp: **Uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (12)
</dt> </dl>

Ein Speicherseiten Prioritäts Hinweis für Speicherseiten, auf die der Thread zugreift.

</dd> <dt>

ProcessId
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (1), Format ("x")
</dt> </dl>

Prozess Bezeichner des am Ereignis beteiligten Threads.

</dd> <dt>

StackBase
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (3), Zeiger
</dt> </dl>

Basisadresse des Thread Stapels.

</dd> <dt>

StackLimit
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (4), Zeiger
</dt> </dl>

Grenzwert für den Thread Stapel.

</dd> <dt>

Subprocesstag
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (10), Format ("x")
</dt> </dl>

Identifiziert den Dienst, wenn der Thread einem Dienst gehört. andernfalls 0 (null).

</dd> <dt>

Tebbase
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (9), Zeiger
</dt> </dl>

Basisadresse für Thread Umgebungsblock.

</dd> <dt>

Threadflags
</dt> <dd> <dl> <dt>

Datentyp: **Uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (14)
</dt> </dl>

Nicht verwendet.

</dd> <dt>

Tthreadid
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (2), Format ("x")
</dt> </dl>

Thread Bezeichner des am Ereignis beteiligten Threads.

</dd> <dt>

Userstackbase
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (5), Zeiger
</dt> </dl>

Basisadresse für den benutzermodusstapel des Threads.

</dd> <dt>

Userstacklimit
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (6), Zeiger
</dt> </dl>

Limit für den benutzermodusstapel des Threads.

</dd> <dt>

Win32StartAddr
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (8), Zeiger
</dt> </dl>

Die Startadresse der Funktion, die von diesem Thread ausgeführt werden soll.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die Ereignis Typen DCStart und DCEnd zählen die Threads, die derzeit zum Zeitpunkt der Kernel Sitzung ausgeführt werden.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Aden**](thread.md)
</dt> </dl>

 

 
