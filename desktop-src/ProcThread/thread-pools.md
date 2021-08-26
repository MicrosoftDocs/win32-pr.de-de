---
description: Ein Threadpool ist eine Sammlung von Arbeitsthreads, die im Auftrag der Anwendung asynchrone Rückrufe effizient ausführen.
ms.assetid: abe0798a-0b60-4bdb-a61e-45393f1e958d
title: Threadpools
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7918a0f6f0b881233ebea8e664d6e743a7bff105e265270063b08af313417e7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120081260"
---
# <a name="thread-pools"></a>Threadpools

Ein *Threadpool* ist eine Sammlung von Arbeitsthreads, die im Auftrag der Anwendung asynchrone Rückrufe effizient ausführen. Der Threadpool wird hauptsächlich verwendet, um die Anzahl von Anwendungsthreads zu reduzieren und die Verwaltung der Arbeitsthreads bereitzustellen. Anwendungen können Arbeitselemente in die Warteschlange stellen, Arbeit mit wartebaren Handles zuordnen, basierend auf einem Timer automatisch in die Warteschlange stellen und E/A binden.

## <a name="thread-pool-architecture"></a>Threadpoolarchitektur

Die folgenden Anwendungen können von der Verwendung eines Threadpools profitieren:

-   Eine Anwendung, die stark parallel ist und eine große Anzahl kleiner Arbeitselemente asynchron verteilen kann (z. B. verteilte Indexsuche oder Netzwerk-E/A).
-   Eine Anwendung, die eine große Anzahl von Threads erstellt und zerstört, die jeweils für kurze Zeit ausgeführt werden. Die Verwendung des Threadpools kann die Komplexität der Threadverwaltung und den Mehraufwand bei der Threaderstellung und -zerstörung reduzieren.
-   Eine Anwendung, die unabhängige Arbeitselemente im Hintergrund und parallel verarbeitet (z. B. mehrere Registerkarten laden).
-   Eine Anwendung, die eine exklusive Wartezeit für Kernelobjekte ausführen oder eingehende Ereignisse für ein Objekt blockieren muss. Die Verwendung des Threadpools kann die Komplexität der Threadverwaltung reduzieren und die Leistung steigern, indem die Anzahl der Kontextwechsel reduziert wird.
-   Eine Anwendung, die benutzerdefinierte Waiterthreads erstellt, um auf Ereignisse zu warten.

Der ursprüngliche Threadpool wurde in Windows Vista vollständig neu geordnet. Der neue Threadpool wurde verbessert, da er einen einzelnen Workerthreadtyp bereitstellt (unterstützt E/A und Nicht-E/A), keinen Timerthread verwendet, eine einzelne Timerwarteschlange bereitstellt und einen dedizierten persistenten Thread bereitstellt. Außerdem werden Bereinigungsgruppen, eine höhere Leistung, mehrere Pools pro Prozess, die unabhängig voneinander geplant werden, und eine neue Threadpool-API bereitgestellt.

Die Threadpoolarchitektur besteht aus folgendem Code:

-   Arbeitsthreads, die die Rückruffunktionen ausführen
-   Waiterthreads, die auf mehrere Wait-Handles warten
-   Eine Arbeitswarteschlange
-   Ein Standardthreadpool für jeden Prozess
-   Eine Workerfactory, die die Arbeitsthreads verwaltet

## <a name="best-practices"></a>Empfehlungen

Die neue [Threadpool-API](thread-pool-api.md) bietet mehr Flexibilität und Kontrolle als die [ursprüngliche Threadpool-API.](thread-pooling.md) Es gibt jedoch einige geringfügige, aber wichtige Unterschiede. In der ursprünglichen API war die Zurücksetzung automatisch. In der neuen API muss die Wartezeit jedes Mal explizit zurückgesetzt werden. Die ursprüngliche API hat den Identitätswechsel automatisch verarbeitet und den Sicherheitskontext des aufrufenden Prozesses an den Thread übertragen. Mit der neuen API muss die Anwendung den Sicherheitskontext explizit festlegen.

Im Folgenden werden bewährte Methoden für die Verwendung eines Threadpools verwendet:

