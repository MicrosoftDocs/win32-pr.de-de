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

Im Pushmodus macht der MPEG-2-Demultiplexer (demux) die [**IReferenceClock-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) verfügbar. Sie fungiert als Livequelle, sodass sie standardmäßig als Graphverweisuhr ausgewählt wird. Weitere Informationen finden Sie unter [Livequellen.](live-sources.md)

-   Bei Transportstreams synchronisiert die Demux-Datei ihre Uhr mit dem PCR-Datenstrom, der dem Audio- oder Videodatenstrom entspricht, der zuletzt von der Anwendung zugeordnet wurde. Intern verfolgt die Demux die PAT- und PMT-Tabellen nach. Wenn die Anwendung eine elementare Datenstrom-PID einem Ausgabepin zusieht, sucht die Demux den PCR-Datenstrom für diese PID und verwendet diesen PCR-Datenstrom. (Derzeit gibt es für die Anwendung keine Möglichkeit, die PCR-PID direkt anzugeben.)
-   Bei Programmstreams synchronisiert die Demux-Datei ihre Uhr mit dem SCR-Stream.

Durch das Synchronisieren der Filteruhr mit dem PCR- oder SCR-Stream wird ein Datenüberlauf oder -unterlauf verhindert. Dies kann dazu führen, dass die Graphuhr von der Streamuhr abstammt. Die Demux übersetzt auch PES-PTS-Werte in DirectShow-Referenzzeiten und verwendet diese Werte, um die Medienbeispiele mit einem Zeitstempel zu versehen. Die Zeitstempel gelten für die nächste Framegrenze. es gibt keine Garantie dafür, dass die Framegrenze am Anfang des Medienbeispiels ausgerichtet ist.

Die Demux garantiert, dass sich die Zeitstempel monoton erhöhen. Dies bedeutet beispielsweise, dass, wenn ein Transportdatenstrom ein Segment enthält, z. B. ein kommerzielles, das mit einer anderen Uhr als dem Hauptprogramm erstellt wurde, die Präsentationszeitstempel so angepasst wird, dass die Zeitausbruchzeit von Downstreamfiltern ausgeblendet wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden des MPEG-2-Demultiplexers](using-the-mpeg-2-demultiplexer.md)
</dt> </dl>

 

 



