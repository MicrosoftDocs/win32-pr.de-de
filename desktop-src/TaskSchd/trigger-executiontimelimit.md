---
title: Trigger.ExecutionTimeLimit-Eigenschaft
description: Für die Skripterstellung ruft die maximale Zeitdauer ab, für die die vom Trigger gestartete Aufgabe ausgeführt werden darf, oder legt diese fest.
ms.assetid: 9993b362-f8f7-429b-a16a-1845d6f0f5e0
keywords:
- ExecutionTimeLimit-Taskplaner
- ExecutionTimeLimit-Eigenschaft Taskplaner , Triggerobjekt
- Triggerobjekt Taskplaner , ExecutionTimeLimit-Eigenschaft
topic_type:
- apiref
api_name:
- Trigger.ExecutionTimeLimit
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 724cc80a1d3bf35d00aff1eba220d657723ee8c5ed8ddb3c95474cf0534bff79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118857073"
---
# <a name="triggerexecutiontimelimit-property"></a>Trigger.ExecutionTimeLimit-Eigenschaft

Für die Skripterstellung ruft die maximale Zeitdauer ab, für die die vom Trigger gestartete Aufgabe ausgeführt werden darf, oder legt diese fest.

## <a name="syntax"></a>Syntax


```VB
Trigger.ExecutionTimeLimit As String
```



## <a name="property-value"></a>Eigenschaftswert

Die maximale Zeitdauer, für die die vom Trigger gestartete Aufgabe ausgeführt werden darf. Das Format für diese Zeichenfolge ist PnYnMnDTnHnMnS, Dabei steht nY für die Anzahl von Jahren, nM für die Anzahl der Monate, nD für die Anzahl von Tagen, "T" für das Datums-/Uhrzeittrennzeichen, nH für die Anzahl von Stunden, nM für die Anzahl von Minuten und nS für die Anzahl von Sekunden (pt5M gibt beispielsweise 5 Minuten an, und P1M4DT2H5M gibt einen Monat, vier Tage, zwei Stunden und fünf Minuten an).

## <a name="remarks"></a>Hinweise

Beim Lesen oder Schreiben von XML für einen Task wird das Ausführungszeitlimit im [**ExecutionTimeLimit-Element**](taskschedulerschema-executiontimelimit-triggerbasetype-element.md) des Taskplaner angegeben.

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

 

 





