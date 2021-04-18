---
description: Verwenden des Video Mischungs Renderers
ms.assetid: 3d0fdfac-ec7e-4e02-886b-2039c607dac7
title: Verwenden des Video Mischungs Renderers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5baf7d559eed0d3111876924520952b55c6da2e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359147"
---
# <a name="using-the-video-mixing-renderer"></a>Verwenden des Video Mischungs Renderers

Im Hinblick auf die Leistung und die Vielzahl der Features stellt der Filter für Video Mischungs Renderer (VMR) die nächste Generation im Video Rendering auf der Windows-Plattform dar. VMR ersetzt den [Überlagerungs Mixer](overlay-mixer-filter.md) und den [Videorenderer](video-renderer-filter.md)und fügt viele neue Mischungs Funktionen hinzu.

Es gibt zwei Versionen von VMR:

-   Die VMR-7, die DirectDraw 7 zum Rendern verwendet.
-   VMR-9, das Direct3D 9 verwendet.

VMR-7 ist unter Windows XP und höher verfügbar, aber nicht für die erneute Verteilung verfügbar. VMR-9 ist für die Weiterverteilung auf allen Plattformen verfügbar, die von DirectX 9 unterstützt werden. Die beiden VMR-Filter sind in ihrer Implementierung und den von Ihnen bereitgestellten Schnittstellen sehr ähnlich.

VMR-9 hat eine eigene CLSID und einen eigenen Satz von Schnittstellen, Strukturen und Enumerationstypen, die nicht immer mit den entsprechenden Datentypen für VMR-7 identisch sind, aufgrund der zugrunde liegenden Unterschiede zwischen DirectDraw 7 und Direct3D 9. Die VMR-9-Schnittstellen enden alle mit "9", z. b. **IVMRStreamConfig9**, und die Strukturen und Enumerationstypen verfügen in Ihrem Namen über "VMR9", um Sie von den Datentypen zu unterscheiden, die mit VMR-7 verwendet werden.

Um Abwärtskompatibilität zu gewährleisten, ist VMR-9 nicht der Standard-Renderer auf einem System. Um VMR-9 verwenden zu können, müssen Sie es mithilfe der [**ifiltergraph:: AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) -Methode explizit dem Filter Diagramm hinzufügen und konfigurieren, bevor Sie es mit upstreamfiltern verbinden.

Dieser Artikel enthält folgende Abschnitte. Sofern nicht angegeben, gelten die Informationen in diesen Abschnitten sowohl für den VMR-7-als auch für den VMR-9-Filter.

-   [Informationen zum Video Mischungs Rendering](about-the-video-mixing-render.md)
-   [VMR-Betriebsmodi](vmr-modes-of-operation.md)
-   [Aufbauen eines VMR-9-Filter Diagramms](building-a-vmr-9-filter-graph.md)
-   [Verwenden des VMR-Mischungs Modus](using-vmr-mixing-mode.md)
-   [Einstellungen für deinterlace werden festgelegt](setting-deinterlace-preferences.md)
-   [Verwenden von VMR für DirectShow-Filter Entwickler](using-the-vmr-for-directshow-filter-developers.md)
-   [Verwenden des Certified Output Protection-Protokolls (COPP)](using-certified-output-protection-protocol--copp.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Video Mischungs-Renderer Filter 7](video-mixing-renderer-filter-7.md)
</dt> <dt>

[Video Mischungs-Renderer Filter 9](video-mixing-renderer-filter-9.md)
</dt> </dl>

 

 



