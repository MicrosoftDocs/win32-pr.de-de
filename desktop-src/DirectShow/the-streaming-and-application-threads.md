---
description: Streaming-und Anwendungsthreads
ms.assetid: 954f7abd-fe06-430a-b6f7-d60852826bc9
title: Streaming-und Anwendungsthreads
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 432e613ff0322377c042e796d84ef7affdda99c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530245"
---
# <a name="the-streaming-and-application-threads"></a>Streaming-und Anwendungsthreads

Alle DirectShow-Anwendungen enthalten mindestens zwei wichtige Threads: den Anwendungs Thread und einen oder mehrere streamingthreads. Die Beispiele werden über die streamingthreads geliefert, und Zustandsänderungen werden im Anwendungs Thread ausgeführt. Der hauptstreamingthread wird von einem Quell-oder Parserfilter erstellt. Andere Filter erstellen möglicherweise Arbeitsthreads, die Beispiele bereitstellen. Diese werden auch als streamingthreads angesehen.

Einige Methoden werden im Anwendungs Thread aufgerufen, während andere in einem streamingthread aufgerufen werden. Beispiel:

-   Streaming Thread (s): [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive), [**IMemInputPin:: receivemultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple), [**IPin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream), [**imemzuzucator:: GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer).
-   Anwendungs Thread: [**imediafilter::P ause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause), [**imediafilter:: Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run), [**imediafilter::**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop)End, [**imediaseeking:: setpositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions), [**IPin:: beginflush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush), [**IPin:: endflush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush).
-   Beides: [**IPin:: newsegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment).

Ein separater streamingthread ermöglicht das Übertragen von Daten durch das Diagramm, während der Anwendungs Thread auf Benutzereingaben wartet. Die Gefahr mehrerer Threads besteht jedoch darin, dass ein Filter Ressourcen erstellen kann, wenn er angehalten wird (im Anwendungs Thread), diese innerhalb einer Streamingmethode verwenden und diese bei Beendigung (auch im Anwendungs Thread) zerstören. Wenn Sie nicht vorsichtig sind, versucht der streamingingthread möglicherweise, die Ressourcen zu verwenden, nachdem Sie zerstört wurden. Die Lösung besteht darin, Ressourcen mithilfe kritischer Abschnitte zu schützen und Streamingmethoden mit Zustandsänderungen zu synchronisieren.

Ein Filter benötigt einen kritischen Abschnitt, um den Filter Zustand zu schützen. Die [**cbasefilter**](cbasefilter.md) -Klasse verfügt über eine Member-Variable für diesen kritischen Abschnitt [**cbasefilter:: m \_ Plock**](cbasefilter-m-plock.md). Dieser kritische Abschnitt wird als Filter Sperre bezeichnet. Außerdem benötigt jede Eingabe-PIN einen kritischen Abschnitt, um die Ressourcen zu schützen, die vom Streaminginhalt verwendet werden. Diese kritischen Abschnitte heißen streamingsperren. Sie müssen Sie in der abgeleiteten Pin-Klasse deklarieren. Es ist am einfachsten, die [**ccritsec**](ccritsec.md) -Klasse zu verwenden, die ein kritisches Windows- **\_ Abschnitts** Objekt umschließt und mithilfe der [**cautolock**](cautolock.md) -Klasse gesperrt werden kann. Die **ccritsec** -Klasse bietet auch einige nützliche Debuggingfunktionen. Weitere Informationen finden Sie im [Abschnitt zum Debuggen von kritischen Abschnitten](critical-section-debugging-functions.md).

Wenn ein Filter beendet oder geleert wird, muss er den Anwendungs Thread mit dem streamingthread synchronisieren. Um Deadlocks zu vermeiden, muss zunächst der streamingingthread blockiert werden. Dies kann aus verschiedenen Gründen blockiert werden:

