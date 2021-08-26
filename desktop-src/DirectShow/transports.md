---
description: Transportprotokolle
ms.assetid: 63c5ff5b-293d-4a80-92e8-3ece41321095
title: Transportprotokolle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cb55542e87939168d1d95350fd71081833e4263f342a3e67c00a7c6814d51e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903720"
---
# <a name="transports"></a>Transportprotokolle

Um Mediendaten durch das Filterdiagramm zu verschieben, muss ein DirectShow-Filter eines von mehreren möglichen Protokollen unterstützen. Diese Protokolle werden als Transporte bezeichnet. Wenn zwei Filter eine Verbindung herstellen, müssen sie denselben Transport unterstützen. Andernfalls können sie keine Mediendaten austauschen. In der Regel erfordert ein Transport, dass einer der Pins eine bestimmte Schnittstelle unterstützt. Wenn die Filter eine Verbindung herstellen, fragt ein Pin den anderen nach der Schnittstelle ab.

Die meisten DirectShow-Filter enthalten Mediendaten im Hauptspeicher und stellen sie für andere Filter über Pinverbindungen hinweg zur Verfügung. Dieser Transporttyp wird als lokaler Speichertransport bezeichnet. Obwohl der lokale Speichertransport der gängigste Transport in DirectShow ist, wird er nicht von allen Filtern verwendet. Einige Filter senden z. B. Mediendaten entlang eines Hardwarepfads und verwenden Pins nur, um Steuerungsinformationen zu übermitteln. Sehen Sie sich beispielsweise die [**IOverlay-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ioverlay) an.

DirectShow definiert zwei Mechanismen für den lokalen Speichertransport: das Pushmodell und das Pullmodell. Im Pushmodell generiert ein Quellfilter Daten und übergibt sie an den nächsten Filter downstream. Dieser Filter empfängt die Daten passiv, verarbeitet sie und sendet sie weiter nachgeschaltet. Im Pullmodell ist der Quellfilter mit einem Parserfilter verbunden. Der Parserfilter fordert Daten vom Quellfilter an. Der Quellfilter antwortet auf die Anforderungen, indem er Daten liefert. Das Pushmodell verwendet die [**IMemInputPin-Schnittstelle,**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) und das Pullmodell verwendet die [**IAsyncReader-Schnittstelle.**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader)

Das Pushmodell ist häufiger als das Pullmodell. Daher wird in den folgenden Artikeln von einem Pushmodell ausgegangen. Im letzten Artikel in diesem Abschnitt, [PullModell,](pull-model.md)wird beschrieben, wie sich die **IAsyncReader-Schnittstelle** von **IMemInputPin unterscheidet.**

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Daten Flow im Filter-Graph](data-flow-in-the-filter-graph.md)
</dt> </dl>

 

 



