---
title: "\"\"-Eigenschaft von \"\""
description: Ruft bei der Skripterstellung einen Wert ab, der angibt, wie oft die Aufgabe ausgeführt wird und wie lange das Wiederholungsmuster nach dem Start der Aufgabe wiederholt wird, oder legt diesen Wert fest.
ms.assetid: f90b935c-8b69-4c82-ac4b-6b049e7b9703
keywords:
- Wiederholungs Eigenschaft Taskplaner
- Wiederholungs Eigenschaft Taskplaner, Auslöserobjekt
- Objekt Taskplaner, Wiederholungs Eigenschaft des Auslösers
topic_type:
- apiref
api_name:
- Trigger.Repetition
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 611c7e42a14de06a8777333a6dc640781943ba06
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339139"
---
# <a name="triggerrepetition-property"></a>""-Eigenschaft von ""

Ruft bei der Skripterstellung einen Wert ab, der angibt, wie oft die Aufgabe ausgeführt wird und wie lange das Wiederholungsmuster nach dem Start der Aufgabe wiederholt wird, oder legt diesen Wert fest.

## <a name="syntax"></a>Syntax


```VB
Trigger.Repetition As RepetitionPattern
```



## <a name="property-value"></a>Eigenschaftswert

Ein [**wiederholungpattern**](repetitionpattern.md) -Objekt, das definiert, wie oft die Aufgabe ausgeführt wird und wie lange das Wiederholungsmuster wiederholt wird, nachdem die Aufgabe gestartet wurde.

## <a name="remarks"></a>Bemerkungen

Beim Lesen oder schreiben Ihrer eigenen XML-Daten für eine Aufgabe wird das Wiederholungsmuster für einen-Vorgang im [**Wiederholungs**](taskschedulerschema-repetition-triggerbasetype-element.md) Element des Taskplaner-Schemas angegeben.

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
</dt> <dt>

[**Repetitionpattern**](repetitionpattern.md)
</dt> </dl>

 

 





