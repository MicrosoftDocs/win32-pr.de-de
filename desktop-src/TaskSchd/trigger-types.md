---
title: Auslösertypen
description: Mit den zeitbasierten und ereignisbasierten Triggern, die unten beschrieben werden, können Sie Aufgaben auf verschiedene Weise starten.
ms.assetid: 2f577103-3892-49ce-9a3b-7a4839da8a83
keywords:
- Trigger Taskplaner, Typen
- Start auslöserTaskplaner
- Taskplaner des Start Auslösers, beschrieben
- Registrierungs-Auslöse Taskplaner
- Registrierungs auslöserTaskplaner, beschrieben
- Kalender-Auslöse Taskplaner
- Taskplaner des Kalender Auslösers, beschrieben
- täglicher Auslöse Taskplaner
- täglicher Taskplaner des Auslösers, beschrieben
- wöchentlicher Auslöse Taskplaner
- wöchentlicher auslöserTaskplaner, beschrieben
- Monatlicher Auslöse Taskplaner
- Monatlicher auslöserTaskplaner, beschrieben
- monthlydow-Taskplaner
- monthlydow-Taskplaner, beschrieben
- Ereignis auslösende Taskplaner
- Taskplaner von Ereignis Auslösers, beschrieben
- Taskplaner LOGON-
- Logon-Taskplaner, beschrieben
- Taskplaner im Leerlauf
- Taskplaner im Leerlauf, beschrieben
- Taskplaner für einen Tag der Woche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fee1e846e4b2fa8138f675cdd39e926884d2bfae
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106339084"
---
# <a name="trigger-types"></a>Auslösertypen

Mit den zeitbasierten und ereignisbasierten Triggern, die unten beschrieben werden, können Sie Aufgaben auf verschiedene Weise starten.

## <a name="task-scheduler-20-triggers"></a>Taskplaner 2,0-Trigger

Die folgenden Auslösertypen werden von der Typ2-Enumeration des [**Task \_ Auslösers \_**](/windows/desktop/api/taskschd/ne-taskschd-task_trigger_type2) definiert.

