---
description: Ein Thread Pool ist eine Sammlung von Arbeitsthreads, die im Auftrag der Anwendung asynchrone Rückrufe effizient ausführen.
ms.assetid: abe0798a-0b60-4bdb-a61e-45393f1e958d
title: Threadpools
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 690aa3eb6fd3ce7a99d71e0f57118529ef79113f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106356212"
---
# <a name="thread-pools"></a>Threadpools

Ein *Thread Pool* ist eine Sammlung von Arbeitsthreads, die im Auftrag der Anwendung asynchrone Rückrufe effizient ausführen. Der Thread Pool wird hauptsächlich verwendet, um die Anzahl der Anwendungsthreads zu verringern und die Verwaltung der Arbeitsthreads zu ermöglichen. Anwendungen können Arbeitselemente in die Warteschlange stellen, Arbeitsaufgaben zuordnen, abnutzbare Handles zuordnen, automatisch basierend auf einem Timer in die Warteschlange eingereiht und mit e/a

## <a name="thread-pool-architecture"></a>Thread Pool Architektur

Die folgenden Anwendungen können von einem Thread Pool profitieren:

-   Eine Anwendung, die sehr parallel ist und eine große Anzahl kleiner Arbeitselemente asynchron (z. b. die Suche nach verteiltem Index oder Netzwerk-e/a) versendet.
-   Eine Anwendung, die eine große Anzahl von Threads erstellt und zerstört, die jeweils für einen kurzen Zeitraum ausgeführt werden. Durch die Verwendung des Thread Pools können die Komplexität der Thread Verwaltung und der Aufwand bei der Thread Erstellung und-Zerstörung reduziert werden.
-   Eine Anwendung, die unabhängige Arbeitselemente im Hintergrund und parallel verarbeitet (z. b. das Laden mehrerer Registerkarten).
-   Eine Anwendung, die einen exklusiven warte Vorgang auf Kernel Objekte oder einen Block für eingehende Ereignisse eines Objekts ausführen muss. Durch die Verwendung des Thread Pools kann die Komplexität der Thread Verwaltung reduziert und die Leistung gesteigert werden, indem die Anzahl von Kontext Schaltern reduziert wird.
-   Eine Anwendung, die benutzerdefinierte kellnerthreads erstellt, um auf Ereignisse zu warten.

Der ursprüngliche Thread Pool wurde in Windows Vista vollständig neu entworfen. Der neue Thread Pool wird verbessert, da er einen einzelnen Arbeitsthreads bereitstellt (sowohl e/a-Vorgänge als auch nicht-e/a unterstützt), keinen Zeit Geber Thread verwendet, eine einzelne Zeit Geber Warteschlange bereitstellt und einen dedizierten permanenten Thread bereitstellt. Außerdem werden Bereinigungs Gruppen, eine höhere Leistung, mehrere Pools pro Prozess, die unabhängig geplant werden, und eine neue Thread Pool-API bereitstellt.

Die Thread Pool Architektur besteht aus den folgenden Elementen:

-   Arbeitsthreads, die die Rückruf Funktionen ausführen
-   Kellnerthreads, die auf mehrere Wait-Handles warten
-   Eine Arbeits Warteschlange
-   Ein Standard Thread Pool für jeden Prozess
-   Eine workerfactory, die die Arbeitsthreads verwaltet.

## <a name="best-practices"></a>Bewährte Methoden

Die neue [Thread Pool-API](thread-pool-api.md) bietet mehr Flexibilität und Kontrolle als die [ursprüngliche Thread Pool-API](thread-pooling.md). Allerdings gibt es einige feine, aber wichtige Unterschiede. In der ursprünglichen API wurde die Wartezeit automatisch zurückgesetzt. in der neuen API muss der Warte Vorgang jedes Mal explizit zurückgesetzt werden. Die ursprüngliche API hat den Identitätswechsel automatisch verarbeitet und den Sicherheitskontext des aufrufenden Prozesses an den Thread übertragen. Mit der neuen API muss die Anwendung den Sicherheitskontext explizit festlegen.

Im folgenden finden Sie bewährte Methoden bei der Verwendung eines Thread Pools:

-   Die Threads eines Prozesses verwenden den Thread Pool gemeinsam. Ein einzelner Arbeits Thread kann mehrere Rückruf Funktionen nacheinander ausführen. Diese Arbeitsthreads werden vom Thread Pool verwaltet. Beenden Sie daher einen Thread aus dem Thread Pool nicht, indem Sie [**TerminateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminatethread) im Thread aufrufen oder [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread) über eine Rückruffunktion aufrufen.
-   Eine e/a-Anforderung kann in jedem Thread im Thread Pool ausgeführt werden. Für das Abbrechen von e/a-Vorgängen in einem Thread Pool Thread ist eine Synchronisierung erforderlich, da die Cancel-Funktion möglicherweise in einem anderen Thread ausgeführt wird als der, der die e/a-Anforderung verarbeitet. Dies kann zu einem Abbruch eines unbekannten Vorgangs führen. Um dies zu vermeiden, geben Sie immer die [**über**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) Lapp Ende Struktur an, mit der eine e/a-Anforderung initiiert wurde, als [**CancelIoEx**](/windows/win32/api/ioapiset/nf-ioapiset-cancelioex) für asynchrone e/a aufgerufen wurde, oder verwenden Sie Ihre eigene Synchronisierung, um sicherzustellen, dass keine andere e/a-Vorgänge im Zielthread gestartet werden können, bevor Sie die Funktion [**CancelSynchronousIo**](/windows/win32/api/ioapiset/nf-ioapiset-cancelsynchronousio) oder **CancelIoEx**
-   Bereinigen Sie alle in der Rückruffunktion erstellten Ressourcen, bevor Sie von der Funktion zurückgegeben werden. Dazu zählen TLS, Sicherheits Kontexte, Thread Priorität und com-Registrierung. Rückruf Funktionen müssen auch den Thread Zustand wiederherstellen, bevor Sie zurückkehren.
-   Behalten Sie Wait-Handles und die zugeordneten Objekte bei, bis der Thread Pool signalisiert hat, dass er mit dem Handle fertig ist.
-   Markieren Sie alle Threads, die auf lange Vorgänge warten (z. b. e/a-Leerungen oder Ressourcen Bereinigung), damit der Thread Pool neue Threads zuordnen kann, anstatt auf diesen zu warten.
-   Bevor Sie eine DLL entladen, die den Thread Pool verwendet, brechen Sie alle Arbeitsaufgaben, e/a-Vorgänge, warte Vorgänge und Timer ab, und warten Sie, bis die Ausführung der Rückrufe beendet ist.
-   Vermeiden Sie Deadlocks, indem Sie Abhängigkeiten zwischen Arbeits Elementen und zwischen Rückrufen vermeiden, indem Sie sicherstellen, dass ein Rückruf nicht auf den Abschluss des Vorgangs wartet, und indem Sie die Thread Priorität beibehalten.
-   Stellen Sie zu viele Elemente in einem Prozess mit anderen Komponenten, die den Standard Thread Pool verwenden, nicht zu schnell in die Warteschlange. Es gibt einen Standard Thread Pool pro Prozess, einschließlich Svchost.exe. Standardmäßig verfügt jeder Thread Pool über maximal 500 Arbeitsthreads. Der Thread Pool versucht, mehr Arbeitsthreads zu erstellen, wenn die Anzahl der Arbeitsthreads im Zustand "bereit/wird" kleiner als die Anzahl der Prozessoren sein muss.
-   Vermeiden Sie das com-Single Thread-Apartment Modell, da es nicht mit dem Thread Pool kompatibel ist. STA erstellt einen Thread Zustand, der sich auf das nächste Arbeits Element für den Thread auswirken kann. STA ist im allgemeinen langlebig und verfügt über Thread Affinität, die das Gegenteil des Thread Pools ist.
-   Erstellen Sie einen neuen Thread Pool zum Steuern der Thread Priorität und-Isolation, zum Erstellen benutzerdefinierter Eigenschaften und zur Verbesserung der Reaktionsfähigkeit. Zusätzliche Thread Pools erfordern jedoch mehr Systemressourcen (Threads, Kernel Arbeitsspeicher). Zu viele Pools erhöhen das Potenzial für CPU-Konflikte.
-   Verwenden Sie nach Möglichkeit ein wabbares Objekt anstelle eines APC-basierten Mechanismus, um einen Thread Pool Thread zu signalisieren. APCs funktionieren nicht ebenso wie andere Signalmechanismen mit Thread Pool-Threads, da die Lebensdauer von Thread Pool-Threads vom System gesteuert wird. Daher ist es möglich, dass ein Thread beendet wird, bevor die Benachrichtigung übermittelt wird.
-   Verwenden Sie die Debugger-Erweiterung für den Thread Pool,! TP. Dieser Befehl weist die folgende Syntax auf:

    -   *pooladressflags* 
    -   obj- *adressflags* 
    -   TDie- *adressflags* 
    -   *kellneradresse*
    -   Worker- *Adresse*

    Für den Pool, den Kellner und den Worker, wenn die Adresse 0 (null) ist, werden mit dem Befehl alle Objekte Abbilder. Für den Kellner und den Worker wird durch Weglassen der Adresse der aktuelle Thread Abbilder. Die folgenden Flags sind definiert: 0x1 (einzeilige Ausgabe), 0x2 (dumpmember) und 0x4 (Arbeits Warteschlange für dumppools).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Thread Pool-API](thread-pool-api.md)
</dt> <dt>

[Verwenden der Thread Pool Funktionen](using-the-thread-pool-functions.md)
</dt> </dl>

 

 