-   Die Threads eines Prozesses nutzen den Threadpool gemeinsam. Ein einzelner Arbeitsthread kann mehrere Rückruffunktionen nacheinander ausführen. Diese Arbeitsthreads werden vom Threadpool verwaltet. Beenden Sie daher keinen Thread aus dem Threadpool, indem [**Sie TerminateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminatethread) für den Thread aufrufen oder [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread) über eine Rückruffunktion aufrufen.
-   Eine E/A-Anforderung kann für jeden Thread im Threadpool ausgeführt werden. Das Abbrechen von E/A in einem Threadpoolthread erfordert eine Synchronisierung, da die Cancel-Funktion möglicherweise in einem anderen Thread als dem ausgeführt wird, der die E/A-Anforderung verarbeitet, was zum Abbruch eines unbekannten Vorgangs führen kann. Um dies zu vermeiden, stellen Sie immer die [**OVERLAPPED-Struktur**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) bereit, mit der eine E/A-Anforderung beim Aufrufen von [**CancelIoEx**](/windows/win32/api/ioapiset/nf-ioapiset-cancelioex) für asynchrone E/A initiiert wurde, oder verwenden Sie Ihre eigene Synchronisierung, um sicherzustellen, dass keine anderen E/A-Vorgänge im Zielthread gestartet werden können, bevor Sie entweder die [**CancelSynchronousIo-**](/windows/win32/api/ioapiset/nf-ioapiset-cancelsynchronousio) oder **CancelIoEx-Funktion** aufrufen.
-   Bereinigen Sie alle Ressourcen, die in der Rückruffunktion erstellt wurden, bevor Sie von der Funktion zurückkehren. Dazu gehören TLS, Sicherheitskontexte, Threadpriorität und COM-Registrierung. Rückruffunktionen müssen auch den Threadzustand wiederherstellen, bevor sie zurückgegeben werden.
-   Halten Sie Wait-Handles und die zugehörigen Objekte aktiv, bis der Threadpool signalisiert hat, dass er mit dem Handle fertig ist.
-   Markieren Sie alle Threads, die auf lange Vorgänge warten (z. B. E/A-Leerungen oder Ressourcenbereinigungen), sodass der Threadpool neue Threads zuordnen kann, anstatt auf diesen zu warten.
-   Brechen Sie vor dem Entladen einer DLL, die den Threadpool verwendet, alle Arbeitselemente, E/A-Vorgänge, Wartevorgänge und Timer ab, und warten Sie, bis die Ausführung von Rückrufen abgeschlossen ist.
-   Vermeiden Sie Deadlocks, indem Sie Abhängigkeiten zwischen Arbeitselementen und Rückrufen beseitigen, indem Sie sicherstellen, dass ein Rückruf nicht auf den Abschluss wartet, und indem Sie die Threadpriorität beibehalten.
-   Stellen Sie in einem Prozess mit anderen Komponenten, der den Standardthreadpool verwendet, nicht zu viele Elemente zu schnell in die Warteschlange. Es gibt einen Standardthreadpool pro Prozess, einschließlich Svchost.exe. Standardmäßig verfügt jeder Threadpool über maximal 500 Arbeitsthreads. Der Threadpool versucht, mehr Arbeitsthreads zu erstellen, wenn die Anzahl der Arbeitsthreads im Zustand Bereit/Ausführung kleiner als die Anzahl der Prozessoren sein muss.
-   Vermeiden Sie das COM-Singlethread-Apartmentmodell, da es nicht mit dem Threadpool kompatibel ist. STA erstellt einen Threadzustand, der sich auf das nächste Arbeitselement für den Thread auswirken kann. STA ist im Allgemeinen langlebig und verfügt über Threadaffinität, was das Gegenteil des Threadpools ist.
-   Erstellen Sie einen neuen Threadpool, um die Threadpriorität und -isolation zu steuern, benutzerdefinierte Merkmale zu erstellen und möglicherweise die Reaktionsfähigkeit zu verbessern. Zusätzliche Threadpools erfordern jedoch mehr Systemressourcen (Threads, Kernelspeicher). Zu viele Pools erhöhen das Potenzial für CPU-Inhalte.
-   Verwenden Sie nach Möglichkeit ein wartebares Objekt anstelle eines APC-basierten Mechanismus, um einen Threadpoolthread zu signalisieren. APCs funktionieren nicht so gut mit Threadpoolthreads wie andere Signalmechanismen, da das System die Lebensdauer von Threadpoolthreads steuert, sodass es möglich ist, dass ein Thread beendet wird, bevor die Benachrichtigung übermittelt wird.
-   Verwenden Sie die Threadpooldebuggererweiterung !tp. Dieser Befehl verwendet Folgendes:

    -   *Pooladressflags* 
    -   *obj-Adressflags* 
    -   *Adressflags*  in die Queue
    -   *Waiteradresse*
    -   *Workeradresse*

    Wenn die Adresse für pool, waiter und worker 0 (null) ist, gibt der Befehl alle Objekte aus. Bei Waiter und Worker wird durch Weglassen der Adresse der aktuelle Thread gedumpt. Die folgenden Flags sind definiert: 0x1 (einzeilige Ausgabe), 0x2 (Dumpmember) und 0x4 (Speicherpoolarbeitswarteschlange).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Threadpool-API](thread-pool-api.md)
</dt> <dt>

[Verwenden der Threadpoolfunktionen](using-the-thread-pool-functions.md)
</dt> </dl>

 

 
