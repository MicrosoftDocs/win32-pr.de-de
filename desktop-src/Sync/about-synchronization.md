---
description: Um den Zugriff auf eine Ressource zu synchronisieren, verwenden Sie eines der Synchronisierungsobjekte in einer der Wartefunktionen.
ms.assetid: 0930bf12-6d5f-4f2c-914d-53e6e862d3bd
title: Informationen zur Synchronisierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb8bca156eec523b30d8f28df8b18a24d9691a33598f5dfe985e4b6b9756ffe3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118886404"
---
# <a name="about-synchronization"></a>Informationen zur Synchronisierung

Um den Zugriff auf eine Ressource zu synchronisieren, verwenden Sie eines der [Synchronisierungsobjekte](synchronization-objects.md) in einer der [Wartefunktionen](wait-functions.md). Der Zustand eines Synchronisierungsobjekts ist entweder *signalisiert* oder *nicht signalisiert.* Die Wait-Funktionen ermöglichen es einem Thread, seine eigene Ausführung zu blockieren, bis ein angegebenes nicht signalisiertes Objekt auf den signalisierten Zustand festgelegt ist. Weitere Informationen finden Sie unter [Prozessübergreifende Synchronisierung.](interprocess-synchronization.md)

Im Folgenden sind weitere Synchronisierungsmechanismen enthalten:

-   [Überlappende Eingabe und Ausgabe](synchronization-and-overlapped-input-and-output.md)
-   [asynchrone Prozeduraufrufe](asynchronous-procedure-calls.md)
-   [Kritische Abschnittsobjekte](critical-section-objects.md)
-   [Bedingungsvariablen](condition-variables.md)
-   [Reader-/Writersperren](slim-reader-writer--srw--locks.md)
-   [Einmalige Initialisierung](one-time-initialization.md)
-   [Interlocked Variable Access](interlocked-variable-access.md)
-   [Interlocked singly linked lists](interlocked-singly-linked-lists.md)
-   [Timerwarteschlangen](timer-queues.md)
-   Das [**MemoryBarrier-Makro**](/windows/win32/api/winnt/nf-winnt-memorybarrier)

Weitere Informationen zur Synchronisierung finden Sie unter [Synchronisierungs- und Multiprozessorprobleme.](synchronization-and-multiprocessor-issues.md)

 

 
