---
title: Informationen zum Taskplaner
description: Mit dem Taskplaner-Dienst können Sie automatisierte Aufgaben auf einem ausgewählten Computer ausführen.
ms.assetid: 13816b8b-3090-4d17-86bb-8e632ca0cd37
keywords:
- Taskplaner Taskplaner, Informationen zu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6022546550efe32504dd0a3d12c94163e78214f6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341868"
---
# <a name="about-the-task-scheduler"></a>Informationen zum Taskplaner

Mit dem Taskplaner-Dienst können Sie automatisierte Aufgaben auf einem ausgewählten Computer ausführen. Mit diesem Dienst können Sie ein beliebiges Programm so planen, dass es zu einem geeigneten Zeitpunkt ausgeführt wird oder wenn ein bestimmtes Ereignis eintritt. Der Taskplaner überwacht die Zeit-oder Ereignis Kriterien, die Sie auswählen, und führt dann die Aufgabe aus, wenn diese Kriterien erfüllt sind.

## <a name="where-task-scheduler-is-installed"></a>Installation von Taskplaner

Der Taskplaner wird automatisch mit mehreren Microsoft-Betriebssystemen installiert.

Taskplaner 1,0 wird mit den Betriebssystemen Windows Server 2003, Windows XP und Windows 2000 installiert.

Taskplaner 2,0 wird mit Windows Vista und Windows Server 2008 installiert.

Die Taskplaner 2,0-API sollte zum Entwickeln von Anwendungen verwendet werden, die den Taskplaner-Dienst unter Windows Vista verwenden. Weitere Informationen finden Sie unter [Taskplaner Referenz](task-scheduler-reference.md).

Taskplaner wird jedes Mal gestartet, wenn das Betriebssystem gestartet wird. Sie kann entweder über die grafische Benutzeroberfläche Taskplaner (GUI) oder über die in diesem SDK beschriebene Taskplaner-API ausgeführt werden.

## <a name="information-about-tasks"></a>Informationen zu Aufgaben

Tasks sind die Hauptkomponente des Taskplaner. Informationen zu den Aufgaben und deren Komponenten finden Sie in den folgenden Themen:

-   [Aufgaben](tasks.md)
-   [Task Aktionen](task-actions.md)
-   [Task Trigger](task-triggers.md)
-   [Aufgaben Registrierungsinformationen](task-registration-information.md)
-   [Aufgaben im Leerlauf](task-idle-conditions.md)
-   [Sicherheits Kontexte für Tasks](security-contexts-for-running-tasks.md)
-   [Wiederholen einer Aufgabe](repeating-a-task.md)
-   [Automatische Wartung](task-maintenence.md)

Weitere Informationen und Beispiele zur Verwendung der Taskplaner Schnittstellen, Skript Objekte und XML finden [Sie unter Verwenden der Taskplaner](using-the-task-scheduler.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 




