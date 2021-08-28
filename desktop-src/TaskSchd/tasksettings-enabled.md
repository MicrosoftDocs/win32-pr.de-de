---
title: TaskSettings.Enabled-Eigenschaft
description: Ruft für die Skripterstellung einen booleschen Wert ab, der angibt, dass der Task aktiviert ist, oder legt diesen fest. Die Aufgabe kann nur ausgeführt werden, wenn diese Einstellung auf True festgelegt ist.
ms.assetid: af8aa237-3402-4a82-b6ef-b713e1757d3a
keywords:
- Aktivierte Taskplaner
- Enabled-Eigenschaft Taskplaner , TaskSettings-Objekt
- TaskSettings-Objekt Taskplaner , Enabled-Eigenschaft
topic_type:
- apiref
api_name:
- TaskSettings.Enabled
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e7853177aecae963e4899a67d2ba5b39d1eaebdc75e25ce6e14523963a70c45
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119738161"
---
# <a name="tasksettingsenabled-property"></a>TaskSettings.Enabled-Eigenschaft

Ruft für die Skripterstellung einen booleschen Wert ab, der angibt, dass der Task aktiviert ist, oder legt diesen fest. Die Aufgabe kann nur ausgeführt werden, wenn diese Einstellung auf True festgelegt ist.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
TaskSettings.Enabled As Boolean
```



## <a name="property-value"></a>Eigenschaftswert

True gibt an, dass die Aufgabe aktiviert ist. False gibt an, dass der Task nicht aktiviert ist.

## <a name="remarks"></a>Hinweise

Beim Lesen oder Schreiben von XML für eine Aufgabe wird diese Einstellung im [**Enabled (settingsType)-Element**](taskschedulerschema-enabled-settingstype-element.md) des Taskplaner Schemas angegeben.

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

 

 





