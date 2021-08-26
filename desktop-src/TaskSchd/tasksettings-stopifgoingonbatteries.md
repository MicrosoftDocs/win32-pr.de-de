---
title: TaskSettings.StopIfGoingOnObjektes-Eigenschaft
description: Ruft für die Skripterstellung einen booleschen Wert ab, der angibt, dass die Aufgabe beendet wird, wenn der Computer zu Akkus fährt, oder legt diesen fest.
ms.assetid: a133cba0-c93e-4963-83a3-7587e323fc6e
keywords:
- StopIfGoingOnQualifiziers-Eigenschaft Taskplaner
- StopIfGoingOnObjektes-Eigenschaft Taskplaner , TaskSettings-Objekt
- TaskSettings-Objekt Taskplaner , StopIfGoingOnTasks-Eigenschaft
topic_type:
- apiref
api_name:
- TaskSettings.StopIfGoingOnBatteries
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 229d5d3beef974e9ce8758f9bd81fc3217bd9c3fcf9bf37be137abe6515cc62a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119974886"
---
# <a name="tasksettingsstopifgoingonbatteries-property"></a>TaskSettings.StopIfGoingOnObjektes-Eigenschaft

Ruft für die Skripterstellung einen booleschen Wert ab, der angibt, dass die Aufgabe beendet wird, wenn der Computer zu Akkus fährt, oder legt diesen fest.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
TaskSettings.StopIfGoingOnBatteries As Boolean
```



## <a name="property-value"></a>Eigenschaftswert

Ein boolescher Wert, der angibt, dass die Aufgabe beendet wird, wenn der Computer zu Akkus fährt. True gibt die -Eigenschaft an, dass die Aufgabe beendet wird, wenn der Computer zu Akkus gelangt. False gibt die -Eigenschaft an, dass die Aufgabe nicht beendet wird, wenn der Computer zu Akkus fährt. Der Standardwert ist True. Weitere Informationen finden Sie unter Hinweise.

## <a name="remarks"></a>Hinweise

Beim Lesen oder Schreiben von XML für eine Aufgabe wird diese Einstellung im [**StopIfGoingOnTasks-Element**](taskschedulerschema-stopifgoingonbatteries-settingstype-element.md) des Taskplaner Schemas angegeben.

## <a name="requirements"></a>Anforderungen



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

 

 





