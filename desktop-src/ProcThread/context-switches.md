---
description: Der Scheduler verwaltet eine Warteschlange mit ausführbaren Threads für jede Prioritätsstufe.
ms.assetid: 82463d71-9cef-4608-b997-25dc9c1e1c0a
title: Kontextwechsel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7628ee9e659cdbc2369b5f69d25847e8864dbd62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104216019"
---
# <a name="context-switches"></a>Kontextwechsel

Der Scheduler verwaltet eine Warteschlange mit ausführbaren Threads für jede Prioritätsstufe. Diese werden als *bereite Threads* bezeichnet. Wenn ein Prozessor verfügbar wird, führt das System einen *Kontextwechsel* aus. Die Schritte in einem Kontextwechsel lauten wie folgt:

1.  Speichern Sie den Kontext des Threads, der gerade ausgeführt wird.
2.  Platzieren Sie den soeben ausgeführten Thread am Ende der Warteschlange für seine Priorität.
3.  Suchen Sie die Warteschlange mit der höchsten Priorität, die bereite Threads enthält.
4.  Entfernen Sie den Thread am Anfang der Warteschlange, laden Sie seinen Kontext, und führen Sie ihn aus.

Bei den folgenden Thread Klassen handelt es sich nicht um bereite Threads.

-   Mit dem Flag zum Erstellen von angehaltenen Threads erstellte Threads \_
-   Threads, die während der Ausführung mit der [**SuspendThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-suspendthread) -oder [**SwitchTo Thread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-switchtothread) -Funktion angehalten wurden
-   Threads, die auf ein Synchronisierungs Objekt oder eine Eingabe warten.

Bis die Threads, die angehalten oder blockiert werden, ausgeführt werden können, weist der Planer unabhängig von ihrer Priorität keine Prozessorzeit zu.

Die häufigsten Gründe für einen Kontextwechsel sind:

-   Der Zeit Slice ist abgelaufen.
-   Ein Thread mit einer höheren Priorität ist für die Durchführung bereit.
-   Ein laufender Thread muss warten.

Wenn ein laufender Thread warten muss, wird der restliche Zeit Slice aufgegeben.

 

 
