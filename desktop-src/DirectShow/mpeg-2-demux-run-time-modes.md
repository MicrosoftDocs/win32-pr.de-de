---
description: MPEG-2-Demux-Run-Time Modi
ms.assetid: b0d0c725-9220-43a5-af1c-d3c5c72e1ef3
title: MPEG-2-Demux-Run-Time Modi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6e4e7a1dea0bfeccd60d8680a31b99cc10271ee
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125216"
---
# <a name="mpeg-2-demux-run-time-modes"></a>MPEG-2-Demux-Run-Time Modi

Der [MPEG-2-Demultiplexer](mpeg-2-demultiplexer.md) ("demux") kann im Pushmodus oder Pullmodus verwendet werden. Im Pushmodus stammen die Daten aus einer Live Quelle, z. b. einem Netzwerk Broadcast. Im Pullmodus stammen die Daten aus einer lokalen Datei.

-   Der Pull-Modus ist in Windows XP und höher für Programm Datenströme verfügbar. Verwenden Sie auf untergeordneten Plattformen den [MPEG-2-Splitter](mpeg-2-splitter.md) Filter.
-   Der Pushmodus ist auf allen Plattformen sowohl für Programmstreams als auch für Transport Datenströme verfügbar.

Das Demux unterstützt daher drei mögliche Modi: Programmstreams im Pullmodus, Programmstreams im Pushmodus und Transportstreams im Pushmodus. Der Demux-Wert bestimmt, welcher Modus zur Laufzeit verwendet werden soll. Der Modus wird bestimmt, wenn die eingabepin eine Verbindung herstellt oder wenn die erste Ausgabepin konfiguriert ist, je nachdem, welcher Vorgang zuerst erfolgt

-   Wenn die eingabepin eine Verbindung herstellt: unter Windows XP und höher fragt Demux den upstreamfilter für die [**iasynkreader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) -Schnittstelle ab. Wenn der upstreamfilter diese Schnittstelle verfügbar macht, konfiguriert sich der Demux selbst für Programmstreams im Pullmodus. Andernfalls verwendet der Demux den Pushmodus, und der Medientyp bestimmt den Streamtyp (Programmstream oder Transportstream). Eine Liste der Eingabetypen finden Sie unter [**MPEG-2 Demultiplexer-Medientypen**](mpeg-2-demultiplexer-media-types.md) .
-   Wenn die erste Ausgabepin konfiguriert ist: Wenn Sie eine Ausgabepin erstellen und Sie nach [**IMPEG2PIDMap**](/previous-versions/windows/desktop/api/Bdaiface/nn-bdaiface-impeg2pidmap)Abfragen, konfiguriert die Demux sich selbst für Transportstreams im Pushmodus. Wenn Sie die PIN für [**IMPEG2StreamIdMap**](/windows/desktop/api/Strmif/nn-strmif-impeg2streamidmap)Abfragen, konfiguriert die Demux sich selbst für Programmstreams, auch im Pushmodus. Alle nachfolgenden Abfragen für die andere Schnittstelle schlagen fehl, da die Demux nicht gleichzeitig in zwei Modi betrieben werden kann.

Sobald die Demux sich für einen bestimmten Modus konfiguriert hat, bleibt Sie in diesem Modus. Um einen anderen Modus zu verwenden, müssen Sie eine neue Instanz der Demux-Instanz erstellen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von MPEG-2 Demultiplexer](using-the-mpeg-2-demultiplexer.md)
</dt> </dl>

 

 



