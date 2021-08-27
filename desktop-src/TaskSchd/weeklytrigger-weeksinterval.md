---
title: WeeklyTrigger.WeeksInterval-Eigenschaft
description: Ruft für die Skripterstellung das Intervall zwischen den Wochen im Zeitplan ab oder legt dieses fest.
ms.assetid: 7992dee2-1725-4325-9fe9-eaff84fa5adc
keywords:
- WeeksInterval-Eigenschaft Taskplaner
- WeeksInterval-Eigenschaft Taskplaner , WeeklyTrigger-Objekt
- WeeklyTrigger-Objekt Taskplaner , WeeksInterval-Eigenschaft
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
ms.openlocfilehash: 547ebc8617d625df3dd0e8dba167bb60682185dfb13897c49524d1894789c933
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080260"
---
# <a name="weeklytriggerweeksinterval-property"></a>WeeklyTrigger.WeeksInterval-Eigenschaft

Ruft für die Skripterstellung das Intervall zwischen den Wochen im Zeitplan ab oder legt dieses fest.

## <a name="syntax"></a>Syntax


```VB
WeeklyTrigger.WeeksInterval As short
```



## <a name="property-value"></a>Eigenschaftswert

Das Intervall zwischen den Wochen im Zeitplan.

## <a name="remarks"></a>Hinweise

Ein Intervall von 1 erzeugt einen wöchentlichen Zeitplan. Ein Intervall von 2 erzeugt einen Zeitplan für jede andere Woche.

Beim Lesen oder Schreiben eigener XML-Daten für eine Aufgabe wird das Intervall für einen wöchentlichen Zeitplan mithilfe des [**WeeksInterval-Elements**](taskschedulerschema-weeksinterval-weeklyscheduletype-element.md) des Taskplaner Schemas angegeben.

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

 

 





