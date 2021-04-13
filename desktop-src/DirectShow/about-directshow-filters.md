---
description: Informationen zu DirectShow-Filtern
ms.assetid: 57b7d32e-2073-46a2-91ec-a34072134489
title: Informationen zu DirectShow-Filtern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11ddfb5dda550bee88c42ef70347c95ba7a2b003
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104568985"
---
# <a name="about-directshow-filters"></a>Informationen zu DirectShow-Filtern

DirectShow verwendet eine modulare Architektur, in der jede Phase der Verarbeitung von einem COM-Objekt, das als Filter bezeichnet wird, durchgeführt wird. DirectShow stellt eine Reihe von Standardfiltern für die zu verwendenden Anwendungen bereit. Entwickler können eigene benutzerdefinierte Filter schreiben, mit denen die Funktionalität von DirectShow erweitert wird. Um dies zu veranschaulichen, führen Sie die folgenden Schritte aus, um eine AVI-Videodatei zusammen mit den Filtern für die einzelnen Schritte auszuführen:

-   Liest die Rohdaten aus der Datei als Bytestream (Datei Quell Filter).
-   Überprüfen Sie die AVI-Header, und analysieren Sie den Bytestream in separate Video Frames und Audiobeispiele (avi-Splitter Filter).
-   Decodieren der Video Frames (verschiedene Decoder-Filter, abhängig vom Komprimierungs Format).
-   Zeichnen Sie die Videorahmen (Videorenderer-Filter).
-   Senden Sie die Audiobeispiele an die Soundkarte (standardmäßiger DirectSound-Geräte Filter).

Diese Filter sind in der folgenden Abbildung dargestellt.

![Diagramm für die Wiedergabe einer AVI-Datei mit komprimiertem Video Filtern](images/avi-filter-graph.png)

Wie das Diagramm zeigt, ist jeder Filter mit einem oder mehreren anderen Filtern verbunden. Die Verbindungspunkte sind auch com-Objekte, die als *Pins* bezeichnet werden. Filter verwenden Pins zum Verschieben von Daten aus einem der nächsten Filter. Die Pfeile in der Abbildung zeigen die Richtung an, in der die Daten verschoben werden. In DirectShow wird ein Satz von Filtern als *Filter Diagramm* bezeichnet.

Filter haben drei mögliche Zustände: "wird ausgeführt", "beendet" und "angehalten". Wenn ein Filter ausgeführt wird, werden Mediendaten verarbeitet. Wenn Sie beendet wird, wird die Datenverarbeitung beendet. Der angehaltene Zustand wird verwendet, um Daten vor dem ausführen zu überführen. im Abschnitt [Datenfluss im Filter Diagramm](data-flow-in-the-filter-graph.md) wird dieses Konzept ausführlicher beschrieben. Bei sehr seltenen Ausnahmen werden Zustandsänderungen im gesamten Filter Diagramm koordiniert. Alle Filter im Graph-Switch werden im Unison-Zustand angezeigt. Daher wird auch das gesamte Filter Diagramm ausgeführt, beendet oder angehalten.

Filter können in verschiedene allgemeine Kategorien eingeteilt werden:

-   Ein *Quell* Filter führt Daten in das Diagramm ein. Die Daten können aus einer Datei, einem Netzwerk, einer Kamera oder einer beliebigen anderen Stelle stammen. Jeder Quell Filter behandelt einen anderen Daten Quellentyp.
-   Ein *Transformations* Filter nimmt einen Eingabestream an, verarbeitet die Daten und erstellt einen Ausgabestream. Encoder und Decoder sind Beispiele für Transformations Filter.
-   *Rendererfilter* befinden sich am Ende der Kette. Sie empfangen Daten und stellen Sie dem Benutzer zur Verfügung. Ein Videorenderer zeichnet z. b. Video Frames auf der Anzeige. ein audiorenderer sendet Audiodaten an die Soundkarte. und ein dateiwriter-Filter schreibt Daten in eine Datei.
-   Ein *Splitter* Filter teilt einen Eingabedaten Strom in zwei oder mehr Ausgaben auf, wobei in der Regel der Eingabedaten Strom gleichzeitig verarbeitet wird. Beispielsweise analysiert der avi-Splitter einen Bytestream in separate Video-und Audiodatenströme.
-   Ein *MUX* -Filter nimmt mehrere Eingaben an und kombiniert Sie in einem einzelnen Datenstrom. Beispielsweise führt der AVI MUX den umgekehrten Vorgang des AVI-Splitters durch. Er nimmt Audiodaten und Videostreams an und erzeugt einen Bytestream mit AVI-Formatierung.

Die Unterschiede zwischen diesen Kategorien sind nicht absolut. Der ASF-Reader-Filter fungiert z. b. sowohl als Quell Filter als auch als Splitter Filter.

Alle DirectShow-Filter machen die [**ibasefilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) -Schnittstelle verfügbar, und alle Pins machen die [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) -Schnittstelle verfügbar. DirectShow definiert auch viele andere Schnittstellen, die spezifischere Funktionen unterstützen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zum Filter Graph-Manager](about-the-filter-graph-manager.md)
</dt> <dt>

[Datenfluss im Filter Diagramm](data-flow-in-the-filter-graph.md)
</dt> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> </dl>

 

 



