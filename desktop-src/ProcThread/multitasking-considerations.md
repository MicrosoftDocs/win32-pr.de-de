---
description: Es wird empfohlen, so wenige Threads wie möglich zu verwenden, wodurch die Verwendung von Systemressourcen minimiert wird.
ms.assetid: ed9bd3cf-b10c-49f9-bf62-7332517350b7
title: Überlegungen zu Multitasking
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fd11b0015db8f3fd3606b74a5bce695aed135f79265b3f1d6ba410002b74a44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032240"
---
# <a name="multitasking-considerations"></a>Überlegungen zu Multitasking

Es wird empfohlen, so wenige Threads wie möglich zu verwenden, wodurch die Verwendung von Systemressourcen minimiert wird. Dadurch wird die Leistung verbessert. Multitasking verfügt über Ressourcenanforderungen und potenzielle Konflikte, die beim Entwerfen Ihrer Anwendung berücksichtigt werden müssen. Die Ressourcenanforderungen sehen wie folgt aus:

-   Das System verbraucht Arbeitsspeicher für die Kontextinformationen, die sowohl von Prozessen als auch von Threads benötigt werden. Daher ist die Anzahl der Prozesse und Threads, die erstellt werden können, durch den verfügbaren Arbeitsspeicher beschränkt.
-   Die Verfolgung einer großen Anzahl von Threads verbraucht erhebliche Prozessorzeit. Wenn es zu viele Threads gibt, sind die meisten davon nicht in der Lage, wesentliche Fortschritte zu erzielen. Befinden sich die meisten der aktuellen Threads in nur einem Prozess, werden Threads in anderen Prozessen seltener eingeplant.

Die Bereitstellung eines gemeinsamen Zugriffs auf Ressourcen kann zu Konflikten führen. Um sie zu vermeiden, müssen Sie den Zugriff auf freigegebene Ressourcen synchronisieren. Dies gilt für Systemressourcen (z. B. Kommunikationsports), Ressourcen, die von mehreren Prozessen gemeinsam genutzt werden (z. B. Dateihandles) oder die Ressourcen eines einzelnen Prozesses (z. B. globale Variablen), auf die von mehreren Threads zugegriffen wird. Wenn der Zugriff nicht ordnungsgemäß synchronisiert wird (in demselben oder in unterschiedlichen Prozessen), kann dies zu Problemen wie Deadlocks und Racebedingungen führen. Die Synchronisierungsobjekte und -funktionen, die Sie verwenden können, um die Gemeinsame Nutzung von Ressourcen zwischen mehreren Threads zu koordinieren. Weitere Informationen zur Synchronisierung finden Sie unter [Synchronisieren der Ausführung mehrerer Threads.](synchronizing-execution-of-multiple-threads.md) Wenn Sie die Anzahl von Threads reduzieren, ist es einfacher und effektiver, Ressourcen zu synchronisieren.

Ein guter Entwurf für eine Multithreadanwendung ist der Pipelineserver. In diesem Entwurf erstellen Sie einen Thread pro Prozessor und Warteschlangen von Anforderungen, für die die Anwendung die Kontextinformationen verwaltet. Ein Thread würde alle Anforderungen in einer Warteschlange verarbeiten, bevor Anforderungen in der nächsten Warteschlange verarbeitet werden.

 

 



