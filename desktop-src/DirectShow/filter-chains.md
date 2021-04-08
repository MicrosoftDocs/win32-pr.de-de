---
description: Filter Ketten
ms.assetid: c17b3b58-65ab-4e83-91f2-54a995f22ddf
title: Filter Ketten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d46e374aca71b024773e4177d09e67c7ee6034ac
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103860407"
---
# <a name="filter-chains"></a>Filter Ketten

Eine *Filterkette* ist eine Sequenz von Filtern, die die folgenden Bedingungen erfüllt:

-   Jeder Filter in der Kette verfügt höchstens über eine verbundene Eingabe-PIN und eine verbundene Ausgabe-PIN.
-   Es ist möglich, jeden Filter in der Kette zu durchlaufen, ohne Filter außerhalb der Kette durchlaufen zu müssen.

Im folgenden Diagramm filtert z. b. ein – B, C – D und F – G – H Filter Ketten. Jede Teil Kette in f – g – H (f – g und G – H) ist ebenfalls eine Filterkette. Eine Filterkette kann aus einem einzelnen Filter bestehen, D. h., die Filter a, B, C, D, F, G und H sind auch unterschiedliche Filter Ketten. Filter e verfügt über zwei Eingabe Verbindungen, sodass jede Sequenz von Filtern, die den Filter e enthält, keine Filterkette ist.

![Filterkette (Beispiel 1)](images/filter-chain1.png)

Die [**ifilterchain**](/windows/desktop/api/Strmif/nn-strmif-ifilterchain) -Schnittstelle stellt die folgenden Methoden zum Steuern von Filter Ketten bereit:



|                                                               |                                 |
|---------------------------------------------------------------|---------------------------------|
| [**Ifilterchain:: startchain**](/windows/desktop/api/Strmif/nf-strmif-ifilterchain-startchain)   | Startet eine Kette.                 |
| [**Ifilterchain:: stopchain**](/windows/desktop/api/Strmif/nf-strmif-ifilterchain-stopchain)     | Beendet eine Kette.                  |
| [**Ifilterchain::P aumenchain**](/windows/desktop/api/Strmif/nf-strmif-ifilterchain-pausechain)   | Hält eine Kette an.                 |
| [**Ifilterchain:: removechain**](/windows/desktop/api/Strmif/nf-strmif-ifilterchain-removechain) | Entfernt eine Kette aus dem Diagramm. |



 

Es gibt keine bestimmte Methode zum Hinzufügen einer Kette. Fügen Sie zum Hinzufügen einer Kette die neuen Filter mithilfe der [**ifiltergraph:: AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) -Methode ein. Verbinden Sie dann die Filter, indem Sie [**igraphbuilder:: Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect), [**igraphbuilder:: Rendering**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render)oder ähnliche Methoden aufrufen.

Wenn das Diagramm ausgeführt wird, kann eine Filterkette zwischen "wird ausgeführt" und "beendet" wechseln. Wenn das Diagramm angehalten wird, kann es zwischen angehalten und beendet wechseln. Dies sind die einzigen Statusübergänge, die mit Filter Ketten möglich sind.

## <a name="filter-chain-guidelines"></a>Filter Ketten Richtlinien

Wenn Sie **ifilterchain** -Methoden verwenden, ist es wichtig sicherzustellen, dass die Filter im Diagramm Filter Verkettungs Vorgänge unterstützen. Andernfalls können Sie Deadlocks oder Graph-Fehler verursachen. An die Kette angeschlossene Filter müssen ordnungsgemäß funktionieren, nachdem der Status der Kette geändert wurde.

Die beste Möglichkeit, **ifilterchain** zu verwenden, ist eine Reihe von Filtern, die Sie speziell für die Verkettung entwickelt haben. Verwenden Sie die folgenden Richtlinien, um sicherzustellen, dass die Filter für Filter Ketten Vorgänge sicher sind. Diese Punkte verweisen auf das folgende Diagramm.

![Filterkette (Beispiel 2)](images/filter-chain2.png)

-   Bevor der Status der Filterkette geändert wird, müssen alle Datenverarbeitungs Aufrufe an der Grenze der Filterkette abgeschlossen werden. Diese Regel gilt für die Methoden [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive), [**IPin:: newsegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment)und [**IPin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream). Filter in der Kette müssen von Aufrufen dieser Methoden zurückgegeben werden, die von Filtern außerhalb der Kette vorgenommen werden. und Filter außerhalb der Kette müssen von Aufrufen von Filtern innerhalb der Kette zurückgegeben werden.

In der vorherigen Abbildung muss Filter B beispielsweise alle Datenverarbeitungs Aufrufe von Filter A abschließen, und Filter E muss alle Aufrufe von Filter D abschließen. Wenn die Pins die [**IPinFlowControl**](/windows/desktop/api/Strmif/nn-strmif-ipinflowcontrol) -Schnittstelle und die [**ipinconnection**](/windows/desktop/api/Strmif/nn-strmif-ipinconnection) -Schnittstelle verfügbar machen, können Sie die Daten über das Diagramm per Push übertragen, indem Sie die Methoden [**IPinFlowControl:: Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block) und [**igraphconfig::P ushdowndata**](/windows/desktop/api/Strmif/nf-strmif-igraphconfig-pushthroughdata) aufrufen, wie in [Dynamic Reconnection](dynamic-reconnection.md)beschrieben. Filter unterstützen möglicherweise auch private Methoden zum Übertragen der Daten.

-   Upstreamfilter müssen erwarten, dass der Status der Kette geändert wird. Angenommen, im vorherigen Diagramm ist beispielsweise die Kette angehalten, aber es wird ein **IMemInputPin:: Receive**-Aufruf gefiltert. Der-Rückruf schlägt fehl, und die Antwort von Filter A besteht darin, das Streaming zu verhindern. Wenn die Anwendung die Kette neu startet, hat Sie keine Auswirkung, da bei Filter A keine Daten mehr gestreamt werden.
-   Downstream-Filter müssen auch erwarten, dass der Status der Kette geändert wird. Wenn dies nicht der Fall ist, kann der Downstream-Filter blockieren, während er auf Stichproben wartet, die nie eintreffen Beispielsweise erfordern Multiplexer-Filter (MUX) häufig Daten von allen Eingabe Pins. Durch das Anhalten des Datenflusses aus einer Eingabe-PIN werden die anderen Streams möglicherweise nicht mehr verarbeitet. Dies kann zu einem Deadlock des Diagramms führen.
-   Jede Pin-Verbindung von einem Filter außerhalb der Kette zu einem Filter in der Kette sollte über eine eigene Zuweisung verfügen, die nicht von anderen Verbindungen gemeinsam genutzt wird. Wenn sich der Zustand der Kette ändert oder aus dem Diagramm entfernt wird, kann die Zuweisung aufgehoben werden. Wenn andere Verbindungen denselben Zuweiser verwenden, können Sie keine Beispiele mehr verarbeiten.
-   Entfernen Sie eine Kette nur dann, wenn die mit der Kette verbundenen Filter dynamische Trennungs Verbindungen unterstützen. In der Regel unterstützen die verbundenen Filter die **ipinconnection** -Schnittstelle oder die **IPinFlowControl** -Schnittstelle, unterstützen jedoch möglicherweise private Schnittstellen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Dynamische Diagramm Bildung](dynamic-graph-building.md)
</dt> </dl>

 

 



