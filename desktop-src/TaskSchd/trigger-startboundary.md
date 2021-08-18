---
title: Trigger.StartBoundary-Eigenschaft
description: Ruft für die Skripterstellung das Datum und die Uhrzeit ab, zu der der Trigger aktiviert wird, oder legt diese fest.
ms.assetid: 0687cdda-e72c-47cd-ac0c-0de2f8afc3e8
keywords:
- Taskplaner der StartBoundary-Eigenschaft
- StartBoundary-Eigenschaft Taskplaner , Trigger-Objekt
- Triggerobjekt Taskplaner , StartBoundary-Eigenschaft
topic_type:
- apiref
api_name:
- Trigger.StartBoundary
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b49fa865c215c3190b2d081390c98eec1336ffb00a4bf1e9dd9d94226105e96
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002078"
---
# <a name="triggerstartboundary-property"></a>Trigger.StartBoundary-Eigenschaft

Ruft für die Skripterstellung das Datum und die Uhrzeit ab, zu der der Trigger aktiviert wird, oder legt diese fest.

## <a name="syntax"></a>Syntax


```VB
Trigger.StartBoundary As String
```



## <a name="property-value"></a>Eigenschaftswert

Datum und Uhrzeit der Aktivierung des Triggers. Datum und Uhrzeit müssen im folgenden Format vorliegen: JJJJ-MM-TTTHH:MM:SS(+-)HH:MM. Beispielsweise würde das Datum 11. Oktober 2005 um 1:21:17 Uhr in der Pacific Time Zone als 2005-10-11T13:21:17-08:00 geschrieben werden. Im Abschnitt (+-)HH:MM des Formats wird die Zeitzone als eine bestimmte Anzahl von Stunden vor oder hinter koordinierte Weltzeit (Greenwich Mean Time) beschrieben.

## <a name="remarks"></a>Hinweise

Beim Lesen oder Schreiben von XML für eine Aufgabe wird die Startgrenze des Triggers im [**StartBoundary-Element**](taskschedulerschema-startboundary-triggerbasetype-element.md) des Taskplaner Schemas angegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





