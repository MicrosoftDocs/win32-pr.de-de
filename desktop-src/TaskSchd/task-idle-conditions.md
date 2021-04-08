---
title: Aufgaben im Leerlauf
description: Eine Aufgabe kann auf verschiedene Arten verarbeitet werden, wenn der Computer in den Leerlauf wechselt. Dies umfasst das Definieren eines Leerlauf Auslösers oder das Festlegen der Leerlauf Bedingungen für den Start des Tasks.
ms.assetid: 1e480681-b77a-48fe-a732-dd1591eaa08d
keywords:
- Leerlauf Bedingungen Taskplaner
- Bedingungen Taskplaner im Leerlauf, Diskussion
- Erstellen von inaktiven Triggern Taskplaner
- Leerlauf Trigger Taskplaner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 501be9b73e3ec355b998697fb5e87c5163224b71
ms.sourcegitcommit: 857e701bbd35004661bb047e1f24622af9ff1dd7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/19/2020
ms.locfileid: "103734665"
---
# <a name="task-idle-conditions"></a>Aufgaben im Leerlauf

Eine Aufgabe kann auf verschiedene Arten verarbeitet werden, wenn der Computer in den Leerlauf wechselt. Dies umfasst das Definieren eines Leerlauf Auslösers oder das Festlegen der Leerlauf Bedingungen für den Start des Tasks.

## <a name="detecting-the-idle-state"></a>Erkennen des Leerlauf Zustands

In Windows 7 überprüft der Taskplaner, ob sich der Computer alle 15 Minuten im Leerlauf befindet. Taskplaner überprüft den Leerlauf Status mithilfe von zwei Kriterien: Benutzer Abwesenheit und fehlender Ressourcenverbrauch. Wenn während dieser Zeitspanne keine Tastatur-oder Maus Eingaben vorhanden sind, wird der Benutzer als nicht vorhanden eingestuft. Der Computer gilt als Leerlauf, wenn alle Prozessoren und alle Datenträger für mehr als 90% des letzten Erkennungs Intervalls im Leerlauf waren. (Eine Ausnahme gilt für jede Präsentationstyp Anwendung, die die es \_ festlegt. \_Erforderliches Flag anzeigen. Dieses Flag zwingt den Task Zeitplan, das System unabhängig von der Benutzeraktivität oder dem Ressourcenverbrauch nicht als im Leerlauf befindlich zu sehen.)

In Windows 7 betrachtet Taskplaner einen Prozessor als Leerlauf, auch wenn Threads mit niedriger Priorität (Thread Priorität < normal) ausgeführt werden.

Wenn die Taskplaner in Windows 7 erkennt, dass sich der Computer im Leerlauf befindet, wartet der Dienst nur auf die Benutzereingabe, um das Ende des Leerlauf Zustands zu markieren.

In Windows 8 führt Taskplaner dieselben allgemeinen Überprüfungen auf Benutzer Abwesenheit und Ressourcenverbrauch durch. Taskplaner jedoch das Betriebssystem-Betriebssystem unterstützt, um das vorhanden sein von Benutzern zu erkennen. Standardmäßig wird der Benutzer nach vier Minuten ohne Tastatur-oder Maus Eingaben als nicht vorhanden eingestuft. Die Überprüfungs Zeit für den Ressourcenverbrauch wird auf 10-Minuten-Intervalle verkürzt, wenn der Benutzer vorhanden ist. Wenn der Benutzer nicht mehr angezeigt wird, wird die Überprüfungs Zeit in Intervallen von 30 Sekunden verkürzt. Taskplaner führt zusätzliche Ressourcenverbrauchs Prüfungen für die folgenden Ereignisse aus:

-   Benutzer Anwesenheitsstatus geändert
-   Stromquelle für AC/DC geändert
-   Akku Pegel geändert (nur bei Batterien)

Wenn eines der oben genannten Ereignisse auftritt, testet Taskplaner den Computer seit der letzten Überprüfung auf die Leerlaufzeit. In der Praxis bedeutet dies, dass Taskplaner das System unmittelbar nach dem Zeitpunkt der letzten Überprüfung als Leerlauf deklarieren kann, wenn die anderen Bedingungen erfüllt sind.

In Windows 8 sind die CPU-und e/a-Schwellenwerte auf 80% festgelegt.

Wenn Sie den Leerlauf Status in Windows 8 Server erkennen, werden Taskplaner keine Benutzer Präsenz oder nicht berücksichtigt. Um das Ende des Leerlauf Zustands zu kennzeichnen, Taskplaner den Ressourcenverbrauch einmal in 90 Minuten.

## <a name="defining-an-idle-trigger"></a>Definieren eines Leerlauf-Auslösers

Ein Task kann gestartet werden, wenn der Computer in den Leerlauf wechselt, indem er einen Leerlauf-Auslösers definiert.

Ein Leerlauf-Triggervorgang löst nur dann eine Task Aktion aus, wenn der Computer nach der Start Grenze des Auslösers in einen Leerlaufzustand wechselt.

Eine Anwendung kann mithilfe der [**iidletimeout**](/windows/win32/api/taskschd/nn-taskschd-iidletrigger) -Schnittstelle einen Leerlauf--Auslösers definieren.

