---
description: Wait-Funktionen ermöglichen es einem Thread, seine eigene Ausführung zu blockieren.
ms.assetid: 9c66c71d-fdfd-42ae-895c-2fc842b5bc7a
title: Wait-Funktionen
ms.topic: article
ms.date: 06/25/2020
ms.openlocfilehash: f5a21b0d95a316b926fcaad037004edc8c418246
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350809"
---
# <a name="wait-functions"></a>Wait-Funktionen

*Wait-Funktionen* ermöglichen es einem Thread, seine eigene Ausführung zu blockieren. Die Wait-Funktionen werden erst zurückgegeben, wenn die angegebenen Kriterien erfüllt wurden. Der Typ der wait-Funktion bestimmt den verwendeten Satz von Kriterien. Wenn eine wait-Funktion aufgerufen wird, überprüft Sie, ob die Warte Kriterien erfüllt wurden. Wenn die Kriterien nicht erfüllt sind, wechselt der aufrufende Thread in den Wartezustand, bis die Bedingungen der Warte Kriterien erfüllt sind oder das angegebene Timeout Intervall abläuft.

-   [Einzelobjektwait-Funktionen](#single-object-wait-functions)
-   [Wait-Funktionen mit mehreren Objekten](#multiple-object-wait-functions)
-   [Wartende Wartefunktionen](#alertable-wait-functions)
-   [Registrierte Wait-Funktionen](#registered-wait-functions)
-   [Warten auf eine Adresse](#waiting-on-an-address)
-   [Warte Funktionen und Timeout Intervalle](#wait-functions-and-time-out-intervals)
-   [Wait-Funktionen und Synchronisierungs Objekte](#wait-functions-and-synchronization-objects)
-   [Wait-Funktionen und Erstellen von Fenstern](#wait-functions-and-creating-windows)

## <a name="single-object-wait-functions"></a>Einzelobjektwait-Funktionen

Die Funktionen " [**signalobjectandwait**](/windows/win32/api/synchapi/nf-synchapi-signalobjectandwait)", " [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject)" und " [**WaitForSingleObjectEx**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex) " erfordern ein Handle für ein Synchronisierungs Objekt. Diese Funktionen geben zurück, wenn eine der folgenden Aktionen auftritt:

-   Das angegebene-Objekt befindet sich im signalisierten Zustand.
-   Das Timeout Intervall ist abgelaufen. Das Timeout Intervall kann auf **unendlich** festgelegt werden, um anzugeben, dass für den warte Vorgang kein Timeout auftritt.

Die [**signalobjectandwait**](/windows/win32/api/synchapi/nf-synchapi-signalobjectandwait) -Funktion ermöglicht es dem aufrufenden Thread, den Zustand eines Objekts atomisch auf "signalisiert" festzulegen und zu warten, bis der Zustand eines anderen Objekts auf "signalisiert" festgelegt ist.

## <a name="multiple-object-wait-functions"></a>Wait-Funktionen mit mehreren Objekten

Die Funktionen [**WaitForMultipleObjects**](/windows/win32/api/synchapi/nf-synchapi-waitformultipleobjects), [**WaitForMultipleObjectsEx**](/windows/win32/api/synchapi/nf-synchapi-waitformultipleobjectsex), [**MsgWaitForMultipleObjects**](/windows/desktop/api/Winuser/nf-winuser-msgwaitformultipleobjects)und [**MsgWaitForMultipleObjectsEx**](/windows/desktop/api/Winuser/nf-winuser-msgwaitformultipleobjectsex) ermöglichen es dem aufrufenden Thread, ein Array anzugeben, das mindestens ein Synchronisierungs Objekt Handle enthält. Diese Funktionen geben zurück, wenn eine der folgenden Aktionen auftritt:

-   Der Status eines der angegebenen-Objekte ist auf "signalisiert" festgelegt, oder die Zustände aller Objekte wurden auf "signalisiert" festgelegt. Sie steuern, ob ein oder alle Zustände im Funktions aufrufsbefehl verwendet werden.
-   Das Timeout Intervall ist abgelaufen. Das Timeout Intervall kann auf **unendlich** festgelegt werden, um anzugeben, dass für den warte Vorgang kein Timeout auftritt.

Mit der [**MsgWaitForMultipleObjects**](/windows/desktop/api/Winuser/nf-winuser-msgwaitformultipleobjects) -und der [**MsgWaitForMultipleObjectsEx**](/windows/desktop/api/Winuser/nf-winuser-msgwaitformultipleobjectsex) -Funktion können Sie Eingabe Ereignis Objekte im Objekt Handle-Array angeben. Dies geschieht, wenn Sie den Typ der Eingabe angeben, auf die in der Eingabe Warteschlange des Threads gewartet werden soll. Ein Thread kann z. b. **MsgWaitForMultipleObjects** verwenden, um die Ausführung zu blockieren, bis der Zustand eines angegebenen Objekts auf "signalisiert" festgelegt wurde und die Maus Eingaben in der Eingabe Warteschlange des Threads verfügbar sind. Der Thread kann die [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) -Funktion oder die [**peekmessagea**](/windows/win32/api/winuser/nf-winuser-peekmessagea) -oder [**peekmessagew**](/windows/win32/api/winuser/nf-winuser-peekmessagew) -Funktion verwenden, um die Eingabe abzurufen.

Wenn Sie darauf warten, dass der Status aller Objekte auf "signalisiert" festgelegt wird, ändern diese Funktionen mit mehreren Objekten die Zustände der angegebenen Objekte erst, wenn die Zustände aller Objekte als signalisiert festgelegt wurden. Beispielsweise kann der Status eines Mutex-Objekts signalisiert werden, aber der aufrufende Thread erhält erst dann den Besitz, wenn die Zustände der anderen im Array angegebenen Objekte ebenfalls auf "signalisiert" festgelegt wurden. In der Zwischenzeit kann ein anderer Thread in den Besitz des Mutex-Objekts gelangen und somit seinen Zustand auf "nicht signalisiert" festlegen.

Wenn Sie darauf warten, dass der Status eines einzelnen Objekts auf "signalisiert" festgelegt wird, überprüfen diese Funktionen mit mehreren Objekten die Handles im Array, damit Sie mit Index 0 beginnen, bis eines der Objekte signalisiert wird. Wenn mehrere Objekte signalisiert werden, gibt die Funktion den Index des ersten Handles im Array zurück, dessen Objekt signalisiert wurde.

## <a name="alertable-wait-functions"></a>Wartende Wartefunktionen

Die Funktionen " [**MsgWaitForMultipleObjectsEx**](/windows/desktop/api/Winuser/nf-winuser-msgwaitformultipleobjectsex)", " [**signalobjectandwait**](/windows/win32/api/synchapi/nf-synchapi-signalobjectandwait)", " [**WaitForMultipleObjectsEx**](/windows/win32/api/synchapi/nf-synchapi-waitformultipleobjectsex)" und " [**WaitForSingleObjectEx**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex) " unterscheiden sich von den anderen warte Funktionen darin, dass Sie optional einen Warn *baren warte Vorgang* ausführen können. Bei einem Warteschlangen-Wait-Vorgang kann die Funktion zurückgeben, wenn die angegebenen Bedingungen erfüllt sind, aber Sie kann auch zurückgeben, wenn das System eine e/a-Abschluss Routine oder eine APC zur Ausführung durch den wartenden Thread in die Warteschlange eingereiht. Weitere Informationen zu Warn baren warte Vorgängen und e/a-Abschluss Routinen finden Sie unter [Synchronisierung und überlappende Eingabe und Ausgabe](synchronization-and-overlapped-input-and-output.md). Weitere Informationen zu APCs finden Sie unter [asynchrone Prozedur Aufrufe](asynchronous-procedure-calls.md).

## <a name="registered-wait-functions"></a>Registrierte Wait-Funktionen

Die [**RegisterWaitForSingleObject**](/windows/desktop/api/WinBase/nf-winbase-registerwaitforsingleobject) -Funktion unterscheidet sich von den anderen Wait-Funktionen darin, dass der Warte Vorgang von einem Thread aus dem [Thread Pool](../procthread/thread-pooling.md)ausgeführt wird. Wenn die angegebenen Bedingungen erfüllt sind, wird die Rückruffunktion von einem Arbeits Thread aus dem Thread Pool ausgeführt.

Standardmäßig ist ein registrierter warte Vorgang ein Vorgang mit mehreren warte Vorgängen. Das System setzt den Timer jedes Mal zurück, wenn das Ereignis signalisiert wird (oder das Timeout Intervall abläuft), bis Sie die [**unregisterwaitex**](unregisterwaitex.md) -Funktion aufrufen, um den Vorgang abzubrechen. Um anzugeben, dass ein warte Vorgang nur einmal ausgeführt werden soll, legen Sie den *dwFlags* -Parameter von [**RegisterWaitForSingleObject**](/windows/desktop/api/WinBase/nf-winbase-registerwaitforsingleobject) auf **WT \_ executeOnlyOnce** fest.

Wenn der Thread Funktionen aufruft, die APCs verwenden, legen Sie den *dwFlags* -Parameter von [**RegisterWaitForSingleObject**](/windows/desktop/api/WinBase/nf-winbase-registerwaitforsingleobject) auf **WT \_ executeinpersistentthread** fest.

## <a name="waiting-on-an-address"></a>Warten auf eine Adresse

Ein Thread kann die [**waitonaddress**](/windows/desktop/api/SynchAPI/nf-synchapi-waitonaddress) -Funktion verwenden, um zu warten, bis der Wert einer Zieladresse von einem unerwünschten Wert in einen anderen Wert geändert wird. Dadurch können Threads darauf warten, dass ein Wert geändert wird, ohne dass Sie die Synchronisierungs Probleme, die auftreten können, wenn der Thread einen unerwünschten Wert erfasst, beenden oder behandeln müssen. der Wert ändert sich jedoch, bevor der Thread warten kann.

[**Waitonaddress**](/windows/desktop/api/SynchAPI/nf-synchapi-waitonaddress) gibt zurück, wenn Code, durch den der Zielwert geändert wird, durch Aufrufen von [**wakebyaddresssingle**](/windows/desktop/api/SynchAPI/nf-synchapi-wakebyaddresssingle) zum Aktivieren eines einzelnen wartenden Threads oder von [**wakebyaddressall**](/windows/desktop/api/SynchAPI/nf-synchapi-wakebyaddressall) zum Aktivieren aller wartenden Threads signalisiert wird. Wenn ein Timeout Intervall mit **waitonaddress** angegeben wird und kein Thread eine Wake-Funktion aufruft, gibt die Funktion zurück, wenn das Timeout Intervall abläuft. Wenn kein Timeout Intervall angegeben ist, wartet der Thread unbegrenzt.

## <a name="wait-functions-and-time-out-intervals"></a>Warte Funktionen und Timeout Intervalle

Die Genauigkeit des angegebenen Timeout Intervalls hängt von der Auflösung der Systemuhr ab. Die Systemuhr wird mit konstanter Geschwindigkeit "Ticks". Wenn das Timeout Intervall kleiner als die Auflösung der Systemuhr ist, kann der Warte Vorgang in weniger als dem angegebenen Zeitraum einen Timeout haben. Wenn das Timeout Intervall größer als ein Tick, aber kleiner als 2 ist, kann der Warte Vorgang zwischen einem und zwei Ticks usw. liegen.

Um die Genauigkeit des Timeout Intervalls für die Wait-Funktionen zu erhöhen, müssen Sie die **timegetdevcaps** -Funktion aufrufen, um die unterstützte minimale Zeit Geber Auflösung und die **TimeBeginPeriod** -Funktion zu bestimmen, um die Zeit Geber Auflösung auf Ihren Minimalwert festzulegen. Gehen Sie beim Aufrufen von **TimeBeginPeriod** vorsichtig vor, da häufige Aufrufe die Systemuhr, den System Energieverbrauch und den Scheduler erheblich beeinflussen können. Wenn Sie **TimeBeginPeriod** aufrufen, nennen Sie es einmal in der Anwendung, und stellen Sie sicher, dass Sie die **timeendperiod** -Funktion am Ende der Anwendung aufrufen.

## <a name="wait-functions-and-synchronization-objects"></a>Wait-Funktionen und Synchronisierungs Objekte

Die Wait-Funktionen können die Zustände einiger Typen von [Synchronisierungs Objekten](synchronization-objects.md)ändern. Die Änderung erfolgt nur für Objekte oder Objekte, deren signalisierter Zustand bewirkt hat, dass die Funktion zurückgegeben wurde. Wait-Funktionen können die Zustände von Synchronisierungs Objekten wie folgt ändern:

-   Die Anzahl eines Semaphor-Objekts wird um eins verringert, und der Zustand des Semaphors wird auf "nicht signalisiert" festgelegt, wenn die Anzahl 0 (null) ist.
-   Die Zustände von Mutex, Auto-Reset-Ereignis und Änderungs Benachrichtigungsobjekten werden auf nicht signalisiert festgelegt.
-   Der Status eines Synchronisierungs Zeit Gebers ist auf "nicht signalisiert" festgelegt.
-   Die Zustände von manuellen Zurücksetzungs Ereignissen, Zeit Geber-, Prozess-, Thread-und Konsolen Eingabe Objekten sind von einer wait-Funktion nicht betroffen.

## <a name="wait-functions-and-creating-windows"></a>Wait-Funktionen und Erstellen von Fenstern

Sie müssen vorsichtig sein, wenn Sie die Wait-Funktionen und den Code verwenden, der direkt oder indirekt Windows erstellt. Wenn ein Thread Windows erstellt, muss er Nachrichten verarbeiten. Nachrichten Übertragungen werden an alle Fenster im System gesendet. Wenn Sie einen Thread haben, der eine wait-Funktion ohne Timeout Intervall verwendet, wird das System in einen Deadlock geraten. Zwei Beispiele für Code, der indirekt Windows erstellt, sind DDE und die **CoInitialize** -Funktion. Wenn Sie also über einen Thread verfügen, der Windows erstellt, verwenden Sie [**MsgWaitForMultipleObjects**](/windows/desktop/api/Winuser/nf-winuser-msgwaitformultipleobjects) oder [**MsgWaitForMultipleObjectsEx**](/windows/desktop/api/Winuser/nf-winuser-msgwaitformultipleobjectsex)anstelle der anderen Wait-Funktionen.

 

 
