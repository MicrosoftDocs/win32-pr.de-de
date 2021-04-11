---
description: Verhalten der Demux-Uhr
ms.assetid: c8a067f7-4e4c-4f25-b26c-f6bb048060b0
title: Verhalten der Demux-Uhr
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9065e6da51acb5387ca06bf921d5cdc91c567843
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104041243"
---
# <a name="demux-clock-behavior"></a>Verhalten der Demux-Uhr

Im Pushmodus macht der MPEG-2-Demultiplexer (Demux) die [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) -Schnittstelle verfügbar. Er fungiert als Live Quelle und wird daher standardmäßig als Graph-verweiszeit ausgewählt. Weitere Informationen finden Sie unter [Live Quellen](live-sources.md) .

-   Bei Transportstreams synchronisiert die Demux die Uhr mit dem PCR-Stream, der dem Audiostream oder Videostream entspricht, der zuletzt von der Anwendung zugeordnet wurde. Intern werden die Tabellen Pat und PMT von der "Debug"-Tabelle nachverfolgt. Wenn die Anwendung einer Ausgabe-PIN eine elementare Datenstrom-PID zuordnet, sucht der Demux den PCR-Stream für diese PID und verwendet diesen PCR-Stream. (Derzeit gibt es für die Anwendung keine Möglichkeit, die PCR-PID direkt anzugeben.)
-   Bei Programmstreams synchronisiert die Demux die Uhr mit dem SCR-Stream.

Durch die Synchronisierung der filteruhr mit dem PCR-oder SCR-Stream wird ein Überlauf oder Unterlauf von Daten verhindert Der Wert von "Debug" übersetzt außerdem die Werte von "PES PTS" in "DirectShow Reference Times" und verwendet diese Werte zum Zeitstempel der Medien Beispiele. Die Zeitstempel gelten für die nächste Frame Grenze. Es gibt keine Garantie, dass die Rahmen Grenze am Anfang des Medien Beispiels ausgerichtet wird.

Die "Debug" gewährleistet, dass die Zeitstempel monoton zunehmen. Dies bedeutet beispielsweise Folgendes: Wenn ein Transportstream ein Segment enthält, z. b. ein kommerzieller, das mit einer anderen Uhr als das Hauptprogramm erstellt wurde, passt die Demux die Präsentationszeit Stempel an, um die Zeit Diskontinuität von downstreamfiltern zu verbergen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von MPEG-2 Demultiplexer](using-the-mpeg-2-demultiplexer.md)
</dt> </dl>

 

 



