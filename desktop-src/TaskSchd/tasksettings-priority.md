---
title: TaskSettings.Priority-Eigenschaft
description: Für die Skripterstellung ruft die Prioritätsebene der Aufgabe ab oder legt diese fest.
ms.assetid: 2548fcb6-c649-4822-a2ea-77546aac2ec5
keywords:
- Prioritätseigenschaft Taskplaner
- Priority-Eigenschaft Taskplaner , TaskSettings-Objekt
- TaskSettings-Objekt Taskplaner , Priority-Eigenschaft
topic_type:
- apiref
api_name:
- TaskSettings.Priority
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7b24c0281e8df314b070e0569176899b96071e1ef43caab17af4978e74f6b18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118354827"
---
# <a name="tasksettingspriority-property"></a>TaskSettings.Priority-Eigenschaft

Für die Skripterstellung ruft die Prioritätsebene der Aufgabe ab oder legt diese fest.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
TaskSettings.Priority As Integer
```



## <a name="property-value"></a>Eigenschaftswert

Die Prioritätsebene (0-10) der Aufgabe. Der Standard ist 7.

## <a name="remarks"></a>Hinweise

Prioritätsstufe 0 ist die höchste Priorität, prioritätsebene 10 die niedrigste Priorität. Der Standardwert ist 7. Die Prioritätsstufen 7 und 8 werden für Hintergrundaufgaben und die Prioritätsebenen 4, 5 und 6 für interaktive Aufgaben verwendet.

Die Aktion der Aufgabe wird in einem Prozess mit einer Priorität gestartet, die auf einem Priority Class-Wert basiert. Ein Wert der Prioritätsebene (Threadpriorität) wird für COM-Handler-, Meldungsfeld- und E-Mail-Aufgabenaktionen verwendet. Weitere Informationen zu den Werten für Priority Class und Priority Level finden Sie unter [Scheduling Priorities](/windows/desktop/ProcThread/scheduling-priorities). In der folgenden Tabelle sind die möglichen Werte für den *Priority-Parameter* sowie die entsprechenden Werte für Priority Class und Priority Level aufgeführt.



| *Aufgabenpriorität* | Priority-Klasse                 | Prioritätsebene                   |
|-----------------|--------------------------------|----------------------------------|
| 0               | REALTIME \_ \_ PRIORITY-KLASSE      | \_ \_ THREADPRIORITÄTSZEIT \_ KRITISCH |
| 1               | HIGH \_ \_ PRIORITY-KLASSE          | \_THREADPRIORITÄT \_ AM HÖCHSTEN        |
| 2               | ÜBER \_ DER NORMAL \_ \_ PRIORITY-KLASSE | \_THREADPRIORITÄT \_ ÜBER \_ NORMAL  |
| 3               | ÜBER \_ DER NORMAL \_ \_ PRIORITY-KLASSE | \_THREADPRIORITÄT \_ ÜBER \_ NORMAL  |
| 4               | NORMAL \_ \_ PRIORITY-KLASSE        | \_THREADPRIORITÄT \_ NORMAL         |
| 5               | NORMAL \_ \_ PRIORITY-KLASSE        | \_THREADPRIORITÄT \_ NORMAL         |
| 6               | NORMAL \_ \_ PRIORITY-KLASSE        | \_THREADPRIORITÄT \_ NORMAL         |
| 7               | UNTERHALB \_ DER \_ NORMAL \_ PRIORITY-KLASSE | \_THREADPRIORITÄT \_ UNTER \_ NORMAL  |
| 8               | UNTERHALB \_ DER \_ NORMAL \_ PRIORITY-KLASSE | \_THREADPRIORITÄT \_ UNTER \_ NORMAL  |
| 9               | IDLE \_ \_ PRIORITY-KLASSE          | \_THREADPRIORITÄT \_ NIEDRIGSTE         |
| 10              | IDLE \_ \_ PRIORITY-KLASSE          | \_THREADPRIORITÄT IM \_ LEERLAUF           |



 

Beim Lesen oder Schreiben von XML für eine Aufgabe wird diese Einstellung im [**Priority (settingsType)-Element**](taskschedulerschema-priority-settingstype-element.md) des Taskplaner angegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**TaskSettings**](tasksettings.md)
</dt> </dl>

 

