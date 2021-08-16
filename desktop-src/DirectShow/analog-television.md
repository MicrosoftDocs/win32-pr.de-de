---
description: Analog Tv
ms.assetid: 9f2c18ec-3684-42a8-a3df-5f8827b27642
title: Analog Tv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 886c2b3f93ca70fb4a533f131611431c4a15df51169f70ed49f321c0ccfc8c2d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117824758"
---
# <a name="analog-television"></a>Analog Tv

Analoge Fernsehsendungen unterscheiden sich von anderen Videoaufnahmeszenarien auf unterschiedliche Weise:

-   Die Tunerkarte wird auf ein analoges Signal optimiert, das dann digitalisiert wird.
-   Audiodaten werden im analogen Signal verwendet. Wie die Audiodaten die Soundkarte erreichen, hängt von der Hardware ab.
-   Das Signal kann zusätzliche Daten im vertikalen Leerungsintervall (Vertical Blanking Interval, VBI) enthalten, z. B. Untertitel (Closed Captions, CC), World Standard Teletext (WST) und erweiterte Datendienste (XDS).

Das folgende Diagramm zeigt ein typisches Filterdiagramm für die Fernsehvorschau.

![analoger Fernsehgraph](images/vidcap06.png)

-   Der [TV-Tuner-Filter](tv-tuner-filter.md) steuert die Optimierung.
-   Der [Filter TV Audio](tv-audio-filter.md) steuert die Audiodecodierung.
-   Wenn die Tunerkarte über mehrere physische Eingaben verfügt, kann die Anwendung mit dem [Analog Video Crossbar-Filter](analog-video-crossbar-filter.md) auswählen, welche Eingabe decodiert und gerendert wird.
-   Der [WDM-Videoerfassungsfilter](wdm-video-capture-filter.md) stellt den digitalisierten Videodatenstrom zur Datenstroms.

Der Capture Graph Builder fügt automatisch alle Filter ein, die vor dem Erfassungsfilter erforderlich sind.

Dieser Abschnitt enthält die folgenden Themen:

-   [Analoge Fernsehoptimierung](analog-television-tuning.md)
-   [Analoge Fernsehaudiodaten](analog-television-audio.md)
-   [Untertitel und Teletext](closed-captions-and-teletext.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Videoaufnahme](video-capture.md)
</dt> </dl>

 

 



