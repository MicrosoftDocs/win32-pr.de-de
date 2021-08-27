---
title: TaskSettings.RestartCount-Eigenschaft
description: Ruft für die Skripterstellung ab oder legt fest, wie oft der Taskplaner versucht, den Task neu zu starten.
ms.assetid: 7d92c2c6-e846-4664-b22a-b2a6ca46c225
keywords:
- RestartCount-Eigenschaft Taskplaner
- RestartCount-Eigenschaft Taskplaner , TaskSettings-Objekt
- TaskSettings-Objekt Taskplaner , RestartCount-Eigenschaft
topic_type:
- apiref
api_name:
- TaskSettings.RestartCount
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3a34e8eef84575548998e39ab47bc5492baca368f7012d5fa096c831539ceb7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072410"
---
# <a name="tasksettingsrestartcount-property"></a>TaskSettings.RestartCount-Eigenschaft

Ruft für die Skripterstellung ab oder legt fest, wie oft der Taskplaner versucht, den Task neu zu starten.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
TaskSettings.RestartCount As Integer
```



## <a name="property-value"></a>Eigenschaftswert

Gibt an, wie oft der Taskplaner versucht, den Task neu zu starten.

## <a name="remarks"></a>Hinweise

Beim Lesen oder Schreiben von XML für eine Aufgabe wird diese Einstellung im [**Count-Element**](taskschedulerschema-count-restarttype-element.md) des Taskplaner Schemas angegeben.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





