---
description: Informationen zu DirectShow-Filtern
ms.assetid: 57b7d32e-2073-46a2-91ec-a34072134489
title: Informationen zu DirectShow-Filtern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cef947fdcec8cc1c01d23d09bce1b46d5b4d7d2268fe1d7cd6df6a57b54d42ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118664465"
---
# <a name="about-directshow-filters"></a>Informationen zu DirectShow-Filtern

DirectShow verwendet eine modulare Architektur, bei der jede Verarbeitungsphase von einem COM-Objekt durchgeführt wird, das als Filter bezeichnet wird. DirectShow bietet eine Reihe von Standardfiltern für anwendungen, die verwendet werden können, und Entwickler können eigene benutzerdefinierte Filter schreiben, die die Funktionalität von DirectShow erweitern. Zur Veranschaulichung sind die folgenden Schritte erforderlich, um eine AVI-Videodatei sowie die Filter wieder zu spielen, die die einzelnen Schritte ausführen:

-   Liest die Rohdaten aus der Datei als Bytestream (Dateiquellenfilter).
-   Untersuchen Sie die AVI-Header, und analysieren Sie den Bytedatenstrom in separate Videoframes und Audiobeispiele (AVI-Splitterfilter).
-   Decodieren Sie die Videoframes (verschiedene Decoderfilter, je nach Komprimierungsformat).
-   Zeichnen der Videoframes (Videorendererfilter)
-   Senden Sie die Audiobeispiele an die Soundkarte (Standardfilter für DirectSound-Geräte).

Diese Filter sind im folgenden Diagramm dargestellt.

![Filterdiagramm für die Wiedergabe einer Avi-Datei mit komprimiertem Video](images/avi-filter-graph.png)

Wie das Diagramm zeigt, ist jeder Filter mit mindestens einem anderen Filter verbunden. Die Verbindungspunkte sind auch COM-Objekte, die als *Pins bezeichnet werden.* Filter verwenden Stecknadeln, um Daten aus einem Filter im nächsten Filter zu verschieben. Die Pfeile im Diagramm zeigen die Richtung, in der sich die Daten bewegen. In DirectShow wird eine Reihe von Filtern als *Filterdiagramm bezeichnet.*

Filter haben drei mögliche Zustände: Wird ausgeführt, beendet und angehalten. Wenn ein Filter ausgeführt wird, werden Mediendaten verarbeitet. Wenn sie beendet wird, wird die Verarbeitung von Daten beendet. Der angehaltene Zustand wird verwendet, um Daten vor der Ausführung zu cue; Im Abschnitt [Data Flow in der Filter-Graph](data-flow-in-the-filter-graph.md) wird dieses Konzept ausführlicher beschrieben. Mit sehr seltenen Ausnahmen werden Zustandsänderungen im gesamten Filterdiagramm koordiniert. alle Filter im Diagramm wechseln die Zustände im Unisono. Daher wird das gesamte Filterdiagramm auch als ausgeführt, beendet oder angehalten bezeichnet.

Filter können in mehrere allgemeine Kategorien unterteilt werden:

-   Ein *Quellfilter* führt Daten in das Diagramm ein. Die Daten können aus einer Datei, einem Netzwerk, einer Kamera oder an einem anderen Ort stammen. Jeder Quellfilter verarbeitet einen anderen Datenquellentyp.
-   Ein *Transformationsfilter* verwendet einen Eingabestream, verarbeitet die Daten und erstellt einen Ausgabestream. Encoder und Decoder sind Beispiele für Transformationsfilter.
-   *Rendererfilter* werden am Ende der Kette verwendet. Sie empfangen Daten und stellen sie dem Benutzer vor. Ein Videorenderer zeichnet beispielsweise Videoframes auf der Anzeige. Ein Audiorenderer sendet Audiodaten an die Soundkarte. und ein Dateiwriterfilter schreibt Daten in eine Datei.
-   Ein *Splitterfilter* teilt einen Eingabestream in zwei oder mehr Ausgaben auf, in der Regel wird der Eingabestream dabei analyset. Beispielsweise analysiert der AVI-Splitter einen Bytestream in separate Video- und Audiostreams.
-   Ein *Muxfilter* verwendet mehrere Eingaben und kombiniert sie in einem einzigen Stream. Beispielsweise führt der AVI Mux den umgekehrten Vorgang des AVI-Splitters aus. Es verwendet Audio- und Videostreams und erzeugt einen BYTE-Stream im AVI-Format.

Die Unterschiede zwischen diesen Kategorien sind nicht absolut. Beispielsweise fungiert der ASF-Readerfilter sowohl als Quellfilter als auch als Splitterfilter.

Alle DirectShow-Filter machen die [**IBaseFilter-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) verfügbar, und alle Pins machen die [**IPin-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ipin) verfügbar. DirectShow definiert auch viele weitere Schnittstellen, die spezifischere Funktionen unterstützen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zum Filter Graph Manager](about-the-filter-graph-manager.md)
</dt> <dt>

[Daten Flow im Filter-Graph](data-flow-in-the-filter-graph.md)
</dt> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> </dl>

 

 



