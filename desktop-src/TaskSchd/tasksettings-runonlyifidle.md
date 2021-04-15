---
title: Tasksettings. runonlyimedle (Eigenschaft)
description: Ruft bei der Skripterstellung einen booleschen Wert ab, der angibt, dass die Taskplaner die Aufgabe nur dann ausführen soll, wenn sich der Computer im Leerlauf befindet, oder legt diesen fest.
ms.assetid: fca1d98e-0544-4301-a709-1e0dae762e07
keywords:
- Runonlyimedle-Eigenschaft Taskplaner
- Runonlyifdle-Eigenschaft Taskplaner, tasksettings-Objekt
- Tasksettings-Objekt Taskplaner, runonlyimedle-Eigenschaft
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
ms.openlocfilehash: 8256b2a3d1dd96db9a8f29b49ce10f6c2fdb266d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391754"
---
# <a name="tasksettingsrunonlyifidle-property"></a>Tasksettings. runonlyimedle (Eigenschaft)

Ruft bei der Skripterstellung einen booleschen Wert ab, der angibt, dass die Taskplaner die Aufgabe nur dann ausführen soll, wenn sich der Computer im Leerlauf befindet, oder legt diesen fest.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
TaskSettings.RunOnlyIfIdle As Boolean
```



## <a name="property-value"></a>Eigenschaftswert

Wenn true, gibt die-Eigenschaft an, dass die Taskplaner die Aufgabe nur dann ausführen soll, wenn sich der Computer im Leerlauf befindet. Die Standardeinstellung lautet „false“.

## <a name="remarks"></a>Bemerkungen

Beim Lesen oder Schreiben von XML für eine Aufgabe wird diese Einstellung im [**runonlyimedle**](taskschedulerschema-runonlyifidle-settingstype-element.md) -Element des Taskplaner-Schemas angegeben.

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

 

 





