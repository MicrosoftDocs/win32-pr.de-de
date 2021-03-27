---
description: Diese Klasse ist die Ereignistyp Klasse für Kontextwechsel Ereignisse. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: 3f9f84d0-18a9-493c-b104-8236b2bd8404
title: Cswitch-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSwitch
- CSwitch.NewThreadId
- CSwitch.OldThreadId
- CSwitch.NewThreadPriority
- CSwitch.OldThreadPriority
- CSwitch.PreviousCState
- CSwitch.SpareByte
- CSwitch.OldThreadWaitReason
- CSwitch.OldThreadWaitMode
- CSwitch.OldThreadState
- CSwitch.OldThreadWaitIdealProcessor
- CSwitch.NewThreadWaitTime
- CSwitch.Reserved
api_type:
- NA
api_location: ''
ms.openlocfilehash: 91004ca276140271e8d73c3fc226e83c4e03d1fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214867"
---
# <a name="cswitch-class"></a>Cswitch-Klasse

Diese Klasse ist die Ereignistyp Klasse für Kontextwechsel Ereignisse.

Die folgende Syntax wird durch den MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[EventType{36}, EventTypeName{"CSwitch"}]
class CSwitch : Thread_V2
{
  uint32 NewThreadId;
  uint32 OldThreadId;
  sint8  NewThreadPriority;
  sint8  OldThreadPriority;
  uint8  PreviousCState;
  sint8  SpareByte;
  sint8  OldThreadWaitReason;
  sint8  OldThreadWaitMode;
  sint8  OldThreadState;
  sint8  OldThreadWaitIdealProcessor;
  uint32 NewThreadWaitTime;
  uint32 Reserved;
};
```

## <a name="members"></a>Member

Die **cswitch** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **cswitch** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Newthreadid**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (1), Format ("x")
</dt> </dl>

Neue Thread-ID nach dem Switch.

</dd> <dt>

**Newthreadpriority**
</dt> <dd> <dl> <dt>

Datentyp: **sint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (3)
</dt> </dl>

Thread Priorität des neuen Threads.

</dd> <dt>

**Newthreadwaittime**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (11), Format ("x")
</dt> </dl>

Die Wartezeit für den neuen Thread.

</dd> <dt>

**Oldthreadid**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (2), Format ("x")
</dt> </dl>

Vorherige Thread-ID.

</dd> <dt>

**Oldthreadpriority**
</dt> <dd> <dl> <dt>

Datentyp: **sint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (4)
</dt> </dl>

Thread Priorität des vorherigen Threads.

</dd> <dt>

**Oldthreadstate**
</dt> <dd> <dl> <dt>

Datentyp: **sint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (9)
</dt> </dl>

Zustand des vorherigen Threads. Im folgenden sind die möglichen Zustands Werte aufgeführt:

| State | BESCHREIBUNG                                   |
|-------|-----------------------------------------------|
| 0     | Initialisiert                                   |
| 1     | Bereit                                         |
| 2     | Wird ausgeführt                                       |
| 3     | Standby                                       |
| 4     | Beendet                                    |
| 5     | Warten                                       |
| 6     | Übergang                                    |
| 7     | Deferredready (für Windows Server 2003 hinzugefügt) |



 

</dd> <dt>

**Oldthreadwaitidealprocessor**
</dt> <dd> <dl> <dt>

Datentyp: **sint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (10), Format ("x")
</dt> </dl>

Die ideale Wartezeit für den vorherigen Thread.

</dd> <dt>

**Oldthreadwaitmode**
</dt> <dd> <dl> <dt>

Datentyp: **sint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (8)
</dt> </dl>

Der Wartemodus für den vorherigen Thread. Folgende Werte sind möglich:

| State | BESCHREIBUNG |
|-------|-------------|
| 0     | Kernel Mode  |
| 1     | UserMode    |



 

</dd> <dt>

**Oldthreadwaitreason**
</dt> <dd> <dl> <dt>

Datentyp: **sint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (7)
</dt> </dl>

Der Warte Grund für den vorherigen Thread. Folgende Werte sind möglich:

| State | BESCHREIBUNG       |
|-------|-------------------|
| 0     | Executive         |
| 1     | Freepage          |
| 2     | PageIn            |
| 3     | Poolallocation    |
| 4     | Delta Execution    |
| 5     | Ausgesetzt         |
| 6     | Userrequest       |
| 7     | Wrexecutive       |
| 8     | Wrfreepage        |
| 9     | Wrpagein          |
| 10    | Wrpoolallocation  |
| 11    | Wrdelta-Ausführungszeit  |
| 12    | Wrangeh alten       |
| 13    | Wruserrequest     |
| 14    | Wreventpair       |
| 15    | Wrqueue           |
| 16    | Wrlpcreceive      |
| 17    | Wrlpkreply        |
| 18    | Wrvirtualmemory   |
| 19    | Wrpageout         |
| 20    | Wrrendezvous      |
| 21    | Wrkeyedebug      |
| 22    | Wrterminiert      |
| 23    | Wrprocessinswap   |
| 24    | Wrcpuratecontrol  |
| 25    | Wrcalloutstack    |
| 26    | Wrkernel          |
| 27    | Wrresource        |
| 28    | Wrpushlock        |
| 29    | Wrmutex           |
| 30    | Wrquantenend      |
| 31    | Wrdispatchint     |
| 32    | Wrpreempted       |
| 33    | Wryieldexecution  |
| 34    | Wrfastmutex       |
| 35    | Wrguardecodmutex    |
| 36    | Wrrundown         |
| 37    | Maximumwaitreason |



 

</dd> <dt>

**Previouscstate**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (5)
</dt> </dl>

Der Index des C-Zustands, der zuletzt vom Prozessor verwendet wurde. Der Wert 0 steht für den leichteren Leerlaufzustand mit höheren Werten, die tiefere C-Zustände darstellen.

</dd> <dt>

**Reserved**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (12)
</dt> </dl>

Reserviert.

</dd> <dt>

**Sparebyte**
</dt> <dd> <dl> <dt>

Datentyp: **sint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (6)
</dt> </dl>

Nicht verwendet.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Ereignisse führen zu einer hohen Anzahl von Ereignissen.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Aden**](thread.md)
</dt> <dt>

[**Thread \_ v2**](thread-v2.md)
</dt> </dl>

 

 




