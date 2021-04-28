---
description: 'Thread_V2_TypeGroup1 Klasse: Diese Klasse ist die Ereignistypklasse für Threadstart- und -endereignisse. Die folgende Syntax wird durch MOF-Code vereinfacht.'
ms.assetid: c24b4bc9-2a05-444c-be41-b4dfd0511b93
title: Thread_V2_TypeGroup1-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Thread_V2_TypeGroup1
- Thread_V2_TypeGroup1.ProcessId
- Thread_V2_TypeGroup1.TThreadId
- Thread_V2_TypeGroup1.StackBase
- Thread_V2_TypeGroup1.StackLimit
- Thread_V2_TypeGroup1.UserStackBase
- Thread_V2_TypeGroup1.UserStackLimit
- Thread_V2_TypeGroup1.StartAddr
- Thread_V2_TypeGroup1.Win32StartAddr
- Thread_V2_TypeGroup1.TebBase
- Thread_V2_TypeGroup1.SubProcessTag
api_type:
- NA
api_location: ''
ms.openlocfilehash: 24ac4655fc374c40eb530828229a319f9ee1375e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105658"
---
# <a name="thread_v2_typegroup1-class"></a>Thread \_ V2 \_ TypeGroup1-Klasse

Diese Klasse ist die Ereignistypklasse für Threadstart- und -endereignisse.

Die folgende Syntax wird durch MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[EventType{1, 2, 3, 4}, EventTypeName{"Start", "End", "DCStart", "DCEnd"}]
class Thread_V2_TypeGroup1 : Thread_V2
{
  uint32 ProcessId;
  uint32 TThreadId;
  uint32 StackBase;
  uint32 StackLimit;
  uint32 UserStackBase;
  uint32 UserStackLimit;
  uint32 StartAddr;
  uint32 Win32StartAddr;
  uint32 TebBase;
  uint32 SubProcessTag;
};
```

## <a name="members"></a>Member

Die **Klasse Thread \_ V2 \_ TypeGroup1** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Klasse Thread \_ V2 \_ TypeGroup1** verfügt über diese Eigenschaften.

<dl> <dt>

ProcessId
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(1), Format("x")
</dt> </dl>

Prozessbezeichner des threads, der am Ereignis beteiligt ist.

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

Limit des Threadstapels.

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

SubProcessTag
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(10), Format("x")
</dt> </dl>

Identifiziert den Dienst, wenn sich der Thread im Besitz eines Diensts befindet. andernfalls 0 (null).

</dd> <dt>

TebBase
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(9), Zeiger
</dt> </dl>

Basisadresse des Threadumgebungsblocks.

</dd> <dt>

TThreadId
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(2), Format("x")
</dt> </dl>

Threadbezeichner des Threads, der am Ereignis beteiligt ist.

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

Limit des Benutzermodusstapels des Threads.

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

## <a name="remarks"></a>Bemerkungen

Die Ereignistypen DCStart und DCEnd aufzählen die Threads, die derzeit zum Zeitpunkt des Starts bzw. Endes der Kernelsitzung ausgeführt werden.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Thread**](thread.md)
</dt> <dt>

[**Thread \_ V2**](thread-v2.md)
</dt> </dl>

 

 




