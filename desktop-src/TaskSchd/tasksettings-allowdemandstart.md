---
title: TaskSettings.AllowDemandStart(Eigenschaft)
description: Für die Skripterstellung ruft einen booleschen Wert ab, der angibt, dass der Task mithilfe des Befehls Ausführen oder des Kontextmenüs gestartet werden kann, oder legt diesen fest.
ms.assetid: 1eae19ae-3b4d-4eb2-82d0-685ef2729f36
keywords:
- AllowDemandStart-Taskplaner
- AllowDemandStart-Eigenschaft Taskplaner , TaskSettings-Objekt
- TaskSettings-Objekt Taskplaner , AllowDemandStart-Eigenschaft
topic_type:
- apiref
api_name:
- TaskSettings.AllowDemandStart
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a48ecaf9010b4269ffff66b556d01cfccc057fd05207f619290af9e50f6c757f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959480"
---
# <a name="tasksettingsallowdemandstart-property"></a>TaskSettings.AllowDemandStart(Eigenschaft)

Für die Skripterstellung ruft einen booleschen Wert ab, der angibt, dass der Task mithilfe des Befehls Ausführen oder des Kontextmenüs gestartet werden kann, oder legt diesen fest.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
TaskSettings.AllowDemandStart As Boolean
```



## <a name="property-value"></a>Eigenschaftswert

True gibt an, dass die Aufgabe mithilfe des Befehls Ausführen oder des Kontextmenüs ausgeführt werden kann. False gibt an, dass die Aufgabe nicht mit dem Befehl Ausführen oder dem Kontextmenü ausgeführt werden kann. Der Standardwert ist True.

## <a name="remarks"></a>Hinweise

Wenn diese Eigenschaft auf True festgelegt ist, kann die Aufgabe unabhängig davon gestartet werden, wann die Aufgabe von Triggern gestartet wird.

Beim Lesen oder Schreiben von XML für eine Aufgabe wird diese Einstellung im [AllowStartOnDemand-Element](taskschedulerschema-allowstartondemand-settingstype-element.md) des Taskplaner angegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





