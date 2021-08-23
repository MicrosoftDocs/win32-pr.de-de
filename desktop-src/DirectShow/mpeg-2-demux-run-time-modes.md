---
description: MPEG-2 Demux-Run-Time Modi
ms.assetid: b0d0c725-9220-43a5-af1c-d3c5c72e1ef3
title: MPEG-2 Demux-Run-Time Modi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0bffe5f58a18ae9e935985e8dae8dc340c3895bd2dc1a2a89965355832e701f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072964"
---
# <a name="mpeg-2-demux-run-time-modes"></a>MPEG-2 Demux-Run-Time Modi

Der [MPEG-2-Demultiplexer](mpeg-2-demultiplexer.md) ("demux") kann im Push- oder Pullmodus ausgeführt werden. Im Pushmodus stammen die Daten aus einer Livequelle, z. B. einer Netzwerkübertragung. Im Pullmodus stammen die Daten aus einer lokalen Datei.

-   Der Pullmodus ist in Windows XP und höher nur für Programmstreams verfügbar. Verwenden Sie auf downlevelbasierten Plattformen den [MPEG-2-Splitterfilter.](mpeg-2-splitter.md)
-   Der Pushmodus ist auf allen Plattformen verfügbar, sowohl für Programmstreams als auch für Transportstreams.

Demux unterstützt daher drei mögliche Modi: Programmstreams im Pullmodus, Programmstreams im Pushmodus und Transportstreams im Pushmodus. Die Demux bestimmt, welcher Modus zur Laufzeit verwendet werden soll. Der Modus wird bestimmt, wenn der Eingabepin eine Verbindung herstellt oder wenn der erste Ausgabepin konfiguriert ist, was zuerst geschieht:

-   Wenn der Eingabepin eine Verbindung herstellt: Windows XP und höher fragt der Demux den Upstreamfilter für die [**IAsyncReader-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) ab. Wenn der Upstreamfilter diese Schnittstelle verfügbar macht, konfiguriert sich der Demux für Programmstreams im Pullmodus. Andernfalls verwendet der Demux den Pushmodus, und der Medientyp bestimmt den Streamtyp (Programmstream oder Transportstream). Eine Liste der Eingabetypen finden Sie unter [**MPEG-2-Demultiplexer-Medientypen.**](mpeg-2-demultiplexer-media-types.md)
-   Wenn der erste Ausgabepin konfiguriert ist: Wenn Sie einen Ausgabepin erstellen und nach [**IMPEG2PIDMap**](/previous-versions/windows/desktop/api/Bdaiface/nn-bdaiface-impeg2pidmap)abfragen, konfiguriert sich der Demux für Transportstreams im Pushmodus. Wenn Sie den Pin für [**IMPEG2StreamIdMap**](/windows/desktop/api/Strmif/nn-strmif-impeg2streamidmap)abfragen, konfiguriert sich der Demux selbst für Programmstreams, auch im Pushmodus. Alle nachfolgenden Abfragen für die andere Schnittstelle führen zu einem Fehler, da die Demux nicht gleichzeitig in zwei Modi betrieben werden kann.

Nachdem sich der Demux für einen bestimmten Modus konfiguriert hat, verbleibt er in diesem Modus. Um einen anderen Modus zu verwenden, müssen Sie eine neue Instanz der Demux erstellen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden des MPEG-2-Demultiplexers](using-the-mpeg-2-demultiplexer.md)
</dt> </dl>

 

 