-   Er wartet darauf, ein Beispiel innerhalb der [**imemzucator:: GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) -Methode zu erhalten, da alle Beispiele der Zuweiser verwendet werden.
-   Er wartet darauf, dass ein anderer Filter von einer Streamingmethode (z. b. **Receive**) zurückgegeben wird.
-   Er wartet innerhalb einer seiner eigenen Streamingmethoden, damit eine Ressource verfügbar wird.
-   Es handelt sich um einen rendererfilter, der auf die Präsentationszeit des nächsten Beispiels wartet.
-   Es handelt sich um einen rendererfilter, der in der **Receive** -Methode wartet

Wenn der Filter beendet oder geleert wird, muss er daher folgende Aktionen ausführen:

-   Geben Sie ein beliebiges Beispiel aus irgendeinem Grund frei. Dadurch wird die Blockierung der **GetBuffer** -Methode aufgehoben.
-   Gibt so schnell wie möglich von jeder Streamingmethode zurück. Wenn eine Streamingmethode auf eine Ressource wartet, muss Sie nicht mehr sofort warten.
-   Beginnen Sie mit dem ablehnen von Beispielen in **Receive**, damit der streamingingthread nicht auf Weitere Ressourcen zugreift. (Die [**cbaseingeputpin**](cbaseinputpin.md) -Klasse verarbeitet dies automatisch.)
-   Die Methode zum **Abbrechen** muss alle Zuweisungen des Filters Decommit aufheben. (Die **cbaseingeputpin** -Klasse verarbeitet dies automatisch.)

Das leeren und beenden beider vorkommen erfolgt im Anwendungs Thread. Ein Filter wird als Reaktion auf die [**IMediaControl:: Stopp**](/windows/desktop/api/Control/nf-control-imediacontrol-stop) -Methode angehalten. Der Filter Graph-Manager gibt den Befehl zum Abbrechen in der upstreamreihenfolge aus, beginnend mit den renderatoren und rückwärts zu den Quell filtern. Der Befehl zum Abbrechen erfolgt vollständig innerhalb der **cbasefilter:: stopmethode** des Filters. Wenn die Methode zurückgegeben wird, sollte der Filter den Status "beendet" aufweisen.

Das leeren erfolgt in der Regel aufgrund eines Seek-Befehls. Ein Flush-Befehl beginnt mit dem Quell-oder Parserfilter und verläuft nach unten. Das leeren erfolgt in zwei Phasen: die [**IPin:: beginflush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) -Methode informiert einen Filter, alle ausstehenden und eingehenden Daten zu verwerfen. die [**IPin:: endflush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) -Methode signalisiert dem Filter, Daten erneut zu akzeptieren. Das Leeren von erfordert zwei Stufen, da sich der **beginflush** -Rückruf im Anwendungs Thread befindet, in dem der streamingthread weiterhin Daten bereitstellt. Daher können nach dem **beginflush** -Aufrufvorgang einige Beispiele eintreffen. Der Filter sollte diese verwerfen. Alle Beispiele, die nach dem **endflush** -Rückruf eintreffen, sind garantiert neu und sollten übermittelt werden.

Die folgenden Abschnitte enthalten Codebeispiele, die zeigen, wie die wichtigsten Filter **Methoden wie anhalten,** **empfangen** usw. implementiert werden, um Deadlocks und Racebedingungen zu vermeiden. Jeder Filter hat jedoch unterschiedliche Anforderungen, sodass Sie diese Beispiele an Ihren speziellen Filter anpassen müssen.

> [!Note]  
> Mit den [**ctransformfilter**](ctransformfilter.md) -und [**ctransinplacefilter**](ctransinplacefilter.md) -Basisklassen werden viele der in diesem Artikel beschriebenen Probleme behandelt. Wenn Sie einen Transformations Filter schreiben und der Filter nicht auf Ereignisse innerhalb einer Streamingmethode wartet oder Beispiele außerhalb des **Empfangs** enthalten, sollten diese Basisklassen ausreichen.

 

 

 



