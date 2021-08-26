---
title: Informationen zum Taskplaner
description: Mit dem Taskplaner Dienst können Sie automatisierte Aufgaben auf einem ausgewählten Computer ausführen.
ms.assetid: 13816b8b-3090-4d17-86bb-8e632ca0cd37
keywords:
- Taskplaner Taskplaner , Informationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dca865fe98ffb56f2bb6e9310e31d38bdaa804a63da07e486bbc89a0cd9ebcdf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072710"
---
# <a name="about-the-task-scheduler"></a>Informationen zum Taskplaner

Mit dem Taskplaner Dienst können Sie automatisierte Aufgaben auf einem ausgewählten Computer ausführen. Mit diesem Dienst können Sie ein beliebiges Programm so planen, dass es zu einem für Sie geeigneten Zeitpunkt oder zu einem bestimmten Ereignis ausgeführt wird. Der Taskplaner überwacht die von Ihnen gewählten Zeit- oder Ereigniskriterien und führt die Aufgabe dann aus, wenn diese Kriterien erfüllt sind.

## <a name="where-task-scheduler-is-installed"></a>Installationsort Taskplaner

Die Taskplaner wird automatisch mit mehreren Microsoft-Betriebssystemen installiert.

Taskplaner 1.0 wird mit den Betriebssystemen Windows Server 2003, Windows XP und Windows 2000 installiert.

Taskplaner 2.0 wird mit Windows Vista und Windows Server 2008 installiert.

Die Taskplaner 2.0-API sollte bei der Entwicklung von Anwendungen verwendet werden, die den Taskplaner-Dienst auf Windows Vista verwenden. Weitere Informationen finden Sie unter [Taskplaner Referenz.](task-scheduler-reference.md)

Taskplaner wird jedes Mal gestartet, wenn das Betriebssystem gestartet wird. Sie kann entweder über die Taskplaner grafische Benutzeroberfläche (GUI) oder über die in diesem SDK beschriebene Taskplaner-API ausgeführt werden.

## <a name="information-about-tasks"></a>Informationen zu Aufgaben

Aufgaben sind die Hauptkomponente der Taskplaner. Informationen dazu, was Aufgaben sind und was ihre Komponenten sind, finden Sie in den folgenden Themen:

-   [Aufgaben](tasks.md)
-   [Aufgabenaktionen](task-actions.md)
-   [Aufgabentrigger](task-triggers.md)
-   [Informationen zur Aufgabenregistrierung](task-registration-information.md)
-   [Leerlaufbedingungen für Aufgaben](task-idle-conditions.md)
-   [Sicherheitskontexte für Aufgaben](security-contexts-for-running-tasks.md)
-   [Wiederholen einer Aufgabe](repeating-a-task.md)
-   [Automatische Wartung](task-maintenence.md)

Weitere Informationen und Beispiele zur Verwendung der Taskplaner Schnittstellen, Skriptobjekte und XML finden Sie unter [Verwenden der Taskplaner](using-the-task-scheduler.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 




