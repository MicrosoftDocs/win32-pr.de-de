---
description: Wait-Funktionen ermöglichen es einem Thread, seine eigene Ausführung zu blockieren.
ms.assetid: 9c66c71d-fdfd-42ae-895c-2fc842b5bc7a
title: Wait-Funktionen
ms.topic: article
ms.date: 06/25/2020
ms.openlocfilehash: 15bfc37dcd8fe541c14b9a0693c7b743cae6ed3e548c418baf0585f078e6d59a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117764964"
---
# <a name="wait-functions"></a>Wait-Funktionen

*Wait-Funktionen* ermöglichen es einem Thread, seine eigene Ausführung zu blockieren. Die Wait-Funktionen geben erst dann zurück, wenn die angegebenen Kriterien erfüllt sind. Der Typ der Wait-Funktion bestimmt den Satz der verwendeten Kriterien. Wenn eine Wartefunktion aufgerufen wird, überprüft sie, ob die Wartekriterien erfüllt wurden. Wenn die Kriterien nicht erfüllt wurden, wechselt der aufrufende Thread in den Wartezustand, bis die Bedingungen der Wartekriterien erfüllt sind oder das angegebene Time out-Intervall verstrichen ist.

-   [Wartefunktionen für einzelne Objekte](#single-object-wait-functions)
-   [Wartefunktionen für mehrere Objekte](#multiple-object-wait-functions)
-   [Warnungsfähige Wartefunktionen](#alertable-wait-functions)
-   [Registrierte Wartefunktionen](#registered-wait-functions)
-   [Warten auf eine Adresse](#waiting-on-an-address)
-   [Wartefunktionen und Time out-Intervalle](#wait-functions-and-time-out-intervals)
-   [Wait-Funktionen und Synchronisierungsobjekte](#wait-functions-and-synchronization-objects)
-   [Wait-Funktionen und Erstellen von Windows](#wait-functions-and-creating-windows)

## <a name="single-object-wait-functions"></a>Wartefunktionen für einzelne Objekte

Die Funktionen [**SignalObjectAndWait,**](/windows/win32/api/synchapi/nf-synchapi-signalobjectandwait) [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject)und [**WaitForSingleObjectEx**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex) erfordern ein Handle für ein Synchronisierungsobjekt. Diese Funktionen geben zurück, wenn eine der folgenden Vorgänge auftritt:

-   Das angegebene Objekt befindet sich im signalisierten Zustand.
-   Das Time out-Intervall vergeht. Das Time out-Intervall kann auf **INFINITE** festgelegt werden, um anzugeben, dass für die Wartezeit kein Time out erfolgt.

Die [**SignalObjectAndWait-Funktion**](/windows/win32/api/synchapi/nf-synchapi-signalobjectandwait) ermöglicht es dem aufrufenden Thread, atomisch den Zustand eines Objekts auf signalisiert festzulegen und zu warten, bis der Zustand eines anderen Objekts auf signalisiert festgelegt ist.

## <a name="multiple-object-wait-functions"></a>Wartefunktionen für mehrere Objekte

Die Funktionen [**WaitForMultipleObjects,**](/windows/win32/api/synchapi/nf-synchapi-waitformultipleobjects) [**WaitForMultipleObjectsEx,**](/windows/win32/api/synchapi/nf-synchapi-waitformultipleobjectsex) [**MsgWaitForMultipleObjects**](/windows/desktop/api/Winuser/nf-winuser-msgwaitformultipleobjects)und [**MsgWaitForMultipleObjectsEx**](/windows/desktop/api/Winuser/nf-winuser-msgwaitformultipleobjectsex) ermöglichen es dem aufrufenden Thread, ein Array anzugeben, das mindestens ein Synchronisierungsobjekthandles enthält. Diese Funktionen geben zurück, wenn eine der folgenden Vorgänge auftritt:

-   Der Zustand eines der angegebenen Objekte ist auf signalisiert festgelegt, oder die Zustände aller Objekte wurden auf signalisiert festgelegt. Sie steuern, ob ein oder alle Zustände im Funktionsaufruf verwendet werden.
-   Das Time out-Intervall vergeht. Das Time out-Intervall kann auf **INFINITE** festgelegt werden, um anzugeben, dass für die Wartezeit kein Time out erfolgt.

Mit den Funktionen [**MsgWaitForMultipleObjects**](/windows/desktop/api/Winuser/nf-winuser-msgwaitformultipleobjects) und [**MsgWaitForMultipleObjectsEx**](/windows/desktop/api/Winuser/nf-winuser-msgwaitformultipleobjectsex) können Sie Eingabeereignisobjekte im Objekthandlearray angeben. Dies erfolgt, wenn Sie den Typ der Eingabe angeben, auf den in der Eingabewarteschlange des Threads gewartet werden soll. Beispielsweise kann ein Thread **MsgWaitForMultipleObjects** verwenden, um seine Ausführung zu blockieren, bis der Zustand eines angegebenen Objekts auf signalisiert festgelegt wurde und mauseingaben in der Eingabewarteschlange des Threads verfügbar sind. Der Thread kann die [**GetMessage-,**](/windows/win32/api/winuser/nf-winuser-getmessage) [**PeekMessageA-**](/windows/win32/api/winuser/nf-winuser-peekmessagea) oder [**PeekMessageW-Funktion**](/windows/win32/api/winuser/nf-winuser-peekmessagew) verwenden, um die Eingabe abzurufen.

Wenn darauf gewartet wird, dass die Zustände aller Objekte auf signalisiert festgelegt werden, ändern diese Funktionen mit mehreren Objekten die Zustände der angegebenen Objekte erst, wenn die Zustände aller Objekte signalisiert wurden. Beispielsweise kann der Zustand eines Mutexobjekts signalisiert werden, aber der aufrufende Thread erhält erst dann den Besitz, wenn die Zustände der anderen im Array angegebenen Objekte ebenfalls auf signalisiert festgelegt wurden. In der Zwischenzeit erhält ein anderer Thread möglicherweise den Besitz des Mutexobjekts, wodurch sein Zustand auf nicht signalisiert festgelegt wird.

Wenn darauf gewartet wird, dass der Zustand eines einzelnen Objekts auf "signaled" festgelegt ist, überprüfen diese Funktionen mit mehreren Objekten die Handles im Array ab Index 0 in der Reihenfolge, bis eines der Objekte signalisiert wird. Wenn mehrere Objekte signalisiert werden, gibt die Funktion den Index des ersten Handles im Array zurück, dessen Objekt signalisiert wurde.

## <a name="alertable-wait-functions"></a>Warnungsfähige Wartefunktionen

Die Funktionen [**MsgWaitForMultipleObjectsEx,**](/windows/desktop/api/Winuser/nf-winuser-msgwaitformultipleobjectsex) [**SignalObjectAndWait,**](/windows/win32/api/synchapi/nf-synchapi-signalobjectandwait) [**WaitForMultipleObjectsEx**](/windows/win32/api/synchapi/nf-synchapi-waitformultipleobjectsex)und [**WaitForSingleObjectEx**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex) unterscheiden sich von den anderen Wartefunktionen darin, dass sie optional einen *warnungsfähigen Wartevorgang* ausführen können. In einem warnungsfähigen Wartevorgang kann die Funktion zurückgeben, wenn die angegebenen Bedingungen erfüllt sind, aber sie kann auch zurückgeben, wenn das System eine E/A-Abschlussroutine oder einen APC zur Ausführung durch den wartenden Thread in die Warteschlange einreiht. Weitere Informationen zu warnungsfähigen Wartevorgängen und E/A-Abschlussroutinen finden Sie unter [Synchronisierung und überlappende Eingabe und Ausgabe.](synchronization-and-overlapped-input-and-output.md) Weitere Informationen zu APCs finden Sie unter [Asynchrone Prozeduraufrufe.](asynchronous-procedure-calls.md)

## <a name="registered-wait-functions"></a>Registrierte Wartefunktionen

Die [**RegisterWaitForSingleObject-Funktion**](/windows/desktop/api/WinBase/nf-winbase-registerwaitforsingleobject) unterscheidet sich von den anderen Wartefunktionen darin, dass der Wartevorgang von einem Thread aus dem [Threadpool](../procthread/thread-pooling.md)ausgeführt wird. Wenn die angegebenen Bedingungen erfüllt sind, wird die Rückruffunktion von einem Arbeitsthread aus dem Threadpool ausgeführt.

Standardmäßig ist ein registrierter Wartevorgang ein Vorgang mit mehreren Wartezeichen. Das System setzt den Timer jedes Mal zurück, wenn das Ereignis signalisiert wird (oder das Time out-Intervall vergeht), bis Sie die [**UnregisterWaitEx-Funktion**](unregisterwaitex.md) aufrufen, um den Vorgang abzubrechen. Um anzugeben, dass ein Wartevorgang nur einmal ausgeführt werden soll, legen Sie den *dwFlags-Parameter* von [**RegisterWaitForSingleObject**](/windows/desktop/api/WinBase/nf-winbase-registerwaitforsingleobject) auf **WT \_ EXECUTEONLYONCE** fest.

Wenn der Thread Funktionen aufruft, die APCs verwenden, legen Sie den *dwFlags-Parameter* von [**RegisterWaitForSingleObject**](/windows/desktop/api/WinBase/nf-winbase-registerwaitforsingleobject) auf **WT \_ EXECUTEINPERSISTENTTHREAD** fest.

## <a name="waiting-on-an-address"></a>Warten auf eine Adresse

Ein Thread kann die [**WaitOnAddress-Funktion**](/windows/desktop/api/SynchAPI/nf-synchapi-waitonaddress) verwenden, um zu warten, bis der Wert einer Zieladresse von einem unerwünschten Wert in einen beliebigen anderen Wert geändert wird. Dadurch können Threads warten, bis sich ein Wert ändert, ohne die Synchronisierungsprobleme behandeln zu müssen, die auftreten können, wenn der Thread einen unerwünschten Wert erfasst, der Wert sich jedoch ändert, bevor der Thread warten kann.

[**WaitOnAddress**](/windows/desktop/api/SynchAPI/nf-synchapi-waitonaddress) gibt zurück, wenn Code, der den Zielwert ändert, die Änderung signalisiert, indem [**WakeByAddressSingle**](/windows/desktop/api/SynchAPI/nf-synchapi-wakebyaddresssingle) aufgerufen wird, um einen einzelnen wartenden Thread zu reaktivieren, oder [**WakeByAddressAll,**](/windows/desktop/api/SynchAPI/nf-synchapi-wakebyaddressall) um alle wartenden Threads zu reaktivieren. Wenn ein Time out-Intervall mit **WaitOnAddress** angegeben wird und kein Thread eine Aktivierungsfunktion aufruft, gibt die Funktion nach Ablauf des Time out-Intervalls zurück. Wenn kein Time out-Intervall angegeben ist, wartet der Thread unbegrenzt.

## <a name="wait-functions-and-time-out-intervals"></a>Wartefunktionen und Time out-Intervalle

Die Genauigkeit des angegebenen Time out-Intervalls hängt von der Auflösung der Systemuhr ab. Die Systemuhr "tickt" mit konstanter Geschwindigkeit. Wenn das Time out-Intervall kleiner als die Auflösung der Systemuhr ist, kann für die Wartezeit ein Time out in weniger als der angegebenen Zeitspanne auftreten. Wenn das Time out-Intervall größer als ein Tick, aber kleiner als zwei ist, kann die Wartezeit zwischen einem und zwei Ticks liegen usw.

Um die Genauigkeit des Time out-Intervalls für die Wartefunktionen zu erhöhen, rufen Sie die **timeGetDevCaps-Funktion** auf, um die unterstützte minimale Timerauflösung zu bestimmen, und die **timeBeginPeriod-Funktion,** um die Timerauflösung auf das Minimum festzulegen. Seien Sie vorsichtig, wenn **Sie timeBeginPeriod** aufrufen, da häufige Aufrufe die Systemuhr, die Auslastung des Systems und den Planer erheblich beeinträchtigen können. Wenn Sie **timeBeginPeriod** aufrufen, rufen Sie es einmal früh in der Anwendung auf, und achten Sie darauf, die **timeEndPeriod-Funktion** ganz am Ende der Anwendung aufzurufen.

## <a name="wait-functions-and-synchronization-objects"></a>Wait-Funktionen und Synchronisierungsobjekte

Die Wartefunktionen können die Zustände einiger Typen von [Synchronisierungsobjekten](synchronization-objects.md)ändern. Änderungen treten nur für das Objekt oder die Objekte auf, deren signalisierter Zustand die Rückgabe der Funktion verursacht hat. Wait-Funktionen können die Zustände von Synchronisierungsobjekten wie folgt ändern:

-   Die Anzahl eines Semaphorobjekts verringert sich um eins, und der Zustand des Semaphors wird auf nicht signalisiert festgelegt, wenn seine Anzahl 0 (null) ist.
-   Die Zustände von Mutex-, Auto-Reset-Ereignis- und Änderungsbenachrichtigungsobjekten werden auf nicht signalisiert festgelegt.
-   Der Status eines Synchronisierungszeitgebers ist auf nicht signalisiert festgelegt.
-   Die Zustände von manuell zurückgesetzten Ereignis-, Zeitgeber-, Prozess-, Thread- und Konsoleneingabeobjekten sind von einer Wartefunktion nicht betroffen.

## <a name="wait-functions-and-creating-windows"></a>Wait-Funktionen und Erstellen von Windows

Sie müssen vorsichtig sein, wenn Sie die Wartefunktionen und den Code verwenden, mit denen Fenster direkt oder indirekt erstellt werden. Wenn ein Thread Fenster erstellt, muss er Nachrichten verarbeiten. Nachrichtenübertragungen werden an alle Fenster im System gesendet. Wenn Sie über einen Thread verfügen, der eine Wartefunktion ohne Time out-Intervall verwendet, führt das System einen Deadlock aus. Zwei Beispiele für Code, der indirekt Fenster erstellt, sind DDE und die **CoInitialize-Funktion.** Wenn Sie über einen Thread verfügen, der Fenster erstellt, verwenden Sie daher [**MsgWaitForMultipleObjects**](/windows/desktop/api/Winuser/nf-winuser-msgwaitformultipleobjects) oder [**MsgWaitForMultipleObjectsEx**](/windows/desktop/api/Winuser/nf-winuser-msgwaitformultipleobjectsex)anstelle der anderen Wartefunktionen.

 

 
