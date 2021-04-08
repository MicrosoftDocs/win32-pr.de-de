---
title: Tasksettings. restartinterval (Eigenschaft)
description: Ruft bei der Skripterstellung einen Wert ab oder legt einen Wert fest, der angibt, wie lange der Taskplaner versucht, den Task neu zu starten.
ms.assetid: ad6f254d-55a8-478e-984e-a459f22043b5
keywords:
- Restartinterval-Eigenschaft Taskplaner
- Restartinterval-Eigenschaft Taskplaner, tasksettings-Objekt
- Tasksettings-Objekt Taskplaner, restartinterval (Eigenschaft)
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
ms.openlocfilehash: f511e43ebb1d61fd80f2fcab34aba092704b8338
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740424"
---
# <a name="tasksettingsrestartinterval-property"></a>Tasksettings. restartinterval (Eigenschaft)

Ruft bei der Skripterstellung einen Wert ab oder legt einen Wert fest, der angibt, wie lange der Taskplaner versucht, den Task neu zu starten.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
TaskSettings.RestartInterval As String
```



## <a name="property-value"></a>Eigenschaftswert

Ein-Wert, der angibt, wie lange der Taskplaner versucht, den Task neu zu starten. Wenn diese Eigenschaft festgelegt ist, muss auch die [**restartcount**](tasksettings-restartcount.md) -Eigenschaft festgelegt werden. Das Format für diese Zeichenfolge ist P <days> dt <hours> H <minutes> M <seconds> S ("PT5M" ist beispielsweise 5 Minuten, "PT1H" ist 1 Stunde, und "PT20M" beträgt 20 Minuten). Die maximal zulässige Dauer beträgt 31 Tage, und die zulässige Mindestanzahl beträgt 1 Minute.

## <a name="remarks"></a>Bemerkungen

Beim Lesen oder Schreiben von XML für eine Aufgabe wird diese Einstellung im [**Interval**](taskschedulerschema-interval-restarttype-element.md) -Element des Taskplaner-Schemas angegeben.

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

 

 





