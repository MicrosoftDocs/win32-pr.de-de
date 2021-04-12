---
title: Task Trigger
description: Ein-Triggersatz besteht aus einer Reihe von Kriterien, die die Ausführung einer Aufgabe starten, wenn diese erfüllt ist.
ms.assetid: 8b4dff8b-9dc3-4856-aed6-648588a089be
keywords:
- Erstellen von Triggern Taskplaner
- Trigger Taskplaner
- Trigger Taskplaner, beschrieben
- Trigger Taskplaner, Zeit basiert
- Trigger Taskplaner, Ereignis basiert
- ereignisbasierte Trigger Taskplaner
- Zeitbasierte Trigger Taskplaner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d465dfa015be19ff220a77d3c85f0cbb223c4899
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206403"
---
# <a name="task-triggers"></a>Task Trigger

Ein-Triggersatz besteht aus einer Reihe von Kriterien, die die Ausführung einer Aufgabe starten, wenn diese erfüllt ist. Taskplaner bietet zeitbasierte und ereignisbasierte Trigger, die eine Aufgabe auf verschiedene Arten starten können. Eine bestimmte Aufgabe kann von einem oder mehreren Triggern gestartet werden. Eine Aufgabe kann maximal 48 Trigger aufweisen.

## <a name="time-based-triggers"></a>Zeitbasierte Trigger

Zeitbasierte Trigger starten Tasks zu bestimmten Zeiten. Dies umfasst das einmalige Starten der Aufgabe zu einem bestimmten Zeitpunkt oder das mehrfache Starten der Aufgabe an einem täglichen, wöchentlichen, monatlichen oder monatlichen Zeitplan.

## <a name="event-based-triggers"></a>Ereignisbasierte Trigger

Ereignisbasierte Trigger starten eine Aufgabe als Reaktion auf bestimmte Systemereignisse. Ereignisbasierte Trigger können z. b. so festgelegt werden, dass eine Aufgabe gestartet wird, wenn das System gestartet wird, wenn sich ein Benutzer am lokalen Computer anmeldet oder wenn sich das System im Leerlauf befindet.

## <a name="multiple-triggers"></a>Mehrere Trigger

Jeder Task kann von einem oder mehreren Triggern gestartet werden, sodass die Aufgabe auf eine beliebige Anzahl von Arten gestartet werden kann. In Taskplaner 1,0 und Taskplaner 2,0 werden jedoch mehrere Trigger anders implementiert.

In Taskplaner 2,0 wird jeder-Vorgang durch eine separate-auslöserapi definiert, die mit der-Aufgabe über die-auslöserauflistung verknüpft ist.

In Taskplaner 1,0 können mehrere Trigger als Zeitplan betrachtet werden. Dies ist ein Satz von Uhrzeiten, zu denen die Aufgabe gestartet wird. In diesem Fall ist der Zeitplan der Satz von Uhrzeiten (angegeben durch die Vereinigung aller Trigger, die mit dem Arbeits Element verknüpft sind), bei denen ein Arbeits Element ausgeführt wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Wiederholen einer Aufgabe](repeating-a-task.md)
</dt> <dt>

[Auslösertypen](trigger-types.md)
</dt> <dt>

[Auslöse Schnittstellen](trigger-interfaces.md)
</dt> <dt>

[Informationen zum Taskplaner](about-the-task-scheduler.md)
</dt> </dl>

 

 




