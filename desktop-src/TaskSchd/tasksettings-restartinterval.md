---
title: TaskSettings.RestartInterval-Eigenschaft
description: Ruft für die Skripterstellung einen Wert ab, der angibt, wie lange der Taskplaner versucht, den Task neu zu starten, oder legt diesen fest.
ms.assetid: ad6f254d-55a8-478e-984e-a459f22043b5
keywords:
- RestartInterval-Eigenschaft Taskplaner
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
ms.openlocfilehash: f127c5d434b5cb1e6dec6d8a3c68ee343fa00ffc
ms.sourcegitcommit: b3a9abea47dea7374eac0f9a95a652ac6977fb2e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/20/2021
ms.locfileid: "107734145"
---
# <a name="tasksettingsrestartinterval-property"></a>TaskSettings.RestartInterval-Eigenschaft

Ruft für die Skripterstellung einen Wert ab, der angibt, wie lange der Taskplaner versucht, den Task neu zu starten, oder legt diesen fest.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
TaskSettings.RestartInterval As String
```



## <a name="property-value"></a>Eigenschaftswert

Ein -Wert, der angibt, wie lange der Taskplaner versucht, den Task neu zu starten. Wenn diese Eigenschaft festgelegt ist, muss auch die [**RestartCount-Eigenschaft**](tasksettings-restartcount.md) festgelegt werden. Das Format für diese Zeichenfolge lautet `P<days>DT<hours>H<minutes>M<seconds>S` (z. B. "PT5M" ist 5 Minuten, "PT1H" ist 1 Stunde und "PT20M" ist 20 Minuten). Die maximal zulässige Zeit beträgt 31 Tage, und die zulässige Mindestzeit beträgt 1 Minute.

## <a name="remarks"></a>Bemerkungen

Beim Lesen oder Schreiben von XML für eine Aufgabe wird diese Einstellung im [**Interval-Element**](taskschedulerschema-interval-restarttype-element.md) des Taskplaner Schemas angegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows \[ Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





