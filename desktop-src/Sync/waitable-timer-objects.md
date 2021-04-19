---
description: Ein wanutzbares Zeit Geber Objekt ist ein Synchronisierungs Objekt, dessen Zustand auf signalisiert festgelegt wird, wenn die angegebene Fälligkeits Zeit erreicht wird.
ms.assetid: 5d39ada0-ea31-40d7-b075-aeb657ee508c
title: Wanutzbare Zeit Geber Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b9597617705fcd78bb71f63e33a475e3bca78e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349598"
---
# <a name="waitable-timer-objects"></a>Wanutzbare Zeit Geber Objekte

Ein *wanutzbares* Zeit Geber Objekt ist ein Synchronisierungs Objekt, dessen Zustand auf signalisiert festgelegt wird, wenn die angegebene Fälligkeits Zeit erreicht wird. Es gibt zwei Typen von aufnutzbaren Timern, die erstellt werden können: manuelles Zurücksetzen und synchronisieren. Ein Timer eines der beiden Typen kann auch ein periodischer Timer sein.



| Object                | BESCHREIBUNG                                                                                                                                                                                             |
|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Timer für manuelles Zurücksetzen    | Ein Timer, dessen Zustand signalisiert bleibt, bis [**setwaitabletimer**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer) aufgerufen wird, um eine neue Fälligkeits Zeit festzulegen.                                                                          |
| Synchronisierungs Zeit Geber | Ein Timer, dessen Zustand signalisiert bleibt, bis ein Thread einen Warte Vorgang für das Timer-Objekt abschließt.                                                                                                     |
| periodischer Timer        | Ein Timer, der jedes Mal erneut aktiviert wird, wenn der angegebene Zeitraum abläuft, bis der Timer zurückgesetzt oder abgebrochen wird. Ein periodischer Timer ist entweder ein periodischer Zeit Geber für manuelles Zurücksetzen oder ein periodischer Synchronisierungs Zeit Geber |



 

> [!Note]  
> Wenn ein Timer signalisiert wird, muss der Prozessor ausgeführt werden, um die zugehörigen Anweisungen zu verarbeiten. Regelmäßige periodische Timer sorgen dafür, dass der Prozessor ständig ausgelastet ist, sodass das System für eine sinnvolle Zeitspanne nicht in einem niedrigeren [Energiezustand](../power/system-power-states.md) verbleiben kann. Dies kann sich negativ auf die Akku Lebensdauer tragbarer Computer und auf Szenarien auswirken, die von einer effektiven Energie Verwaltung, z. b. großen Rechenzentren, abhängen. Um die Energieeffizienz zu erhöhen, sollten Sie Ereignisbasierte Benachrichtigungen anstelle von zeitbasierten Benachrichtigungen in der Anwendung verwenden. Wenn ein Timer erforderlich ist, verwenden Sie einen Timer, der einmal anstelle eines periodischen Timers signalisiert wird, oder legen Sie das Intervall auf einen Wert fest, der größer als eine Sekunde ist.

 

Ein Thread verwendet die Funktion " [**foratewaitabletimer**](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerw) " oder " [**foratewaitabletimerex**](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerexw) ", um ein Zeit Geber Objekt zu erstellen. Der Erstellungsthread gibt an, ob es sich um einen Zeit Geber oder einen Synchronisierungs Zeit Geber handelt. Der Erstellungsthread kann einen Namen für das Timer-Objekt angeben. Threads in anderen Prozessen können ein Handle für einen vorhandenen Timer öffnen, indem Sie den Namen in einem Aufrufen der [**openwaitabletimer**](/windows/win32/api/synchapi/nf-synchapi-openwaitabletimerw) -Funktion angeben. Jeder Thread mit einem Handle für ein Timer-Objekt kann eine der [Wait-Funktionen](wait-functions.md) verwenden, um zu warten, bis der Zeit Geber Zustand auf "signalisiert" festgelegt ist.

-   Der Thread ruft die [**setwaitabletimer**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer) -Funktion auf, um den Timer zu aktivieren. Beachten Sie die Verwendung der folgenden Parameter für " **setwaitabletimer**":
-   Verwenden Sie den *lpduetime* -Parameter, um den Zeitpunkt anzugeben, zu dem der Timer auf den signalisierten Zustand festgelegt werden soll. Wenn ein Timer für manuelles Zurücksetzen auf den signalisierten Zustand festgelegt wird, verbleibt er in diesem Status, bis " [**setwaitabletimer**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer) " eine neue Fälligkeits Zeit festlegt. Wenn ein Synchronisierungs Zeit Geber auf den signalisierten Zustand festgelegt ist, verbleibt er in diesem Status, bis ein Thread einen Warte Vorgang für das Timer-Objekt abschließt.
-   Verwenden Sie den *lperiod* -Parameter der [**setwaitabletimer**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer) -Funktion, um den Zeit Geber Zeitraum anzugeben. Wenn der Zeitraum nicht 0 (null) ist, ist der Timer ein periodischer Timer. Sie wird jedes Mal erneut aktiviert, wenn der Zeitraum abläuft, bis der Timer zurückgesetzt oder abgebrochen wird. Wenn der Punkt 0 (null) ist, ist der Timer kein periodischer Timer. Es wird einmal signalisiert und anschließend deaktiviert.

Ein Thread kann die [**cancelwaitabletimer**](/windows/win32/api/synchapi/nf-synchapi-cancelwaitabletimer) -Funktion verwenden, um den Timer auf den inaktiven Zustand festzulegen. Um den Timer zurückzusetzen, nennen Sie [**setwaitabletimer**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer). Wenn Sie mit dem Timer-Objekt fertig sind, wird [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle) aufgerufen, um das Handle für das Timer-Objekt zu schließen.

Das Verhalten eines wanutzbaren Timers kann wie folgt zusammengefasst werden:

-   Wenn ein Timer festgelegt ist, wird er abgebrochen, wenn er bereits aktiv war, der Zustand des Timers nicht signalisiert wurde und der Timer in der Zeit Geber Warteschlange des Kernels platziert wird.
-   Wenn ein Timer abläuft, wird der Zeitgeber auf den signalisierten Zustand festgelegt. Wenn der Timer über eine Abschluss Routine verfügt, wird er in die Warteschlange des Threads eingereiht, der den Timer festgelegt hat. Die Abschluss Routine verbleibt in der APC-Warteschlange ( [asynchronen Procedure aufrufen](asynchronous-procedure-calls.md) ) des Threads, bis der Thread in einen warteschlangenwarteschlangenzustand wechselt. Zu diesem Zeitpunkt wird das APC versendet und die Abschluss Routine aufgerufen. Wenn der Timer periodisch ist, wird er wieder in der Kernelzeitgeber-Warteschlange abgelegt.
-   Wenn ein Timer abgebrochen wird, wird er aus der Kernelzeit Geber Warteschlange entfernt, wenn er aussteht. Wenn der Timer abgelaufen ist und noch ein APC in der Warteschlange für den Thread vorhanden ist, der den Timer festgelegt hat, wird das APC aus der APC-Warteschlange des Threads entfernt. Der signalisierten Zustand des Timers ist nicht betroffen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Asynchrone Prozedur Aufrufe](asynchronous-procedure-calls.md)
</dt> <dt>

[Verwenden von wanutzbaren Timer-Objekten](using-waitable-timer-objects.md)
</dt> </dl>

 

 
