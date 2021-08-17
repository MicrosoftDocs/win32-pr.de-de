---
description: Der Scheduler verwaltet eine Warteschlange ausführbarer Threads für jede Prioritätsebene.
ms.assetid: 82463d71-9cef-4608-b997-25dc9c1e1c0a
title: Kontextwechsel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c15f5d762525fd4a80030ea10e128e2c30a1ab914e9f17d0f954d80ecfd2e204
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143133"
---
# <a name="context-switches"></a>Kontextwechsel

Der Scheduler verwaltet eine Warteschlange ausführbarer Threads für jede Prioritätsebene. Diese werden als *bereite Threads* bezeichnet. Wenn ein Prozessor verfügbar wird, führt das System einen *Kontextwechsel aus.* Die Schritte in einem Kontextwechsel sind:

1.  Speichern Sie den Kontext des Threads, der die Ausführung gerade abgeschlossen hat.
2.  Platzieren Sie den Gerade ausgeführten Thread für seine Priorität am Ende der Warteschlange.
3.  Suchen Sie die Warteschlange mit der höchsten Priorität, die bereite Threads enthält.
4.  Entfernen Sie den Thread am Anfang der Warteschlange, laden Sie seinen Kontext, und führen Sie ihn aus.

Die folgenden Threadklassen sind keine bereiten Threads.

-   Threads, die mit dem \_ CREATE SUSPENDED-Flag erstellt wurden
-   Threads wurden während der Ausführung mit der [**SuspendThread-**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-suspendthread) oder [**SwitchToThread-Funktion**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-switchtothread) angehalten.
-   Threads, die auf ein Synchronisierungsobjekt oder eine Eingabe warten.

Bis angehaltene oder blockierte Threads zur Ausführung bereit sind, ordnet der Scheduler ihnen unabhängig von ihrer Priorität keine Prozessorzeit zu.

Die häufigsten Gründe für einen Kontextwechsel sind:

-   Der Zeitslice ist verstrichen.
-   Ein Thread mit einer höheren Priorität ist nun für die Ausführung bereit.
-   Ein ausgeführter Thread muss warten.

Wenn ein ausgeführter Thread warten muss, gibt er den Rest seines Zeitslices ab.

 

 
