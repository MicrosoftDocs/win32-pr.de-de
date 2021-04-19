---
title: TaskSettings.Executiontimelimit-Eigenschaft
description: Ruft bei der Skripterstellung die Zeitspanne ab, die zum Ausführen der Aufgabe zulässig ist, oder legt diese fest.
ms.assetid: 5b8b8d4b-e705-4407-95c9-bf8baacb58c1
keywords:
- Executiontimelimit-Eigenschaft Taskplaner
- Executiontimelimit-Eigenschaft Taskplaner, tasksettings-Objekt
- Tasksettings-Objekt Taskplaner, executiontimelimit-Eigenschaft
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
ms.openlocfilehash: de01d68fa7fe6c21f022d8a21863887e57016c5c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339359"
---
# <a name="tasksettingsexecutiontimelimit-property"></a>TaskSettings.Executiontimelimit-Eigenschaft

Ruft bei der Skripterstellung die Zeitspanne ab, die zum Ausführen der Aufgabe zulässig ist, oder legt diese fest. Standardmäßig wird eine Aufgabe 72 Stunden nach dem Start angehalten. Sie können dies ändern, indem Sie diese Einstellung ändern.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
TaskSettings.ExecutionTimeLimit As String
```



## <a name="property-value"></a>Eigenschaftswert

Die Zeitspanne, die zum Ausführen der Aufgabe zulässig ist. Das Format dieser Zeichenfolge lautet pnynmndtnhnmns. dabei ist "NY" die Anzahl der Jahre, "nm" die Anzahl von Monaten, "ND" die Anzahl der Tage, "t" ist das Trennzeichen für Datum/Uhrzeit, "NH" die Anzahl von Stunden, "nm" die Anzahl der Minuten und "NS" die Anzahl von Sekunden (z Mit dem Wert PT0S kann der Task unbegrenzt ausgeführt werden. Wenn dieser Parameter auf "Nothing" festgelegt ist, ist das Ausführungszeit Limit unendlich.

## <a name="remarks"></a>Bemerkungen

Beim Lesen oder Schreiben von XML für eine Aufgabe wird diese Einstellung im [**executiontimelimit**](taskschedulerschema-executiontimelimit-settingstype-element.md) -Element des Taskplaner Schemas angegeben.

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

 

 





