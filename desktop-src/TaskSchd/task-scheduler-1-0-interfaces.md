---
title: Taskplaner 1.0-Schnittstellen
description: Die in den folgenden Themen beschriebenen Schnittstellen bieten programmgesteuerten Zugriff auf die Funktionen, die in den Taskplaner verfügbar sind, die in den Betriebssystemen Windows 2000, Windows XP und Windows Server 2003 verwendet werden.
ms.assetid: 25f9c1ad-1859-4788-a876-6f4faa6e556e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60d2033c78594c0f4ef1d9f871275f425ef5189240ed7b432266464343cf86e2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119975030"
---
# <a name="task-scheduler-10-interfaces"></a>Taskplaner 1.0-Schnittstellen

\[\[Diese API kann in nachfolgenden Versionen des Betriebssystems oder Produkts geändert oder nicht verfügbar sein. Verwenden Sie stattdessen [die Taskplaner 2.0-Schnittstellen](task-scheduler-2-0-interfaces.md) oder [Taskplaner 2.0-Enumerationstypen.](task-scheduler-2-0-enumerated-types.md) \]\]

Die in den folgenden Themen beschriebenen Schnittstellen bieten programmgesteuerten Zugriff auf die Funktionen, die in den Taskplaner verfügbar sind, die in den Betriebssystemen Windows 2000, Windows XP und Windows Server 2003 verwendet werden.

Diese Themen enthalten eine Beschreibung der Schnittstelle, eine Liste der von der Schnittstelle definierten Eigenschaften und Methoden sowie Hinweise zu besonderen Umständen, die bei Verwendung der -Schnittstelle zu beachten sind.


Die folgenden Schnittstellen werden durch Taskplaner 1.0 eingeführt.



| Schnittstelle                                        | BESCHREIBUNG                                                                                                                                                                                                                           |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IEnumWorkItems**](/windows/desktop/api/Mstask/nn-mstask-ienumworkitems)         | Stellt die Methoden zum Aufzählen der Aufgaben im [*Ordner Geplante Aufgaben*](s.md)bereit.                                                                                                              |
| [**IProvideTaskPage**](/windows/desktop/api/Mstask/nn-mstask-iprovidetaskpage)     | Stellt die Methoden für den Zugriff auf die Eigenschaftenblatteinstellungen einer Aufgabe bereit.                                                                                                                                                                 |
| [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) | Stellt die Methoden zum Verwalten bestimmter [*Arbeitselemente bereit.*](w.md)                                                                                                                                                 |
| [**Itask**](/windows/desktop/api/Mstask/nn-mstask-itask)                           | Stellt die Methoden zum Ausführen von Aufgaben, Abrufen oder Festlegen von Taskinformationen und Beenden von Tasks bereit. Sie wird von der [**IScheduledWorkItem-Schnittstelle**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) abgeleitet und erbt alle Methoden dieser Schnittstelle. |
| [**ITaskScheduler**](/windows/desktop/api/Mstask/nn-mstask-itaskscheduler)         | Stellt die Methoden zum Planen von Aufgaben bereit.                                                                                                                                                                                            |
| [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger)             | Stellt die Methoden zum Zugreifen auf und Festlegen von Triggern für eine Aufgabe bereit. Trigger geben Taskstartzeiten, Wiederholungskriterien und andere Parameter an, die steuern, wann eine Aufgabe ausgeführt wird.                                                     |



 

 

 




