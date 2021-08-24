---
description: Jeder Prozess stellt die Ressourcen bereit, die zum Ausführen eines Programms erforderlich sind.
ms.assetid: 055458cf-9fc7-4a16-be14-1122b3cf0251
title: Informationen zu Prozessen und Threads
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62cbce9375d3c27fd58d6bab48c11fe2bdb825dfc729c2176dd2f14eba0a958e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032620"
---
# <a name="about-processes-and-threads"></a>Informationen zu Prozessen und Threads

Jeder *Prozess* stellt die Ressourcen bereit, die zum Ausführen eines Programms erforderlich sind. Ein Prozess verfügt über einen virtuellen Adressraum, ausführbaren Code, offene Handles für Systemobjekte, einen Sicherheitskontext, einen eindeutigen Prozessbezeichner, Umgebungsvariablen, eine Prioritätsklasse, minimale und maximale Arbeitssatzgrößen und mindestens einen Ausführungsthread. Jeder Prozess wird mit einem einzelnen Thread gestartet, der häufig als *primärer Thread* bezeichnet wird, kann aber zusätzliche Threads aus jedem seiner Threads erstellen.

Ein *Thread* ist die Entität in einem Prozess, die für die Ausführung geplant werden kann. Alle Threads eines Prozesses nutzen den virtuellen Adressraum und die Systemressourcen gemeinsam. Darüber hinaus verwaltet jeder Thread Ausnahmehandler, eine Planungspriorität, lokalen Threadspeicher, einen eindeutigen Threadbezeichner und eine Reihe von Strukturen, die das System verwendet, um den Threadkontext zu speichern, bis er geplant ist. Der *Threadkontext* umfasst den Threadsatz von Computerregistern, den Kernelstapel, einen Threadumgebungsblock und einen Benutzerstapel im Adressraum des Threadprozesses. Threads können auch über einen eigenen Sicherheitskontext verfügen, der zum Annehmen der Identität von Clients verwendet werden kann.

Microsoft Windows unterstützt *präemptives Multitasking,* das die Auswirkungen der gleichzeitigen Ausführung mehrerer Threads aus mehreren Prozessen erzeugt. Auf einem Multiprozessorcomputer kann das System gleichzeitig so viele Threads ausführen, wie Prozessoren auf dem Computer vorhanden sind.

Mit einem *Auftragsobjekt* können Gruppen von Prozessen als Einheit verwaltet werden. Auftragsobjekte sind verschreibbare, sicherungsfähige, trennbare Objekte, die Attribute der ihnen zugeordneten Prozesse steuern. Vorgänge, die für das Auftragsobjekt ausgeführt werden, wirken sich auf alle Prozesse aus, die dem Auftragsobjekt zugeordnet sind.

Eine Anwendung kann den *Threadpool* verwenden, um die Anzahl der Anwendungsthreads zu reduzieren und die Verwaltung der Arbeitsthreads bereitzustellen. Anwendungen können Arbeitselemente in die Warteschlange stellen, Arbeit mit wartebaren Handles zuordnen, basierend auf einem Timer automatisch in die Warteschlange stellen und E/A binden.

*Die Benutzermodusplanung (User-Mode Scheduling,* UMS) ist ein einfacher Mechanismus, mit dem Anwendungen ihre eigenen Threads planen können. Eine Anwendung kann zwischen UMS-Threads im Benutzermodus wechseln, ohne den [Systemplaner](scheduling.md) einzubeziehen und die Kontrolle über den Prozessor zurückzuerlangen, wenn ein UMS-Thread im Kernel blockiert wird. Jeder UMS-Thread verfügt über einen eigenen Threadkontext, anstatt den Threadkontext eines einzelnen Threads zu teilen. Die Möglichkeit, zwischen Threads im Benutzermodus zu wechseln, macht UMS effizienter als Threadpools für kurzzeitige Arbeitselemente, die nur wenige Systemaufrufe erfordern.

Eine *Fiber* ist eine Ausführungseinheit, die von der Anwendung manuell geplant werden muss. Fibers werden im Kontext der Threads ausgeführt, die sie planen. Jeder Thread kann mehrere Fibers planen. Im Allgemeinen bieten Fibers keine Vorteile gegenüber einer gut entworfenen Multithreadanwendung. Die Verwendung von Fibers kann jedoch das Portieren von Anwendungen vereinfachen, die für die Planung ihrer eigenen Threads entwickelt wurden.

Weitere Informationen finden Sie in den folgenden Themen:

-   [Multitasking](multitasking.md)
-   [Zeitplanung](scheduling.md)
-   [Mehrere Threads](multiple-threads.md)
-   [Untergeordnete Prozesse](child-processes.md)
-   [Threadpools](thread-pools.md)
-   [Auftragsobjekte](job-objects.md)
-   [Benutzermodusplanung](user-mode-scheduling.md)
-   [Fasern](fibers.md)

 

 



