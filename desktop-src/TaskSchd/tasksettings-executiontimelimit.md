---
title: TaskSettings.ExecutionTimeLimit-Eigenschaft
description: Für die Skripterstellung ruft die Zeit ab, die zum Abschließen der Aufgabe zulässig ist, oder legt diese fest.
ms.assetid: 5b8b8d4b-e705-4407-95c9-bf8baacb58c1
keywords:
- ExecutionTimeLimit-Taskplaner
- ExecutionTimeLimit-Eigenschaft Taskplaner , TaskSettings-Objekt
- TaskSettings-Objekt Taskplaner , ExecutionTimeLimit-Eigenschaft
topic_type:
- apiref
api_name:
- TaskSettings.ExecutionTimeLimit
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f54f17d2eda2b80f46b243ae3c670864831635ec7d7ed6ef0608cfcfaf9d776
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118857173"
---
# <a name="tasksettingsexecutiontimelimit-property"></a>TaskSettings.ExecutionTimeLimit-Eigenschaft

Für die Skripterstellung ruft die Zeit ab, die zum Abschließen der Aufgabe zulässig ist, oder legt diese fest. Standardmäßig wird eine Aufgabe 72 Stunden nach beginn der Ausführung beendet. Sie können dies ändern, indem Sie diese Einstellung ändern.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
TaskSettings.ExecutionTimeLimit As String
```



## <a name="property-value"></a>Eigenschaftswert

Die Zeit, die zum Abschließen der Aufgabe zulässig ist. Das Format für diese Zeichenfolge ist PnYnMnDTnHnMnS, Dabei steht nY für die Anzahl von Jahren, nM für die Anzahl der Monate, nD für die Anzahl von Tagen, "T" für das Datums-/Uhrzeittrennzeichen, nH für die Anzahl von Stunden, nM für die Anzahl von Minuten und nS für die Anzahl von Sekunden (pt5M gibt beispielsweise 5 Minuten an, und P1M4DT2H5M gibt einen Monat, vier Tage, zwei Stunden und fünf Minuten an). Mit dem Wert PT0S kann die Aufgabe unbegrenzt ausgeführt werden. Wenn dieser Parameter auf Nothing festgelegt ist, ist das Ausführungszeitlimit unendlich.

## <a name="remarks"></a>Hinweise

Beim Lesen oder Schreiben von XML für eine Aufgabe wird diese Einstellung im [**ExecutionTimeLimit-Element**](taskschedulerschema-executiontimelimit-settingstype-element.md) des Taskplaner angegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





