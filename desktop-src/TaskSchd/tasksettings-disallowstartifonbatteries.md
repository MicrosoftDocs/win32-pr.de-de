---
title: Tasksettings. disallowstartifonakkus (Eigenschaft)
description: Ruft bei der Skripterstellung einen booleschen Wert ab, der angibt, dass der Task nicht gestartet wird, wenn der Computer unter Akkus ausgeführt wird, oder legt ihn fest.
ms.assetid: 5e13f168-a396-495f-a486-e64e8524c8cd
keywords:
- Disallowstartifonakkus-Eigenschaft Taskplaner
- Disallowstartifonakkus-Eigenschaft Taskplaner, tasksettings-Objekt
- Tasksettings-Objekt Taskplaner, disallowstartifonakkus (Eigenschaft)
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
ms.openlocfilehash: d35a7fde3012b25dfeab65e6e6088bb1d950892d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105345"
---
# <a name="tasksettingsdisallowstartifonbatteries-property"></a>Tasksettings. disallowstartifonakkus (Eigenschaft)

Ruft bei der Skripterstellung einen booleschen Wert ab, der angibt, dass der Task nicht gestartet wird, wenn der Computer unter Akkus ausgeführt wird, oder legt ihn fest.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
TaskSettings.DisallowStartIfOnBatteries As Boolean
```



## <a name="property-value"></a>Eigenschaftswert

Ein boolescher Wert, der angibt, dass der Task nicht gestartet wird, wenn der Computer unter Akkus ausgeführt wird. True gibt an, dass der Task nicht gestartet wird, wenn der Computer unter Akkus ausgeführt wird. Bei "false" wird der Task gestartet, wenn der Computer unter "Akkus" ausgeführt wird. Der Standardwert ist True.

## <a name="remarks"></a>Bemerkungen

Beim Lesen oder Schreiben von XML für eine Aufgabe wird diese Einstellung im [**disallowstartifonakkus**](taskschedulerschema-disallowstartifonbatteries-settingstype-element.md) -Element des Taskplaner-Schemas angegeben.

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

 

 





