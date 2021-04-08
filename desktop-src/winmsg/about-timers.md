---
description: In diesem Thema wird beschrieben, wie Timer erstellt, identifiziert, festgelegt und gelöscht werden.
ms.assetid: 509a6fc4-ddee-4ff4-88a2-25dad4c48c2f
title: Informationen zu Timern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3163dbfd5357de516e0202665cd76d017335593
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960851"
---
# <a name="about-timers"></a>Informationen zu Timern

In diesem Thema wird beschrieben, wie Timer erstellt, identifiziert, festgelegt und gelöscht werden. Eine Anwendung verwendet einen Timer, um ein Ereignis für ein Fenster zu planen, nachdem eine angegebene Zeit abgelaufen ist. Jedes Mal, wenn das angegebene Intervall (oder Timeout Wert) für einen Timer abläuft, benachrichtigt das System das Fenster, das dem Timer zugeordnet ist. Da die Genauigkeit eines Timers von der systemtaktrate abhängig ist und die Häufigkeit, mit der die Anwendung Nachrichten aus der Nachrichten Warteschlange abruft, ist der Timeout Wert nur annähernd.

Das Thema enthält folgende Abschnitte:

-   [Timer-Vorgänge](#timer-operations)
-   [Zeitgeber mit hoher Auflösung](#high-resolution-timer)
-   [Wanutzbare Zeit Geber Objekte](#waitable-timer-objects)
-   [Zugehörige Themen](#related-topics)

## <a name="timer-operations"></a>Timer-Vorgänge

Anwendungen erstellen Timer [**mithilfe der Funktion**](/windows/win32/api/winuser/nf-winuser-settimer) "Funktion". Ein neuer Timer beginnt mit der zeitlichen Steuerung des Intervalls, sobald es erstellt wird. Eine Anwendung kann den Timeout Wert eines Timers mithilfe von **SETTIMER** ändern und einen Timer mithilfe der [**killtimer**](/windows/win32/api/winuser/nf-winuser-killtimer) -Funktion zerstören. Um Systemressourcen effizient zu verwenden, sollten Anwendungen nicht mehr benötigte Timer zerstören.

Jeder Timer verfügt über einen eindeutigen Bezeichner. Beim Erstellen eines Timers kann eine Anwendung entweder einen Bezeichner angeben oder festlegen, dass das System einen eindeutigen Wert erstellt. Der erste Parameter einer [**WM- \_**](wm-timer.md) Zeit Geber Nachricht enthält den Bezeichner des Timers, der die Nachricht gepostet hat.

Wenn Sie im aufzurufenden [**SETTIMER**](/windows/win32/api/winuser/nf-winuser-settimer)-Befehl ein Fenster Handle angeben, ordnet die Anwendung den Timer diesem Fenster zu. Jedes Mal, wenn der Timeout Wert für den Timer abläuft, stellt das System eine [**WM \_**](wm-timer.md) -Zeit Geber Meldung an das Fenster, das dem Timer zugeordnet ist. Wenn im aufzurufenden **SETTIMER**-Befehl kein Fenster handle angegeben ist, muss die Anwendung, die den Timer erstellt hat, die Meldungs Warteschlange für die Zeit Geber Nachrichten der **\_ WM** überwachen und Sie an das entsprechende Fenster verteilen Wenn Sie eine [**timerproc**](/windows/win32/api/winuser/nc-winuser-timerproc) -Rückruffunktion angeben, ruft die Standardfenster Prozedur die Rückruffunktion auf, wenn Sie den **WM- \_ Timer** verarbeitet. Daher müssen Sie Nachrichten in den aufrufenden Thread verteilen, auch wenn Sie **timerproc** anstelle der Verarbeitung des **WM- \_ Timers** verwenden.

Wenn Sie benachrichtigt werden müssen, wenn ein Timer abläuft, verwenden Sie einen aktivierbaren Timer. Weitere Informationen finden Sie unter [wanutzbare Timer-Objekte](/windows/desktop/Sync/waitable-timer-objects).

## <a name="high-resolution-timer"></a>High-Resolution Timer

Ein-Wert ist ein allgemeiner Begriff, der beim Programmieren verwendet wird, um auf eine inkrementvariable zu verweisen Einige Systeme beinhalten einen hochleistungsfähigen Leistungs Bewert, der eine zeitintensive Zeitspanne mit hoher Auflösung bereitstellt.

Wenn ein Leistungsindikatoren mit hoher Auflösung auf dem System vorhanden ist, können Sie die [**QueryPerformanceFrequency**](/windows/desktop/api/profileapi/nf-profileapi-queryperformancefrequency) -Funktion verwenden, um die Häufigkeit in Zählungen pro Sekunde auszudrücken. Der Wert der Anzahl ist Prozessor abhängig. Bei einigen Prozessoren kann die Anzahl z. b. die Taktrate der Prozessoruhr sein.

Die [**QueryPerformanceCounter**](/windows/desktop/api/profileapi/nf-profileapi-queryperformancecounter) -Funktion Ruft den aktuellen Wert des Leistungs Zählers mit hoher Auflösung ab. Wenn diese Funktion am Anfang und Ende eines Code Abschnitts aufgerufen wird, verwendet eine Anwendung den Zähler im Wesentlichen als Zeit Geber mit hoher Auflösung. Nehmen Sie beispielsweise an, dass [**QueryPerformanceFrequency**](/windows/desktop/api/profileapi/nf-profileapi-queryperformancefrequency) angibt, dass die Häufigkeit des Leistungs Zählers für hohe Auflösung 50.000 Zähler pro Sekunde ist. Wenn die Anwendung **QueryPerformanceCounter** unmittelbar vor und unmittelbar nach dem zu überprüfenden Code Abschnitt aufruft, können die Zählerwerte 1500 Zähler bzw. 3500 Zähler sein. Diese Werte geben an, dass .04 Sekunden (2000 Zählungen) während der Ausführung des Codes verstrichen sind.

## <a name="waitable-timer-objects"></a>Wanutzbare Zeit Geber Objekte

Ein wanutzbares Zeit Geber Objekt ist ein Synchronisierungs Objekt, dessen Zustand auf signalisiert festgelegt wird, wenn die angegebene Fälligkeits Zeit erreicht wird. Es gibt zwei Typen von aufnutzbaren Timern, die erstellt werden können: manuelles Zurücksetzen und synchronisieren. Ein Timer eines der beiden Typen kann auch ein periodischer Timer sein.

Ein Thread verwendet die Funktion " [**foratewaitabletimer**](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerw) " oder " [**foratewaitabletimerex**](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerexw) ", um ein Zeit Geber Objekt zu erstellen. Der Erstellungsthread gibt an, ob es sich um einen Zeit Geber oder einen Synchronisierungs Zeit Geber handelt. Der Erstellungsthread kann einen Namen für das Timer-Objekt angeben. Threads in anderen Prozessen können ein Handle für einen vorhandenen Timer öffnen, indem Sie den Namen in einem Aufrufen der [**openwaitabletimer**](/windows/win32/api/synchapi/nf-synchapi-openwaitabletimerw) -Funktion angeben. Jeder Thread mit einem Handle für ein Timer-Objekt kann eine der Wait-Funktionen verwenden, um zu warten, bis der Zeit Geber Zustand auf "signalisiert" festgelegt ist.

Weitere Informationen zur Verwendung von ausnutzbaren Zeit Geber Objekten für die Thread Synchronisierung finden Sie unter [wanutzbare](/windows/desktop/Sync/waitable-timer-objects)Zeit Geber Objekte.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Timern](using-timers.md)
</dt> </dl>

 

 
