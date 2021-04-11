---
title: Taskplaner 1,0-Schnittstellen
description: Die in den folgenden Themen beschriebenen Schnittstellen ermöglichen den programmgesteuerten Zugriff auf die Funktionalität, die in der Taskplaner verfügbar ist, die in den Betriebssystemen Windows 2000, Windows XP und Windows Server 2003 verwendet wird.
ms.assetid: 25f9c1ad-1859-4788-a876-6f4faa6e556e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bab12b59d4b4561ecbe46c09a76c69209574c9d
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104213082"
---
# <a name="task-scheduler-10-interfaces"></a>Taskplaner 1,0-Schnittstellen

\[\[Diese API kann in nachfolgenden Versionen des Betriebssystems oder des Produkts geändert werden oder nicht verfügbar sein. Verwenden Sie stattdessen die [Taskplaner 2,0-Schnittstellen](task-scheduler-2-0-interfaces.md) oder die [Taskplaner 2,0-Enumerationstypen](task-scheduler-2-0-enumerated-types.md) . \]\]

Die in den folgenden Themen beschriebenen Schnittstellen ermöglichen den programmgesteuerten Zugriff auf die Funktionalität, die in der Taskplaner verfügbar ist, die in den Betriebssystemen Windows 2000, Windows XP und Windows Server 2003 verwendet wird.

Diese Themen enthalten eine Beschreibung der-Schnittstelle, eine Liste der Eigenschaften und Methoden, die von der-Schnittstelle definiert werden, sowie Hinweise zu allen besonderen Umständen, die bei der Verwendung der-Schnittstelle zu beachten sind.


Die folgenden Schnittstellen werden von Taskplaner 1,0 eingeführt.



| Schnittstelle                                        | BESCHREIBUNG                                                                                                                                                                                                                           |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Ienumworkitems**](/windows/desktop/api/Mstask/nn-mstask-ienumworkitems)         | Stellt die Methoden zum Auflisten der Aufgaben im [*Ordner "geplante Aufgaben*](s.md)" bereit.                                                                                                              |
| [**Iprovidetaskpage**](/windows/desktop/api/Mstask/nn-mstask-iprovidetaskpage)     | Stellt die Methoden für den Zugriff auf die Eigenschaften Blatt Einstellungen einer Aufgabe bereit.                                                                                                                                                                 |
| [**Ischeduledworkitem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) | Stellt die Methoden zum Verwalten bestimmter [*Arbeitsaufgaben*](w.md)bereit.                                                                                                                                                 |
| [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask)                           | Stellt die Methoden zum Ausführen von Aufgaben, zum erhalten oder Festlegen von Aufgabeninformationen und zum Beenden von Aufgaben bereit. Sie wird von der [**ischeduledworkitem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) -Schnittstelle abgeleitet und erbt alle Methoden dieser Schnittstelle. |
| [**Itaskscheduler**](/windows/desktop/api/Mstask/nn-mstask-itaskscheduler)         | Stellt die Methoden zum Planen von Aufgaben bereit.                                                                                                                                                                                            |
| [**Itaskauslöst**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger)             | Stellt die Methoden für den Zugriff auf und das Festlegen von Triggern für eine Aufgabe bereit. Trigger geben Task Startzeiten, Wiederholungs Kriterien und andere Parameter an, die Steuern, wann eine Aufgabe ausgeführt wird.                                                     |



 

 

 




