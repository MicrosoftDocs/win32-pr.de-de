---
description: Einführung in DirectShow-Bearbeitungs Dienste
ms.assetid: 247c4ba9-53c1-46ed-83ef-a454351920e3
title: Einführung in DirectShow-Bearbeitungs Dienste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c75d9cf22eba81ebb9794310f63983b991bcf22
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481614"
---
# <a name="introduction-to-directshow-editing-services"></a>Einführung in DirectShow-Bearbeitungs Dienste

\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.\]

Der Kern von DirectShow ist eine leistungsstarke Architektur für die Verarbeitung von Streamingmedien. Eine Anwendung kann Sie zum Wiedergeben von multimediarewendungen verwenden, die in einer Vielzahl von Formaten erstellt wurden, ohne dass der Entwickler sich Gedanken über die Dateikomprimierung und andere mühsame Details machen muss. Vor [DirectShow-Bearbeitungs Diensten](directshow-editing-services.md) fehlte in DirectShow jedoch die für die nichtlineare Bearbeitung benötigte Flexibilität.

Angenommen, Sie möchten z. b. eine Videosequenz erstellen, die aus 4 Sekunden aus Quelle a besteht, gefolgt von 10 Sekunden von Quelle B und mit 5 Sekunden aus Quelle C. Dies kann sehr einfach durch die zentrale DirectShow-API erreicht werden.

Aber was ist, wenn Sie entschieden haben, dass Quelle C vor Quelle B und nicht nach die Sequenz sollte 8 Sekunden aus Quelle A, nicht 4, verwenden. und dass die gesamte Produktion eine separate Audiospur benötigt, die im Hintergrund gespielt wird? Auch kleinere Änderungen wie diese können schwierig zu implementieren sein. Das soeben beschriebene Szenario ist jedoch ein triviales Bearbeitungs Projekt in des – Sie können es mit einigen Methoden aufrufen.

Im folgenden finden Sie einige der Features, die von den DirectShow-Funktionen verwendet werden:

-   Ein Zeitachsen Modell, das Video-und Audiospuren in den in der Liste eingefügten Schichten organisiert, sodass die endgültige Produktion leicht bearbeitet werden kann
-   Die Möglichkeit, im Handumdrehen ein Videoprojekt anzuzeigen
-   Projekt Persistenz durch ein XML-basiertes Format
-   Unterstützung für Video-und Audioeffekte sowie Übergänge zwischen Videospuren (z. b. "Fades" und "Wipes")
-   Über 100 Standard-Wipes, wie von der Motion Picture-und TV Engineers (SMPTE) definiert
-   Schlüssel Erstellung basierend auf Hue, Leuchtkraft, RGB-Wert oder Alpha-Wert
-   Automatische Konvertierung von Frameraten und audiosamplings, sodass in einer Produktionsumgebung heterogene Quellen verwendet werden können
-   Ändern der Größe oder des schneidende eines Videos

Einschränkungen:

-   DES unterstützt keine MPEG-2-oder H. 264-Videoquellen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Bearbeitungs Dienste](directshow-editing-services.md)
</dt> </dl>

 

 



