---
description: Informationen zu den renderengines
ms.assetid: 80299b1a-09bf-4660-95d3-41a2b0074745
title: Informationen zu den renderengines
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70fe3a9956bee0d167de9e6618187bfd1f2a6e39
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522235"
---
# <a name="about-the-render-engines"></a>Informationen zu den renderengines

\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.\]

In diesem Artikel wird beschrieben, wie [DirectShow-Bearbeitungs Dienste](directshow-editing-services.md) (des) ein Video Bearbeitungs Projekt rendern.

In des wird ein Projekt als Zeitachse dargestellt. Die Zeitachse ist nützlich, da Sie die gängigsten Aufgaben bei der Videobearbeitung vereinfacht, z. b. das Ändern von Quell Clips und das Hinzufügen von Video Effekten Die DirectShow-streamarchitektur erfordert dagegen ein Filter Diagramm. Daher müssen Sie zum Rendering des Projekts eine Zeitachse in ein Filter Diagramm übersetzen. Die Komponente, die dies bewirkt, wird als *Rendering-Engine* bezeichnet. DirectShow bietet zwei renderengines:

-   Grundlegende Rendering-Engine: erstellt ein Filter Diagramm, das eine nicht komprimierte Ausgabe bereitstellt.
-   Smart-Rendering-Engine: erstellt ein Filter Diagramm, das eine komprimierte Ausgabe bereitstellt.

Die Smart-Rendering-Engine verwendet die intelligente Neukomprimierung zur Verbesserung der Leistung. Bei der intelligenten Neukomprimierung werden Quelldateien nur dann erneut komprimiert, wenn sich das ursprüngliche Dateiformat vom endgültigen Ausgabeformat unterscheidet. Wenn die Formate Stimmen, wird die Quelle nie entpackt. Die intelligente Neukomprimierung wird nur für die Video Komprimierung und nicht für die Audiokomprimierung unterstützt.

Verwenden Sie für die Vorschauversion die einfache Renderingengine. Die intelligente Renderingengine kann auch eine Vorschau anzeigen, aber weniger effizient, da Sie den komprimierten Datenstrom dekomprimieren muss. Verwenden Sie zum Schreiben von Dateien die Smart-Rendering-Engine, wenn Sie eine intelligente Neukomprimierung wünschen. Verwenden Sie andernfalls die einfache Renderingengine. Die intelligente Neukomprimierung kann den Zeitaufwand für das Schreiben der Datei erheblich verkürzen.

> [!IMPORTANT]
> Verwenden Sie die Smart-Rendering-Engine nicht zum Lesen oder Schreiben von Windows Media-Dateien.

 

> [!IMPORTANT]
> Beide renderingengines erstellen ein unsichtbares Fenster, das Nachrichten verarbeitet. Der Thread, der die Renderingengine erstellt, muss über eine Nachrichten Schleife verfügen, um Nachrichten zu senden. Außerdem darf der Thread erst beendet werden, wenn die Renderingengine und der Filter-Graph-Manager freigegeben werden. Andernfalls könnte die Anwendung einen Deadlock verursachen.

 

Erstellen des Filter Diagramms

Das Filter Diagramm wird in zwei Phasen erstellt. In der ersten Phase erstellt die Renderengine ein "Front-End", bei dem es sich um ein partielles Filter Diagramm handelt. Das folgende Diagramm veranschaulicht ein typisches Front-End:

![Diagramm-Front-End Filtern](images/rendeng1.png)

Die Subsysteme enthalten verschiedene spezialisierte Filter, die von der Rendering-Engine automatisch assembliert werden. Das Front-End enthält eine Ausgabe-PIN für jede Gruppe in der Zeitachse. Die Ausgabe Pins liefern unkomprimierte Daten, wenn Sie die einfache Renderingengine verwenden, oder komprimierte Daten, wenn Sie die Smart-Rendering-Engine verwenden.

Im zweiten Schritt werden die Ausgabe Pins mit renderingfiltern verbunden. In der Vorschau sind Renderfilter Video-und audiorenderer. Beim Schreiben von Dateien sind die renderingfilter Multiplexer-Filter (MUX) und dateiwriter-Filter.

![Vervollständigen des Filter Diagramms](images/rendeng2.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Anzeigen einer Vorschau eines Projekts](previewing-a-project.md)
</dt> <dt>

[Schreiben eines Projekts in eine Datei](writing-a-project-to-a-file.md)
</dt> </dl>

 

 



