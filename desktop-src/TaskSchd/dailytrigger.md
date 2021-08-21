---
title: DailyTrigger-Objekt
description: Skriptobjekt, das einen Trigger darstellt, der eine Aufgabe basierend auf einem täglichen Zeitplan startet.
ms.assetid: f03f53a0-0060-4793-96c1-b47a96852579
keywords:
- täglicher Trigger Taskplaner , Objekt
- DailyTrigger-Objekt Taskplaner
- DailyTrigger-Objekt Taskplaner beschrieben
topic_type:
- apiref
api_name:
- DailyTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7b330906b309bbd672fcb9c333bc254fb02ee668549764d7dc1375f6ac405a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060178"
---
# <a name="dailytrigger-object"></a>DailyTrigger-Objekt

Skriptobjekt, das einen Trigger darstellt, der eine Aufgabe basierend auf einem täglichen Zeitplan startet.

## <a name="members"></a>Member

Das **DailyTrigger-Objekt** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Das **DailyTrigger-Objekt** verfügt über diese Eigenschaften.



| Eigenschaft                                                            | Zugriffstyp           | Beschreibung                                                                                                                                                                                 |
|:--------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DaysInterval**](dailytrigger-daysinterval.md)<br/>        | Lesen/Schreiben<br/> | Ruft das Intervall zwischen den Tagen im Zeitplan ab oder legt dieses fest.<br/>                                                                                                                      |
| [**Aktiviert**](trigger-enabled.md)<br/>                       | Lesen/Schreiben<br/> | Geerbt [](trigger.md) vom Trigger-Objekt. Ruft einen booleschen Wert ab, der angibt, ob der Trigger aktiviert ist, oder legt diesen fest.<br/>                                                |
| [**EndBoundary**](trigger-endboundary.md)<br/>               | Lesen/Schreiben<br/> | Geerbt [](trigger.md) vom Trigger-Objekt. Ruft das Datum und die Uhrzeit der Deaktivierung des Triggers ab oder legt diese fest. Der Trigger kann die Aufgabe nicht starten, nachdem sie deaktiviert wurde.<br/> |
| [**ExecutionTimeLimit**](trigger-executiontimelimit.md)<br/> | Lesen/Schreiben<br/> | Geerbt [](trigger.md) vom Trigger-Objekt. Ruft die maximale Zeit ab, die der vom Trigger gestartete Task ausführen darf, oder legt diese fest.<br/>                           |
| [**Id**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | Lesen/Schreiben<br/> | Geerbt [](trigger.md) vom Trigger-Objekt. Ruft den Bezeichner für den Trigger ab oder legt den Bezeichner fest.<br/>                                                                               |
| [**RandomDelay**](dailytrigger-randomdelay.md)<br/>          | Lesen/Schreiben<br/> | Ruft eine Verzögerungszeit ab, die der Startzeit des Triggers zufällig hinzugefügt wird, oder legt diese fest.<br/>                                                                                               |
| [**Wiederholen**](trigger-repetition.md)<br/>                 | Lesen/Schreiben<br/> | Geerbt [](trigger.md) vom Trigger-Objekt. Ruft ab oder legt fest, wie oft der Task ausgeführt wird und wie lange das Wiederholungsmuster wiederholt wird, nachdem der Task gestartet wurde.<br/>          |
| [**StartBoundary**](trigger-startboundary.md)<br/>           | Lesen/Schreiben<br/> | Geerbt [](trigger.md) vom Trigger-Objekt. Ruft das Datum und die Uhrzeit der Aktivierung des Triggers ab oder legt diese fest.<br/>                                                              |
| [**Typ**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | Schreibgeschützt<br/>  | Geerbt [](trigger.md) vom Trigger-Objekt. Ruft den Typ des Triggers ab.<br/>                                                                                              |



 

## <a name="remarks"></a>Hinweise

Die Tageszeit, zu der der Task gestartet wird, wird durch die [**StartBoundary-Eigenschaft**](trigger-startboundary.md) festgelegt.

Ein Intervall von 1 erzeugt einen täglichen Zeitplan. Ein Intervall von 2 erzeugt einen Zeitplan für jeden zweiten Tag usw.

Beim Lesen oder Schreiben eigener XML-Daten für eine Aufgabe wird ein täglicher Trigger mithilfe des [**ScheduleByDay-Elements**](taskschedulerschema-schedulebyday-calendartriggertype-element.md) des Taskplaner Schemas angegeben.

## <a name="examples"></a>Beispiele

Weitere Informationen und ein Codebeispiel für dieses Skriptobjekt finden Sie unter [Daily Trigger Example (Scripting) (Tägliches Triggerbeispiel (Skripterstellung)).](daily-trigger-example--scripting-.md)

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

 

 





