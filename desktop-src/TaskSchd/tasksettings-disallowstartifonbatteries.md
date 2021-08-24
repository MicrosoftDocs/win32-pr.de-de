---
title: TaskSettings.DisallowStartIfOnFolgens-Eigenschaft
description: Ruft für die Skripterstellung einen booleschen Wert ab, der angibt, dass der Task nicht gestartet wird, wenn der Computer mit Akkus ausgeführt wird, oder legt diesen fest.
ms.assetid: 5e13f168-a396-495f-a486-e64e8524c8cd
keywords:
- DisallowStartIfOnFolgens-Eigenschaft Taskplaner
- DisallowStartIfOnFolgens-Eigenschaft Taskplaner , TaskSettings-Objekt
- TaskSettings-Objekt Taskplaner , DisallowStartIfOnFolgens-Eigenschaft
topic_type:
- apiref
api_name:
- TaskSettings.DisallowStartIfOnBatteries
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e08e3e57a961f08a5f1ddae17c8334c9f1d3501b34590b1f98676195108444d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099720"
---
# <a name="tasksettingsdisallowstartifonbatteries-property"></a>TaskSettings.DisallowStartIfOnFolgens-Eigenschaft

Ruft für die Skripterstellung einen booleschen Wert ab, der angibt, dass der Task nicht gestartet wird, wenn der Computer mit Akkus ausgeführt wird, oder legt diesen fest.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
TaskSettings.DisallowStartIfOnBatteries As Boolean
```



## <a name="property-value"></a>Eigenschaftswert

Ein boolescher Wert, der angibt, dass die Aufgabe nicht gestartet wird, wenn der Computer mit Akkus ausgeführt wird. True gibt an, dass die Aufgabe nicht gestartet wird, wenn der Computer mit Akkus ausgeführt wird. False gibt an, dass die Aufgabe gestartet wird, wenn der Computer mit Akkus ausgeführt wird. Der Standardwert ist True.

## <a name="remarks"></a>Hinweise

Beim Lesen oder Schreiben von XML für eine Aufgabe wird diese Einstellung im [**DisallowStartIfOnFolgens-Element**](taskschedulerschema-disallowstartifonbatteries-settingstype-element.md) des Taskplaner Schemas angegeben.

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

 

 





