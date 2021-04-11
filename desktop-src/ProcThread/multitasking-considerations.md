---
description: Die empfohlene Richtlinie besteht darin, möglichst wenige Threads zu verwenden und so die Verwendung von Systemressourcen zu minimieren.
ms.assetid: ed9bd3cf-b10c-49f9-bf62-7332517350b7
title: Überlegungen zum Multitasking
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ec64bf1b7d59a42a1aec3511a72328f18bfaa88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131669"
---
# <a name="multitasking-considerations"></a>Überlegungen zum Multitasking

Die empfohlene Richtlinie besteht darin, möglichst wenige Threads zu verwenden und so die Verwendung von Systemressourcen zu minimieren. Dadurch wird die Leistung verbessert. Multitasking verfügt über Ressourcenanforderungen und potenzielle Konflikte, die beim Entwerfen der Anwendung berücksichtigt werden müssen. Die Ressourcenanforderungen sehen wie folgt aus:

-   Das System beansprucht Arbeitsspeicher für die Kontextinformationen, die von Prozessen und Threads benötigt werden. Daher wird die Anzahl der Prozesse und Threads, die erstellt werden können, durch den verfügbaren Arbeitsspeicher beschränkt.
-   Die Verfolgung einer großen Anzahl von Threads verbraucht erhebliche Prozessorzeit. Wenn zu viele Threads vorhanden sind, können die meisten von Ihnen keinen signifikanten Fortschritt machen. Befinden sich die meisten der aktuellen Threads in nur einem Prozess, werden Threads in anderen Prozessen seltener eingeplant.

Die Bereitstellung eines gemeinsamen Zugriffs auf Ressourcen kann zu Konflikten führen. Um diese zu vermeiden, müssen Sie den Zugriff auf freigegebene Ressourcen synchronisieren. Dies gilt für Systemressourcen (z. b. Kommunikationsports), Ressourcen, die von mehreren Prozessen (z. b. Datei Handles) gemeinsam verwendet werden, oder die Ressourcen eines einzelnen Prozesses (z. b. globale Variablen), auf die von mehreren Threads zugegriffen wird. Wenn der Zugriff nicht ordnungsgemäß (in demselben oder in unterschiedlichen Prozessen) synchronisiert wird, kann dies zu Problemen führen, wie z. b. Deadlock-und Racebedingungen Die Synchronisierungs Objekte und-Funktionen, die Sie verwenden können, um die Ressourcen Freigabe zwischen mehreren Threads zu koordinieren. Weitere Informationen zur Synchronisierung finden Sie unter [Synchronisieren der Ausführung mehrerer Threads](synchronizing-execution-of-multiple-threads.md). Durch das Reduzieren der Anzahl von Threads wird die Synchronisierung von Ressourcen vereinfacht und effektiver.

Ein guter Entwurf für eine Multithread-Anwendung ist der Pipeline Server. In diesem Entwurf erstellen Sie einen Thread pro Prozessor und erstellen Warteschlangen von Anforderungen, für die die Anwendung die Kontextinformationen verwaltet. Von einem Thread werden alle Anforderungen in einer Warteschlange verarbeitet, bevor Anforderungen in der nächsten Warteschlange verarbeitet werden.

 

 



