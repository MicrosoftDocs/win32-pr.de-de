---
description: Verwenden Sie zum Synchronisieren des Zugriffs auf eine Ressource eines der Synchronisierungs Objekte in einer der Warte Funktionen.
ms.assetid: 0930bf12-6d5f-4f2c-914d-53e6e862d3bd
title: Informationen zur Synchronisierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ad53dc8c309d8ec55f37cef5f78839348071477
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352206"
---
# <a name="about-synchronization"></a>Informationen zur Synchronisierung

Verwenden Sie zum Synchronisieren des Zugriffs auf eine Ressource eines der [Synchronisierungs Objekte](synchronization-objects.md) in einer der [warte Funktionen](wait-functions.md). Der Status eines Synchronisierungs Objekts wird entweder *signalisiert* oder *nicht signalisiert*. Mit den Wait-Funktionen kann ein Thread seine eigene Ausführung blockieren, bis ein angegebenes nicht signalisiertes Objekt auf den signalisierten Zustand festgelegt ist. Weitere Informationen finden Sie unter [prozessübergreifende Synchronisierung](interprocess-synchronization.md).

Im folgenden werden andere Synchronisierungs Mechanismen aufgeführt:

-   [überlappende Eingabe und Ausgabe](synchronization-and-overlapped-input-and-output.md)
-   [asynchrone Prozedur Aufrufe](asynchronous-procedure-calls.md)
-   [kritische Abschnitts Objekte](critical-section-objects.md)
-   [Bedingungsvariablen](condition-variables.md)
-   [schlanke Lese-/Schreibsperren](slim-reader-writer--srw--locks.md)
-   [einmalige Initialisierung](one-time-initialization.md)
-   [Interlocked-Variablen Zugriff](interlocked-variable-access.md)
-   [miteinander verknüpfte, einzeln verknüpfte Listen](interlocked-singly-linked-lists.md)
-   [Timer-Warteschlangen](timer-queues.md)
-   Das [**MemoryBarrier**](/windows/win32/api/winnt/nf-winnt-memorybarrier) -Makro

Weitere Informationen zur Synchronisierung finden Sie unter [Synchronisierung und Multiprozessorprobleme](synchronization-and-multiprocessor-issues.md).

 

 
