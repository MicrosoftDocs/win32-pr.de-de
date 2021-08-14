---
description: Demux-Uhrverhalten
ms.assetid: c8a067f7-4e4c-4f25-b26c-f6bb048060b0
title: Demux-Uhrverhalten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06ab1976bf123e971f6c3ec08e18c743352d37b73de95901a67abfee5d10a054
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117821185"
---
# <a name="demux-clock-behavior"></a>Demux-Uhrverhalten

Im Pushmodus macht der MPEG-2-Demultiplexer (demux) die [**IReferenceClock-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) verfügbar. Sie fungiert als Livequelle und wird standardmäßig als Graphreferenzuhr ausgewählt. Weitere [Informationen finden Sie](live-sources.md) unter Livequellen.

-   Bei Transportstreams synchronisiert der Demux seine Uhr mit dem PCR-Datenstrom, der dem Audio- oder Videostream entspricht, der zuletzt von der Anwendung zugeordnet wurde. Intern verfolgt der Demux die PAT- und PMT-Tabellen nach. Wenn die Anwendung eine elementare Datenstrom-PID einem Ausgabepin zuteilt, sucht die Demux nach dem PCR-Datenstrom für diese PID und verwendet diesen PCR-Stream. (Derzeit gibt es keine Möglichkeit für die Anwendung, die PCR-PID direkt anzugeben.)
-   Bei Programmstreams synchronisiert der Demux seine Uhr mit dem SCR-Stream.

Durch die Synchronisierung der Filteruhr mit dem PCR- oder DEMB-Datenstrom wird ein Datenüberlauf oder -unterlauf verhindert. Dies kann dazu führen, dass die Graphuhr von der Streamuhr abläuft. Der Demux übersetzt außerdem PES PTS-Werte in DirectShow-Referenzzeiten und verwendet diese Werte, um die Medienbeispiele mit einem Zeitstempel zu versehen. Die Zeitstempel gelten für die nächste Rahmengrenze. es gibt keine Garantie, dass die Rahmengrenze am Anfang des Medienbeispiels ausgerichtet wird.

Die Demux garantiert, dass die Zeitstempel monoton erhöht werden. Dies bedeutet beispielsweise, dass die Demux die Präsentationszeitstempel an die Präsentationszeitstempel anpassen, um die Unterbrechung der Zeit vor Downstreamfiltern auszublenden, wenn ein Transportstream ein Segment enthält, z. B. einen Kommerziellen, der mit einer anderen Uhr als dem Hauptprogramm erstellt wurde.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden des MPEG-2-Demultiplexers](using-the-mpeg-2-demultiplexer.md)
</dt> </dl>

 

 



