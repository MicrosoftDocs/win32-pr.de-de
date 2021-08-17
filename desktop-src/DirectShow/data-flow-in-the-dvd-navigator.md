---
description: Daten Flow im DVD-Navigator
ms.assetid: 14f9cfa3-5ef6-419c-9196-2e4060549c03
title: Daten Flow im DVD-Navigator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56e649edfacf0a1fad56cfbe8e73a5e1e9aaf099b9c17463858bf776ab06605c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953359"
---
# <a name="data-flow-in-the-dvd-navigator"></a>Daten Flow im DVD-Navigator

Der DVD-Navigator verfügt über Methoden zum Beenden und Anhalten der Wiedergabe. Diese Methoden ähneln – aber nicht identisch – den **Stop-** und **Pause-Methoden** in [**IMediaControl.**](/windows/desktop/api/Control/nn-control-imediacontrol) Dies ist der Unterschied zwischen ihnen:

-   Die **IDvdControl2-Methoden** ändern, was der DVD-Navigator vom Datenträger liest. Sie ändern den Zustand des Graphen nicht.
-   Die **IMediaControl-Methoden** ändern den Zustand des Graphen. Sie ändern nicht, was der DVD-Navigator vom Datenträger liest. (Es gibt eine wichtige Ausnahme, die im nächsten Abschnitt im Zusammenhang mit der **Stop-Methode erläutert** wird.)

Beispielsweise gibt die [**IDvdControl2::P ause-Methode**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-pause) den Befehl "Pause On" in Anhang J aus, hält das Filterdiagramm \_ jedoch nicht an. Die [**IMediaControl::P ause-Methode**](/windows/desktop/api/Control/nf-control-imediacontrol-pause) hält dagegen das Diagramm an, gibt jedoch keinen DVD-Befehl aus.

Verwenden Sie im Allgemeinen die **Methoden IMediaControl::P ause** und **Stop** anstelle der entsprechenden **IDvdControl2-Methoden.** Die **IMediaControl-Methoden** haben sehr geringe Latenzen, während die **IDvdControl2-Methoden** bis zu zwei Sekunden Wartezeit haben können.

Beenden der Wiedergabe

Das Verhalten von [**IMediaControl::Stop hängt**](/windows/desktop/api/Control/nf-control-imediacontrol-stop) von einem Flag ab, das Sie mit der [**IDvdControl2::SetOption-Methode festlegen**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) können.

-   Wenn das ResetOnStop-Flag der DVD \_ **FALSE** ist, beendet **IMediaControl::Stop** das Diagramm, ändert jedoch nicht die Domäne des DVD-Navigators. Wenn Sie run erneut aufrufen, wird die Wiedergabe von der aktuellen Position aus fortgesetzt.
-   Wenn DVD \_ ResetOnStop **true ist,** bewirkt **IMediaControl::Stop,** dass der DVD-Navigator zurückgesetzt wird. Wenn Sie [**IMediaControl::Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) erneut aufrufen, wird der DVD-Navigator aus der Domäne "Erste Wiedergabe" wiedergerufen, als ob Sie die DVD zum ersten Mal einfügen würden.

Das Dvd \_ ResetOnStop-Flag ist **aus Kompatibilitäts-** und Kompatibilitätseinstellungen mit älteren Anwendungen standardmäßig TRUE. Im Allgemeinen sollten Sie jedoch den Standardwert überschreiben und das Flag auf **FALSE festlegen.** Der Grund dafür ist, dass bestimmte Ereignisse dazu führen können, dass das Diagramm während der Wiedergabe stoppt. Wenn sich beispielsweise die Auflösung der Anzeige ändert, wird das Filterdiagramm beendet, der Videorenderer erneut verbunden und neu gestartet. Wenn DVD \_ ResetOnStop **true ist,** wird die Wiedergabe vom Anfang des Datenträgers neu gestartet. Dies ist wahrscheinlich nicht das, was der Benutzer erwartet.

Rufen Sie daher am Anfang ihrer Anwendung **SetOption** auf, und legen Sie DVD \_ ResetOnStop auf **FALSE fest.** Wenn Sie die Wiedergabe beenden und von demselben Speicherort fortsetzen möchten, rufen Sie **IMediaControl::Stop** oder **IMediaControl::P ause auf.** Wenn Sie die Wiedergabe beenden und den Datenträger zurücksetzen möchten, rufen Sie **SetOption** mit DVD ResetOnStop gleich TRUE auf. Rufen Sie \_ dann **IMediaControl::Stop** auf. Rufen Sie schließlich **setOption** erneut auf, und setzen Sie DVD  \_ ResetOnStop auf FALSE **zurück.**

