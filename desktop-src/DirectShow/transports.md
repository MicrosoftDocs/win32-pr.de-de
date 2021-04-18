---
description: Transportprotokolle
ms.assetid: 63c5ff5b-293d-4a80-92e8-3ece41321095
title: Transportprotokolle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c3d87ffacc871fc45ef1e8e645849afc956fb1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351733"
---
# <a name="transports"></a>Transportprotokolle

Um Mediendaten über das Filter Diagramm zu verschieben, muss ein DirectShow-Filter eines von mehreren möglichen Protokollen unterstützen. Diese Protokolle werden als Transporte bezeichnet. Wenn zwei Filter eine Verbindung herstellen, müssen Sie denselben Transport unterstützen. Andernfalls können Sie keine Mediendaten austauschen. In der Regel erfordert ein Transport, dass einer der Pins eine bestimmte Schnittstelle unterstützt. Wenn die Filter eine Verbindung herstellen, fragt eine PIN die andere nach der Schnittstelle ab.

Die meisten DirectShow-Filter enthalten Mediendaten im Hauptspeicher und übermitteln Sie an andere Filter über PIN-Verbindungen. Diese Art von Transport wird als lokaler Speicher Transport bezeichnet. Obwohl der lokale Speicher Transport der am häufigsten verwendete Transport in DirectShow ist, wird er nicht von allen Filtern verwendet. Beispielsweise werden von einigen Filtern Mediendaten an einem Hardware Pfad gesendet, und es werden nur Pins verwendet, um Steuerungsinformationen bereitzustellen. Informationen hierzu finden Sie beispielsweise in der [**IOverlay**](/windows/desktop/api/Strmif/nn-strmif-ioverlay) -Schnittstelle.

DirectShow definiert zwei Mechanismen für den lokalen Speicher Transport, das Push-Modell und das Pull-Modell. Im Push-Modell generiert ein Quell Filterdaten und übermittelt Sie an den nächsten Filter Downstream. Dieser Filter empfängt die Daten passiv, verarbeitet sie und sendet Sie weiter nach unten. Im Pull-Modell ist der Quell Filter mit einem Parserfilter verbunden. Der Parserfilter fordert Daten aus dem Quell Filter an. Der Quell Filter antwortet auf die Anforderungen, indem er Daten bereitstellt. Das Pushmodell verwendet die [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) -Schnittstelle, und das Pull-Modell verwendet die [**iasynkreader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) -Schnittstelle.

Das Push-Modell ist häufiger als das Pull-Modell. Daher wird von den folgenden Artikeln ein Push-Modell angenommen. Im letzten Artikel in diesem Abschnitt, [Pull Model](pull-model.md), wird beschrieben, wie die **iasynkreader** -Schnittstelle von **IMemInputPin** abweicht.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Datenfluss im Filter Diagramm](data-flow-in-the-filter-graph.md)
</dt> </dl>

 

 



