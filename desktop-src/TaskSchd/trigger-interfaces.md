---
title: Triggerschnittstellen
description: Die APIs, die zum Verwalten von Triggern verwendet werden, variieren je nach Version der Taskplaner. In beiden Fällen können Sie mit diesen APIs jedoch neue Trigger erstellen, vorhandene Trigger abrufen und aktualisieren und nicht mehr benötigte Trigger löschen.
ms.assetid: 94c11f11-72e2-404f-b396-ab7b1be71942
keywords:
- Trigger Taskplaner , Schnittstellen
- Trigger Taskplaner , Schnittstellen, beschrieben
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5515f2b1e2f5b4a7694dec28bb8831c690da0d303cda53338714c1b0e03ddaa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002186"
---
# <a name="trigger-interfaces"></a>Triggerschnittstellen

Die APIs, die zum Verwalten von Triggern verwendet werden, variieren je nach Version der Taskplaner. In beiden Fällen können Sie mit diesen APIs jedoch neue Trigger erstellen, vorhandene Trigger abrufen und aktualisieren und nicht mehr benötigte Trigger löschen.


Anwendungen, die mit Taskplaner 2.0 entwickelt werden, können Objekte und Schnittstellen verwenden, um die Trigger für eine Aufgabe zu erstellen, abzurufen, zu ändern und zu löschen.

In der folgenden Abbildung gibt eine Aufgabe mithilfe der Trigger-Eigenschaft eine Auflistung von Triggern an. Diese Sammlung enthält eine oder mehrere einzelne Trigger-APIs, bei der jede API einen bestimmten Triggertyp an gibt. In der Abbildung unten enthält die Triggersammlung beispielsweise einen Starttrigger, einen Logon-Trigger und einen täglichen Trigger.

![Triggerschnittstellen des Taskplaners 2.0](images/tsktri4.png)

### <a name="object-apis-for-scripting-development"></a>Objekt-APIs für die Skriptentwicklung

Weitere Informationen zu den Methoden und Eigenschaften der Objekte, die zum Angeben von Triggern verwendet werden, finden Sie unter:

-   [**TaskDefinition**](taskdefinition.md)
-   [**Triggercollection**](triggercollection.md)
-   [**Trigger**](trigger.md)
-   [**BootTrigger**](boottrigger.md)
-   [**DailyTrigger**](dailytrigger.md)
-   [**EventTrigger**](eventtrigger.md)
-   [**IdleTrigger**](idletrigger.md)
-   [**LogonTrigger**](logontrigger.md)
-   [**MonthlyDOWTrigger**](monthlydowtrigger.md)
-   [**MonthlyTrigger**](monthlytrigger.md)
-   [**RegistrationTrigger**](registrationtrigger.md)
-   [**TimeTrigger**](timetrigger.md)
-   [**WeeklyTrigger**](weeklytrigger.md)

### <a name="interfaces-apis-for-c-development"></a>Schnittstellen-APIs für die C++-Entwicklung

Weitere Informationen zu den Methoden und Eigenschaften der Schnittstellen, die zum Angeben von Triggern verwendet werden, finden Sie unter:

-   [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition)
-   [**ITriggerCollection**](/windows/desktop/api/taskschd/nn-taskschd-itriggercollection)
-   [**ITrigger**](/windows/desktop/api/taskschd/nn-taskschd-itrigger)
-   [**IBootTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iboottrigger)
-   [**IDailyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-idailytrigger)
-   [**IEventTrigger**](/windows/desktop/api/taskschd/nn-taskschd-ieventtrigger)
-   [**IIdleTrigger**](/windows/win32/api/taskschd/nn-taskschd-iidletrigger)
-   [**ILogonTrigger**](/windows/desktop/api/taskschd/nn-taskschd-ilogontrigger)
-   [**IMonthlyDOWTrigger**](/windows/desktop/api/taskschd/nn-taskschd-imonthlydowtrigger)
-   [**IMonthlyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-imonthlytrigger)
-   [**IRegistrationTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iregistrationtrigger)
-   [**ITimeTrigger**](/windows/desktop/api/taskschd/nn-taskschd-itimetrigger)
-   [**IWeeklyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iweeklytrigger)

## <a name="task-scheduler-10-trigger-interfaces"></a>Taskplaner 1.0-Triggerschnittstellen

Vorhandene Anwendungen, die mit Taskplaner 1.0 entwickelt werden, können die methoden verwenden, die über die Taskplaner 1.0-Schnittstellen verfügbar sind, um die Trigger für ein Arbeitselement zu erstellen, abzurufen, zu ändern und zu [*löschen.*](w.md) Beachten Sie jedoch, dass Taskplaner 1.0-Schnittstellen, -Enumerationen und -Strukturen veraltet sind und nicht für die Entwicklung neuer Anwendungen verwendet werden sollten.

Die beiden Schnittstellen, die dazu verwendet werden, sind in der folgenden Abbildung dargestellt. Die [**IScheduledWorkItem-Schnittstelle**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) wird verwendet, um alle Trigger zu verwalten, die einem Arbeitselement zugeordnet sind (eine solche Verwaltung umfasst das Erstellen eines neuen Triggers für das Arbeitselement). Die [**ITaskTrigger-Schnittstelle**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) wird verwendet, um einen bestimmten Trigger zu verwalten.

![Triggerschnittstellen des Taskplaners 1.0](images/tsktri2.png)

Die [**IScheduledWorkItem-Schnittstelle**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) bietet Methoden zum Erstellen eines neuen Triggers für ein Arbeitselement, zum Abrufen [](t.md) der Anzahl von Triggern, die [](t.md) einem Arbeitselement zugeordnet sind, zum Abrufen der Triggerstrukturen, die dem Arbeitselement zugeordnet sind, zum Abrufen von Triggerzeichenfolgen, die dem Arbeitselement zugeordnet sind, und zum Löschen von Triggern.

Sobald das Triggerobjekt verfügbar ist, können Sie mithilfe der [**ITaskTrigger-Schnittstelle**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) die Triggerstruktur und die Zeichenfolge des Triggers abrufen und die Kriterien festlegen, die zum Auslösen des Triggers verwendet werden. Diese Schnittstelle wird nur verwendet, wenn Sie mit einem Aufgabentriggerobjekt [*arbeiten.*](t.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Aufgabentrigger](task-triggers.md)
</dt> <dt>

[Triggertypen](trigger-types.md)
</dt> <dt>

[Triggerstrukturen](trigger-structures.md)
</dt> </dl>

 

 