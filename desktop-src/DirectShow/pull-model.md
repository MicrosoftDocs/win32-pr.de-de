---
description: Pull-Modell
ms.assetid: b5246dfe-e6ee-4b91-bfe3-2ec8b8723938
title: Pull-Modell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8dd4becd54bffb39acf30b6d29fca45e6a117989
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521344"
---
# <a name="pull-model"></a>Pull-Modell

In der [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) -Schnittstelle bestimmt der Upstream-Filter, welche Daten gesendet werden sollen, und überträgt die Daten an den downstreamfilter. Für einige Filter ist ein *Pull* -Modell besser geeignet. Hier fordert der Downstream-Filterdaten aus dem upstreamfilter an. Die Beispiele sind nach dem Wechsel nach unten, von der Ausgabe-Pin bis zur Eingabe-PIN, aber der Downstream-Filter initiiert den Datenfluss Dieser Verbindungstyp verwendet die [**iasynkreader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) -Schnittstelle.

Die typische Verwendung für das Pull-Modell ist die Dateiwiedergabe. Beispielsweise führt der asynchrone [Datei Quell](file-source--async--filter.md) Filter in einem AVI-Wiedergabe Diagramm generische Datei Lesevorgänge durch und übermittelt die Daten als Bytestream ohne Formatinformationen. Der [avi-Splitter](avi-splitter-filter.md) Filter liest die AVI-Header und analysiert den Stream in Video-und Audiobeispiele. Der avi-Splitter kann ermitteln, welche Daten Sie besser benötigen als der asynchrone Quell Filter für Dateien, weshalb er anstelle von **IMemInputPin** **iasynkreader** verwendet.

Um Daten aus dem Ausgabepin anzufordern, ruft die Eingabe-PIN eine der folgenden Methoden auf:

-   [**Iasynkreader:: Request**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-request)
-   [**Iasynkreader:: synkread**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-syncread)
-   [**Iasynkreader:: synkreadausgerichtete**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-syncreadaligned).

Die erste Methode ist asynchron, um mehrere überlappende Lesevorgänge zu unterstützen. Die anderen sind synchron.

Theoretisch kann ein beliebiger Filter **iasynkreader** unterstützen, in der Praxis ist er jedoch für Quell Filter konzipiert, die eine Verbindung mit Parserfiltern herstellen. Der Parser verhält sich sehr ähnlich wie der Quell Filter im Push-Modell. Wenn er angehalten wird, erstellt er einen streamingindthread, der Daten aus der **iasynkreader** -Verbindung abruft und diese nach unten verschiebt. Die Ausgabe Pins verwenden **IMemInputPin**, und der Rest des Diagramms verwendet das Standard-Push-Modell.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Datenfluss im Filter Diagramm](data-flow-in-the-filter-graph.md)
</dt> </dl>

 

 



