---
description: VMR im Vergleich zu
ms.assetid: 45b3f964-6ec7-48b8-a66e-3c9883e6d780
title: VMR im Vergleich zu vorherigen DirectShow-Renderern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef9401361c5b258fdff09bf25351a79bf8315dabfb0c82636d7d8c3c9ffcdd93
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903270"
---
# <a name="vmr-vs-previous-directshow-renderers"></a>VMR im Vergleich zu vorherigen DirectShow-Renderern

Bei den alten Filtern sind abhängig von der Hardwarekonfiguration verschiedene Renderer im Diagramm erforderlich.

Der [Videorenderer-Filter](video-renderer-filter.md) wurde verwendet, um einen einzelnen Videostream in Nicht-Videoportszenarien zu rendern. Es basiert auf Grafikhardwaretechnologie, die jetzt über fünf Jahre alt ist, und auf einer älteren Version von DirectDraw. In bestimmten Szenarien wird GDI für das Rendering verwendet. Dies geschieht entweder, um Videoressourcen zu sparen, die vor fünf Jahren viel eingeschränkter waren, oder um Einschränkungen in DirectDraw zu überwinden, die mit der Unterstützung für mehrere Monitore in Zusammenhang stehen. Weder VMR-7 noch VMR-9 verwenden jemals GDI für das Rendering. VMR-7 basiert vollständig auf DirectDraw 7 und VMR-9 auf Direct3D 9.

In Szenarien mit einem Videoport oder mehreren Videoeingabestreams wurde vor der VMR der [Overlay](overlay-mixer-filter.md) Mixer Filter für das Rendering verwendet. Dieser Filter verwendet nur die Hardwareüberlagerung auf der Grafikkarte und ist daher im Allgemeinen auf die von den meisten Karten bereitgestellte Überlagerungsoberfläche beschränkt. Der Overlay Mixer führt die Zielfarbschlüsselung aus, kann aber nicht alphablenden. Da es keinen Fenster-Manager hat, muss er einen zweiten Filter, den Videorenderer, für die Fensterverwaltung verwenden. Der VMR kann echte Alphablendings ausführen und kann zusätzlich zu den Hardwareüberlagerungen mehrere Überlagerungen in der Software erstellen.

In Videoportszenarien, in denen Anwendungen Untertitel oder andere VBI-Daten im Video überlagern, war ein zusätzlicher Filter, die [VBI Surface Allocator,](vbi-surface-allocator.md)erforderlich, um den zusätzlichen Videospeicher für den VBI-Text zu reservieren. Bei ISVs vereinfacht VMR-7 die Anwendungsentwicklung, indem Zuordnungs- und Renderingfunktionen in einem einzigen Filter kombiniert werden, der in allen Szenarien verwendet wird. Mit der VMR wird die VBI Surface Allocator nicht mehr benötigt. Dieser Filter wird in Windows XP durch den neuen [Videoport-Manager-Filter](video-port-manager.md) ersetzt, der alle Videoportaufgaben ausführt, die zuvor vom Overlay-Mixer.

> [!Note]  
> VMR-9 unterstützt keine Videoports.

 

Die VMR ist stabiler als die früheren Renderer, zum Teil, da sie nur DirectDraw 7 -Schnittstellen (oder Direct3D 9, wenn Sie VMR-9 verwenden) verwendet, im Gegensatz zu den alten Renderern, die eine Mischung aus Schnittstellen aus älteren und neueren Versionen von DirectDraw verwendet haben. Der VMR verwendet auch einen neuen Bildpräsentationsmechanismus, der für aktuelle und zukünftige Generationen von Adaptern konzipiert ist, die Direct3D, erhöhte VRAM- und Videospeicherbandbreite sowie Hardwarebeschleunigungsfeatures unterstützen. Bei der VMR liegt der Schwerpunkt auf der Front-End-Verarbeitung und der reduzierten Abhängigkeit von Videoports und Overlays. Aber auch bei allen neuen Funktionen ist die VMR auf maximale Kompatibilität mit vorhandenen Anwendungen ausgelegt.

Die VMR ist ebenfalls erweiterbar. Anwendungen können eigene Unterkomponenten bereitstellen, um benutzerdefinierte Videoeffekte durchzuführen und/oder die Kontrolle über den Zuordnungs- und Renderingprozess zu übernehmen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zum Rendern von Videos](about-the-video-mixing-render.md)
</dt> </dl>

 

 



