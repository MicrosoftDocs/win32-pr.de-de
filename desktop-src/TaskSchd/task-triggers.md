---
title: Aufgabentrigger
description: Ein Trigger ist ein Satz von Kriterien, die bei Erfüllung die Ausführung eines Tasks starten.
ms.assetid: 8b4dff8b-9dc3-4856-aed6-648588a089be
keywords:
- Erstellen von Triggern Taskplaner
- triggers Taskplaner
- Trigger Taskplaner beschrieben
- Trigger Taskplaner , zeitbasiert
- triggers Taskplaner , ereignisbasiert
- ereignisbasierte Trigger Taskplaner
- zeitbasierte Trigger Taskplaner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b0060511556615c638eb8385a757e9c44147720b659bb11bfe4f0849e4499ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002298"
---
# <a name="task-triggers"></a>Aufgabentrigger

Ein Trigger ist ein Satz von Kriterien, die bei Erfüllung die Ausführung eines Tasks starten. Taskplaner stellt sowohl zeitbasierte als auch ereignisbasierte Trigger bereit, die eine Aufgabe auf verschiedene Weise starten können. Eine bestimmte Aufgabe kann von einem oder mehreren Triggern gestartet werden. Eine Aufgabe kann maximal 48 Trigger aufweisen.

## <a name="time-based-triggers"></a>Zeitbasierte Trigger

Zeitbasierte Trigger starten Aufgaben zu bestimmten Zeiten. Dies umfasst das einmalige Starten der Aufgabe zu einem bestimmten Zeitpunkt oder das mehrmalige Starten der Aufgabe nach einem täglichen, wöchentlichen, monatlichen oder monatlichen Wochentagszeitplan.

## <a name="event-based-triggers"></a>Ereignisbasierte Trigger

Ereignisbasierte Trigger starten eine Aufgabe als Reaktion auf bestimmte Systemereignisse. Beispielsweise können ereignisbasierte Trigger so festgelegt werden, dass eine Aufgabe gestartet wird, wenn das System gestartet wird, wenn sich ein Benutzer beim lokalen Computer anmeldet oder wenn das System in den Leerlauf übergeht.

## <a name="multiple-triggers"></a>Mehrere Trigger

Jede Aufgabe kann von einem oder mehreren Triggern gestartet werden, sodass die Aufgabe auf verschiedene Arten gestartet werden kann. Mehrere Trigger werden jedoch in Taskplaner 1.0 und Taskplaner 2.0 unterschiedlich implementiert.

In Taskplaner 2.0 wird jeder Trigger durch eine separate Trigger-API definiert, die der Aufgabe über die Triggersammlung zugeordnet ist.

In Taskplaner 1.0 können mehrere Trigger als Zeitplan betrachtet werden, eine Reihe von Zeiten, zu denen der Task gestartet wird. In diesem Fall ist der Zeitplan der Satz von Zeiten (angegeben durch die Vereinigung aller Trigger, die dem Arbeitselement zugeordnet sind), zu denen ein Arbeitselement ausgeführt wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Wiederholen einer Aufgabe](repeating-a-task.md)
</dt> <dt>

[Triggertypen](trigger-types.md)
</dt> <dt>

[Triggerschnittstellen](trigger-interfaces.md)
</dt> <dt>

[Informationen zum Taskplaner](about-the-task-scheduler.md)
</dt> </dl>

 

 




