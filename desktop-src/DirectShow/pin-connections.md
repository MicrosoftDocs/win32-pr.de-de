---
description: Stecknadelverbindungen
ms.assetid: 1406ade4-77d8-49a7-8f36-cc49ff007a26
title: Stecknadelverbindungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cfcd407e785e15f4243f3113a63569f8b4b84de517cdde0f63a88eaef79f85c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119432290"
---
# <a name="pin-connections"></a>Stecknadelverbindungen

Filter stellen über die [**IPin-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ipin) eine Verbindung an ihren Stecknadeln her. Ausgabepins stellen eine Verbindung mit Eingabepins her. Jede Pinverbindung verfügt über einen Medientyp, der von der [**AM \_ MEDIA \_ TYPE-Struktur**](/windows/win32/api/strmif/ns-strmif-am_media_type) beschrieben wird.

Eine Anwendung verbindet Filter durch Aufrufen von Methoden im Filter-Graph-Manager, niemals durch Aufrufen von Methoden für die Filter oder Pins selbst. Die Anwendung kann direkt angeben, welche Filter eine Verbindung herstellen sollen, indem sie die [**Methode IFilterGraph::ConnectDirect**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-connectdirect) oder [**IGraphBuilder::Verbinden**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) aufruft. Oder filtert indirekt mithilfe einer Grapherstellungsmethode wie [**IGraphBuilder::RenderFile.**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile)

Damit die Verbindung erfolgreich hergestellt werden kann, müssen beide Filter im Filterdiagramm angezeigt werden. Die Anwendung kann dem Diagramm einen Filter hinzufügen, indem sie die [**IFilterGraph::AddFilter-Methode**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) aufruft. Der Filter Graph-Manager kann dem Diagramm ebenfalls Filter hinzufügen. Wenn ein Filter hinzugefügt wird, ruft der Filter Graph Manager die [**IBaseFilter::JoinFilterGraph-Methode**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph) des Filters auf, um den Filter zu benachrichtigen.

Die allgemeine Übersicht über den Verbindungsprozess lautet wie folgt:

1.  Der Filter Graph-Manager ruft [**IPin::Verbinden**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) auf dem Ausgabepin auf und übergibt einen Zeiger auf den Eingabepin.
2.  Wenn der Ausgabepin die Verbindung akzeptiert, ruft er [**IPin::ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) auf dem Eingabepin auf.
3.  Wenn der Eingabepin auch die Verbindung akzeptiert, ist der Verbindungsversuch erfolgreich, und die Pins sind verbunden.

Einige Pins können getrennt und erneut verbunden werden, während der Filter aktiv ist. Diese Art der erneuten Verbindung wird als *dynamische* Erneute Verbindung bezeichnet. Weitere Informationen finden Sie unter [Dynamic Graph Building](dynamic-graph-building.md). Die meisten Filter unterstützen jedoch keine dynamische Wiederherstellung der Verbindung.

Filter werden in der Regel in downstreamer Reihenfolge verbunden, d. h., die Eingabepins des Filters werden vor den Ausgabepins verbunden. Ein Filter sollte diese Verbindungsreihenfolge immer unterstützen. Einige Filter unterstützen auch Verbindungen in umgekehrter Reihenfolge – ausgabepins first, gefolgt von Eingabepins. Beispielsweise kann es möglich sein, den Ausgabepin eines MUX-Filters mit dem Dateiwriterfilter zu verbinden, bevor sie die Eingabepins des MUX-Filters verbinden.

Wenn die **Verbinden-** oder **ReceiveConnection-Methode** eines Pins aufgerufen wird, muss der Pin überprüfen, ob er die Verbindung unterstützen kann. Die Details hängen vom jeweiligen Filter ab. Die gängigsten Aufgaben umfassen Folgendes:

-   Überprüfen Sie, ob der Medientyp akzeptabel ist.
-   Aushandeln einer Zuweisung
-   Fragen Sie den anderen Pin nach erforderlichen Schnittstellen ab.

 

 



