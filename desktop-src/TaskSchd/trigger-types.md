---
title: Triggertypen
description: Mit den unten beschriebenen zeitbasierten und ereignisbasierten Triggern können Sie Aufgaben auf unterschiedliche Weise starten.
ms.assetid: 2f577103-3892-49ce-9a3b-7a4839da8a83
keywords:
- triggers Taskplaner , types
- Taskplaner des Starttriggers
- Starttrigger Taskplaner beschrieben
- Taskplaner des Registrierungstriggers
- Registrierungstrigger Taskplaner beschrieben
- kalendertrigger Taskplaner
- Kalendertrigger Taskplaner beschrieben
- täglicher Trigger Taskplaner
- täglicher Trigger Taskplaner beschrieben
- wöchentlicher Trigger Taskplaner
- wöchentlicher Trigger Taskplaner beschrieben
- monatlicher Trigger Taskplaner
- monatlicher Trigger Taskplaner beschrieben
- monthlyDOW-Trigger Taskplaner
- monthlyDOW-Trigger Taskplaner beschrieben
- Ereignistrigger Taskplaner
- Ereignistrigger Taskplaner beschrieben
- Taskplaner des Anmeldetriggers
- Anmeldetrigger Taskplaner beschrieben
- Taskplaner im Leerlauf
- Leerlauftrigger Taskplaner beschrieben
- Day-of-Week-Trigger Taskplaner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a0e09b6ecc1ac3c817f374e70c6756fa09afc78ccaac7e549f3f04ad074c8d0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099690"
---
# <a name="trigger-types"></a>Triggertypen

Mit den unten beschriebenen zeitbasierten und ereignisbasierten Triggern können Sie Aufgaben auf unterschiedliche Weise starten.

## <a name="task-scheduler-20-triggers"></a>Taskplaner 2.0-Trigger

Die folgenden Triggertypen werden durch die [**TASK \_ TRIGGER \_ TYPE2-Enumeration**](/windows/desktop/api/taskschd/ne-taskschd-task_trigger_type2) definiert.

