---
title: Taskplaner Strukturen und Unions
description: Listet die Strukturen und Unions auf, die von den Taskplaner 1,0-APIs verwendet werden.
ms.assetid: 37dc7818-7719-4975-b7bd-f8c2d5cc008b
keywords:
- Taskplaner Taskplaner, Referenz, Strukturen und Unions
- Trigger Taskplaner, Strukturen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bdb73620ccd92eed3ce8aea9bf5a17c5734d926
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206372"
---
# <a name="task-scheduler-structures-and-unions"></a>Taskplaner Strukturen und Unions

In diesem Abschnitt werden die Strukturen und Unions beschrieben, die von den Taskplaner-APIs verwendet werden.

Alle unten aufgeführten Strukturen und Unions werden von Taskplaner 1,0 verwendet.



| Name                                               | BESCHREIBUNG                                                                                                                     |
|----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [**Tä**](/windows/desktop/api/Mstask/ns-mstask-daily)                             | Definiert das Intervall (in Tagen), in dem eine Aufgabe ausgeführt wird.                                                                          |
| [**Monthlydate**](/windows/desktop/api/Mstask/ns-mstask-monthlydate)                 | Definiert den Tag des Monats, an dem die Aufgabe ausgeführt wird.                                                                                 |
| [**Monthlydow**](/windows/desktop/api/Mstask/ns-mstask-monthlydow)                   | Definiert das Datum (n), an dem der Task nach Monat, Woche und Wochentag ausgeführt wird.                                                     |
| [**Task-Auslösung \_**](/windows/desktop/api/Mstask/ns-mstask-task_trigger)              | Definiert die Zeiten für die Ausführung eines geplanten [*Arbeits Elements*](w.md).                                                  |
| [**\_auslösertyp \_ Union**](/windows/desktop/api/Mstask/ns-mstask-trigger_type_union) | Definiert den Aufruf Zeitplan des Auslösers innerhalb des **Typmembers** einer [**Task \_ triggerstruktur**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) . |
| [**Arbei**](/windows/desktop/api/Mstask/ns-mstask-weekly)                           | Definiert das Intervall (in Wochen) zwischen den Aufrufen einer Aufgabe.                                                                  |



 

 

 




