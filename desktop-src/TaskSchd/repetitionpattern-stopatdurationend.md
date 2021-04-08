---
title: Repetitionpattern. stopatdurationend-Eigenschaft
description: Ruft bei der Skripterstellung einen booleschen Wert ab, der angibt, ob eine laufende Instanz der Aufgabe am Ende der Wiederholungsmuster Dauer beendet wird, oder legt diesen fest.
ms.assetid: 421f2d6f-7c35-44b4-97f2-45f46ca5e40e
keywords:
- Stopatdurationend-Eigenschaft Taskplaner
- Stopatdurationend-Eigenschaft Taskplaner, repetitionpattern-Objekt
- Repetitionpattern-Objekt Taskplaner, stopatdurationend-Eigenschaft
topic_type:
- apiref
api_name:
- RepetitionPattern.StopAtDurationEnd
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20b95d7e8941a4249991692dffbd3cac9ad1ca7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742440"
---
# <a name="repetitionpatternstopatdurationend-property"></a>Repetitionpattern. stopatdurationend-Eigenschaft

Ruft bei der Skripterstellung einen booleschen Wert ab, der angibt, ob eine laufende Instanz der Aufgabe am Ende der Wiederholungsmuster Dauer beendet wird, oder legt diesen fest.

## <a name="syntax"></a>Syntax


```VB
RepetitionPattern.StopAtDurationEnd As Boolean
```



## <a name="property-value"></a>Eigenschaftswert

Ein boolescher Wert, der angibt, ob eine laufende Instanz der Aufgabe am Ende der Wiederholungsmuster Dauer angehalten wird.

## <a name="remarks"></a>Bemerkungen

Beim Lesen oder Schreiben von XML für eine Aufgabe werden diese Informationen im [**stopatdurationend**](taskschedulerschema-stopatdurationend-repetitiontype-element.md) -Element des Taskplaner-Schemas angegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





