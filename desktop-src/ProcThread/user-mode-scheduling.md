---
description: Die benutzermodusplanung (ums) ist ein schlanker Mechanismus, mit dem Anwendungen ihre eigenen Threads planen können.
ms.assetid: f9dd92fe-6d7a-452c-893e-e6df1757e377
title: User-Mode Planung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3ceea3c4d4e40d73f48414d074bcb5b4f6e911d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106367992"
---
# <a name="user-mode-scheduling"></a>User-Mode Planung

Die benutzermodusplanung (ums) ist ein schlanker Mechanismus, mit dem Anwendungen ihre eigenen Threads planen können. Eine Anwendung kann im Benutzermodus zwischen den Verarbeitungsthreads wechseln, ohne den [Systemplaner](scheduling.md) einzubeziehen, und die Steuerung des Prozessors wiederherzustellen, wenn ein ums-Thread im Kernel blockiert wird. UMS-Threads unterscheiden sich von [Fibers](fibers.md) darin, dass jeder ums-Thread über einen eigenen Thread Kontext verfügt, anstatt den Thread Kontext eines einzelnen Threads gemeinsam zu nutzen. Durch die Möglichkeit, zwischen Threads im Benutzermodus zu wechseln, werden die ums effizienter als [Thread Pools](thread-pools.md) für die Verwaltung einer großen Anzahl von Arbeitsaufgaben mit kurzer Laufzeit, für die nur wenige Systemaufrufe erforderlich sind.

UMS werden für Anwendungen mit hohen Leistungsanforderungen empfohlen, die viele Threads gleichzeitig auf Multiprozessor-oder Multikernsystemen ausführen müssen. Um von den Vorteilen zu profitieren, muss eine Anwendung eine Scheduler-Komponente implementieren, die die UMS-Threads der Anwendung verwaltet und festlegt, wann Sie ausgeführt werden sollen. Entwickler sollten berücksichtigen, ob Ihre Anwendungs Leistungsanforderungen die Arbeit bei der Entwicklung einer solchen Komponente rechtfertigen. Anwendungen mit mittleren Leistungsanforderungen werden möglicherweise besser bedient, indem der Systemplaner die Planung Ihrer Threads ermöglicht.

UMS steht für 64-Bit-Anwendungen zur Verfügung, die auf 64-Bit-Versionen von Windows 7 und Windows Server 2008 R2 oder neueren 64-Bit-Versionen von Windows ausgeführt werden. Diese Funktion ist in 32-Bit-Versionen von Windows nicht verfügbar.

Weitere Informationen finden Sie in den folgenden Abschnitten:

