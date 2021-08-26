---
description: Die Benutzermodusplanung (UMS) ist ein schlanker Mechanismus, mit dem Anwendungen ihre eigenen Threads planen können.
ms.assetid: f9dd92fe-6d7a-452c-893e-e6df1757e377
title: User-Mode Planung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8a13b30685dbcbfc4d3d502e02bdbfdc10d15ea1f804cc6a8391073c44ce447
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074240"
---
# <a name="user-mode-scheduling"></a>User-Mode Planung

Die Benutzermodusplanung (UMS) ist ein schlanker Mechanismus, mit dem Anwendungen ihre eigenen Threads planen können. Eine Anwendung kann im Benutzermodus zwischen UMS-Threads wechseln, ohne den [Systemplaner](scheduling.md) zu verwenden, und die Kontrolle über den Prozessor wiedererlangen, wenn ein UMS-Thread im Kernel blockiert wird. UMS-Threads unterscheiden sich von [Fibers,](fibers.md) da jeder UMS-Thread über einen eigenen Threadkontext verfügt, anstatt den Threadkontext eines einzelnen Threads gemeinsam zu verwenden. Die Möglichkeit, zwischen Threads im Benutzermodus zu [](thread-pools.md) wechseln, macht UMS effizienter als Threadpools für die Verwaltung einer großen Anzahl von Arbeitselementen mit kurzer Dauer, die nur wenige Systemaufrufe erfordern.

UMS wird für Anwendungen mit hohen Leistungsanforderungen empfohlen, die viele Threads effizient gleichzeitig auf Systemen mit mehreren Prozessoren oder Kernen ausführen müssen. Um UMS nutzen zu können, muss eine Anwendung eine Planerkomponente implementieren, die die UMS-Threads der Anwendung verwaltet und bestimmt, wann sie ausgeführt werden sollen. Entwickler sollten überlegen, ob ihre Anwendungsleistungsanforderungen die Arbeit an der Entwicklung einer solchen Komponente rechtfertigen. Anwendungen mit mittleren Leistungsanforderungen können besser bedient werden, indem dem Systemplaner ermöglicht wird, ihre Threads zu planen.

UMS ist für 64-Bit-Anwendungen verfügbar, die auf 64-Bit-Versionen von Windows 7 und Windows Server 2008 R2 oder höher 64-Bit-Versionen von Windows. Dieses Feature ist in 32-Bit-Versionen von Windows.

Weitere Informationen finden Sie in den folgenden Abschnitten:

