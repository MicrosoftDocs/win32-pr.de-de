---
description: Informationen zu Render-Engines
ms.assetid: 80299b1a-09bf-4660-95d3-41a2b0074745
title: Informationen zu Render-Engines
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92a398cbe342ed2e92fc23e7da034dd69cae492208e3201b3419b3999594a135
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118664376"
---
# <a name="about-the-render-engines"></a>Informationen zu Render-Engines

\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht mehr verfügbar sein.\]

In diesem Artikel wird beschrieben, [wie DirectShow Editing Services](directshow-editing-services.md) (DES) ein Videobearbeitungsprojekt rendert.

In DES wird ein Projekt als Zeitachse dargestellt. Die Zeitachse ist nützlich, da sie die gängigsten Aufgaben bei der Videobearbeitung vereinfacht, z. B. das Neugeordneten von Quellclips und das Hinzufügen von Videoeffekten. Die DirectShow-Streamarchitektur erfordert dagegen ein Filterdiagramm. Daher müssen Sie zum Rendern Ihres Projekts eine Zeitachse in ein Filterdiagramm übersetzen. Die Komponente, die dies tut, wird als *Render-Engine bezeichnet.* DirectShow bietet zwei Render-Engines:

-   Einfache Render-Engine: Erstellt ein Filterdiagramm, das unkomprimierte Ausgaben liefert.
-   Intelligente Render-Engine: Erstellt ein Filterdiagramm, das komprimierte Ausgaben liefert.

Die intelligente Render-Engine verwendet die intelligente Rekomprimierung, um die Leistung zu verbessern. Bei der intelligenten Rekomprimierung werden Quelldateien nur dann erneut komprimiert, wenn sich das ursprüngliche Dateiformat vom endgültigen Ausgabeformat unterscheidet. Wenn die Formate übereinstimmen, wird die Quelle nie dekomprimiert. Die intelligente Rekomprimierung wird nur für die Videokomprimierung und nicht für die Audiokomprimierung unterstützt.

Verwenden Sie für die Vorschau die einfache Render-Engine. Die intelligente Render-Engine kann auch eine Vorschau anzeigen, aber weniger effizient, da sie den komprimierten Stream dekomprimieren muss. Verwenden Sie zum Schreiben von Dateien die intelligente Render-Engine, wenn Sie eine intelligente Neukomprimierung wünschen. Verwenden Sie andernfalls die einfache Render-Engine. Die intelligente Rekomprimierung kann die Zeit, die zum Schreiben der Datei benötigt wird, deutlich reduzieren.

> [!IMPORTANT]
> Verwenden Sie die intelligente Render-Engine nicht zum Lesen oder Schreiben Windows Mediendateien.

 

> [!IMPORTANT]
> Beide Render-Engines erstellen ein unsichtbares Fenster, das Nachrichten verarbeitet. Der Thread, der die Render-Engine erstellt, muss über eine Nachrichtenschleife verfügen, um Nachrichten zu senden. Außerdem darf dieser Thread erst beendet werden, wenn die Render-Engine und der Filter Graph-Manager freigegeben wurden. Andernfalls kann es zu einem Deadlock der Anwendung führen.

 

Erstellen des Graph

Das Filterdiagramm wird in zwei Phasen erstellt. In der ersten Phase erstellt die Render-Engine ein "Front-End", bei dem es sich um ein partielles Filterdiagramm handelt. Das folgende Diagramm veranschaulicht ein typisches Front-End:

![Filterdiagramm-Front-End](images/rendeng1.png)

Die Subsysteme enthalten verschiedene spezialisierte Filter, die die Render-Engine automatisch zusammenstellen kann. Das Front-End enthält einen Ausgabepin für jede Gruppe auf der Zeitachse. Die Ausgabepins liefern unkomprimierte Daten, wenn Sie die einfache Render-Engine verwenden, oder komprimierte Daten, wenn Sie die intelligente Render-Engine verwenden.

Im zweiten Schritt sind die Ausgabepins mit Renderingfiltern verbunden. Für die Vorschauversion sind die Renderingfilter Video- und Audiorenderer. Beim Schreiben von Dateien sind die Renderingfilter Multiplexerfilter (mux) und Dateiwriterfilter.

![Abschließen des Filterdiagramms](images/rendeng2.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vorschau einer Project](previewing-a-project.md)
</dt> <dt>

[Schreiben eines Project in eine Datei](writing-a-project-to-a-file.md)
</dt> </dl>

 

 



