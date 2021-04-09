---
description: Koordinaten Zuordnung in der VMR
ms.assetid: f0821b90-51d1-4e77-8aed-04337a3dd623
title: Koordinaten Zuordnung in der VMR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c18b38249471e6e68e36f1b9051f51e920f62b31
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103860112"
---
# <a name="coordinate-mapping-in-the-vmr"></a>Koordinaten Zuordnung in der VMR

In diesem Abschnitt werden die fünf Transformationen beschrieben, die auf ein Quell Abbild angewendet werden, bevor es von VMR auf das endgültige Ausgabe Bild zugeordnet wird.

1.  Die Transformation *T (src)* ordnet das Quell Rechteck dem Ziel Rechteck zu. Diese werden von den **rcSource** -und **rctarget** -Membern der [**videoinfoheader**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) -oder [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) -Struktur im Medientyp angegeben. Diese Zuordnung führt das Quell Abbild vor, wenn es an den VMR weitergeleitet wird.
2.  Die Transformation *T (Flag)* führt alle Bildmanipulationen aus, die von Flags im Medien Beispiel angegeben werden. Diese enthielten Transformationen, wie z. b. die vertikale Übersetzung und Skalierung, um die Bob-damit-Flags Die damit-Transformation verdoppelt die Bildhöhe und übersetzt das Bild möglicherweise um die Hälfte einer videolinie, wenn Sie sich im ungeraden Feld befindet.
3.  Die Transformation *T (AR)* passt das Bild basierend auf dem Bildseiten Verhältnis an quadratische Pixel an. Für **videoinfoheader** -Medientypen wird das Seitenverhältnis durch die Bildgröße bestimmt. Für **VIDEOINFOHEADER2** -Typen wird das Seitenverhältnis durch die Felder **dwpictaspectratiox** und **dwpictaspectratioy** bestimmt, es sei denn, die Felder amcontrol \_ Pad \_ auf \_ 16x9 oder amcontrol \_ Pad \_ bis \_ 4X3 werden festgelegt. Diese Transformation geht davon aus, dass die Anzeige Einstellung des Monitors mit dem physischen Seitenverhältnis des Monitors übereinstimmt. Wenn der Benutzer beispielsweise über einen Monitor mit 4 x 3-Seitenverhältnis verfügt, aber die Anzeige auf 1280 x 768 Pixel (5 x 3) festlegt, weist das Bild nicht das richtige Seitenverhältnis auf.
4.  Die Transformation *T (Mix)* transformiert das Bild innerhalb des Ziel Bilds und verwendet dabei die normalisierten Rechtecke, die in den [**ivmrmixercontrol**](/windows/desktop/api/Strmif/nn-strmif-ivmrmixercontrol) -Methoden angegeben sind. Mit den normalisierten Rechtecke kann die Anwendung organisieren, wie die Quelldaten Ströme zueinander positioniert und skaliert werden. Der VMR berechnet das Zielbild, indem es die maximalen Dimensionen aller Quell Images berechnet und jede innerhalb eines allgemeinen umgebenden Rechtecks zentriert. Den Ecken des umgebenden Rechtecks wird der Bereich (0,0) zugewiesen (1, 1). Das umgebende Rechteck wird vor dem Ausführen des Diagramms korrigiert und bleibt auch dann konstant, wenn Streams hinzugefügt oder gelöscht werden. Die Ziel Rechtecke für jeden Stream können außerhalb des Bereichs (0,0) bis (1, 1) liegen und sind immer noch gültig.
5.  Schließlich kann ein Teil des gemischten Bilds von der Zuordnung *T (DST)* transformiert werden, die von den Quell-und Ziel Rechtecke in der [**ibasicvideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) -Schnittstelle in der VMR festgelegt wird. Wenn die Allocator-Presenter ersetzt wird und die **ibasicvideo** -Schnittstelle nicht verwendet wird, muss die Anwendung die [**ivmrwindowlesscontrol**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol) -Schnittstelle implementieren und die Koordinaten wieder einem linearen 2D-Bereich zuordnen. Die an den DVD-Navigator zurückgegebenen Maus Koordinaten müssen sich ebenfalls in diesem Bereich befinden. Wenn eine Anwendung z. b. Video auf einem drehenden Cube rendert, würde Sie die gesamte Anzeige für das fensterlose Steuerelement zurückgeben und die Maus Koordinaten relativ zur Anzeige zurückgeben.

Die Transformation für das Gesamtbild von den Quelldaten zum endgültigen Renderer lautet wie folgt:

T = t (src) \* t (Flag) t (AR) t (Mix) \* t (DST)\*

\*dabei gibt an, dass das Bild in dieser Phase auf das Zielbild zugeschnitten werden konnte. Beachten Sie, dass es sich hierbei um affine Transformationen handelt, sodass die VMR Sie in einer einzigen Transformation kombinieren kann.

Die Umkehrung der Transformation ist:

![umgekehrte Transformation](images/vmrmapping-t-1.png)

Der Faktor t (src) t (Flag) t (AR) ist relativ zur Quell Auflösung. Im Faktor T (Mix) ist das normalisierte Quell Rechteck relativ zum Bild, das mit einem Aspekt korrigiert wurde. Das normalisierte Ziel Rechteck ist relativ zur Ausgabeauflösung. Das folgende Diagramm zeigt diese Beziehungen.

![Schritte zur Bild Transformation](images/vmrmapping-transform-steps.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von VMR für DirectShow-Filter Entwickler](using-the-vmr-for-directshow-filter-developers.md)
</dt> </dl>

 

 



