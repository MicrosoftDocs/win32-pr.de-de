---
description: Koordinatenzuordnung in der VMR
ms.assetid: f0821b90-51d1-4e77-8aed-04337a3dd623
title: Koordinatenzuordnung in der VMR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad128e4d4e40fe3141f0b23edde1e06df8c5044e0a9877e2d9a2fcc3f293a9fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073794"
---
# <a name="coordinate-mapping-in-the-vmr"></a>Koordinatenzuordnung in der VMR

In diesem Abschnitt werden die fünf Transformationen beschrieben, die auf ein Quellimage angewendet werden, bevor es von der VMR dem endgültigen Ausgabeimage zugeordnet wird.

1.  Die Transformation *T(Src)* ordnet das Quellrechteck dem Zielrechteck zu. Diese werden von den **rcSource-** und **rcTarget-Membern** der [**VIDEOINFOHEADER-**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) oder [**VIDEOINFOHEADER2-Struktur**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) im Medientyp angegeben. Durch diese Zuordnung wird das Quellimage vorverarbeitet, wenn es an die VMR übergeben wird.
2.  Die Transformation *T(Flag)* führt alle Bildbearbeitungen durch, die von Flags im Medienbeispiel angegeben werden. Dazu gehörten Transformationen wie die vertikale Übersetzung und Skalierung, um die Bob-Interlace-Flags aufzunehmen. Die Interlacetransformation verdoppelt die Bildhöhe und übersetzt das Bild möglicherweise um die Hälfte einer Videolinie, wenn es sich im ungeraden Feld befindet.
3.  Die Transformation *T(AR)* passt das Bild basierend auf dem Seitenverhältnis des Bilds auf quadratische Pixel an. Bei **VIDEOINFOHEADER-Medientypen** wird das Seitenverhältnis durch die Bildgröße bestimmt. Bei **VIDEOINFOHEADER2-Typen** wird das Seitenverhältnis durch die Felder **dwPictAspectRatioX** und **dwPictAspectRatioY** bestimmt, es sei denn, die Flags AMCONTROL \_ PAD TO \_ \_ 16x9 oder AMCONTROL \_ PAD TO \_ \_ 4x3 sind festgelegt. Bei dieser Transformation wird davon ausgegangen, dass die Anzeigeeinstellung des Monitors mit dem physischen Seitenverhältnis des Monitors übereinstimmt. Wenn der Benutzer beispielsweise über einen Monitor mit einem Seitenverhältnis von 4 x 3 verfügt, die Anzeige jedoch auf 1280 x 768 Pixel (5 x 3) festlegt, weist das Bild nicht das richtige Seitenverhältnis auf.
4.  Die Transformation *T(Mix)* transformiert die Position des Bilds innerhalb des Zielbilds unter Verwendung der normalisierten Rechtecke, die in den [**IVMRMixerControl-Methoden**](/windows/desktop/api/Strmif/nn-strmif-ivmrmixercontrol) angegeben sind. Mit den normalisierten Rechtecke kann die Anwendung organisieren, wie die Quelldatenströme relativ zueinander positioniert und skaliert werden. Die VMR berechnet das Zielimage, indem sie die maximalen Abmessungen aller Quellimages berechnet und jedes innerhalb eines gesamten umgrenzenden Rechtecks zentriert. Den Ecken des umgrenzenden Rechtecks wird der Bereich (0,0) bis (1,1) zugewiesen. Das umgebende Rechteck wird vor der Ausführung des Diagramms korrigiert und bleibt konstant, auch wenn Streams hinzugefügt oder gelöscht werden. Zielrechtecke für jeden Stream können sich außerhalb des Bereichs (0,0) bis (1,1) befinden und weiterhin gültig sein.
5.  Schließlich kann ein Teil des gemischten Images durch die Zuordnung *T(Dst)* transformiert werden, die durch die Quell- und Zielrechtecke in der [**IBasicVideo-Schnittstelle**](/windows/desktop/api/Control/nn-control-ibasicvideo) auf der VMR angegeben wird. Wenn die Allocator-Presenter ersetzt wird und die **IBasicVideo-Schnittstelle** nicht verwendet wird, muss die Anwendung die [**IVMRWindowlessControl-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol) implementieren und die Koordinaten wieder einem linearen 2D-Raum zuordnen. Die an den DVD-Navigator zurückgegebenen Mauskoordinaten müssen sich ebenfalls in diesem Raum befinden. Wenn eine Anwendung z. B. Videos in einem sich drehenden Würfel rendert, meldet sie die gesamte Anzeige für das fensterlose Steuerelement zurück und gibt Mauskoordinaten relativ zur Anzeige zurück.

Die gesamte Bildtransformation von den Quelldaten zum endgültigen Renderer lautet:

T = T(Src) \* T(Flag)T(Ar)T(Mix) \* T(Dst)\*

gibt \* an, dass das Bild in dieser Phase auf das Zielimage abgeschnitten werden kann. Beachten Sie, dass es sich hierbei um affine Transformationen handelt, sodass die VMR sie in einer einzigen Transformation kombinieren kann.

Die Umkehrung der Transformation ist:

![Inverse Transformation](images/vmrmapping-t-1.png)

Der Faktor T(Src) T(Flag) T(Ar) ist relativ zur Quellauflösung. Im Faktor T(Mix) ist das normalisierte Quellrechteck relativ zum vom Seiten korrigierten Bild. Das normalisierte Zielrechteck ist relativ zur Ausgabeauflösung. Das folgende Diagramm zeigt diese Beziehungen.

![Schritte zur Bildtransformation](images/vmrmapping-transform-steps.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden der VMR für DirectShow-Filterentwickler](using-the-vmr-for-directshow-filter-developers.md)
</dt> </dl>

 

 



