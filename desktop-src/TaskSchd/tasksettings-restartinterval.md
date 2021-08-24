---
title: TaskSettings.RestartInterval (Eigenschaft)
description: Für die Skripterstellung ruft einen Wert ab, der angibt, wie lange der Taskplaner versucht, den Task neu zu starten, oder legt diesen fest.
ms.assetid: ad6f254d-55a8-478e-984e-a459f22043b5
keywords:
- RestartInterval-Taskplaner
- RestartInterval-Eigenschaft Taskplaner , TaskSettings-Objekt
- TaskSettings-Objekt Taskplaner , RestartInterval-Eigenschaft
topic_type:
- apiref
api_name:
- TaskSettings.RestartInterval
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3293072fcec50b140a298887b12ed8f5dd1fb6a298c3b486069fe2e7eccaef00
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119681610"
---
# <a name="tasksettingsrestartinterval-property"></a>TaskSettings.RestartInterval (Eigenschaft)

Für die Skripterstellung ruft einen Wert ab, der angibt, wie lange der Taskplaner versucht, den Task neu zu starten, oder legt diesen fest.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
TaskSettings.RestartInterval As String
```



## <a name="property-value"></a>Eigenschaftswert

Ein -Wert, der angibt, wie Taskplaner der Task neu gestartet werden soll. Wenn diese Eigenschaft festgelegt ist, muss auch [**die RestartCount-Eigenschaft**](tasksettings-restartcount.md) festgelegt werden. Das Format für diese Zeichenfolge ist (z. B. `P<days>DT<hours>H<minutes>M<seconds>S` ist "PT5M" 5 Minuten, "PT1H" ist 1 Stunde und "PT20M" beträgt 20 Minuten). Die maximal zulässige Zeit beträgt 31 Tage, und die zulässige Mindestzeit beträgt 1 Minute.

## <a name="remarks"></a>Hinweise

Beim Lesen oder Schreiben von XML für eine Aufgabe wird diese Einstellung im [**Interval-Element**](taskschedulerschema-interval-restarttype-element.md) des Taskplaner angegeben.

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

 

 