-   [UMS-Scheduler](#ums-scheduler)
-   [UMS-Scheduler-Thread](#ums-scheduler-thread)
-   [UMS-Arbeitsthreads, Thread Kontexte und Vervollständigungs Listen](#ums-worker-threads-thread-contexts-and-completion-lists)
-   [UMS Scheduler-Einstiegspunkt Funktion](#ums-scheduler-entry-point-function)
-   [UMS-Thread-Ausführung](#ums-thread-execution)
-   [Bewährte Methoden für ums](#ums-best-practices)

## <a name="ums-scheduler"></a>UMS-Scheduler

Der ums-Scheduler einer Anwendung ist für das Erstellen, verwalten und Löschen von UMS-Threads und das Ermitteln des auszuführenden UMS-Threads verantwortlich. Der Scheduler einer Anwendung führt die folgenden Aufgaben aus:

-   Erstellt einen ums-schedulerthread für jeden Prozessor, auf dem die Anwendung ums Workerthreads ausgeführt wird.
-   Erstellt ums-Arbeitsthreads, um die Arbeit der Anwendung auszuführen.
-   Verwaltet eine eigene Warteschlange für Arbeitsthreads von Arbeitsthreads, die zur Ausführung bereit sind, und wählt Threads aus, die basierend auf den Planungsrichtlinien der Anwendung ausgeführt werden.
-   Erstellt und überwacht eine oder mehrere Vervollständigungs Listen, in denen das System Threads in die Warteschlange eingereiht, nachdem die Verarbeitung im Kernel abgeschlossen ist Dies schließt neu erstellte Arbeitsthreads und Threads ein, die zuvor bei einem System aufruter blockiert wurden, die blockiert werden.
-   Stellt eine Einstiegspunkt Funktion für den Scheduler bereit, um Benachrichtigungen vom System zu verarbeiten. Das System ruft die Einstiegspunkt Funktion auf, wenn ein Scheduler-Thread erstellt wird, wenn ein Arbeits Thread bei einem Systemaufruf blockiert oder wenn ein Arbeits Thread die Steuerung explizit übergibt.
-   Führt Cleanuptasks für Arbeitsthreads aus, deren Ausführung abgeschlossen ist.
-   Führt ein ordnungsgemäßes Herunterfahren des Schedulers aus, wenn er von der Anwendung angefordert wird.

## <a name="ums-scheduler-thread"></a>UMS-Scheduler-Thread

Ein ums-Scheduler-Thread ist ein gewöhnlicher Thread, der sich durch Aufrufen der Funktion " [**enterumsschedulingmode**](/windows/desktop/api/WinBase/nf-winbase-enterumsschedulingmode) " in "ums" konvertiert hat. Der Systemplaner bestimmt, wann der ums-Scheduler-Thread basierend auf seiner Priorität in Bezug auf andere bereite Threads ausgeführt wird. Der Prozessor, auf dem der Scheduler-Thread ausgeführt wird, wird durch die Thread Affinität beeinflusst, wie bei nicht-UMS-Threads.

Der Aufrufer von [**enterumsschedulingmode**](/windows/desktop/api/WinBase/nf-winbase-enterumsschedulingmode) gibt eine Vervollständigungsliste und eine [*umsschedulerproc*](/windows/desktop/api/WinNT/nc-winnt-rtl_ums_scheduler_entry_point) -Einstiegspunkt Funktion an, die dem ums-planerthread zugeordnet werden soll. Das System ruft die angegebene Einstiegspunkt Funktion auf, wenn die Umstellung des aufrufenden Threads in ums abgeschlossen ist. Die Einstiegspunkt Funktion des Schedulers ist dafür verantwortlich, die geeignete nächste Aktion für den angegebenen Thread festzulegen. Weitere Informationen finden Sie weiter unten in diesem Thema unter " [ums Scheduler-Einstiegspunkt Funktion](#ums-scheduler-entry-point-function) ".

Eine Anwendung kann einen ums-Scheduler-Thread für jeden Prozessor erstellen, der zum Ausführen von UMS-Threads verwendet wird. Die Anwendung kann auch die Affinität jedes ums-planerthreads für einen bestimmten logischen Prozessor festlegen, der in der Regel nicht verknüpfte Threads von der Ausführung auf diesem Prozessor ausschließt und Sie für diesen Zeit Planungs Thread reserviert. Beachten Sie, dass das Festlegen der Thread Affinität auf diese Weise die Gesamtsystemleistung beeinträchtigt, indem andere Prozesse, die möglicherweise auf dem System ausgeführt werden, verhungert werden. Weitere Informationen zur Thread Affinität finden Sie unter [mehrere Prozessoren](multiple-processors.md).

## <a name="ums-worker-threads-thread-contexts-and-completion-lists"></a>UMS-Arbeitsthreads, Thread Kontexte und Vervollständigungs Listen

Ein ums-Arbeits Thread wird erstellt, indem [**createremotethreadex**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethreadex) mit dem "proc \_ Thread \_ Attribute \_ ums" \_ -Thread Attribut aufgerufen und ein ums-Thread Kontext und eine Vervollständigungsliste angegeben werden.

Ein ums-Thread Kontext stellt den ums-Thread Zustand eines Arbeitsthreads dar und wird verwendet, um den Arbeits Thread in ums-Funktionsaufrufen zu identifizieren. Sie wird erstellt, indem [**createumsthlecontext**](/windows/desktop/api/WinBase/nf-winbase-createumsthreadcontext)aufgerufen wird.

Eine Vervollständigungsliste wird durch Aufrufen der [**createumscompletionlist**](/windows/desktop/api/WinBase/nf-winbase-createumscompletionlist) -Funktion erstellt. Eine Vervollständigungsliste empfängt ums-Worker-Threads, deren Ausführung im Kernel abgeschlossen ist und die für die Ausführung im Benutzermodus bereit sind. Nur das System kann Arbeitsthreads in eine Vervollständigungsliste in eine Warteschlange stellen. Neue ums-Arbeitsthreads werden automatisch in die Warteschlange eingereiht, wenn die Threads erstellt wurden. Zuvor blockierte Arbeitsthreads werden auch in der Vervollständigungsliste in die Warteschlange eingereiht, wenn Sie nicht mehr blockiert werden.

Jedem ums-schedulerthread ist eine einzelne Vervollständigungsliste zugeordnet. Allerdings kann die gleiche Vervollständigungsliste mit einer beliebigen Anzahl von ums-planerthreads verknüpft werden, und ein Scheduler-Thread kann die ums-Kontexte aus jeder Vervollständigungsliste abrufen, für die er einen Zeiger hat.

Jede Vervollständigungsliste verfügt über ein zugeordnetes Ereignis, das vom System signalisiert wird, wenn ein oder mehrere Arbeitsthreads in eine leere Liste eingereiht werden. Die [**getumscompletionlistevent**](/windows/desktop/api/WinBase/nf-winbase-getumscompletionlistevent) -Funktion Ruft ein Handle für das-Ereignis für eine angegebene Vervollständigungsliste ab. Eine Anwendung kann mit anderen Ereignissen, die für die Anwendung sinnvoll sind, auf mehr als ein Vervollständigungs Listen Ereignis warten.

## <a name="ums-scheduler-entry-point-function"></a>UMS Scheduler-Einstiegspunkt Funktion

Die Einstiegspunkt Funktion einer Anwendung ist als " [*umsschedulerproc*](/windows/desktop/api/WinNT/nc-winnt-rtl_ums_scheduler_entry_point) "-Funktion implementiert. Das System ruft die Scheduler-Einstiegspunkt Funktion der Anwendung zu den folgenden Zeiten auf:

-   Wenn ein nicht-ums-Thread durch Aufrufen von " [**enterumsschedulingmode**](/windows/desktop/api/WinBase/nf-winbase-enterumsschedulingmode)" in einen ums-planerthread konvertiert wird.
-   Wenn ein ums-Workerthread [**umsthumyield**](/windows/desktop/api/WinBase/nf-winbase-umsthreadyield)aufruft.
-   Wenn ein ums-Arbeitsthreads in einem Systemdienst blockiert, z. b. ein System-oder Seiten Fehler.

Der *reason* -Parameter der [*umsschedulerproc*](/windows/desktop/api/WinNT/nc-winnt-rtl_ums_scheduler_entry_point) -Funktion gibt den Grund an, warum die Einstiegspunkt Funktion aufgerufen wurde. Wenn die Einstiegspunkt Funktion aufgerufen wurde, weil ein neuer ums-Scheduler-Thread erstellt wurde, enthält der *schedulerparam* -Parameterdaten, die vom Aufrufer von [**enterumsschedulingmode**](/windows/desktop/api/WinBase/nf-winbase-enterumsschedulingmode)angegeben werden. Wenn die Einstiegspunkt Funktion aufgerufen wurde, weil ein ums-Arbeits Thread zurückgegeben wurde, enthält der *schedulerparam* -Parameterdaten, die vom Aufrufer von [**umsthlesyield**](/windows/desktop/api/WinBase/nf-winbase-umsthreadyield)angegeben werden. Wenn die Einstiegspunkt Funktion aufgerufen wurde, weil ein ums-Arbeitsthreads im Kernel blockiert wurde, ist der *schedulerparam* -Parameter NULL.

Die Einstiegspunkt Funktion des Schedulers ist dafür verantwortlich, die geeignete nächste Aktion für den angegebenen Thread festzulegen. Wenn z. b. ein Arbeits Thread blockiert ist, kann die Scheduler-Einstiegspunkt Funktion den nächsten verfügbaren Arbeits Thread ausführen.

Wenn die Scheduler-Einstiegspunkt Funktion aufgerufen wird, sollte der Scheduler der Anwendung versuchen, alle Elemente in der zugehörigen Vervollständigungsliste abzurufen, indem die Funktion [**dequeueumscompletionlistitems**](/windows/desktop/api/WinBase/nf-winbase-dequeueumscompletionlistitems) aufgerufen wird. Diese Funktion Ruft eine Liste der ums-Thread Kontexte ab, die die Verarbeitung im Kernel abgeschlossen haben und zur Laufzeit im Benutzermodus bereit sind. Der Scheduler der Anwendung sollte keine UMS-Threads direkt aus dieser Liste ausführen, da dies zu unvorhersehbarem Verhalten in der Anwendung führen kann. Stattdessen sollte der Planer alle ums-Thread Kontexte abrufen, indem er die [**getnextumslistitem**](/windows/desktop/api/WinBase/nf-winbase-getnextumslistitem) -Funktion für jeden Kontext einmal aufrufen, die ums-Thread Kontexte in die bereite Thread Warteschlange des Planers einfügt und nur UMS-Threads aus der Warteschlange für den bereiten Thread ausführt.

Wenn der Planer nicht auf mehrere Ereignisse warten muss, sollte er [**dequeueumscompletionlistitems**](/windows/desktop/api/WinBase/nf-winbase-dequeueumscompletionlistitems) mit einem Timeout Parameter ungleich NULL aufrufen, damit die Funktion vor der Rückgabe auf das Abschluss Listen Ereignis wartet. Wenn der Scheduler auf mehrere Ereignisse der Vervollständigungsliste warten muss, sollte er **dequeueumscompletionlistitems** mit einem Timeout Parameter von 0 aufrufen, sodass die Funktion sofort zurückgibt, auch wenn die Vervollständigungsliste leer ist. In diesem Fall kann der Planer explizit auf Vervollständigungs Listenereignisse warten, z. b. mit [**WaitForMultipleObjects**](/windows/win32/api/synchapi/nf-synchapi-waitformultipleobjects).

## <a name="ums-thread-execution"></a>UMS-Thread-Ausführung

Ein neu erstellter ums-Arbeits Thread wird in die angegebene Vervollständigungsliste eingereiht und wird erst ausgeführt, wenn der es-Zeitplaner der Anwendung die Ausführung auswählt. Dies unterscheidet sich von nicht-UMS-Threads, die der Systemplaner automatisch plant, auszuführen, es sei denn, der Aufrufer erstellt explizit den Thread angehalten.

Der Scheduler führt einen Arbeits Thread durch Aufrufen von [**executeessthread**](/windows/desktop/api/WinBase/nf-winbase-executeumsthread) mit dem ums-Kontext des Arbeitsthreads aus. Ein ums-Arbeits Thread wird ausgeführt, bis er durch Aufrufen der [**umsthleyield**](/windows/desktop/api/WinBase/nf-winbase-umsthreadyield) -Funktion oder-Blöcke ausgeführt wird.

## <a name="ums-best-practices"></a>Bewährte Methoden für ums

Anwendungen, die ums implementieren, sollten die folgenden bewährten Methoden befolgen:

-   Die zugrunde liegenden Strukturen für ums-Thread Kontexte werden vom System verwaltet und sollten nicht direkt geändert werden. Verwenden Sie stattdessen [**queryumsthinfoinformation**](/windows/desktop/api/WinBase/nf-winbase-queryumsthreadinformation) und [**setumsthinfoinformation**](/windows/desktop/api/WinBase/nf-winbase-setumsthreadinformation) , um Informationen über einen ums-Arbeitsthreads abzurufen und festzulegen.
-   Um Deadlocks zu verhindern, sollte der ums-Scheduler-Thread keine Sperren mit ums-Arbeitsthreads freigeben. Dies schließt sowohl von der Anwendung erstellte Sperren als auch System Sperren ein, die indirekt durch Vorgänge wie das zuordnen aus dem Heap oder das Laden von DLLs erworben werden. Nehmen Sie beispielsweise an, der Planer führt einen ums-Workerthread aus, der eine DLL lädt. Der Arbeits Thread erhält die Loadersperre und-Blöcke. Das System ruft die Scheduler-Einstiegspunkt Funktion auf, die dann eine DLL lädt. Dies führt zu einem Deadlock, da die Loadersperre bereits aufrechterhalten wurde und nicht freigegeben werden kann, bis der erste Thread die Blockierung aufgehoben. Um dieses Problem zu vermeiden, delegieren Sie die Arbeit, die möglicherweise Sperren mit ums-Arbeitsthreads gemeinsam verwendet, an einen dedizierten ums-Arbeits Thread oder einen nicht-ums-Thread.
-   UMS ist am effizientesten, wenn die meisten Verarbeitungsvorgänge im Benutzermodus ausgeführt werden. Vermeiden Sie, wenn möglich, Systemaufrufe in ums-Arbeitsthreads.
-   UMS-Arbeitsthreads sollten nicht davon ausgehen, dass der Systemplaner verwendet wird. Diese Annahme kann feine Auswirkungen haben. Wenn ein Thread im unbekannten Code z. b. eine Thread Priorität oder-Affinität festlegt, kann der ums-Scheduler ihn trotzdem überschreiben. Code, der annimmt, dass der Systemplaner verwendet wird, verhält sich möglicherweise nicht erwartungsgemäß und kann beim Aufrufen durch einen ums-Thread unterbrechen.
-   Möglicherweise muss das System den Thread Kontext eines ums-Arbeitsthreads sperren. Beispielsweise kann ein asynchroner Prozedur Aufrufe (APC) im Kernel Modus den Kontext des UMS-Threads ändern, sodass der Thread Kontext gesperrt werden muss. Wenn der Scheduler versucht, den ums-Thread Kontext auszuführen, während er gesperrt ist, tritt ein Fehler auf. Dieses Verhalten ist Entwurfs bedingt, und der Scheduler sollte so entworfen werden, dass der Zugriff auf den ums-Thread Kontext wiederholt wird.

 

 