Anhalten der Wiedergabe

Wenn Sie dem DVD-Navigator einen Befehl geben, während das Diagramm angehalten ist, wird der Befehl möglicherweise erst abgeschlossen, wenn das Diagramm erneut ausgeführt wird. In einigen Situationen kann dies zu einem Deadlock in Ihrer Anwendung führen. Es gibt zwei Regeln, die Sie befolgen sollten, um Deadlocks zu vermeiden:

-   Geben Sie während der Pause nicht mehr als einen asynchronen DVD-Befehl aus.
-   Blockieren Sie während der Pause nicht den Ui-Thread der Anwendung oder den Thread, der den Zustand des Graphen ändert.

Die zweite Regel ist eine ausführlichere Untersuchung. Im Folgenden finden Sie einige spezifische Szenarien, die zu einem Deadlock führen können:

-   **Szenario:** Während der Unterbrechung gibt die Anwendung einen DVD-Befehl mit dem Blockierungsflag aus. Dies kann zu einem Deadlock führen, wenn der Thread, der den DVD-Befehl aus gibt, derselbe Thread ist, der den Ausführungsbefehl aus gibt. Der DVD-Befehl wird blockiert, bis das Diagramm ausgeführt wird, aber das Diagramm kann erst ausgeführt werden, wenn der Befehl abgeschlossen ist.

    **Empfehlung:** Geben Sie den DVD-Befehl in einem separaten Arbeitsthread aus, oder verwenden Sie nicht das Blockierungsflag.

-   **Szenario:** Während der Pause gibt die Anwendung einen DVD-Befehl aus und ruft [**dann IDvdCmd::WaitForEnd**](/windows/desktop/api/Strmif/nf-strmif-idvdcmd-waitforend) für das Befehlsobjekt auf. Diese Situation entspricht dem vorherigen Beispiel. Wenn Sie **Wait über** den UI-Thread aufrufen, kann der UI-Thread das Diagramm erst ausführen, wenn die Blockierung durch die **Wait-Methode** aufgehoben wird, aber die **Wait-Methode** entsperrt die Blockierung erst, wenn das Diagramm ausgeführt wird.

    **Empfehlung:** Rufen Sie **Wait** für einen Arbeitsthread auf.

-   **Szenario:** Während das Diagramm ausgeführt wird, gibt die Anwendung einen DVD-Befehl mit dem Blockierungsflag aus und ruft dann pause von einem anderen Thread aus auf. Dies ist eine mögliche Racebedingung, da das Diagramm möglicherweise angehalten wird, bevor der Befehl ausgegeben wird. Wenn einer der beiden Threads der UI-Thread ist, können Sie ähnlich wie in den beiden vorherigen Beispielen einen Deadlock verursachen. In diesem Beispiel wird veranschaulicht, wie wichtig das Schreiben von threadsicherem Code ist, wenn Ihre Anwendung mehrere Threads verwendet.

    **Empfehlung:** Wenn Sie Arbeitsthreads verwenden, stellen Sie sicher, dass Ihr Code threadsicher ist.

-   **Szenario:** Während der Pause deaktiviert die Anwendung den Befehl run über die Benutzeroberfläche und gibt dann einen asynchronen DVD-Befehl aus. Dieser Fall ist kein Deadlock, da der Anwendungsthread noch ausgeführt wird. Allerdings wird der Benutzer jetzt daran gehindert, den Graphen auszuführen, und daher wird der Befehl nie abgeschlossen.

    **Empfehlung:** Lassen Sie beim Anhalten immer den Befehl run aktiviert.

Suchen einer DVD zu einem angegebenen Zeitpunkt

Rufen Sie [**IMediaControl::Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run)auf, um genau zu einer bestimmten Zeit auf einem Datenträger zu suchen. Rufen Sie [**dann IDvdControl2::P layAtTime**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playattime)auf, geben Sie die Uhrzeit an, und legen Sie *dwFlags* auf DVD \_ CMD FLAG Flush \_ \_ fest.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DVD-Anwendungen](dvd-applications.md)
</dt> </dl>

 

 