Beim Lesen oder Schreiben von XML wird der Leerlauf-Auslösung durch das [**Idle-Auslöserelement**](taskschedulerschema-idletrigger-triggergroup-element.md) des Taskplaner-Schemas angegeben.

## <a name="task-settings-for-idle-conditions"></a>Aufgaben Einstellungen für Leerlauf Bedingungen

Mithilfe der Task Einstellungen können Sie definieren, wie die Taskplaner die Aufgabe verarbeitet, wenn der Computer in den Leerlauf wechselt.

In den folgenden Abbildungen sind drei mögliche Zeitachsen enthalten, die zeigen, wie sich diese unterschiedlichen Leerlauf Bedingungen aufeinander beziehen. Beachten Sie, dass die Abbildungen gestartet werden, wenn der Task-oder-Task ausgelöst wird, oder wenn die Aufgabe bei Bedarf gestartet wird (ohne dass [die vorhandenen Aufgaben Einschränkungen ignoriert](/windows/win32/api/taskschd/ne-taskschd-task_run_flags)werden müssen).

> [!NOTE]
> Die Einstellungen für *Dauer* und *WaitTimeout* sind veraltet. Sie sind weiterhin in der Taskplaner-Benutzeroberfläche vorhanden, und ihre Schnittstellen Methoden geben möglicherweise weiterhin gültige Werte zurück, aber Sie werden nicht mehr verwendet.

![Leerlauf Bedingungs Zeitachse](images/idle-conditions2.png)

In der folgenden Liste werden die Leerlauf Bedingungen beschrieben.
- Leerlauf Start: die Zeit, zu der der Computer in den Leerlauf wechselt.
- Leerlauf Ende: die Zeit, zu der der Computer in den Leerlauf wechselt. Beachten Sie, dass die Zeitspanne, in der sich der Computer im Leerlauf befindet, unabhängig von der zuvor beschriebenen Leerlauf Dauer ist.

Leerlauf Wartezeit und Leerlauf Dauer sind veraltet.
- Leerlauf Wartezeit: die Zeitspanne, die der Taskplaner auf einen Leerlauf Status wartet, nachdem ein Task-ausgelöst wurde, oder nachdem der Task bei Bedarf gestartet wurde.
- Leerlauf Dauer: die Zeitspanne, in der sich der Computer im Leerlauf befinden soll, bevor der Task gestartet wird.

Wenn ein Task z. b. nur gestartet wird, wenn der Computer 30 Minuten lang im Leerlauf ist und der Task darauf wartet, dass der Computer 10 Minuten lang im Leerlauf ist, wird der Task nur dann in 5 Minuten gestartet, wenn sich der Computer vor der Aktivierung des Auslösers 25 Minuten lang im Leerlauf befunden hat. Der Task wird nicht gestartet, wenn der Computer nach der Aktivierung des Auslösers 5 Minuten in den Leerlauf wechselt.

Standardmäßig ist eine Task [**disallowstartifonakkus**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_disallowstartifonbatteries) -Eigenschaft auf true festgelegt. Dies bedeutet, dass der Taskplaner-Dienst keine Tasks durchführt, die von einem Leerlauf Trigger (oder einem Trigger mit Leerlauf Bedingungen) ausgelöst werden, wenn ein Computer im Akku Betrieb ausgeführt wird. Sie können dieses Verhalten ändern, indem Sie die **disallowstartifonakkus** -Eigenschaft auf false festlegen.

Wenn eine Aufgabe durch einen Leerlauf Trigger ausgelöst wird, wird die [**WaitTimeout**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_waittimeout) -Eigenschaft der [**iidlesettings**](/windows/desktop/api/taskschd/nn-taskschd-iidlesettings) -Schnittstelle ([**idlesettings**](idlesettings.md) for Scripting) ignoriert.

Anwendungen können die Leerlauf Bedingungen steuern, indem Sie die Eigenschaften in den Schnittstellen [**iidlesettings**](/windows/desktop/api/taskschd/nn-taskschd-iidlesettings) und [**iidletriggern**](/windows/win32/api/taskschd/nn-taskschd-iidletrigger) festlegen.

Beim Lesen oder Schreiben von XML werden diese Bedingungen im [**Settings**](taskschedulerschema-settings-tasktype-element.md) -Element des Taskplaner-Schemas angegeben.

## <a name="cycling-idle-condition"></a>Leerlauf Bedingung für das Radfahren

Wenn der Computer in den Leerlauf wechselt und aus dem Leerlauf wechselt, können Sie den Task mithilfe der folgenden Leerlauf Bedingungen beenden und neu starten. Um einen Task zu beenden und neu zu starten, müssen die Eigenschaften und Elemente auf "true" festgelegt werden:

-   Um die Aufgabe zu beenden, wenn die Leerlauf Bedingung endet, legen Sie die [**stoponidleend**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_stoponidleend) -Eigenschaft oder das [**stoponidleend**](taskschedulerschema-terminateonidleend-idlesettingstype-element.md) -Element auf "true" fest.
-   Um den Task erneut zu starten, wenn der Computer wieder in den Leerlaufzustand wechselt, legen Sie die [**restartondle**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_restartonidle) -Eigenschaft oder das [**restartondle**](taskschedulerschema-restartonidle-idlesettingstype-element.md) -Element auf true fest.
