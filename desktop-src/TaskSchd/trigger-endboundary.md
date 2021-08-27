---
title: Trigger.EndBoundary-Eigenschaft
description: Ruft für die Skripterstellung das Datum und die Uhrzeit ab, zu der der Trigger deaktiviert wird, oder legt diese fest. Der Trigger kann die Aufgabe nicht starten, nachdem sie deaktiviert wurde.
ms.assetid: f34e6ba8-f6ef-43a0-8e3a-76c6a5f1ac04
keywords:
- EndBoundary-Eigenschaft Taskplaner
- EndBoundary-Eigenschaft Taskplaner , Trigger-Objekt
- Triggerobjekt Taskplaner , EndBoundary-Eigenschaft
topic_type:
- apiref
api_name:
- Trigger.EndBoundary
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4f2b72100a7b981246788b38572c014a722c126115ab5a77d77eb7d96273f5c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120010450"
---
# <a name="triggerendboundary-property"></a>Trigger.EndBoundary-Eigenschaft

Ruft für die Skripterstellung das Datum und die Uhrzeit ab, zu der der Trigger deaktiviert wird, oder legt diese fest. Der Trigger kann die Aufgabe nicht starten, nachdem sie deaktiviert wurde.

## <a name="syntax"></a>Syntax


```VB
Trigger.EndBoundary As String
```



## <a name="property-value"></a>Eigenschaftswert

Datum und Uhrzeit der Deaktivierung des Triggers. Datum und Uhrzeit müssen im folgenden Format vorliegen: JJJJ-MM-TTTHH:MM:SS(+-)HH:MM. Beispielsweise würde das Datum 11. Oktober 2005 um 1:21:17 Uhr in der Zeitzone Pazifik als 2005-10-11T13:21:17-08:00 geschrieben werden. Im Abschnitt (+-)HH:MM des Formats wird die Zeitzone als eine bestimmte Anzahl von Stunden vor oder hinter koordinierte Weltzeit (Greenwich Mean Time) beschrieben.

## <a name="remarks"></a>Hinweise

Beim Lesen oder Schreiben von XML für eine Aufgabe wird die aktivierte Eigenschaft mithilfe des [**EndBoundary-Elements**](taskschedulerschema-endboundary-triggerbasetype-element.md) des Taskplaner Schemas angegeben.

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

 

 





