---
description: Bereitstellung von Beispielen
ms.assetid: 31aabb6d-dec6-41fa-b24d-35a77b67bc4a
title: Bereitstellung von Beispielen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 083bc8c88649c04bdf9f93f86ebcc277ee48e75e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392897"
---
# <a name="delivering-samples"></a>Bereitstellung von Beispielen

In diesem Artikel wird beschrieben, wie ein Filter eine Stichprobe liefert. Sie beschreibt sowohl das Push-Modell als auch die [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) -Methoden und das Pull-Modell mithilfe von [**iasynkreader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader).

**Pushmodell: Bereitstellung eines Beispiels**

Die Ausgabe-PIN liefert ein Beispiel, indem die [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) -Methode oder die [**IMemInputPin:: receivemultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) -Methode aufgerufen wird, die gleichwertig ist, aber ein Array von Beispielen liefert. Die Eingabe-PIN kann innerhalb von **Receive** (oder **receivemultiple**) blockiert werden. Wenn die PIN blockiert werden kann, sollte die [**IMemInputPin:: receivecanblock**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivecanblock) -Methode S OK zurückgeben \_ . Wenn die PIN garantiert, dass nie blockiert wird, sollte **receivecanblock** den Wert S false zurückgeben \_ . Der \_ Rückgabewert S OK bedeutet nicht, dass **Receive** immer blockiert, genau dass dies möglich ist.

Obwohl **Receive** die Möglichkeit blockieren kann, auf die Verfügbarkeit einer Ressource zu warten, sollte nicht blockiert werden, um auf weitere Daten aus dem upstreamfilter zu warten. Dies kann zu einem Deadlock führen, bei dem der Upstream-Filter darauf wartet, dass der downstreamfilter das Beispiel freigibt. Dies geschieht nie, weil der Downstream-Filter auf den upstreamfilter wartet. Wenn ein Filter über mehrere Eingabe Pins verfügt, kann eine PIN jedoch auf den Empfang von Daten durch eine andere Pin warten. Der [AVI MUX](avi-mux-filter.md) -Filter führt dies z. b. so aus, dass er Audio-und Videodaten interhinterlegen kann.

Eine PIN könnte eine Stichprobe aus mehreren Gründen ablehnen:

-   Die PIN wird geleert [(siehe leeren](flushing.md)).
-   Die PIN ist nicht verbunden.
-   Der Filter wurde beendet.
-   Ein anderer Fehler ist aufgetreten.

Die **Receive** -Methode sollte \_ im ersten Fall S false und in anderen Fällen einen Fehlercode zurückgeben. Der upstreamfilter sollte das Senden von Beispielen beenden, wenn der Rückgabecode etwas anderes als S \_ OK ist.

Die ersten drei Fälle können als "erwartete" Fehler angesehen werden, in dem Sinne, dass sich der Filter im falschen Zustand befunden hat, um Beispiele zu erhalten. Ein unerwarteter Fehler ist eine, die bewirkt, dass die PIN eine Stichprobe ablehnt, auch wenn sich die PIN in einem empfangenden Zustand befindet. Wenn ein Fehler dieses Typs auftritt, sollte die PIN eine downstreambenachrichtigung senden und ein [**EC \_ errorabort**](ec-errorabort.md) -Ereignis an den Filter Graph-Manager senden.

In den DirectShow-Basisklassen überprüft die [**cbaseinputpin:: checkstreaming**](cbaseinputpin-checkstreaming.md) -Methode die allgemeinen Fehlerfälle – leeren, beendeten usw. Die abgeleitete Klasse muss auf Fehler prüfen, die für den Filter spezifisch sind. Wenn ein Fehler auftritt, sendet die [**cbaseinputpin:: Receive**](cbaseinputpin-receive.md) -Methode die datenstreambenachrichtigung und das EC \_ errorabort-Ereignis.

**Pull-Modell: Anfordern einer Stichprobe**

In der **iasyncreader** -Schnittstelle fordert die Eingabe-PIN Stichproben aus der Ausgabe-PIN an, indem eine der folgenden Methoden aufgerufen wird:

-   [**Iasynkreader:: Request**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-request)
-   [**Iasynkreader:: synkread**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-syncread)
-   [**Iasynkreader:: synkreadausgerichteten**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-syncreadaligned)

Die **Anforderungs** Methode ist asynchron. die Eingabe-PIN ruft [**iasynkreader:: waitfornext**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-waitfornext) auf, um auf den Abschluss der Anforderung zu warten. Die anderen beiden Methoden sind synchron.

**Bereitstellung von Daten**

Ein Filter liefert immer Beispiele, während er sich im Status wird ausgeführt befindet. In den meisten Fällen werden bei angehaltenen Filtern auch Beispiele angezeigt. Dies ermöglicht es dem Diagramm, die Daten zu überprüfen, sodass die Wiedergabe sofort beim Aufrufen von **Run** gestartet wird (siehe [Filter Zustände](filter-states.md)). Wenn der Filter keine Daten bereitstellt, während Sie angehalten werden, sollte die **imediafilter:: GetState** -Methode des Filters den VFW s-Fehler \_ im \_ \_ angehaltenen Zustand zurückgeben. Dieser Rückgabecode signalisiert dem Filter Diagramm, nicht auf Daten aus dem Filter zu warten, bevor der Pausen Übergang abgeschlossen ist. Andernfalls wird die **Pause** -Methode unbegrenzt blockiert. Beispielcode finden Sie unter [**cbasefilter:: GetState**](cbasefilter-getstate.md).

Im folgenden finden Sie einige Beispiele für den Fall, dass ein Filter möglicherweise einen VFW-nicht-Hinweis zurückgibt \_ \_ \_ :

-   Live Quellen, z. b. Erfassungs Filter, sollten keine Daten senden, während Sie angehalten werden. Siehe [Erstellen von Daten in einem Erfassungs Filter](producing-data-in-a-capture-filter.md).
-   Abhängig von der Implementierung kann es vorkommen, dass ein Splitter Filterdaten an die Warteschlange sendet. Wenn der Filter separate Threads verwendet, um Daten für jede Ausgabepin in die Warteschlange zu stellen, kann er Daten senden, während Sie angehalten werden Wenn der Filter jedoch einen einzelnen Thread für jede Ausgabepin verwendet, blockiert die erste Pin den Thread, wenn er **Receive** aufruft, wodurch verhindert wird, dass die anderen Pins Daten senden. In diesem Fall sollten Sie VFW S cant-Hinweis zurückgeben \_ \_ \_ .
-   Ein Filter kann sporadisch Daten bereitstellt. Beispielsweise kann ein benutzerdefinierter Datenstrom analysiert und einige Pakete herausgefiltert werden, während andere Benutzer bereitgestellt werden. In diesem Fall ist es unter Umständen nicht garantiert, dass der Filterdaten bereitstellt, während Sie angehalten werden.

Ein Quell Filter (mit dem Push-Modell) oder ein Parserfilter (mithilfe des Push/Pull-Modells) erstellt mindestens einen streamingingthread, der Beispiele so schnell wie möglich liefert. Downstreamfilter, z. b. Decoder und Transformationen, senden Daten in der Regel nur, wenn **Receive** auf Ihren Eingabe Pins aufgerufen wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Empfangen und Bereitstellung von Beispielen](receiving-and-delivering-samples.md)
</dt> </dl>

 

 



