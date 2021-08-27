---
description: Implementieren Sie Multitasking, planen Sie Prioritäten, und arbeiten Sie mit Prozessen, Threads, Threadpools, Auftragsobjekten und Fibers. Verwenden Sie die Zeitplanung im Benutzermodus, um Threads zu planen.
ms.assetid: 6bff848c-0c55-41e7-aff1-84c6b21a1b8d
title: Prozesse und Threads
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 482f9f394001503350d4e213bd51e441ea43d073aacd8d10a49512e04404ba17
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120081310"
---
# <a name="processes-and-threads"></a>Prozesse und Threads

Eine Anwendung besteht aus einem oder mehreren Prozessen. Ein *Prozess*, ganz einfach ausgedrückt, ist ein ausgeführtes Programm. Mindestens ein Thread wird im Kontext des Prozesses ausgeführt. Ein *Thread* ist die grundlegende Einheit, der das Betriebssystem Prozessorzeit zuteilen kann. Ein Thread kann einen beliebigen Teil des Prozesscodes ausführen, einschließlich der Teile, die derzeit von einem anderen Thread ausgeführt werden.

Mit *einem Auftragsobjekt* können Gruppen von Prozessen als Einheit verwaltet werden. Auftragsobjekte sind lesbare, sicherungsfähige, sharable-Objekte, die Attribute der ihnen zugeordneten Prozesse steuern. Vorgänge, die für das Auftragsobjekt ausgeführt werden, wirken sich auf alle Prozesse aus, die dem Auftragsobjekt zugeordnet sind.

Ein *Threadpool ist* eine Sammlung von Arbeitsthreads, die asynchrone Rückrufe effizient im Auftrag der Anwendung ausführen. Der Threadpool wird hauptsächlich verwendet, um die Anzahl von Anwendungsthreads zu reduzieren und die Verwaltung der Arbeitsthreads zu ermöglichen.

Eine *Fiber* ist eine Ausführungseinheit, die von der Anwendung manuell geplant werden muss. Fibers werden im Kontext der Threads ausgeführt, die sie planen.

*Die Benutzermodusplanung* (UMS) ist ein schlanker Mechanismus, mit dem Anwendungen ihre eigenen Threads planen können. UMS-Threads unterscheiden sich von [Fibers,](fibers.md) da jeder UMS-Thread über einen eigenen Threadkontext verfügt, anstatt den Threadkontext eines einzelnen Threads gemeinsam zu verwenden.

-   [Neues in Prozessen und Threads](what-s-new-in-processes-and-threads.md)
-   [About Processes and Threads (Informationen zu Prozessen und Threads)](about-processes-and-threads.md)
-   [Verwenden von Prozessen und Threads](using-processes-and-threads.md)
-   [Prozess- und Threadreferenz](process-and-thread-reference.md)

 

 



