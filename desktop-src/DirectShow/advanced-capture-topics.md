---
description: Erweiterte Erfassungs Themen
ms.assetid: 407702b2-5f4f-424d-a3ec-b0473e1b0da3
title: Erweiterte Erfassungs Themen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4c4e5a077f6f8b17543250efa0f10091f0917e8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125066"
---
# <a name="advanced-capture-topics"></a>Erweiterte Erfassungs Themen

In diesem Abschnitt werden einige erweiterte Aspekte der Video Erfassung in DirectShow beschrieben. Die meisten der in diesem Abschnitt beschriebenen Probleme werden automatisch von der [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) -Schnittstelle behandelt. Die hier aufgeführten Informationen sind jedoch möglicherweise nützlich, wenn Sie Probleme mit einer Video Erfassungs Anwendung beheben müssen. Sie sollten diesen Abschnitt auch lesen, wenn Ihre Anwendung ein benutzerdefiniertes Erfassungs Diagramm erstellt und Sie feststellen, dass ICaptureGraphBuilder2 nicht Ihren Anforderungen entspricht. Zum Schluss enthält dieser Abschnitt einige Informationen zur Verwendung des VMR-Filters (Video Mischungs-Renderer) in einer Video Erfassungs Anwendung.

Es ist möglich, ein Video Erfassungs Diagramm vollständig mit [**igraphbuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) -Methoden zu erstellen. Sie können auch die beiden Schnittstellen kombinieren, indem Sie ICaptureGraphBuilder2 für einige Aufgaben und igraphbuilder für andere Benutzer verwenden.

Dieser Abschnitt enthält die folgenden Themen:

-   [Behandeln von Repaint-Ereignissen in der Video Erfassung](handling-repaint-events-in-video-capture.md)
-   [Arbeiten mit PIN-Kategorien](working-with-pin-categories.md)
-   [Verwenden des Smart Tee-Filters](using-the-smart-tee-filter.md)
-   [Verwenden des Overlay-Mischers bei der Video Erfassung](using-the-overlay-mixer-in-video-capture.md)
-   [VideoPort-Pins](video-port-pins.md)
-   [VideoInfo2-Formattyp](videoinfo2-format-type.md)
-   [Erstellen von Kernel-Mode filtern](creating-kernel-mode-filters.md)
-   [WDM-Klassen Treiber Filter](wdm-class-driver-filters.md)
-   [Verwenden der WDDM-Erfassung in DirectShow](using-wddm-capture-in-directshow.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Video Erfassung](video-capture.md)
</dt> </dl>

 

 



