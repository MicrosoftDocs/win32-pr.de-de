---
description: Diese Klasse ist die Ereignistyp Klasse für bereite Thread Ereignisse. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: 861ab070-5536-4897-b523-9b09a7d59b3e
title: "\"Leserythread\"-Klasse"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ReadyThread
- ReadyThread.TThreadId
- ReadyThread.AdjustReason
- ReadyThread.AdjustIncrement
- ReadyThread.Flag
- ReadyThread.Reserved
api_type:
- NA
api_location: ''
ms.openlocfilehash: e10029c0397c16a5a5eb30be6e3db64c0baec596
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862876"
---
# <a name="readythread-class"></a>"Leserythread"-Klasse

Diese Klasse ist die Ereignistyp Klasse für bereite Thread Ereignisse.

Die folgende Syntax wird durch den MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[EventType{50}, EventTypeName{"ReadyThread"}]
class ReadyThread : Thread_V2
{
  uint32 TThreadId;
  sint8  AdjustReason;
  sint8  AdjustIncrement;
  sint8  Flag;
  sint8  Reserved;
};
```

## <a name="members"></a>Member

Die " **leserythread** "-Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die " **leserythread** "-Klasse verfügt über diese Eigenschaften.

<dl> <dt>

Anpassung erhöhen
</dt> <dd> <dl> <dt>

Datentyp: **sint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (3)
</dt> </dl>

Der Wert, mit dem die Priorität angepasst wird.

</dd> <dt>

Adjustreason
</dt> <dd> <dl> <dt>

Datentyp: **sint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (2)
</dt> </dl>

Der Grund für die Prioritäts Erhöhung.



| Wert                                                                        | Bedeutung                                                                                                                 |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Das Inkrement wird ignoriert.<br/>                                                                                        |
| <dl> <dt>1</dt> </dl> | Wenden Sie das Inkrement an, das am Ende jedes Quantums inkrementell beeinträchtigt wird.<br/>                              |
| <dl> <dt>2</dt> </dl> | Wenden Sie das Inkrement als Verstärkung an, die vollständig bei Quantum (in der Regel für die Prioritäts Spende) verfällt.<br/> |



 

</dd> <dt>

Flag
</dt> <dd> <dl> <dt>

Datentyp: **sint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (4)
</dt> </dl>

Im folgenden sind die möglichen Statusflags aufgeführt:



| Wert                                                                          | Bedeutung                                                                    |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <dt>0x1</dt> </dl> | Der Thread wurde von DPC (verzögerter Prozedur aufzurufen) neu erstellt.<br/> |
| <dl> <dt>0x2</dt> </dl> | Der Kernel Stapel wird zurzeit ausgetauscht.<br/>                      |
| <dl> <dt>0x4</dt> </dl> | Der Prozess Adressraum wird ausgetauscht.<br/>                       |



 

Beachten Sie Folgendes: Wenn der Kernel Stapel oder der Prozess Adressraum ausgetauscht wird, gibt es nach dem Kernel Stapel ein zusätzliches "Read-Thread"-Ereignis, oder der Prozess Adressraum wird wieder in den Austausch eingefügt, und der Thread wird für die Weiterleitung bereit.

</dd> <dt>

Reserviert
</dt> <dd> <dl> <dt>

Datentyp: **sint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (5)
</dt> </dl>

Reserviert.

</dd> <dt>

Tthreadid
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (1), Format ("x")
</dt> </dl>

Der Thread Bezeichner des Threads, der für die Ausführung neu erstellt wird.

</dd> </dl>

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>       |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Thread \_ v2**](thread-v2.md)
</dt> </dl>

 

 