-   [UMS Scheduler](#ums-scheduler)
-   [UMS Scheduler-Thread](#ums-scheduler-thread)
-   [UMS-Arbeitsthreads, Threadkontexte und Vervollständigungslisten](#ums-worker-threads-thread-contexts-and-completion-lists)
-   [Einstiegspunktfunktion des UMS-Planers](#ums-scheduler-entry-point-function)
-   [UMS-Threadausführung](#ums-thread-execution)
-   [Bewährte Methoden für UMS](#ums-best-practices)

## <a name="ums-scheduler"></a>UMS Scheduler

Der UMS-Planer einer Anwendung ist dafür verantwortlich, UMS-Threads zu erstellen, zu verwalten und zu löschen und zu bestimmen, welcher UMS-Thread ausgeführt werden soll. Der Planer einer Anwendung führt die folgenden Aufgaben aus:

-   Erstellt einen UMS-Planerthread für jeden Prozessor, auf dem die Anwendung UMS-Arbeitsthreads ausführen soll.
-   Erstellt UMS-Arbeitsthreads, um die Arbeit der Anwendung durchzuführen.
-   Verwaltet eine eigene Bereitthreadwarteschlange von Arbeitsthreads, die ausgeführt werden können, und wählt Threads aus, die basierend auf den Planungsrichtlinien der Anwendung ausgeführt werden sollen.
-   Erstellt und überwacht eine oder mehrere Vervollständigungslisten, in denen das System Threads in die Warteschlange einreiht, nachdem sie die Verarbeitung im Kernel abgeschlossen haben. Dazu gehören neu erstellte Arbeitsthreads und Threads, die zuvor für einen Systemaufruf blockiert wurden, der nicht mehr blockiert wird.
-   Stellt eine Planereinstiegspunktfunktion zum Behandelt von Benachrichtigungen vom System zur Seite. Das System ruft die Einstiegspunktfunktion auf, wenn ein Planerthread erstellt wird, wenn ein Arbeitsthread bei einem Systemaufruf blockiert wird oder wenn ein Arbeitsthread die Steuerung explizit ergibt.
-   Führt Bereinigungsaufgaben für Arbeitsthreads aus, deren Ausführung beendet wurde.
-   Führt ein geordnetes Herunterfahren des Schedulers durch, wenn dies von der Anwendung angefordert wird.

## <a name="ums-scheduler-thread"></a>UMS Scheduler-Thread

Ein UMS-Planerthread ist ein gewöhnlicher Thread, der sich selbst durch Aufrufen der [**EnterUmsSchedulingMode-Funktion**](/windows/desktop/api/WinBase/nf-winbase-enterumsschedulingmode) in UMS konvertiert hat. Der Systemplaner bestimmt, wann der UMS-Planerthread basierend auf seiner Priorität relativ zu anderen bereiten Threads ausgeführt wird. Der Prozessor, auf dem der Schedulerthread ausgeführt wird, wird von der Affinität des Threads beeinflusst, wie bei Nicht-UMS-Threads.

Der Aufrufer von [**EnterUmsSchedulingMode**](/windows/desktop/api/WinBase/nf-winbase-enterumsschedulingmode) gibt eine Vervollständigungsliste und eine [*UmsSchedulerProc-Einstiegspunktfunktion*](/windows/desktop/api/WinNT/nc-winnt-rtl_ums_scheduler_entry_point) an, die dem UMS-Planerthread zugeordnet werden soll. Das System ruft die angegebene Einstiegspunktfunktion auf, wenn die Konvertierung des aufrufenden Threads in UMS abgeschlossen ist. Die Scheduler-Einstiegspunktfunktion ist dafür verantwortlich, die entsprechende nächste Aktion für den angegebenen Thread zu bestimmen. Weitere Informationen finden Sie unter [UMS Scheduler Entry Point Function](#ums-scheduler-entry-point-function) weiter unten in diesem Thema.

Eine Anwendung kann einen UMS-Planerthread für jeden Prozessor erstellen, der zum Ausführen von UMS-Threads verwendet wird. Die Anwendung kann auch die Affinität jedes UMS-Planerthreads für einen bestimmten logischen Prozessor festlegen, der tendenziell nicht verbundene Threads von der Ausführung auf diesem Prozessor ausschließt und diesen effektiv für diesen Planerthread reservieren kann. Beachten Sie, dass sich das Festlegen der Threadaffinität auf diese Weise auf die Gesamtleistung des Systems auswirken kann, indem andere Prozesse, die möglicherweise auf dem System ausgeführt werden, nicht mehr ausgeführt werden. Weitere Informationen zur Threadaffinität finden Sie unter [Mehrere Prozessoren.](multiple-processors.md)

## <a name="ums-worker-threads-thread-contexts-and-completion-lists"></a>UMS-Arbeitsthreads, Threadkontexte und Vervollständigungslisten

Ein UMS-Arbeitsthread wird erstellt, indem [**CreateRemoteThreadEx**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethreadex) mit dem UMS THREAD-Attribut PROC THREAD ATTRIBUTE aufgerufen und ein UMS-Threadkontext und eine Vervollständigungsliste \_ \_ angegeben \_ \_ werden.

Ein UMS-Threadkontext stellt den UMS-Threadzustand eines Arbeitsthreads dar und wird verwendet, um den Arbeitsthread in UMS-Funktionsaufrufen zu identifizieren. Sie wird durch Aufrufen von [**CreateUmsThreadContext erstellt.**](/windows/desktop/api/WinBase/nf-winbase-createumsthreadcontext)

Eine Vervollständigungsliste wird durch Aufrufen der [**CreateUmsCompletionList-Funktion**](/windows/desktop/api/WinBase/nf-winbase-createumscompletionlist) erstellt. Eine Vervollständigungsliste empfängt UMS-Arbeitsthreads, die die Ausführung im Kernel abgeschlossen haben und im Benutzermodus ausgeführt werden können. Nur das System kann Arbeitsthreads in eine Vervollständigungsliste einreiht. Neue UMS-Arbeitsthreads werden automatisch in die Warteschlange der Vervollständigungsliste gestellt, die beim Erstellen der Threads angegeben wurde. Zuvor blockierte Arbeitsthreads werden ebenfalls in die Vervollständigungsliste aufgenommen, wenn sie nicht mehr blockiert werden.

Jeder UMS-Planerthread ist einer einzelnen Vervollständigungsliste zugeordnet. Die gleiche Vervollständigungsliste kann jedoch einer beliebigen Anzahl von UMS-Planerthreads zugeordnet werden, und ein Planerthread kann UMS-Kontexte aus jeder Vervollständigungsliste abrufen, für die er über einen Zeiger verfügt.

Jede Vervollständigungsliste verfügt über ein zugeordnetes Ereignis, das vom System signalisiert wird, wenn ein oder mehrere Arbeitsthreads in eine leere Liste in die Warteschlange gestellt werden. Die [**GetUmsCompletionListEvent-Funktion**](/windows/desktop/api/WinBase/nf-winbase-getumscompletionlistevent) ruft ein Handle für das Ereignis für eine angegebene Vervollständigungsliste ab. Eine Anwendung kann auf mehrere Vervollständigungslistenereignisse sowie auf andere Ereignisse warten, die für die Anwendung sinnvoll sind.

## <a name="ums-scheduler-entry-point-function"></a>Einstiegspunktfunktion des UMS-Planers

Die Planereinstiegspunktfunktion einer Anwendung wird als [*UmsSchedulerProc-Funktion*](/windows/desktop/api/WinNT/nc-winnt-rtl_ums_scheduler_entry_point) implementiert. Das System ruft die Planereinstiegspunktfunktion der Anwendung zu den folgenden Zeiten auf:

-   Wenn ein Nicht-UMS-Thread durch Aufrufen von [**EnterUmsSchedulingMode**](/windows/desktop/api/WinBase/nf-winbase-enterumsschedulingmode)in einen UMS-Planerthread konvertiert wird.
-   Wenn ein UMS-Arbeitsthread [**UmsThreadYield aufruft.**](/windows/desktop/api/WinBase/nf-winbase-umsthreadyield)
-   Wenn ein UMS-Arbeitsthread für einen Systemdienst blockiert wird, z. B. einen Systemaufruf oder einen Seitenfehler.

Der *Reason-Parameter* der [*UmsSchedulerProc-Funktion*](/windows/desktop/api/WinNT/nc-winnt-rtl_ums_scheduler_entry_point) gibt den Grund an, aus dem die Einstiegspunktfunktion aufgerufen wurde. Wenn die Einstiegspunktfunktion aufgerufen wurde, weil ein neuer UMS-Planerthread erstellt wurde, enthält der *SchedulerParam-Parameter* Daten, die vom Aufrufer von [**EnterUmsSchedulingMode angegeben werden.**](/windows/desktop/api/WinBase/nf-winbase-enterumsschedulingmode) Wenn die Einstiegspunktfunktion aufgerufen wurde, weil ein UMS-Arbeitsthread ergibt, enthält der *SchedulerParam-Parameter* Daten, die vom Aufrufer von [**UmsThreadYield angegeben werden.**](/windows/desktop/api/WinBase/nf-winbase-umsthreadyield) Wenn die Einstiegspunktfunktion aufgerufen wurde, weil ein UMS-Arbeitsthread im Kernel blockiert wurde, ist der *SchedulerParam-Parameter* NULL.

Die Scheduler-Einstiegspunktfunktion ist dafür verantwortlich, die entsprechende nächste Aktion für den angegebenen Thread zu bestimmen. Wenn beispielsweise ein Arbeitsthread blockiert wird, kann die Planereinstiegspunktfunktion den nächsten verfügbaren bereiten UMS-Arbeitsthread ausführen.

Wenn die Scheduler-Einstiegspunktfunktion aufgerufen wird, sollte der Planer der Anwendung versuchen, alle Elemente in der zugehörigen Vervollständigungsliste abzurufen, indem die [**DequeueUmsCompletionListItems-Funktion**](/windows/desktop/api/WinBase/nf-winbase-dequeueumscompletionlistitems) aufgerufen wird. Diese Funktion ruft eine Liste von UMS-Threadkontexten ab, die die Verarbeitung im Kernel abgeschlossen haben und im Benutzermodus ausgeführt werden können. Der Planer der Anwendung sollte UMS-Threads nicht direkt aus dieser Liste ausführen, da dies zu unvorhersehbarem Verhalten in der Anwendung führen kann. Stattdessen sollte der Planer alle UMS-Threadkontexte abrufen, indem er die [**GetNextUmsListItem-Funktion**](/windows/desktop/api/WinBase/nf-winbase-getnextumslistitem) einmal für jeden Kontext aufruft, die UMS-Threadkontexte in die bereite Threadwarteschlange des Schedulers einfüge und erst dann UMS-Threads aus der bereiten Threadwarteschlange aus ausführen.

Wenn der Scheduler nicht auf mehrere Ereignisse warten muss, sollte er [**DequeueUmsCompletionListItems**](/windows/desktop/api/WinBase/nf-winbase-dequeueumscompletionlistitems) mit einem Timeoutparameter ungleich 0 (null) aufrufen, damit die Funktion vor der Rückgabe auf das Abschlusslistenereignis wartet. Wenn der Scheduler nicht auf mehrere Vervollständigungslistenereignisse warten muss, sollte er **DequeueUmsCompletionListItems** mit einem timeout-Parameter von 0 aufrufen, damit die Funktion sofort zurückgegeben wird, auch wenn die Vervollständigungsliste leer ist. In diesem Fall kann der Planer explizit auf Abschlusslistenereignisse warten, z. B. mit [**waitForMultipleObjects**](/windows/win32/api/synchapi/nf-synchapi-waitformultipleobjects).

## <a name="ums-thread-execution"></a>UMS-Threadausführung

Ein neu erstellter UMS-Arbeitsthread wird in die Warteschlange der angegebenen Vervollständigungsliste gestellt und wird erst ausgeführt, wenn der UMS-Planer der Anwendung ihn für die Ausführung auswählt. Dies unterscheidet sich von Nicht-UMS-Threads, deren Ausführung vom Systemplaner automatisch geplant wird, es sei denn, der Aufrufer erstellt den angehaltenen Thread explizit.

Der Planer führt einen Arbeitsthread aus, indem [**er ExecuteUmsThread mit**](/windows/desktop/api/WinBase/nf-winbase-executeumsthread) dem UMS-Kontext des Arbeitsthreads aufruft. Ein UMS-Arbeitsthread wird ausgeführt, bis er durch Aufrufen der [**UmsThreadYield-Funktion,**](/windows/desktop/api/WinBase/nf-winbase-umsthreadyield) blöcket oder beendet wird.

## <a name="ums-best-practices"></a>Bewährte Methoden für UMS

Anwendungen, die UMS implementieren, sollten die folgenden bewährten Methoden befolgen:

-   Die zugrunde liegenden Strukturen für UMS-Threadkontexte werden vom System verwaltet und sollten nicht direkt geändert werden. Verwenden Sie stattdessen [**QueryUmsThreadInformation**](/windows/desktop/api/WinBase/nf-winbase-queryumsthreadinformation) und [**SetUmsThreadInformation,**](/windows/desktop/api/WinBase/nf-winbase-setumsthreadinformation) um Informationen zu einem UMS-Arbeitsthread abzurufen und fest zu legen.
-   Um Deadlocks zu verhindern, sollte der UMS-Planerthread Sperren nicht für UMS-Arbeitsthreads freigeben. Dies schließt sowohl von der Anwendung erstellte Sperren als auch Systemsperren ein, die indirekt durch Vorgänge wie das Zuordnen aus dem Heap oder das Laden von DLLs erworben werden. Angenommen, der Planer führt einen UMS-Arbeitsthread aus, der eine DLL lädt. Der Arbeitsthread übernimmt die Loadersperre und -blöcke. Das System ruft die Scheduler-Einstiegspunktfunktion auf, die dann eine DLL lädt. Dies führt zu einem Deadlock, da die Ladesperre bereits gehalten wurde und erst wieder aufgehoben werden kann, wenn die Blockierung des ersten Threads aufgehoben wird. Um dieses Problem zu vermeiden, delegieren Sie Arbeit, die Sperren mit UMS-Arbeitsthreads gemeinsam verwenden kann, an einen dedizierten UMS-Arbeitsthread oder einen Nicht-UMS-Thread.
-   UMS ist am effizientesten, wenn die meiste Verarbeitung im Benutzermodus erfolgt. Vermeiden Sie nach Möglichkeit Systemaufrufe in UMS-Arbeitsthreads.
-   UMS-Arbeitsthreads sollten nicht davon ausgehen, dass der Systemplaner verwendet wird. Diese Annahme kann dezente Auswirkungen haben. Wenn z. B. ein Thread im unbekannten Code eine Threadpriorität oder Affinität festschreibt, kann der UMS-Planer diese trotzdem überschreiben. Code, der annimmt, dass der Systemplaner verwendet wird, verhält sich möglicherweise nicht wie erwartet und kann beim Aufrufen durch einen UMS-Thread zu Einem Fehler führen.
-   Möglicherweise muss das System den Threadkontext eines UMS-Arbeitsthreads sperren. Beispielsweise kann ein asynchroner Prozeduraufruf (APC) im Kernelmodus den Kontext des UMS-Threads ändern, sodass der Threadkontext gesperrt werden muss. Wenn der Planer versucht, den UMS-Threadkontext auszuführen, während er gesperrt ist, schlägt der Aufruf fehl. Dieses Verhalten ist entwurfsgemäß, und der Scheduler sollte so entworfen werden, dass der Zugriff auf den UMS-Threadkontext wiederholt wird.

 

 
