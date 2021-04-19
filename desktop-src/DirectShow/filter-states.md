---
description: Filter Zustände
ms.assetid: 97418307-eb50-4c8e-b03b-a2cd08139bdc
title: Filter Zustände
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d61f66e1446d97d289f7e489f116f747f339d9a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106343142"
---
# <a name="filter-states"></a>Filter Zustände

Filter haben drei mögliche Zustände: "beendet", "angehalten" und "wird ausgeführt". Der Zweck des angehaltenen Zustands besteht darin, Daten im Diagramm zu finden, sodass ein Run-Befehl sofort antwortet. Der Filter Graph-Manager steuert alle Zustandsübergänge. Wenn eine Anwendung [**IMediaControl:: Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run), [**IMediaControl::P ause**](/windows/desktop/api/Control/nf-control-imediacontrol-pause)oder [**IMediaControl:: beenden**](/windows/desktop/api/Control/nf-control-imediacontrol-stop)aufruft, ruft der Filter Graph-Manager die entsprechende [**imediafilter**](/windows/desktop/api/Strmif/nn-strmif-imediafilter) -Methode für alle Filter auf. Übergänge zwischen dem Status "beendet" und "wird ausgeführt" durchlaufen immer den angehaltenen Status. wenn die Anwendungs Aufrufe in einem beendeten Diagramm **ausgeführt** werden, hält der Filter-Graph-Manager das Diagramm vor dem Ausführen an.

Bei den meisten Filtern sind die Zustände "wird ausgeführt" und "angehalten" identisch. Sehen Sie sich das folgende Filter Diagramm an:

Quelle > Transform > Renderer

Nehmen Sie jetzt an, dass der Quell Filter keine Live Erfassungs Quelle ist. Wenn der Quell Filter angehalten wird, erstellt er einen Thread, der neue Daten generiert und so schnell wie möglich in Medien Beispiele schreibt. Der Thread überträgt die Beispiele durch Aufrufen von [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) in der Eingabe-PIN des Transformations Filters. Der Transformations Filter empfängt die Beispiele für den Thread des Quell Filters. Es kann einen Arbeits Thread verwenden, um die Beispiele an den Renderer zu übermitteln, in der Regel werden Sie jedoch im gleichen Thread bereitstellt. Während der Renderer angehalten wird, wartet er auf den Empfang eines Beispiels. Nachdem eine solche Anwendung empfangen wurde, wird Sie auf unbestimmte Zeit blockiert und aufbewahrt. Wenn es sich um einen Videorenderer handelt, wird das Beispiel als Poster-Bild angezeigt, und das Bild wird bei Bedarf neu gezeichnet.

An diesem Punkt ist der Stream vollständig gepuffert und zum Rendern bereit. Wenn das Diagramm angehalten bleibt, werden die Beispiele im Diagramm hinter dem ersten Beispiel zusammengefasst, bis jeder Filter in [**Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) oder [**imemzucator:: GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer)blockiert wird. Obwohl keine Daten verloren gehen. Nachdem die Blockierung des Quell Threads aufgehoben wurde, wird er von dem Zeitpunkt, an dem er blockiert wurde, einfach wieder aufgenommen.

Der Quell Filter und der Transformations Filter ignorieren den Übergang von "angehalten" zu "wird ausgeführt" – Sie verarbeiten die Daten einfach so schnell wie möglich. Wenn der Renderer jedoch ausgeführt wird, beginnt er mit dem Rendern von Beispielen. Zuerst wird das Beispiel gerendert, während es angehalten wurde. Dann wird jedes Mal, wenn ein neues Beispiel empfangen wird, die Präsentationszeit des Beispiels berechnet. (Ausführliche Informationen finden Sie unter [Zeit und Uhren in DirectShow](time-and-clocks-in-directshow.md).) Der Renderer hält jede Stichprobe bis zur Präsentationszeit an. an dieser Stelle wird das Beispiel gerendert. Beim Warten auf die Präsentationszeit werden entweder in der [**Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) -Methode blockiert, oder es werden neue Beispiele für einen Arbeits Thread mit einer Warteschlange empfangen. Filter, die vom Renderer abgeleitet werden, sind nicht an der Planung beteiligt.

Live Quellen, z. b. Erfassungsgeräte, stellen eine Ausnahme von dieser allgemeinen Architektur dar. Bei einer Live Quelle ist es nicht sinnvoll, Daten vorab zu über leiten. Die Anwendung hält das Diagramm möglicherweise an und wartet dann lange, bevor es ausgeführt wird. Das Diagramm sollte keine "veralteten" Beispiele darstellen. Daher erzeugt eine Live Quelle keine Stichproben, die während der Ausführung angehalten werden. Um diese Tatsache an den Filter Graph-Manager zu signalisieren, gibt die [**imediafilter:: GetState**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getstate) -Methode des Quell Filters die Vfw s-Funktion "cant" zurück \_ \_ \_ . Dieser Rückgabecode gibt an, dass der Filter in den angehaltenen Zustand gewechselt ist, obwohl der Renderer keine Daten empfangen hat.

Wenn ein Filter anhält, lehnt er alle weiteren abgelieferten Beispiele ab. Quell Filter beenden ihre streamingthreads, und andere Filter beenden alle Arbeitsthreads, die Sie möglicherweise erstellt haben. PIN-Zuordnungen werden deaktiviert.

### <a name="state-transitions"></a>Statusübergänge

Der Filter Graph-Manager führt alle Zustandsübergänge in der Upstream-Reihenfolge aus, beginnend mit dem Renderer und geht rückwärts zum Quell Filter zurück. Diese Reihenfolge ist erforderlich, um zu verhindern, dass Beispiele gelöscht werden, und um zu verhindern, dass das Diagramm blockiert wird. Die wichtigsten Statusübergänge liegen zwischen angehalten und beendet:

-   Angehalten: da jeder Filter angehalten wird, wird er zum Empfangen von Beispielen vom nächsten Filter bereit. Der Quell Filter ist der letzte, der angehalten werden soll. Er erstellt den Streaminginhalt und beginnt mit der Übermittlung von Beispielen. Da alle downstreamfilter angehalten werden, lehnt der Filter keine Stichproben ab. Der Filter Graph-Manager schließt den Übergang erst ab, wenn jeder Renderer im Diagramm ein Beispiel erhalten hat (mit Ausnahme von Live Quellen, wie zuvor beschrieben).
-   Angehalten an beendet: Wenn ein Filter angehalten wird, werden alle darin befindlichen Beispiele freigegeben, wodurch alle in [**GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer)wartenden upstreamfilter aufgehoben werden. Wenn der Filter auf eine Ressource in der [**Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) -Methode wartet, wartet er nicht mehr und kehrt von **Receive** zurück, wodurch der aufrufende Filter aufgehoben wird. Wenn der Filter Graph-Manager den nächsten upstreamfilter stoppt, wird dieser Filter daher weder in **GetBuffer** noch im **Empfangs** Vorgang blockiert, und er kann auf den Befehl "beenden" reagieren. Der upstreamfilter liefert möglicherweise einige zusätzliche Stichproben, bevor er den Befehl "beenden" erhält, aber der downstreamfilter lehnt sie ab, weil er bereits beendet wurde.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Datenfluss im Filter Diagramm](data-flow-in-the-filter-graph.md)
</dt> </dl>

 

 



