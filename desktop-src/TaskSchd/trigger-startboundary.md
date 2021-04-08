---
title: Auslöse. StartBoundary (Eigenschaft)
description: Ruft bei der Skripterstellung das Datum und die Uhrzeit der Aktivierung des Auslösers ab oder legt diese fest.
ms.assetid: 0687cdda-e72c-47cd-ac0c-0de2f8afc3e8
keywords:
- StartBoundary-Eigenschaft Taskplaner
- StartBoundary-Eigenschaft Taskplaner, Auslöserobjekt
- Auslöse Objekt Taskplaner, StartBoundary-Eigenschaft
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
ms.openlocfilehash: 141e7e4d80d090e92ecb951917f60f972587d4b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740793"
---
# <a name="triggerstartboundary-property"></a>Auslöse. StartBoundary (Eigenschaft)

Ruft bei der Skripterstellung das Datum und die Uhrzeit der Aktivierung des Auslösers ab oder legt diese fest.

## <a name="syntax"></a>Syntax


```VB
Trigger.StartBoundary As String
```



## <a name="property-value"></a>Eigenschaftswert

Das Datum und die Uhrzeit der Aktivierung des Auslösers. Das Datum und die Uhrzeit müssen im folgenden Format vorliegen: yyyy-mm-ddThh: mm: SS (+-) hh: mm. Beispielsweise würde das Datum am 11. Oktober 2005 um 1:21:17 in der Pacific Time Zone als "2005-10-11t13:21:17-08:00" geschrieben werden. Der Abschnitt (+-) hh: mm des Formats beschreibt die Zeitzone als eine bestimmte Anzahl von Stunden vor oder hinter koordinierter Weltzeit (Greenwich Mean Time).

## <a name="remarks"></a>Bemerkungen

Beim Lesen oder Schreiben von XML für eine Aufgabe wird die Start Grenze des Auslösers im [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) -Element des Taskplaner Schemas angegeben.

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

 

 





