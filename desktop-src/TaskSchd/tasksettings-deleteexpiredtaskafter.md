---
title: TaskSettings.DeleteExpiredTaskAfter-Eigenschaft
description: Für die Skripterstellung ruft die Zeit ab, die der Taskplaner abwarten soll, bevor der Task nach ablaufen gelöscht wird, oder legt diesen fest.
ms.assetid: c57d736c-e3ce-44b8-809e-44f7c0321d70
keywords:
- DeleteExpiredTaskAfter-Taskplaner
- DeleteExpiredTaskAfter-Eigenschaft Taskplaner , TaskSettings-Objekt
- TaskSettings-Objekt Taskplaner , DeleteExpiredTaskAfter-Eigenschaft
topic_type:
- apiref
api_name:
- TaskSettings.DeleteExpiredTaskAfter
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 521f07a5712165c282a36bbfe2c3b66769239c53d652ae49a03fa6a50c19cb05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119658450"
---
# <a name="tasksettingsdeleteexpiredtaskafter-property"></a>TaskSettings.DeleteExpiredTaskAfter-Eigenschaft

Für die Skripterstellung ruft die Zeit ab, die der Taskplaner abwarten soll, bevor der Task nach ablaufen gelöscht wird, oder legt diesen fest. Wenn für diese Eigenschaft kein Wert angegeben wird, löscht der Taskplaner den Task nicht.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
TaskSettings.DeleteExpiredTaskAfter As String
```



## <a name="property-value"></a>Eigenschaftswert

Eine Zeichenfolge, die die Zeit abgibt, die der Taskplaner task nach ablaufendem Vorgang vor dem Löschen wartet, oder legt diese fest. Das Format für diese Zeichenfolge ist PnYnMnDTnHnMnS, Dabei steht nY für die Anzahl von Jahren, nM für die Anzahl der Monate, nD für die Anzahl von Tagen, "T" für das Datums-/Uhrzeittrennzeichen, nH für die Anzahl von Stunden, nM für die Anzahl von Minuten und nS für die Anzahl von Sekunden (pt5M gibt beispielsweise 5 Minuten an, und P1M4DT2H5M gibt einen Monat, vier Tage, zwei Stunden und fünf Minuten an).

## <a name="remarks"></a>Hinweise

Eine Aufgabe läuft ab, nachdem die Endgrenze für alle Trigger überschritten wurde, die der Aufgabe zugeordnet sind. Die Endgrenze für einen Trigger wird von der [EndBoundary-Eigenschaft angegeben,](trigger-endboundary.md) die von allen Triggerobjekten geerbt wird.

Beim Lesen oder Schreiben von XML für eine Aufgabe wird diese Einstellung im [**DeleteExpiredTaskAfter-Element (settingsType)**](taskschedulerschema-deleteexpiredtaskafter-settingstype-element.md) des Taskplaner angegeben.

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

 

 