| Trigger                                                                                                                                                                                                                                                                                                                                                                                                                | BESCHREIBUNG                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ereignis Trigger (ereignisbasierter Trigger) für die Skript Entwicklung finden Sie unter [**EventTrigger**](eventtrigger.md).<br/> Informationen zur C++-Entwicklung finden Sie unter [**ieventvent**](/windows/desktop/api/taskschd/nn-taskschd-ieventtrigger).<br/> Informationen zur XML-Entwicklung finden Sie unter [**EventTrigger-Element**](taskschedulerschema-eventtrigger-triggergroup-element.md).<br/>                                                                                             | Startet die Aufgabe, wenn ein bestimmtes System Ereignis auftritt.                                                                                                                                         |
| Zeit Auslösung (zeitbasierter-Auslösung) für die Skript Entwicklung finden Sie unter [**timetimeout**](timetrigger.md).<br/> Informationen zur C++-Entwicklung finden Sie unter [**itimelöst**](/windows/desktop/api/taskschd/nn-taskschd-itimetrigger).<br/> Informationen zur XML-Entwicklung finden Sie unter [**time-Auslöse Element**](taskschedulerschema-timetrigger-triggergroup-element.md).<br/>                                                                                                      | Startet die Aufgabe zu einem bestimmten Zeitpunkt (Datum und Uhrzeit).                                                                                                                                                 |
| Täglicher-Fehler (zeitbasierter Kalender-Auslösung) für die Skript Entwicklung finden Sie unter [**Daily-**](dailytrigger.md)Fehler.<br/> Informationen zur C++-Entwicklung finden Sie unter [**idailylöst**](/windows/desktop/api/taskschd/nn-taskschd-idailytrigger).<br/> Informationen zur XML-Entwicklung finden Sie unter [**calendarauslöserelement**](taskschedulerschema-calendartrigger-triggergroup-element.md).<br/>                                                                                | Startet die Aufgabe zu einem bestimmten Zeitpunkt nach einem täglichen Zeitplan. Der Task wird z. b. täglich um 8:00 Uhr oder jeden anderen Tag gestartet.                                                                |
| Der wöchentliche-Auslösung (zeitbasierter Kalender-Auslösung) für die Skript Entwicklung finden Sie unter [**Weekly-**](weeklytrigger.md)Fehler.<br/> Informationen zur C++-Entwicklung finden Sie unter [**iweeklylöst**](/windows/desktop/api/taskschd/nn-taskschd-iweeklytrigger).<br/> Informationen zur XML-Entwicklung finden Sie unter [**calendarauslöserelement**](taskschedulerschema-calendartrigger-triggergroup-element.md).<br/>                                                                           | Startet die Aufgabe zu einem bestimmten Zeitpunkt in einem wöchentlichen Zeitplan. Der Task wird z. b. jede Woche um 8:00 Uhr an einem bestimmten Wochentag oder an einem bestimmten Wochentag in der Woche gestartet. |
| Monatlicher-Auslösung (zeitbasierter Kalender-Auslösung) für die Skript Entwicklung finden Sie unter [**Monthly-**](monthlytrigger.md)Auslösung.<br/> Informationen zur C++-Entwicklung finden Sie unter [**imonthlyauslöst**](/windows/desktop/api/taskschd/nn-taskschd-imonthlytrigger).<br/> Informationen zur XML-Entwicklung finden Sie unter [**calendarauslöserelement**](taskschedulerschema-calendartrigger-triggergroup-element.md).<br/>                                                                      | Startet die Aufgabe zu einem bestimmten Zeitpunkt nach einem monatlichen Zeitplan. Der Task wird z. b. um 8:00 Uhr an bestimmten Tagen des Monats in bestimmten Monaten gestartet.                                          |
| Monatlicher "Day of week"-(Dow-) (zeitbasierter Kalender-Auslösung) für die Skript Entwicklung finden Sie unter [**monthlydow-**](monthlydowtrigger.md)Auslösung.<br/> Informationen zur C++-Entwicklung finden Sie unter [**imonthlydowlöst**](/windows/desktop/api/taskschd/nn-taskschd-imonthlydowtrigger).<br/> Informationen zur XML-Entwicklung finden Sie unter [**calendarauslöserelement**](taskschedulerschema-calendartrigger-triggergroup-element.md).<br/>                                        | Startet die Aufgabe zu einem bestimmten Zeitpunkt an einem monatlichen Zeitplan für Wochentage. Der Task wird beispielsweise um 8:00 Uhr an bestimmten Tagen der Woche, Wochen des Monats und Monaten des Jahres gestartet.      |
| Der Leerlauf-(ereignisbasierte) für die Skript Entwicklung finden Sie unter [**Idle-**](idletrigger.md)Auslösung.<br/> Informationen zur C++-Entwicklung finden Sie unter [**iidleauslöst**](/windows/win32/api/taskschd/nn-taskschd-iidletrigger).<br/> Informationen zur XML-Entwicklung finden Sie unter [**idleauslöserelement**](taskschedulerschema-idletrigger-triggergroup-element.md).<br/>                                                                                                     | Startet den Task, wenn der Computer in den Leerlauf wechselt.                                                                                                                                      |
| Registrierungs-(ereignisbasierter) Registrierungs-(ereignisbasierter) Registrierungs-Assistent für die Skript Entwicklung finden Sie unter [**Registration**](registrationtrigger.md)<br/> Informationen zur C++-Entwicklung finden Sie unter [**iregistrationlöst**](/windows/desktop/api/taskschd/nn-taskschd-iregistrationtrigger).<br/> Informationen zur XML-Entwicklung finden Sie unter [**Registration-Auslöse Element**](taskschedulerschema-registrationtrigger-triggergroup-element.md).<br/>                                             | Startet die Aufgabe, wenn die Aufgabe registriert oder aktualisiert wird.                                                                                                                                      |
| Start-und ereignisbasierter Auslösung für die Skript Entwicklung finden Sie unter [**boottrigger**](boottrigger.md).<br/> Informationen zur C++-Entwicklung finden Sie unter [**iboottrigger**](/windows/desktop/api/taskschd/nn-taskschd-iboottrigger).<br/> Informationen zur XML-Entwicklung finden Sie unter [**boottrigger-Element**](taskschedulerschema-boottrigger-triggergroup-element.md).<br/>                                                                                                     | Startet die Aufgabe, wenn das System gestartet wird.                                                                                                                                                   |
| Ein Logon-(ereignisbasierter) Logon-Ereignis für die Skript Entwicklung finden Sie unter [**logonlöst**](logontrigger.md).<br/> Informationen zur C++-Entwicklung finden Sie unter [**ilogonlöst**](/windows/desktop/api/taskschd/nn-taskschd-ilogontrigger).<br/> Informationen zur XML-Entwicklung finden Sie unter [**logonauslöst-Element**](taskschedulerschema-logontrigger-triggergroup-element.md).<br/>                                                                                              | Startet die Aufgabe, wenn sich ein Benutzer anmeldet.                                                                                                                                                         |
| Der Sitzungs Status Änderungs-Auslösung (ereignisbasierter-Auslösung) für die Skript Entwicklung finden Sie unter [**sessionstatechangelöst**](sessionstatechangetrigger.md).<br/> Informationen zur C++-Entwicklung finden Sie unter [**isessionstatechangelöst**](/windows/desktop/api/taskschd/nn-taskschd-isessionstatechangetrigger).<br/> Informationen zur XML-Entwicklung finden Sie unter [**sessionstatechange-Element**](taskschedulerschema-sessionstatechangetrigger-triggergroup-element.md).<br/> | Startet die Aufgabe, wenn sich der Status einer Terminal Server Sitzung ändert.                                                                                                                                |



 

## <a name="task-scheduler-10-triggers"></a>Taskplaner 1,0-Trigger

Die folgenden [**\_ \_ Auslösertypen**](/windows/desktop/api/Mstask/ne-mstask-task_trigger_type) werden von der Aufgabentyp-Enumeration des Tasks definiert. Wenn Sie einen der folgenden Trigger implementieren möchten, finden Sie weitere Informationen unter [**Task \_ triggerstruktur**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) .

-   Once-Auslösung: startet die Aufgabe einmalig.
-   Täglicher-Vorgang: startet die Aufgabe in einem täglichen Intervall.
-   Wöchentlicher-Auslösers: startet die Aufgabe nach einem wöchentlichen Zeitplan.
-   Monatlicher Auslösung: startet die Aufgabe nach einem monatlichen Zeitplan.
-   Monatlicher Dow-Vorgang: startet die Aufgabe an einem monatlichen Wochentag.
-   On Idle-Auslösung: startet die Aufgabe, wenn sich der Computer im Leerlauf befindet.
-   System Start-Fehler: startet den Task, wenn der Computer gestartet wird.
-   Logon-auslöst: startet die Aufgabe, wenn sich ein bestimmter Benutzer anmeldet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Task Trigger](task-triggers.md)
</dt> <dt>

[Auslöse Schnittstellen](trigger-interfaces.md)
</dt> <dt>

[Auslöserstrukturen](trigger-structures.md)
</dt> </dl>

 

