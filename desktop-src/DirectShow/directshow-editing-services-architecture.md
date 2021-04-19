---
description: Architektur der DirectShow-Bearbeitungs Dienste
ms.assetid: ba6cc3f1-9130-4197-8501-c2d0a088e847
title: Architektur der DirectShow-Bearbeitungs Dienste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85c6059eebe9228e61d3de9677972eedfcb51c62
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106345981"
---
# <a name="directshow-editing-services-architecture"></a>Architektur der DirectShow-Bearbeitungs Dienste

\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.\]

In der folgenden Abbildung ist die Architektur von [DirectShow-Bearbeitungs Diensten](directshow-editing-services.md) (de) dargestellt.

![Architektur der DirectShow-Bearbeitungs Dienste](images/architecture.png)

-   Timeline: stellt eine Videoproduktion als eine Auflistung von Quell Clips,-Übergängen und-Effekten dar, die in einer Reihe von untergeordneten Titeln angeordnet sind. Weitere Informationen finden Sie [im Zeitachsen Modell](the-timeline-model.md).
-   XML-Parser: analysiert die Zeitachse und generiert eine Ausgabedatei, oder liest eine Eingabedatei und generiert eine Zeitachse. DES unterstützt ein XML-basiertes Persistenzformat.
-   Rendering-Engine: übersetzt die Zeitachse in ein Formular, das als Streamingmedien gerendert werden kann. Standardmäßig erzeugt die Renderingengine ein DirectShow-Filter Diagramm (siehe nächster Abschnitt).
-   Medienlocator: verwaltet einen Cache von Speicherorten von Medien Elementen. Wenn der Versuch, ein Medien Element zu öffnen, fehlschlägt, verwendet des den Cache, um das-Element zu suchen, basierend auf einem erfolgreichen Öffnungs Verlauf.

Die Zeitachse ist eine abstrakte Beschreibung eines Video Bearbeitungs Projekts. Sie gibt die im Projekt verwendeten Quell Ausschnitte, Start-und Endzeiten, Effekte und Übergänge usw. an. Die Zeitachse stellt jedoch nicht die Video-und Audiostreams dar. Stattdessen übersetzt die Renderengine die Zeitachse für die Vorschau oder die Dateiausgabe in ein Filter Diagramm. Eine Anwendung bearbeitet die Zeitachse, anstatt das Filter Diagramm direkt zu bearbeiten, was mühsam und fehleranfällig wäre.

In der folgenden Tabelle sind die Hauptaufgaben aufgeführt, die eine typische Video Bearbeitungs Anwendung ausführt, sowie die Schnittstellen, die die einzelnen Aufgaben unterstützen. In späteren Abschnitten werden diese Aufgaben und die-Schnittstellen ausführlicher beschrieben.



| Aufgabe                                     | Schnittstelle (n)                                                                             |
|------------------------------------------|------------------------------------------------------------------------------------------|
| Erstellen oder ändern Sie eine Zeitachse.          | [**Iamtimeline**](iamtimeline.md) und die anderen **iamtimelinexxxx** -Schnittstellen          |
| Speichern und Laden von Projektdateien.             | [**IXml2Dex**](ixml2dex.md)                                                             |
| Anzeigen einer Vorschau eines Projekts oder schreiben in eine Datei. | " [**Unenderengine**](irenderengine.md)", " [ **ismartrenderengine** "](ismartrenderengine.md) |



 

Außerdem kann eine Anwendung einige oder alle der folgenden sekundären Tasks ausführen.



| Aufgabe                                                                                           | Schnittstelle (n)                                                                 |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| Abrufen von Informationen zu Mediendateien (Anzahl der Streams, Format und Dauer jedes Streams.) | [**Imediadet**](imediadet.md)                                               |
| Legen Sie Eigenschaften für Übergänge und Effekte fest.                                                     | [**Ipropertysetter**](ipropertysetter.md)                                   |
| Benachrichtigung erhalten, wenn während des Renderings Fehler auftreten.                                       | [**Iamseterrorlog**](iamseterrorlog.md), [ **iamerrorlog**](iamerrorlog.md) |
| Abrufen von Poster-Frames.                                                                        | [**Imediadet**](imediadet.md), [ **isamplegrabber**](isamplegrabber.md)     |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Einführung in DirectShow-Bearbeitungs Dienste](getting-started-with-directshow-editing-services.md)
</dt> </dl>

 

 



