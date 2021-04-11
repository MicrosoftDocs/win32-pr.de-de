---
description: Analog Fernsehen
ms.assetid: 9f2c18ec-3684-42a8-a3df-5f8827b27642
title: Analog Fernsehen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33af8ba94831afed59d783598dbf6bc0eaee0ec6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124250"
---
# <a name="analog-television"></a>Analog Fernsehen

Das analoge Fernsehen unterscheidet sich auf verschiedene Arten von anderen Video Erfassungs Szenarien:

-   Die Tuner-Karte wird auf ein analoges Signal optimiert, das dann digitalisiert wird.
-   Audiodaten werden im analogen Signal übertragen. Wie die Audiokarte die Audiokarte erreicht, hängt von der Hardware ab.
-   Das Signal enthält möglicherweise zusätzliche Daten im vertikalen Auslassungs Intervall (VBI), wie z. b. gesperrte Untertitel (CC), World Standard Teletext (WST) und erweiterte Datendienste (XDS).

Das folgende Diagramm zeigt ein typisches Filter Diagramm für die Fernseh Vorschau.

![Analog Fernseh Diagramm](images/vidcap06.png)

-   Der [TV-Tuner-](tv-tuner-filter.md) Filter steuert die Optimierung.
-   Der [TV-Audiofilter](tv-audio-filter.md) steuert die Audiodecodierung.
-   Wenn die Tuner-Karte über mehr als eine physische Eingabe verfügt, kann die Anwendung mithilfe des [Querbalken Filters für analoge Video](analog-video-crossbar-filter.md) auswählen, welche Eingabe decodiert und gerendert wird.
-   Der [WDM-Video Erfassungs](wdm-video-capture-filter.md) Filter liefert den digitalisierten Videostream.

Der Erfassungs Diagramm-Generator fügt automatisch alle erforderlichen Filter aus dem Erfassungs Filter ein.

Dieser Abschnitt enthält die folgenden Themen:

-   [Optimierung des analogen Fernseh ERS](analog-television-tuning.md)
-   [Analog zum Fernsehgerät](analog-television-audio.md)
-   [Untertitel und Teletext](closed-captions-and-teletext.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Video Erfassung](video-capture.md)
</dt> </dl>

 

 



