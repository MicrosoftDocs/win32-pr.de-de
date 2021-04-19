---
description: Implementieren Sie Multitasking, planen Sie Prioritäten, und arbeiten Sie mit Prozessen, Threads, Thread Pools, Auftrags Objekten und Fibers. Planen Sie Threads mithilfe der benutzermodusplanung.
ms.assetid: 6bff848c-0c55-41e7-aff1-84c6b21a1b8d
title: Prozesse und Threads
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f469806a5f803910a773c78c9847d0f7b0ecc7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106367934"
---
# <a name="processes-and-threads"></a>Prozesse und Threads

Eine Anwendung besteht aus einem oder mehreren Prozessen. Ein *Prozess* ist in den einfachsten Begriffen ein ausführendes Programm. Mindestens ein Thread wird im Kontext des Prozesses ausgeführt. Ein *Thread* ist die Basiseinheit, der die Prozessorzeit vom Betriebssystem zugewiesen wird. Ein Thread kann einen beliebigen Teil des Prozess Codes ausführen, einschließlich der Teile, die gerade von einem anderen Thread ausgeführt werden.

Ein *Auftrags Objekt* ermöglicht das Verwalten von Gruppen von Prozessen als Einheit. Auftrags Objekte sind namable-, Securable-und freigegeben-Objekte, die Attribute der zugeordneten Prozesse steuern. Die für das Auftrags Objekt ausgeführten Vorgänge wirken sich auf alle Prozesse aus, die dem Auftrags Objekt zugeordnet sind.

Ein *Thread Pool* ist eine Sammlung von Arbeitsthreads, die im Auftrag der Anwendung asynchrone Rückrufe effizient ausführen. Der Thread Pool wird hauptsächlich verwendet, um die Anzahl der Anwendungsthreads zu verringern und die Verwaltung der Arbeitsthreads zu ermöglichen.

Eine *Fiber* ist eine Ausführungs Einheit, die manuell von der Anwendung geplant werden muss. Fibers werden im Kontext der Threads ausgeführt, die Sie planen.

Die *benutzermodusplanung* (ums) ist ein schlanker Mechanismus, mit dem Anwendungen ihre eigenen Threads planen können. UMS-Threads unterscheiden sich von [Fibers](fibers.md) darin, dass jeder ums-Thread über einen eigenen Thread Kontext verfügt, anstatt den Thread Kontext eines einzelnen Threads gemeinsam zu nutzen.

-   [Neues bei Prozessen und Threads](what-s-new-in-processes-and-threads.md)
-   [About Processes and Threads (Informationen zu Prozessen und Threads)](about-processes-and-threads.md)
-   [Verwenden von Prozessen und Threads](using-processes-and-threads.md)
-   [Prozess-und Thread Verweis](process-and-thread-reference.md)

 

 



