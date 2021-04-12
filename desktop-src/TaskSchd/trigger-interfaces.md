---
title: Auslöse Schnittstellen
description: Die APIs, die zum Verwalten von Triggern verwendet werden, variieren je nach Version der Taskplaner. In beiden Fällen können Sie mit diesen APIs jedoch neue Trigger erstellen, vorhandene Trigger abrufen und aktualisieren sowie nicht mehr benötigte Trigger löschen.
ms.assetid: 94c11f11-72e2-404f-b396-ab7b1be71942
keywords:
- Trigger Taskplaner, Schnittstellen
- Trigger Taskplaner, Schnittstellen, beschrieben
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5357bb745b43c51707d9571c7582a44c9225a7fe
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104316815"
---
# <a name="trigger-interfaces"></a>Auslöse Schnittstellen

Die APIs, die zum Verwalten von Triggern verwendet werden, variieren je nach Version der Taskplaner. In beiden Fällen können Sie mit diesen APIs jedoch neue Trigger erstellen, vorhandene Trigger abrufen und aktualisieren sowie nicht mehr benötigte Trigger löschen.


Anwendungen, die mit Taskplaner 2,0 entwickelt wurden, können-Objekte und-Schnittstellen verwenden, um die Trigger für eine Aufgabe zu erstellen, abzurufen, zu ändern und zu löschen.

In der folgenden Abbildung gibt eine Aufgabe eine Auflistung von Triggern mithilfe der Triggers-Eigenschaft an. Diese Sammlung enthält eine oder mehrere individuelle auslöserapis, wobei jede API einen bestimmten auslösertyp angibt. Beispielsweise enthält die Auflistung in der Abbildung unten einen Start-und einen LOGON-und einen täglichen-Auslösers.

![Taskplaner 2,0-Auslöse Schnittstellen](images/tsktri4.png)

### <a name="object-apis-for-scripting-development"></a>Objekt-APIs für die Skript Entwicklung

Weitere Informationen zu den Methoden und Eigenschaften der Objekte, die zum Angeben von Triggern verwendet werden, finden Sie unter:

-   [**Task Definition**](taskdefinition.md)
-   [**TriggerCollection**](triggercollection.md)
-   [**Trigger**](trigger.md)
-   [**Boottrigger**](boottrigger.md)
-   [**Dailylöst**](dailytrigger.md)
-   [**EventTrigger**](eventtrigger.md)
-   [**Idle-Auslösung**](idletrigger.md)
-   [**Logonauslöst**](logontrigger.md)
-   [**Monthlydowlöst**](monthlydowtrigger.md)
-   [**Monthly-auslöst**](monthlytrigger.md)
-   [**Registration-Auslösers**](registrationtrigger.md)
-   [**TimeTrigger**](timetrigger.md)
-   [**Weeklyauslösers**](weeklytrigger.md)

### <a name="interfaces-apis-for-c-development"></a>Schnittstellen-APIs für die C++-Entwicklung

Weitere Informationen zu den Methoden und Eigenschaften der Schnittstellen, die zum Angeben von Triggern verwendet werden, finden Sie unter:

-   [**Itaskdefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition)
-   [**ITriggerCollection**](/windows/desktop/api/taskschd/nn-taskschd-itriggercollection)
-   [**I-Auslösung**](/windows/desktop/api/taskschd/nn-taskschd-itrigger)
-   [**Iboottrigger**](/windows/desktop/api/taskschd/nn-taskschd-iboottrigger)
-   [**Idaily-Fehler**](/windows/desktop/api/taskschd/nn-taskschd-idailytrigger)
-   [**Ieventvent**](/windows/desktop/api/taskschd/nn-taskschd-ieventtrigger)
-   [**Iidle-Auslösung**](/windows/win32/api/taskschd/nn-taskschd-iidletrigger)
-   [**ILogon-Auslösers**](/windows/desktop/api/taskschd/nn-taskschd-ilogontrigger)
-   [**Imonthlydowlöst**](/windows/desktop/api/taskschd/nn-taskschd-imonthlydowtrigger)
-   [**Imonthly-Auslösung**](/windows/desktop/api/taskschd/nn-taskschd-imonthlytrigger)
-   [**Iregistration-Auslösers**](/windows/desktop/api/taskschd/nn-taskschd-iregistrationtrigger)
-   [**Itimelöst**](/windows/desktop/api/taskschd/nn-taskschd-itimetrigger)
-   [**Iweeklylöst**](/windows/desktop/api/taskschd/nn-taskschd-iweeklytrigger)

## <a name="task-scheduler-10-trigger-interfaces"></a>Taskplaner 1,0-auslöserschnittstellen

Vorhandene Anwendungen, die mit Taskplaner 1,0 entwickelt wurden, können die Methoden verwenden, die über die Taskplaner 1,0-Schnittstellen verfügbar sind, um die Trigger für ein [*Arbeits Element*](w.md)zu erstellen, abzurufen, zu ändern und zu löschen. Beachten Sie jedoch, dass alle Taskplaner 1,0-Schnittstellen, Enumerationen und Strukturen veraltet sind und nicht für die Entwicklung neuer Anwendungen verwendet werden sollten.

Die beiden Schnittstellen, die dazu verwendet werden, sind in der folgenden Abbildung dargestellt. Die [**ischeduledworkitem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) -Schnittstelle wird zum Verwalten aller Trigger verwendet, die mit einer Arbeitsaufgabe verknüpft sind (diese Verwaltung umfasst das Erstellen eines neuen Triggers für das Arbeits Element). Die [**itaskauslöserschnittstelle**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) wird zum Verwalten eines bestimmten Auslösers verwendet.

![Taskplaner 1,0-Auslöse Schnittstellen](images/tsktri2.png)

Die [**ischeduledworkitem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) -Schnittstelle stellt Methoden zum Erstellen eines neuen Triggers für ein Arbeits Element, zum Abrufen der Anzahl von Triggern, die einer Arbeitsaufgabe zugeordnet sind, zum Abrufen der [*triggerstrukturen*](t.md) , die dem Arbeits Element zugeordnet sind, zum Abrufen der [*triggerzeichenfolgen*](t.md) , die der Arbeitsaufgabe zugeordnet sind, sowie zum Löschen von Triggern zur Verfügung.

Sobald das Triggerobjekt verfügbar ist, können Sie die [**itasktrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) -Schnittstelle verwenden, um die triggerstruktur und die Zeichenfolge des Auslösers abzurufen und die Kriterien festzulegen, mit denen der Trigger ausgelöst wird. Diese Schnittstelle wird nur verwendet, wenn Sie mit einem [*taskauslöserobjekt*](t.md)arbeiten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Task Trigger](task-triggers.md)
</dt> <dt>

[Auslösertypen](trigger-types.md)
</dt> <dt>

[Auslöserstrukturen](trigger-structures.md)
</dt> </dl>

 

 