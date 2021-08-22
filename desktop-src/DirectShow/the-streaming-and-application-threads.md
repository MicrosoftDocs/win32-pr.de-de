---
description: Die Streaming- und Anwendungsthreads
ms.assetid: 954f7abd-fe06-430a-b6f7-d60852826bc9
title: Die Streaming- und Anwendungsthreads
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a90916c14395a21aa5c53481c96b03fb6bbb2a8d4162cf996ef18ac15ce5e856
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119583120"
---
# <a name="the-streaming-and-application-threads"></a>Die Streaming- und Anwendungsthreads

Jede DirectShow-Anwendung enthält mindestens zwei wichtige Threads: den Anwendungsthread und einen oder mehrere Streamingthreads. Beispiele werden für die Streamingthreads übermittelt, und Zustandsänderungen werden im Anwendungsthread vorgenommen. Der Hauptstreamingthread wird von einem Quell- oder Parserfilter erstellt. Andere Filter können Arbeitsthreads erstellen, die Beispiele liefern, und diese werden auch als Streamingthreads betrachtet.

Einige Methoden werden im Anwendungsthread aufgerufen, während andere in einem Streamingthread aufgerufen werden. Beispiel:

-   Streamingthreads: [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive), [**IMemInputPin::ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple), [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream), [**IMemAllocator::GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer).
-   Anwendungsthread: [**IMediaFilter::P ause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause), [**IMediaFilter::Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run), [**IMediaFilter::Stop**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop), [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions), [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush), [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush).
-   Entweder: [**IPin::NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment).

Durch die Verwendung eines separaten Streamingthreads können Daten durch das Diagramm fließen, während der Anwendungsthread auf Benutzereingaben wartet. Die Gefahr mehrerer Threads besteht jedoch darin, dass ein Filter Ressourcen erstellen kann, wenn er angehalten wird (im Anwendungsthread), sie in einer Streamingmethode verwendet und zerstört, wenn er beendet wird (auch im Anwendungsthread). Wenn Sie nicht vorsichtig sind, versucht der Streamingthread möglicherweise, die Ressourcen zu verwenden, nachdem sie zerstört wurden. Die Lösung besteht im Schützen von Ressourcen mit kritischen Abschnitten und synchronisieren Streamingmethoden mit Zustandsänderungen.

Ein Filter benötigt einen kritischen Abschnitt, um den Filterzustand zu schützen. Die [**CBaseFilter-Klasse**](cbasefilter.md) verfügt über eine Membervariable für diesen kritischen Abschnitt, [**CBaseFilter::m \_ pLock.**](cbasefilter-m-plock.md) Dieser kritische Abschnitt wird als Filtersperre bezeichnet. Außerdem benötigt jeder Eingabepin einen kritischen Abschnitt, um die vom Streamingthread verwendeten Ressourcen zu schützen. Diese kritischen Abschnitte werden als Streamingsperren bezeichnet. Sie müssen sie in der abgeleiteten Pinklasse deklarieren. Es ist am einfachsten, die [**CCritSec-Klasse**](ccritsec.md) zu verwenden, die ein Windows **CRITICAL \_ SECTION-Objekt** umschließt und mithilfe der [**CAutoLock-Klasse gesperrt werden**](cautolock.md) kann. Die **CCritSec-Klasse** bietet auch einige nützliche Debugfunktionen. Weitere Informationen finden Sie unter [Wichtige Abschnitt Debugfunktionen](critical-section-debugging-functions.md).

Wenn ein Filter beendet oder geleert wird, muss er den Anwendungsthread mit dem Streamingthread synchronisieren. Um Deadlocks zu vermeiden, muss zuerst die Blockierung des Streamingthreads aufgehoben werden, der aus verschiedenen Gründen blockiert werden kann:

-   Sie wartet darauf, ein Beispiel in der [**IMemAllocator::GetBuffer-Methode**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) zu erhalten, da alle Beispiele der Zuweisung verwendet werden.
-   Er wartet darauf, dass ein anderer Filter von einer Streamingmethode wie Receive **zurückgekehrt wird.**
-   Es wartet in einer seiner eigenen Streamingmethoden, bis eine Ressource verfügbar wird.
-   Es handelt sich um einen Rendererfilter, der auf die Präsentationszeit des nächsten Beispiels wartet.
-   Es handelt sich um einen Rendererfilter, der in der **Receive-Methode** wartet, während er angehalten wurde.

Wenn der Filter beendet oder geleert wird, muss er daher Folgendes tun:

-   Geben Sie jedes Beispiel frei, das es aus irgendeinem Grund enthält. Dadurch wird die Blockierung der **GetBuffer-Methode** aufgehoben.
-   Geben Sie so schnell wie möglich von jeder Streamingmethode zurück. Wenn eine Streamingmethode auf eine Ressource wartet, muss sie sofort warten.
-   Beginnen Sie mit dem Ablehnen von Beispielen in **Receive,** damit der Streamingthread nicht mehr auf Ressourcen zutritt. (Die [**CBaseInputPin-Klasse**](cbaseinputpin.md) verarbeitet dies automatisch.)
-   Die **Stop-Methode** muss denCommit aller Zuweisungen des Filters decommit machen. (Die **CBaseInputPin-Klasse** verarbeitet dies automatisch.)

Beides wird im Anwendungsthread geleert und beendet. Ein Filter wird als Reaktion auf die [**IMediaControl::Stop-Methode**](/windows/desktop/api/Control/nf-control-imediacontrol-stop) beendet. Der Filter-Graph-Manager gibt den Befehl stop in upstream-Reihenfolge aus, beginnend bei den Renderern und der Rückwärtsarbeit zu den Quellfiltern. Der Stop-Befehl erfolgt vollständig innerhalb der **CBaseFilter::Stop-Methode des** Filters. Wenn die Methode zurückgegeben wird, sollte der Filter beendet sein.

Das Leeren erfolgt in der Regel aufgrund eines Seek-Befehls. Ein Flush-Befehl beginnt mit dem Quell- oder Parserfilter und wird nachgeschaltet. Das Leeren erfolgt in zwei Phasen: Die [**IPin::BeginFlush-Methode**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) informiert einen Filter, um alle ausstehenden und eingehenden Daten zu verwerfen. Die [**IPin::EndFlush-Methode signalisiert**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) dem Filter, daten erneut zu akzeptieren. Das Leeren erfordert zwei Phasen, da sich der **BeginFlush-Aufruf** im Anwendungsthread befindet, in dem der Streamingthread weiterhin Daten liefert. Daher können einige Beispiele nach dem **BeginFlush-Aufruf** eintreffen. Diese sollten vom Filter verworfen werden. Alle Beispiele, die nach dem **EndFlush-Aufruf** eintreffen, sind garantiert neu und sollten übermittelt werden.

Die folgenden Abschnitte enthalten Codebeispiele, die zeigen, wie sie die wichtigsten Filtermethoden wie **Anhalten,** **Empfangen** usw. so implementieren, dass Deadlocks und Racebedingungen vermieden werden. Jeder Filter hat jedoch andere Anforderungen, daher müssen Sie diese Beispiele an Ihren speziellen Filter anpassen.

> [!Note]  
> Die [**Basisklassen CTransformFilter**](ctransformfilter.md) und [**CTransInPlaceFilter**](ctransinplacefilter.md) behandeln viele der in diesem Artikel beschriebenen Probleme. Wenn Sie einen Transformationsfilter schreiben und ihr Filter nicht auf Ereignisse in einer Streamingmethode wartet oder sich nicht an Stichproben außerhalb von **Receive** hält, sollten diese Basisklassen ausreichend sein.

 

 

 



