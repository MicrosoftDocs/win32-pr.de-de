---
title: Weeklyauslöst. weeksinterval (Eigenschaft)
description: Ruft bei der Skripterstellung das Intervall zwischen den Wochen im Zeitplan ab oder legt es fest.
ms.assetid: 7992dee2-1725-4325-9fe9-eaff84fa5adc
keywords:
- Weeksinterval-Eigenschaft Taskplaner
- Weeksinterval-Eigenschaft Taskplaner, weeklyauslöserobjekt
- Weeklyauslöserobjekt Taskplaner, weeksinterval (Eigenschaft)
topic_type:
- apiref
api_name:
- WeeklyTrigger.WeeksInterval
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4668b68d0b3f83e096284db35df799a63eb677b8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340768"
---
# <a name="weeklytriggerweeksinterval-property"></a>Weeklyauslöst. weeksinterval (Eigenschaft)

Ruft bei der Skripterstellung das Intervall zwischen den Wochen im Zeitplan ab oder legt es fest.

## <a name="syntax"></a>Syntax


```VB
WeeklyTrigger.WeeksInterval As short
```



## <a name="property-value"></a>Eigenschaftswert

Das Intervall zwischen den Wochen im Zeitplan.

## <a name="remarks"></a>Bemerkungen

Ein Intervall von 1 erzeugt einen wöchentlichen Zeitplan. Ein Intervall von 2 erzeugt einen Zeitplan für jede Woche.

Beim Lesen oder schreiben Ihrer eigenen XML-Daten für eine Aufgabe wird das Intervall für einen wöchentlichen Zeitplan mit dem [**weeksinterval**](taskschedulerschema-weeksinterval-weeklyscheduletype-element.md) -Element des Taskplaner-Schemas angegeben.

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

 

 





