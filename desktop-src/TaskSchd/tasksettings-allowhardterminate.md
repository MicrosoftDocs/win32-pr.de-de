---
title: Tasksettings. zugewhardend-Eigenschaft
description: Ruft bei der Skripterstellung einen booleschen Wert ab, der angibt, dass der Task vom Taskplaner Dienst mithilfe von TerminateProcess beendet werden kann, oder legt ihn fest.
ms.assetid: 1dfd692e-efbe-41a2-8dbd-b14cf26bbcb7
keywords:
- Eigenschaft ' zugeTaskplaner Zuweisung '
- Eigenschaft "zugeTaskplaner Zuweisung", Task Settings-Objekt
- Tasksettings-Objekt Taskplaner, Eigenschaft "Zuweisung beenden"
topic_type:
- apiref
api_name:
- TaskSettings.AllowHardTerminate
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c38e117ebc3d2175b952f01698987ccb65f7af5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742416"
---
# <a name="tasksettingsallowhardterminate-property"></a>Tasksettings. zugewhardend-Eigenschaft

Ruft bei der Skripterstellung einen booleschen Wert ab, der angibt, dass der Task vom Taskplaner Dienst mithilfe von [**TerminateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminateprocess)beendet werden kann, oder legt ihn fest. Der Dienst versucht, die ausgelaufende Aufgabe zu schließen, indem er die Benachrichtigung zum [**\_ Schließen der WM**](../winmsg/wm-close.md) sendet. wenn die Aufgabe nicht antwortet, wird die Aufgabe nur beendet, wenn diese Eigenschaft auf "true" festgelegt ist.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
TaskSettings.AllowHardTerminate As Boolean
```



## <a name="property-value"></a>Eigenschaftswert

True gibt an, dass die Aufgabe mithilfe von [**TerminateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminateprocess)beendet werden kann. Wenn der Wert false ist, kann die Aufgabe nicht mithilfe von **TerminateProcess** beendet werden.

## <a name="remarks"></a>Bemerkungen

Beim Lesen oder Schreiben von XML für eine Aufgabe wird diese Einstellung im Element "- [Zuweisung](taskschedulerschema-allowhardterminate-settingstype-element.md) " des Taskplaner-Schemas angegeben.

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

 

