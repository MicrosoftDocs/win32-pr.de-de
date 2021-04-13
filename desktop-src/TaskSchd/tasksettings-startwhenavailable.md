---
title: Tasksettings. startaccessavailable (Eigenschaft)
description: Ruft bei der Skripterstellung einen booleschen Wert ab, der angibt, dass die Taskplaner die Aufgabe jederzeit nach dem geplanten Zeitpunkt starten kann, oder legt diesen fest.
ms.assetid: 911de67c-baf8-4346-9b4c-e39e5f96c0fe
keywords:
- Startin verfügbare Eigenschaft Taskplaner
- Starteinavailable-Eigenschaft Taskplaner, tasksettings-Objekt
- Tasksettings-Objekt Taskplaner, start\verfüg Bare Eigenschaft
topic_type:
- apiref
api_name:
- TaskSettings.StartWhenAvailable
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63325fbf7aa9186e5748294c2ef57302efa0c79b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478363"
---
# <a name="tasksettingsstartwhenavailable-property"></a>Tasksettings. startaccessavailable (Eigenschaft)

Ruft bei der Skripterstellung einen booleschen Wert ab, der angibt, dass die Taskplaner die Aufgabe jederzeit nach dem geplanten Zeitpunkt starten kann, oder legt diesen fest.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
TaskSettings.StartWhenAvailable As Boolean
```



## <a name="property-value"></a>Eigenschaftswert

Wenn true, gibt die-Eigenschaft an, dass die Taskplaner die Aufgabe jederzeit nach Ablauf der geplanten Zeit starten kann. Die Standardeinstellung lautet „false“.

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft gilt nur für zeitbasierte Aufgaben mit einer endbegrenzung oder zeitbasierten Aufgaben, die so festgelegt werden, dass Sie unendlich wiederholt werden.

Tasks, die nach dem geplanten Zeitpunkt gestartet werden (da die [**start\available**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_startwhenavailable) -Eigenschaft auf true festgelegt ist), werden in die Warteschlange der Aufgaben des Taskplaner dienstangs eingereiht und nach einer Verzögerung gestartet. Die Standard Verzögerung beträgt 10 Minuten.

Beim Lesen oder Schreiben von XML für eine Aufgabe wird diese Einstellung im [**starteinavailable**](taskschedulerschema-startwhenavailable-settingstype-element.md) -Element des Taskplaner-Schemas angegeben.

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

 

 





