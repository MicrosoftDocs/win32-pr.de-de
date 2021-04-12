---
description: Jeder Prozess stellt die Ressourcen bereit, die zum Ausführen eines Programms benötigt werden.
ms.assetid: 055458cf-9fc7-4a16-be14-1122b3cf0251
title: Informationen zu Prozessen und Threads
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 650eab4421971bdc08e71c031aec433ed84471bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104216021"
---
# <a name="about-processes-and-threads"></a>Informationen zu Prozessen und Threads

Jeder *Prozess* stellt die Ressourcen bereit, die zum Ausführen eines Programms benötigt werden. Ein Prozess verfügt über einen virtuellen Adressraum, einen ausführbaren Code, offene Handles für Systemobjekte, einen Sicherheitskontext, eine eindeutige Prozess-ID, Umgebungsvariablen, eine Prioritäts Klasse, minimale und maximale workingsetgrößen und mindestens einen Ausführungs Thread. Jeder Prozess wird mit einem einzelnen Thread gestartet, der häufig als *primärer Thread* bezeichnet wird, kann jedoch zusätzliche Threads aus allen Threads erstellen.

Ein *Thread* ist die Entität innerhalb eines Prozesses, die für die Ausführung geplant werden kann. Alle Threads eines Prozesses verwenden den virtuellen Adressraum und die Systemressourcen gemeinsam. Außerdem werden von jedem Thread Ausnahmehandler, eine Planungs Priorität, ein Thread lokaler Speicher, ein eindeutiger Thread Bezeichner und ein Satz von Strukturen verwaltet, mit denen das System den Thread Kontext so lange speichert, bis er geplant ist. Der *Thread Kontext* enthält den Thread Satz der Computer Register, den Kernel Stapel, einen Thread Umgebungsblock und einen Benutzer Stapel im Adressraum des Thread Prozesses. Threads können auch über einen eigenen Sicherheitskontext verfügen, der zum Annehmen der Identität von Clients verwendet werden kann.

Microsoft Windows unterstützt ein *präemptives Multitasking*, das die Auswirkungen der gleichzeitigen Ausführung mehrerer Threads aus mehreren Prozessen erzeugt. Auf einem Multiprozessorcomputer kann das System gleichzeitig so viele Threads ausführen, wie Prozessoren auf dem Computer vorhanden sind.

Ein *Auftrags Objekt* ermöglicht das Verwalten von Gruppen von Prozessen als Einheit. Auftrags Objekte sind namable-, Securable-und freigegeben-Objekte, die Attribute der zugeordneten Prozesse steuern. Die für das Auftrags Objekt ausgeführten Vorgänge wirken sich auf alle Prozesse aus, die dem Auftrags Objekt zugeordnet sind.

Eine Anwendung kann den *Thread Pool* verwenden, um die Anzahl der Anwendungsthreads zu verringern und die Verwaltung der Arbeitsthreads zu ermöglichen. Anwendungen können Arbeitselemente in die Warteschlange stellen, Arbeitsaufgaben zuordnen, abnutzbare Handles zuordnen, automatisch basierend auf einem Timer in die Warteschlange eingereiht und mit e/a

Die *benutzermodusplanung* (ums) ist ein schlanker Mechanismus, mit dem Anwendungen ihre eigenen Threads planen können. Eine Anwendung kann im Benutzermodus zwischen den Verarbeitungsthreads wechseln, ohne den [Systemplaner](scheduling.md) einzubeziehen, und die Steuerung des Prozessors wiederherzustellen, wenn ein ums-Thread im Kernel blockiert wird. Jeder ums-Thread verfügt über einen eigenen Thread Kontext, anstatt den Thread Kontext eines einzelnen Threads freizugeben. Durch die Möglichkeit, zwischen Threads im Benutzermodus zu wechseln, werden die ums effizienter als Thread Pools für kurze Arbeitsaufgaben, für die nur wenige Systemaufrufe erforderlich sind.

Eine *Fiber* ist eine Ausführungs Einheit, die manuell von der Anwendung geplant werden muss. Fibers werden im Kontext der Threads ausgeführt, die Sie planen. Jeder Thread kann mehrere Fibers planen. Im Allgemeinen bieten Fibers keine Vorteile gegenüber einer gut entworfenen Multithread-Anwendung. Die Verwendung von Fibers kann jedoch das Portieren von Anwendungen erleichtern, die zum Planen Ihrer eigenen Threads entworfen wurden.

Weitere Informationen finden Sie unter den folgenden Themen:

-   [Multitasking](multitasking.md)
-   [Zeitplanung](scheduling.md)
-   [Mehrere Threads](multiple-threads.md)
-   [Untergeordnete Prozesse](child-processes.md)
-   [Thread Pools](thread-pools.md)
-   [Auftrags Objekte](job-objects.md)
-   [Benutzermodusplanung](user-mode-scheduling.md)
-   [STAP](fibers.md)

 

 



