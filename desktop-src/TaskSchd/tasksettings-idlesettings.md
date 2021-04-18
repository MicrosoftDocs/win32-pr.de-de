---
title: Tasksettings. idlesettings-Eigenschaft
description: Ruft bei der Skripterstellung die Informationen ab, die angeben, wie die Taskplaner Aufgaben ausführt, wenn sich der Computer im Leerlauf befindet, oder legt diese Informationen fest.
ms.assetid: 5205db6d-668e-498a-bbd5-edfcf66eec7f
keywords:
- Idlesettings-Eigenschaft Taskplaner
- Idlesettings-Eigenschaft Taskplaner, tasksettings-Objekt
- Tasksettings-Objekt Taskplaner, idlesettings-Eigenschaft
topic_type:
- apiref
api_name:
- TaskSettings.IdleSettings
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 972d341d205ff5719f94a9c0a3b44f64c5678495
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344482"
---
# <a name="tasksettingsidlesettings-property"></a>Tasksettings. idlesettings-Eigenschaft

Ruft bei der Skripterstellung die Informationen ab, die angeben, wie die Taskplaner Aufgaben ausführt, wenn sich der Computer im Leerlauf befindet, oder legt diese Informationen fest. Informationen zu Bedingungen im Leerlauf finden Sie unter [Aufgaben im Leerlauf](task-idle-conditions.md).

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
TaskSettings.IdleSettings As IdleSettings
```



## <a name="property-value"></a>Eigenschaftswert

Ein [**idlesettings**](idlesettings.md) -Objekt, das angibt, wie die Taskplaner den Task verarbeitet, wenn der Computer in einen Leerlaufzustand wechselt.

## <a name="remarks"></a>Bemerkungen

Beim Lesen oder Schreiben von XML für eine Aufgabe wird diese Einstellung im [**idlesettings**](taskschedulerschema-idlesettings-settingstype-element.md) -Element des Taskplaner-Schemas angegeben.

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

 

 





