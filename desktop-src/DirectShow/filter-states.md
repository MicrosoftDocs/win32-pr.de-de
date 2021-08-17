---
description: Filterzustände
ms.assetid: 97418307-eb50-4c8e-b03b-a2cd08139bdc
title: Filterzustände
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 487b2f5e71cfebd8a9c7282679aa39b2264f0460dd72ad23e1b2b26926e0c979
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015738"
---
# <a name="filter-states"></a>Filterzustände

Filter haben drei mögliche Zustände: angehalten, angehalten und ausgeführt. Der Zweck des angehaltenen Zustands besteht darin, Daten im Diagramm anzuleiten, sodass ein Ausführungsbefehl sofort reagiert. Der Filter Graph-Manager steuert alle Zustandsübergänge. Wenn eine Anwendung [**IMediaControl::Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run), [**IMediaControl::P ause**](/windows/desktop/api/Control/nf-control-imediacontrol-pause)oder [**IMediaControl::Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop)aufruft, ruft der Filter Graph Manager die entsprechende [**IMediaFilter-Methode**](/windows/desktop/api/Strmif/nn-strmif-imediafilter) für alle Filter auf. Übergänge zwischen "Beendet" und "Wird ausgeführt" durchlaufen immer den angehaltenen Zustand. Wenn also die Anwendung **Ausführen** für ein beendetes Diagramm aufruft, hält der Filter Graph Manager das Diagramm an, bevor es ausgeführt wird.

Bei den meisten Filtern sind die Status "Wird ausgeführt" und "Angehalten" identisch. Betrachten Sie das folgende Filterdiagramm:

Source > Transform > Renderer

Nehmen wir vorerst an, dass der Quellfilter keine Liveerfassungsquelle ist. Wenn der Quellfilter angehalten wird, wird ein Thread erstellt, der neue Daten generiert und so schnell wie möglich in Medienbeispiele schreibt. Der Thread "pusht" die Beispiele nachgeschaltet, indem [**er IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) auf dem Eingabepin des Transformationsfilters aufruft. Der Transformationsfilter empfängt die Beispiele im Thread des Quellfilters. Es kann einen Arbeitsthread verwenden, um die Beispiele an den Renderer zu übermitteln, aber in der Regel werden sie im gleichen Thread übermittelt. Während der Renderer angehalten wird, wartet er auf den Empfang eines Beispiels. Nachdem ein Beispiel empfangen wurde, wird das Beispiel blockiert und unbegrenzt aufbewahrt. Wenn es sich um einen Videorenderer handelt, zeigt es das Beispiel als Posterbild an und zeichnet das Bild nach Bedarf neu.

An diesem Punkt ist der Stream vollständig cued und bereit für das Rendern. Wenn das Diagramm angehalten bleibt, "stapeln" sich die Beispiele im Diagramm hinter dem ersten Beispiel, bis jeder Filter in [**Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) oder [**IMemAllocator::GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer)blockiert wird. Es geht jedoch keine Daten verloren. Nachdem die Blockierung des Quellthreads aufgehoben wurde, wird er einfach ab dem Punkt fortgesetzt, an dem er blockiert wurde.

Der Quellfilter und der Transformationsfilter ignorieren den Übergang von angehalten zu ausgeführt– sie fahren einfach so schnell wie möglich mit der Verarbeitung von Daten fort. Wenn der Renderer ausgeführt wird, beginnt er jedoch mit dem Rendern von Beispielen. Zuerst rendert es das Sample, das während des Anhaltens gehalten wurde. Bei jedem Empfang einer neuen Stichprobe wird dann die Präsentationszeit der Stichprobe berechnet. (Weitere Informationen finden Sie unter [Uhrzeit und Uhren in DirectShow](time-and-clocks-in-directshow.md).) Der Renderer hält jedes Beispiel bis zur Präsentationszeit, an dem es das Beispiel rendert. Während sie auf die Präsentationszeit wartet, wird sie entweder in der [**Receive-Methode**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) blockiert oder empfängt neue Beispiele für einen Arbeitsthread mit einer Warteschlange. Filter, die vom Renderer vorgelagert werden, sind nicht an der Planung beteiligt.

Livequellen, z. B. Erfassungsgeräte, sind eine Ausnahme von dieser allgemeinen Architektur. Bei einer Livequelle ist es nicht sinnvoll, im Voraus Daten zu cuetieren. Die Anwendung kann das Diagramm anhalten und dann lange warten, bevor sie ausgeführt wird. Das Diagramm sollte keine "veralteten" Beispiele rendern. Daher erzeugt eine Livequelle keine Stichproben, während sie angehalten wird, nur während der Ausführung. Um diese Tatsache an den Filter Graph Manager zu signalisieren, gibt die [**IMediaFilter::GetState-Methode**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getstate) des Quellfilters VFW \_ S \_ CANT \_ CUE zurück. Dieser Rückgabecode gibt an, dass der Filter in den angehaltenen Zustand gewechselt ist, obwohl der Renderer keine Daten empfangen hat.

Wenn ein Filter beendet wird, werden alle weiteren an ihn übermittelten Stichproben abgelehnt. Quellfilter fahren ihre Streamingthreads herunter, und andere Filter fahren alle Arbeitsthreads herunter, die sie möglicherweise erstellt haben. Pins decommitmit their allocators.

### <a name="state-transitions"></a>Statusübergänge

Der Filter Graph Manager führt alle Zustandsübergänge in Upstreamreihenfolge aus, beginnend vom Renderer bis hin zum Quellfilter. Diese Reihenfolge ist erforderlich, um zu verhindern, dass Stichproben gelöscht werden und das Diagramm nicht blockiert wird. Die wichtigsten Statusübergänge sind zwischen angehalten und beendet:

-   Angehalten bis angehalten: Wenn jeder Filter angehalten wird, kann er Stichproben vom nächsten Filter erhalten. Der Quellfilter ist der letzte, der angehalten werden soll. Er erstellt den Streamingthread und beginnt mit der Übermittlung von Beispielen. Da alle Downstreamfilter angehalten werden, lehnt kein Filter Stichproben ab. Der Filter Graph Manager schließt den Übergang erst ab, wenn jeder Renderer im Diagramm ein Beispiel erhalten hat (mit Ausnahme von Livequellen, wie zuvor beschrieben).
-   Angehalten bis beendet: Wenn ein Filter beendet wird, gibt er alle darin enthaltenen Beispiele frei, wodurch die Blockierung aller Upstreamfilter aufgehoben wird, die in [**GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer)warten. Wenn der Filter auf eine Ressource innerhalb der [**Receive-Methode**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) wartet, beendet er das Warten und gibt von **Receive** zurück, wodurch die Blockierung des aufrufenden Filters aufgehoben wird. Wenn der Filter Graph Manager den nächsten Upstreamfilter beendet, wird dieser Filter daher weder in **GetBuffer** noch in **Receive** blockiert und kann auf den Befehl stop reagieren. Der Upstreamfilter liefert möglicherweise einige zusätzliche Stichproben, bevor er den Stop-Befehl erhält, aber der Downstreamfilter lehnt sie einfach ab, da er bereits beendet wurde.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Daten Flow im filter-Graph](data-flow-in-the-filter-graph.md)
</dt> </dl>

 

 



