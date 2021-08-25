---
title: TaskSettings.RunOnlyIfIdle (Eigenschaft)
description: Für die Skripterstellung ruft einen booleschen Wert ab, der angibt, dass der Taskplaner die Aufgabe nur dann ausführen wird, wenn sich der Computer in einer Leerlaufbedingung befindet, oder legt diesen fest.
ms.assetid: fca1d98e-0544-4301-a709-1e0dae762e07
keywords:
- RunOnlyIfIdle-Taskplaner
- RunOnlyIfIdle-Eigenschaft Taskplaner , TaskSettings-Objekt
- TaskSettings-Taskplaner , RunOnlyIfIdle-Eigenschaft
topic_type:
- apiref
api_name:
- TaskSettings.RunOnlyIfIdle
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed423dc4cd34a03bd3b76401284a4d6bfb98270e7c0d0feed0a45046a82e7d3a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119990820"
---
# <a name="tasksettingsrunonlyifidle-property"></a>TaskSettings.RunOnlyIfIdle (Eigenschaft)

Für die Skripterstellung ruft einen booleschen Wert ab, der angibt, dass der Taskplaner die Aufgabe nur dann ausführen wird, wenn sich der Computer in einer Leerlaufbedingung befindet, oder legt diesen fest.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
TaskSettings.RunOnlyIfIdle As Boolean
```



## <a name="property-value"></a>Eigenschaftswert

True gibt an, dass der Taskplaner task nur ausgeführt wird, wenn sich der Computer in einem Leerlaufzustand befindet. Die Standardeinstellung lautet „false“.

## <a name="remarks"></a>Hinweise

Beim Lesen oder Schreiben von XML für eine Aufgabe wird diese Einstellung im [**RunOnlyIfIdle-Element**](taskschedulerschema-runonlyifidle-settingstype-element.md) des Taskplaner angegeben.

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

 

 





