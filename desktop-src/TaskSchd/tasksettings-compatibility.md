---
title: Tasksettings. Compatibility (Eigenschaft)
description: Ruft bei der Skripterstellung einen ganzzahligen Wert ab, der angibt, mit welcher Version von Taskplaner eine Aufgabe kompatibel ist, oder legt ihn fest
ms.assetid: bbe21177-e010-4770-9068-9c5b41974ee5
keywords:
- Kompatibilitäts Eigenschaft Taskplaner
- Kompatibilitäts Eigenschaft Taskplaner, tasksettings-Objekt
- Tasksettings-Objekt Taskplaner, Compatibility-Eigenschaft
topic_type:
- apiref
api_name:
- TaskSettings.Compatibility
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08ba93d3716a8fb0e701cc783ec83abba40190d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740816"
---
# <a name="tasksettingscompatibility-property"></a>Tasksettings. Compatibility (Eigenschaft)

Ruft bei der Skripterstellung einen ganzzahligen Wert ab, der angibt, mit welcher Version von Taskplaner eine Aufgabe kompatibel ist, oder legt ihn fest

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
TaskSettings.Compatibility As Integer
```



## <a name="property-value"></a>Eigenschaftswert



| Wert                                                                                                                                                                                                                                         | Bedeutung                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span id="TASK_COMPATIBILITY_AT"></span><span id="task_compatibility_at"></span><dl> <dt>**Aufgabe \_ Kompatibilität \_ bei**</dt> <dt>0</dt> </dl> | Der Task ist mit dem AT-Befehl kompatibel.<br/>     |
| <span id="TASK_COMPATIBILITY_V1"></span><span id="task_compatibility_v1"></span><dl> <dt>**Aufgabe \_ Kompatibilität \_ v1**</dt> <dt>1</dt> </dl> | Der Task ist mit Taskplaner 1,0 kompatibel.<br/> |
| <span id="TASK_COMPATIBILITY_V2"></span><span id="task_compatibility_v2"></span><dl> <dt>**Aufgabe \_ Kompatibilität \_ v2**</dt> <dt>2</dt> </dl> | Der Task ist mit Taskplaner 2,0 kompatibel.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Die mit der [**Compatibility**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_compatibility) -Eigenschaft festgelegte Task Kompatibilität sollte nur auf Task Compatibility v1 festgelegt werden, \_ \_ Wenn ein Task auf einen Computer mit Windows XP, Windows Server 2003 oder Windows 2000 zugreifen oder diese ändern muss. Andernfalls wird empfohlen, dass die Kompatibilität mit Taskplaner 2,0 verwendet wird, da die Aufgabe mehr Funktionen enthält.

Aufgaben, die mit dem AT-Befehl kompatibel sind, können nur einen Zeit-und Zeit-

Aufgaben, die mit Taskplaner 1,0 kompatibel sind, können nur einen Zeit-oder einen Logon-Triggern oder einen Start-Triggervorgang aufweisen, und der Task kann nur eine ausführbare Aktion aufweisen.

Weitere Informationen zur Aufgaben Kompatibilität finden Sie unter [Neues in Taskplaner](what-s-new-in-task-scheduler.md) und [Aufgaben](tasks.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Aufgaben \_ Kompatibilität**](/windows/desktop/api/taskschd/ne-taskschd-task_compatibility)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





