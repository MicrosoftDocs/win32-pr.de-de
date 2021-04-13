---
title: Tasksettings. deleteexpiredtaskafter-Eigenschaft
description: Ruft bei der Skripterstellung die Zeitspanne ab, die der Taskplaner wartet, bevor der Task nach Ablauf gelöscht wird, oder legt ihn fest.
ms.assetid: c57d736c-e3ce-44b8-809e-44f7c0321d70
keywords:
- Deleteexpiredtaskafter-Eigenschaft Taskplaner
- Deleteexpiredtaskafter-Eigenschaft Taskplaner, tasksettings-Objekt
- Tasksettings-Objekt Taskplaner, deleteexpiredtaskafter-Eigenschaft
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
ms.openlocfilehash: 9005ff7988353daa902b1bc3151c539713bb94ea
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475957"
---
# <a name="tasksettingsdeleteexpiredtaskafter-property"></a>Tasksettings. deleteexpiredtaskafter-Eigenschaft

Ruft bei der Skripterstellung die Zeitspanne ab, die der Taskplaner wartet, bevor der Task nach Ablauf gelöscht wird, oder legt ihn fest. Wenn für diese Eigenschaft kein Wert angegeben wird, wird die Aufgabe vom Taskplaner-Dienst nicht gelöscht.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
TaskSettings.DeleteExpiredTaskAfter As String
```



## <a name="property-value"></a>Eigenschaftswert

Eine Zeichenfolge, mit der die Zeitspanne abgerufen oder festgelegt wird, die der Taskplaner wartet, bevor die Aufgabe nach Ablauf gelöscht wird. Das Format dieser Zeichenfolge lautet pnynmndtnhnmns. dabei ist "NY" die Anzahl der Jahre, "nm" die Anzahl von Monaten, "ND" die Anzahl der Tage, "t" ist das Trennzeichen für Datum/Uhrzeit, "NH" die Anzahl von Stunden, "nm" die Anzahl der Minuten und "NS" die Anzahl von Sekunden (z

## <a name="remarks"></a>Bemerkungen

Ein Task läuft ab, nachdem die Endgrenze für alle der Aufgabe zugeordneten Trigger überschritten wurde. Die Endgrenze für einen-Endpunkt wird durch die [endboundary](trigger-endboundary.md) -Eigenschaft angegeben, die von allen auslöserobjekten geerbt wird.

Beim Lesen oder Schreiben von XML für eine Aufgabe wird diese Einstellung im [**deleteexpiredtaskafter-Element (settingstype)**](taskschedulerschema-deleteexpiredtaskafter-settingstype-element.md) des Taskplaner-Schemas angegeben.

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

 

 