| Trigger                                                                                                                                                                                                                                                                                                                                                                                                                | BESCHREIBUNG                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ereignistrigger (ereignisbasierter Trigger) Informationen zur Skriptentwicklung finden Sie unter [**EventTrigger**](eventtrigger.md).<br/> Informationen zur C++-Entwicklung finden Sie unter [**IEventTrigger**](/windows/desktop/api/taskschd/nn-taskschd-ieventtrigger).<br/> Informationen zur XML-Entwicklung finden Sie unter [**EventTrigger-Element.**](taskschedulerschema-eventtrigger-triggergroup-element.md)<br/>                                                                                             | Startet die Aufgabe, wenn ein bestimmtes Systemereignis auftritt.                                                                                                                                         |
| Zeittrigger (zeitbasierter Trigger)Informationen zur Skriptentwicklung finden Sie unter [**TimeTrigger**](timetrigger.md).<br/> Informationen zur C++-Entwicklung finden Sie unter [**ITimeTrigger**](/windows/desktop/api/taskschd/nn-taskschd-itimetrigger).<br/> Informationen zur XML-Entwicklung finden Sie unter [**TimeTrigger-Element.**](taskschedulerschema-timetrigger-triggergroup-element.md)<br/>                                                                                                      | Startet die Aufgabe zu einem bestimmten Datum und einer bestimmten Uhrzeit.                                                                                                                                                 |
| Täglicher Trigger (zeitbasierter Kalendertrigger)Informationen zur Skriptentwicklung finden Sie unter [**DailyTrigger**](dailytrigger.md).<br/> Informationen zur C++-Entwicklung finden Sie unter [**IDailyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-idailytrigger).<br/> Informationen zur XML-Entwicklung finden Sie unter [**CalendarTrigger-Element.**](taskschedulerschema-calendartrigger-triggergroup-element.md)<br/>                                                                                | Startet die Aufgabe zu einem bestimmten Zeitpunkt nach einem täglichen Zeitplan. Die Aufgabe beginnt beispielsweise täglich um 8:00 Uhr oder jeden zweiten Tag.                                                                |
| Wöchentlicher Trigger (zeitbasierter Kalendertrigger)Informationen zur Skriptentwicklung finden Sie unter [**WeeklyTrigger**](weeklytrigger.md).<br/> Informationen zur C++-Entwicklung finden Sie unter [**IWeeklyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iweeklytrigger).<br/> Informationen zur XML-Entwicklung finden Sie unter [**CalendarTrigger-Element.**](taskschedulerschema-calendartrigger-triggergroup-element.md)<br/>                                                                           | Startet die Aufgabe zu einem bestimmten Zeitpunkt nach einem wöchentlichen Zeitplan. Die Aufgabe beginnt beispielsweise jede Woche um 8:00 Uhr an einem bestimmten Wochentag oder jede andere Woche an einem bestimmten Wochentag. |
| Monatlicher Trigger (zeitbasierter Kalendertrigger)Informationen zur Skriptentwicklung finden Sie unter [**MonthlyTrigger**](monthlytrigger.md).<br/> Informationen zur C++-Entwicklung finden Sie unter [**IMonthlyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-imonthlytrigger).<br/> Informationen zur XML-Entwicklung finden Sie unter [**CalendarTrigger-Element.**](taskschedulerschema-calendartrigger-triggergroup-element.md)<br/>                                                                      | Startet die Aufgabe zu einem bestimmten Zeitpunkt nach einem monatlichen Zeitplan. Die Aufgabe beginnt z. B. um 8:00 Uhr an bestimmten Tagen des Monats für bestimmte Monate.                                          |
| Monatlicher DOW-Trigger (Day-of-Week) (zeitbasierter Kalendertrigger)Informationen zur Skriptentwicklung finden Sie unter [**MonthlyDOWTrigger**](monthlydowtrigger.md).<br/> Informationen zur C++-Entwicklung finden Sie unter [**IMonthlyDOWTrigger.**](/windows/desktop/api/taskschd/nn-taskschd-imonthlydowtrigger)<br/> Informationen zur XML-Entwicklung finden Sie unter [**CalendarTrigger-Element.**](taskschedulerschema-calendartrigger-triggergroup-element.md)<br/>                                        | Startet die Aufgabe zu einem bestimmten Zeitpunkt nach einem monatlichen Wochentagszeitplan. Die Aufgabe beginnt z. B. um 8:00 Uhr an bestimmten Wochentagen, Wochen des Monats und Monaten des Jahres.      |
| Leerlauftrigger (ereignisbasierter Trigger)Informationen zur Skriptentwicklung finden Sie unter [**IdleTrigger**](idletrigger.md).<br/> Informationen zur C++-Entwicklung finden Sie unter [**IIdleTrigger.**](/windows/win32/api/taskschd/nn-taskschd-iidletrigger)<br/> Informationen zur XML-Entwicklung finden Sie unter [**IdleTrigger-Element.**](taskschedulerschema-idletrigger-triggergroup-element.md)<br/>                                                                                                     | Startet die Aufgabe, wenn der Computer in den Leerlauf wechselt.                                                                                                                                      |
| Registrierungstrigger (ereignisbasierter Trigger)Informationen zur Skriptentwicklung finden Sie unter [**RegistrationTrigger**](registrationtrigger.md).<br/> Informationen zur C++-Entwicklung finden Sie unter [**IRegistrationTrigger.**](/windows/desktop/api/taskschd/nn-taskschd-iregistrationtrigger)<br/> Informationen zur XML-Entwicklung finden Sie unter [**RegistrationTrigger-Element.**](taskschedulerschema-registrationtrigger-triggergroup-element.md)<br/>                                             | Startet die Aufgabe, wenn der Task registriert oder aktualisiert wird.                                                                                                                                      |
| Starttrigger (ereignisbasierter Trigger)Informationen zur Skriptentwicklung finden Sie unter [**BootTrigger**](boottrigger.md).<br/> Informationen zur C++-Entwicklung finden Sie unter [**IBootTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iboottrigger).<br/> Informationen zur XML-Entwicklung finden Sie unter [**BootTrigger-Element.**](taskschedulerschema-boottrigger-triggergroup-element.md)<br/>                                                                                                     | Startet die Aufgabe, wenn das System gestartet wird.                                                                                                                                                   |
| Logon-Trigger (ereignisbasierter Trigger)Informationen zur Skriptentwicklung finden Sie unter [**LogonTrigger**](logontrigger.md).<br/> Informationen zur C++-Entwicklung finden Sie unter [**ILogonTrigger**](/windows/desktop/api/taskschd/nn-taskschd-ilogontrigger).<br/> Informationen zur XML-Entwicklung finden Sie unter [**LogonTrigger-Element.**](taskschedulerschema-logontrigger-triggergroup-element.md)<br/>                                                                                              | Startet die Aufgabe, wenn sich ein Benutzer anmeldet.                                                                                                                                                         |
| Sitzungszustandsänderungstrigger (ereignisbasierter Trigger)Informationen zur Skriptentwicklung finden Sie unter [**SessionStateChangeTrigger.**](sessionstatechangetrigger.md)<br/> Informationen zur C++-Entwicklung finden Sie unter [**ISessionStateChangeTrigger.**](/windows/desktop/api/taskschd/nn-taskschd-isessionstatechangetrigger)<br/> Informationen zur XML-Entwicklung finden Sie unter [**SessionStateChangeTrigger-Element.**](taskschedulerschema-sessionstatechangetrigger-triggergroup-element.md)<br/> | Startet die Aufgabe, wenn sich der Zustand einer Terminalserversitzung ändert.                                                                                                                                |



 

## <a name="task-scheduler-10-triggers"></a>Taskplaner 1.0-Trigger

Die folgenden Triggertypen werden durch die [**TASK \_ TRIGGER \_ TYPE-Enumeration**](/windows/desktop/api/Mstask/ne-mstask-task_trigger_type) definiert. Informationen zum Implementieren eines der folgenden Trigger finden Sie in der [**TASK \_ TRIGGER-Struktur.**](/windows/desktop/api/Mstask/ns-mstask-task_trigger)

-   Einmal ausgelöst: Startet die Aufgabe ein einziges Mal.
-   Täglicher Trigger: Startet die Aufgabe in einem täglichen Intervall.
-   Wöchentlicher Trigger: Startet die Aufgabe nach einem wöchentlichen Zeitplan.
-   Monatlicher Trigger: Startet die Aufgabe nach einem monatlichen Zeitplan.
-   Monatlicher DOW-Trigger: Startet die Aufgabe nach einem monatlichen Zeitplan für den Wochentag.
-   Bei Leerlauftrigger: Startet die Aufgabe, wenn sich der Computer im Leerlauf befindet.
-   Systemstarttrigger: Startet die Aufgabe, wenn der Computer gestartet wird.
-   Anmeldetrigger: Startet die Aufgabe, wenn sich ein bestimmter Benutzer anmeldet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Aufgabentrigger](task-triggers.md)
</dt> <dt>

[Triggerschnittstellen](trigger-interfaces.md)
</dt> <dt>

[Triggerstrukturen](trigger-structures.md)
</dt> </dl>

 

