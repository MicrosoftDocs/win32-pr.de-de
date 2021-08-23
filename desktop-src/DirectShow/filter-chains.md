---
description: Filterketten
ms.assetid: c17b3b58-65ab-4e83-91f2-54a995f22ddf
title: Filterketten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4650c49dd796ff3aa7ddecbd21076a4e217def9bfb6504149fdb740c2810b48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119685480"
---
# <a name="filter-chains"></a>Filterketten

Eine *Filterkette* ist eine Sequenz von Filtern, die die folgenden Bedingungen erfüllt:

-   Jeder Filter in der Kette verfügt über mindestens einen verbundenen Eingabepin und einen verbundenen Ausgabepin.
-   Es ist möglich, jeden Filter in der Kette zu durchlaufen, ohne Filter außerhalb der Kette zu durchlaufen.

Im folgenden Diagramm sind die Filter A–B, C–D und F–G–H beispielsweise Filterketten. Jede Unterkette in F–G–H (F–G und G–H) ist ebenfalls eine Filterkette. Eine Filterkette kann aus einem einzelnen Filter bestehen, sodass die Filter A, B, C, D, F, G und H ebenfalls unterschiedliche Filterketten sind. Filter E verfügt über zwei Eingabeverbindungen, sodass jede Filtersequenz, die Filter E enthält, keine Filterkette ist.

![Filterkette (Beispiel 1)](images/filter-chain1.png)

Die [**IFilterChain-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ifilterchain) stellt die folgenden Methoden zum Steuern von Filterketten bereit:



| Bezeichnung | Wert |
|---------------------------------------------------------------|---------------------------------|
| [**IFilterChain::StartChain**](/windows/desktop/api/Strmif/nf-strmif-ifilterchain-startchain)   | Startet eine Kette.                 |
| [**IFilterChain::StopChain**](/windows/desktop/api/Strmif/nf-strmif-ifilterchain-stopchain)     | Beendet eine Kette.                  |
| [**IFilterChain::P auseChain**](/windows/desktop/api/Strmif/nf-strmif-ifilterchain-pausechain)   | Hält eine Kette an.                 |
| [**IFilterChain::RemoveChain**](/windows/desktop/api/Strmif/nf-strmif-ifilterchain-removechain) | Entfernt eine Kette aus dem Diagramm. |



 

Es gibt keine bestimmte Methode zum Hinzufügen einer Kette. Um eine Kette hinzuzufügen, fügen Sie die neuen Filter mithilfe der [**IFilterGraph::AddFilter-Methode**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) ein. Verbinden Sie dann die Filter, indem [**Sie IGraphBuilder::Verbinden,**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) [**IGraphBuilder::Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render)oder ähnliche Methoden aufrufen.

Wenn das Diagramm ausgeführt wird, kann eine Filterkette zwischen ausgeführt und beendet wechseln. Wenn das Diagramm angehalten wird, kann es zwischen angehalten und beendet wechseln. Dies sind die einzigen Zustandsübergänge, die mit Filterketten möglich sind.

## <a name="filter-chain-guidelines"></a>Richtlinien für Die Filterkette

Wenn Sie **IFilterChain-Methoden** verwenden, ist es wichtig sicherzustellen, dass die Filter im Diagramm Filterkettenvorgänge unterstützen können. Andernfalls können Deadlocks oder Graphfehler auftreten. Mit der Kette verbundene Filter müssen ordnungsgemäß funktionieren, nachdem sich der Zustand der Kette geändert hat.

**IFilterChain** kann am besten mit einer Reihe von Filtern verwendet werden, die Sie speziell für die Verkettung entworfen haben. Verwenden Sie die folgenden Richtlinien, um sicherzustellen, dass Ihre Filter für Filterkettenvorgänge sicher sind. Diese Punkte beziehen sich auf das folgende Diagramm.

![Filterkette (Beispiel 2)](images/filter-chain2.png)

-   Bevor sich der Zustand der Filterkette ändert, müssen alle Datenverarbeitungsaufrufe an der Grenze der Filterkette abgeschlossen werden. Diese Regel gilt für die Methoden [**IMemInputPin::Receive,**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) [**IPin::NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment)und [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream). Filter in der Kette müssen von Aufrufen dieser Methoden zurückgeben, die von Filtern außerhalb der Kette vorgenommen wurden. Filter und außerhalb der Kette müssen von Aufrufen zurückgeben, die von Filtern innerhalb der Kette vorgenommen wurden.

Im vorherigen Diagramm muss filter B beispielsweise alle Datenverarbeitungsaufrufe von Filter A und Filter E alle Aufrufe aus Filter D abschließen. Wenn die Pins die [**Schnittstellen IPinFlowControl**](/windows/desktop/api/Strmif/nn-strmif-ipinflowcontrol) und [**IPinConnection**](/windows/desktop/api/Strmif/nn-strmif-ipinconnection) verfügbar machen, können Sie die Daten über das Diagramm pushen, indem Sie die [**Methoden IPinFlowControl::Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block) und [**IGraphConfig::P ushThroughData**](/windows/desktop/api/Strmif/nf-strmif-igraphconfig-pushthroughdata) aufrufen, wie in [Dynamic Reconnection beschrieben.](dynamic-reconnection.md) Filter können auch private Methoden zum Pushen der Daten unterstützen.

-   Upstreamfilter müssen erwarten, dass sich der Zustand der Kette ändert. Nehmen wir beispielsweise im vorherigen Diagramm an, dass die Kette beendet wurde, aber A ruft **IMemInputPin::Receive auf.** Der Aufruf schlägt fehl, und die Antwort von Filter A ist das Beenden des Streamings. Wenn die Anwendung die Kette neu startet, hat dies keine Auswirkungen, da Filter A keine Daten mehr streamt.
-   Downstreamfilter müssen auch erwarten, dass sich der Zustand der Kette ändert. Falls nicht, kann der Downstreamfilter blockiert werden, während er auf Stichproben wartet, die nie eintreffen. Beispielsweise erfordern Multiplexerfilter (MUX) häufig Daten von allen ihren Eingabepins. Das Anhalten des Datenflusses von einem Eingabepin kann die Verarbeitung der anderen Datenströme blockieren. Dies kann zu einem Deadlock des Graphen führen.
-   Jede Stecknadelverbindung von einem Filter außerhalb der Kette zu einem Filter innerhalb der Kette sollte über eine eigene Zuweisung verfügen, die nicht von anderen Verbindungen gemeinsam genutzt wird. Wenn sich der Zustand der Kette ändert oder aus dem Diagramm entfernt wird, wird die Zuweisung möglicherweise aufgehoben. Wenn andere Verbindungen dieselbe Zuweisung verwendet haben, können sie keine Beispiele mehr verarbeiten.
-   Entfernen Sie eine Kette nur, wenn die mit der Kette verbundenen Filter die dynamische Trennung unterstützen. In der Regel unterstützen die verbundenen Filter die **IPinConnection-** oder **IPinFlowControl-Schnittstelle,** aber möglicherweise auch private Schnittstellen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Dynamic Graph Building](dynamic-graph-building.md)
</dt> </dl>

 

 



