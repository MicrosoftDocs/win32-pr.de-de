---
description: Pullmodell
ms.assetid: b5246dfe-e6ee-4b91-bfe3-2ec8b8723938
title: Pullmodell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9832f719e21d85fd09fbf92303e404290d7d99efd6953ace398f77167d0263a1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747890"
---
# <a name="pull-model"></a>Pullmodell

In der [**IMemInputPin-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) bestimmt der Upstreamfilter, welche Daten gesendet werden, und pusht die Daten an den Downstreamfilter. Für einige Filter ist *ein Pullmodell* besser geeignet. Hier fordert der Downstreamfilter Daten vom Upstreamfilter an. Die Stichproben werden weiterhin nachgeschaltet, vom Ausgabepin zum Eingabepin, aber der Downstreamfilter initiiert den Datenfluss. Dieser Verbindungstyp verwendet die [**IAsyncReader-Schnittstelle.**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader)

Die typische Verwendung für das Pullmodell ist die Dateiwiedergabe. Beispielsweise führt der Filter [Async File Source](file-source--async--filter.md) in einem AVI-Wiedergabediagramm generische Dateilesevorgänge aus und stellt die Daten als Bytestream ohne Formatinformationen zur Verfügung. Der [AVI-Splitterfilter](avi-splitter-filter.md) liest die AVI-Header und analysiert den Stream in Video- und Audiobeispiele. Der AVI-Splitter kann bestimmen, welche Daten er besser benötigt als der Filter Async File Source und verwendet daher **IAsyncReader** anstelle von **IMemInputPin**.

Zum Anfordern von Daten vom Ausgabepin ruft der Eingabepin eine der folgenden Methoden auf:

-   [**IAsyncReader::Request**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-request)
-   [**IAsyncReader::SyncRead**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-syncread)
-   [**IAsyncReader::SyncReadAligned**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-syncreadaligned).

Die erste Methode ist asynchron, um mehrere überlappende Leses zu unterstützen. Die anderen sind synchron.

Theoretisch kann jeder Filter **IAsyncReader** unterstützen, aber in der Praxis ist er für Quellfilter konzipiert, die eine Verbindung mit Parserfiltern herstellen. Der Parser verhält sich sehr ähnlich wie ein Quellfilter im Pushmodell. Wenn er angehalten wird, wird ein Streamingthread erstellt, der Daten aus der **IAsyncReader-Verbindung** pullt und nachgeschaltet pusht. Die Ausgabepins verwenden **IMemInputPin,** und der Rest des Diagramms verwendet das Standardmäßige Pushmodell.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Daten Flow im Filter-Graph](data-flow-in-the-filter-graph.md)
</dt> </dl>

 

 



