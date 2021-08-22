---
title: WeeklyTrigger-Objekt
description: Skriptobjekt, das einen Trigger darstellt, der eine Aufgabe basierend auf einem wöchentlichen Zeitplan startet.
ms.assetid: a000d7a8-0239-440f-b49b-7f0c55b01e8e
keywords:
- wöchentlicher Trigger Taskplaner , -Objekt
- WeeklyTrigger-Objekt Taskplaner
- WeeklyTrigger-Objekt Taskplaner beschrieben
topic_type:
- apiref
api_name:
- WeeklyTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51eb48b03efb49bd5642909af4b99b99bfb1f7f139b97f8410e0d5f014843ddf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001788"
---
# <a name="weeklytrigger-object"></a>WeeklyTrigger-Objekt

Skriptobjekt, das einen Trigger darstellt, der eine Aufgabe basierend auf einem wöchentlichen Zeitplan startet. Die Aufgabe beginnt z. B. um 8:00 Uhr. an einem bestimmten Wochentag jede Woche oder jede andere Woche.

## <a name="members"></a>Member

Das **WeeklyTrigger-Objekt** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Das **WeeklyTrigger-Objekt** verfügt über diese Eigenschaften.



| Eigenschaft                                                            | Zugriffstyp           | BESCHREIBUNG                                                                                                                                                                                 |
|:--------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DaysOfWeek**](weeklytrigger-daysofweek.md)<br/>           | Lesen/Schreiben<br/> | Ruft die Wochentage ab, an denen der Task ausgeführt wird, oder legt diese fest.<br/>                                                                                                                        |
| [**Aktiviert**](trigger-enabled.md)<br/>                       | Lesen/Schreiben<br/> | Geerbt [](trigger.md) vom Trigger-Objekt. Ruft einen booleschen Wert ab, der angibt, ob der Trigger aktiviert ist, oder legt diesen fest.<br/>                                                |
| [**EndBoundary**](trigger-endboundary.md)<br/>               | Lesen/Schreiben<br/> | Geerbt [](trigger.md) vom Trigger-Objekt. Ruft das Datum und die Uhrzeit der Deaktivierung des Triggers ab oder legt diese fest. Der Trigger kann die Aufgabe nicht starten, nachdem sie deaktiviert wurde.<br/> |
| [**ExecutionTimeLimit**](trigger-executiontimelimit.md)<br/> | Lesen/Schreiben<br/> | Geerbt [](trigger.md) vom Trigger-Objekt. Ruft die maximale Zeit ab, die der vom Trigger gestartete Task ausführen darf, oder legt diese fest.<br/>                           |
| [**Id**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | Lesen/Schreiben<br/> | Geerbt [](trigger.md) vom Trigger-Objekt. Ruft den Bezeichner für den Trigger ab oder legt den Bezeichner fest.<br/>                                                                               |
| [**RandomDelay**](weeklytrigger-randomdelay.md)<br/>         | Lesen/Schreiben<br/> | Ruft eine Verzögerungszeit ab, die der Startzeit des Triggers zufällig hinzugefügt wird, oder legt diese fest.<br/>                                                                                               |
| [**Wiederholen**](trigger-repetition.md)<br/>                 | Lesen/Schreiben<br/> | Geerbt [](trigger.md) vom Trigger-Objekt. Ruft ab oder legt fest, wie oft der Task ausgeführt wird und wie lange das Wiederholungsmuster wiederholt wird, nachdem der Task gestartet wurde.<br/>          |
| [**StartBoundary**](trigger-startboundary.md)<br/>           | Lesen/Schreiben<br/> | Geerbt [](trigger.md) vom Trigger-Objekt. Ruft das Datum und die Uhrzeit der Aktivierung des Triggers ab oder legt diese fest.<br/>                                                              |
| [**type**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | Schreibgeschützt<br/>  | Geerbt [](trigger.md) vom Trigger-Objekt. Ruft den Typ des Triggers ab.<br/>                                                                                              |
| [**WeeksInterval**](weeklytrigger-weeksinterval.md)<br/>     | Lesen/Schreiben<br/> | Ruft das Intervall zwischen den Wochen im Zeitplan ab oder legt dieses fest.<br/>                                                                                                                     |



 

## <a name="remarks"></a>Hinweise

Die Tageszeit, zu der der Task gestartet wird, wird durch die [**StartBoundary-Eigenschaft**](trigger-startboundary.md) festgelegt.

Beim Lesen oder Schreiben eigener XML-Daten für eine Aufgabe wird ein wöchentlicher Trigger mithilfe des [**ScheduleByWeek-Elements**](taskschedulerschema-schedulebyweek-calendartriggertype-element.md) des Taskplaner Schemas angegeben.

## <a name="examples"></a>Beispiele

Weitere Informationen und ein Codebeispiel für dieses Skriptobjekt finden Sie unter Beispiel für [wöchentliche Trigger (Skripterstellung).](weekly-trigger-example--scripting-.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Trigger**](trigger.md)
</dt> <dt>

[**Triggercollection**](triggercollection.md)
</dt> <dt>

[**TriggerCollection.Create**](triggercollection-create.md)
</dt> </dl>

 

 





