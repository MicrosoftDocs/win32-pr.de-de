---
description: VMR im Vergleich zu
ms.assetid: 45b3f964-6ec7-48b8-a66e-3c9883e6d780
title: VMR im Vergleich zu vorherigen DirectShow-Renderer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db40f9789a73446cb2dac4ed7033bdb163141bff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345812"
---
# <a name="vmr-vs-previous-directshow-renderers"></a>VMR im Vergleich zu vorherigen DirectShow-Renderer

Mit den alten Filtern sind abhängig von der Hardwarekonfiguration verschiedene Renderer im Diagramm erforderlich.

Der [Videorendererfilter](video-renderer-filter.md) wurde zum Rendern eines einzelnen Video Datenstroms in Szenarios verwendet, die keine Video-Ports sind. Es basiert auf Grafikhardware Technologie, die nun über fünf Jahre alt ist, und auf einer älteren Version von DirectDraw. In bestimmten Szenarien wird GDI für das Rendering verwendet. Dies geschieht entweder, um Video Ressourcen zu sparen, die vor fünf Jahren noch vor fünf Jahren eingeschränkt waren, oder um Einschränkungen in DirectDraw zu umgehen, die sich auf die Unterstützung mehrerer Monitore bezogen haben. Weder VMR-7 noch VMR-9 verwenden GDI zum Rendern. VMR-7 basiert vollständig auf DirectDraw 7, und VMR-9 basiert auf Direct3D 9.

In Szenarien, in denen entweder ein Videoport oder mehrere Video Eingabestreams verwendet werden, wurde vor der VMR der [Überlagerungs-Mischungs](overlay-mixer-filter.md) Filter zum Rendering verwendet. Dieser Filter verwendet nur die Hardware Überlagerung auf der Grafikkarte und ist daher in der Regel auf die von den meisten Karten bereitgestellte über Lagerungs Oberfläche beschränkt. Der Überlagerungs-Mixer führt die Zielfarbe aus, kann aber keine Alpha Mischung sein. Da Sie nicht über einen Fenster-Manager verfügt, muss Sie für die Fensterverwaltung einen zweiten Filter, den Videorenderer, verwenden. VMR ist in der Lage, eine echte Alpha Mischung zu erzeugen, und kann zusätzlich zu den Hardware Überlagerungen auch mehrere Überlagerungen in der Software erstellen.

In Video Port Szenarios, in denen Anwendungen Untertitel oder andere VBI-Daten im Video überlagern, war ein zusätzlicher Filter, der [VBI Surface Allocator](vbi-surface-allocator.md), erforderlich, um den zusätzlichen Videospeicher für den VBI-Text zuzuordnen. Für ISVs vereinfacht VMR-7 die Anwendungsentwicklung, indem die Zuordnungs-und Renderingfunktionen in einem einzelnen Filter kombiniert werden, der in allen Szenarien verwendet wird. Mit VMR ist die VBI-Oberflächen Zuweisung nicht mehr erforderlich. Dieser Filter wird in Windows XP durch den neuen [Video Port Manager](video-port-manager.md) -Filter ersetzt, der alle Video Port Tasks ausführt, die zuvor vom Überlagerungs-Mixer ausgeführt wurden.

> [!Note]  
> VMR-9 unterstützt keine Videoports.

 

Die VMR ist stabiler als die früheren Renderer, da Sie nur DirectDraw 7 (oder Direct3D 9, wenn Sie die VMR-9-Schnittstellen verwenden) im Gegensatz zu den alten renderatoren verwendet, die eine Mischung aus Schnittstellen aus älteren und neueren Versionen von DirectDraw verwendeten. VMR setzt auch einen neuen Bild Präsentations Mechanismus ein, der für aktuelle und zukünftige Generationen von Adaptern konzipiert ist, die Unterstützung für Direct3D, größere VRAM-und Videospeicher Bandbreite und Hardware Beschleunigungs Features haben. Bei der VMR liegt der Schwerpunkt auf der Front-End-Verarbeitung und der geringeren Abhängigkeit von Videoports und Überlagerungen. Aber selbst mit all ihren neuen Funktionen ist die VMR für maximale Kompatibilität mit vorhandenen Anwendungen konzipiert.

VMR ist auch erweiterbar. Anwendungen können eigene unter Komponenten zur Durchführung von benutzerdefinierten Video Effekten und/oder zum Steuern des Zuordnungs-und Renderingprozesses bereitstellen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zum Video Mischungs Rendering](about-the-video-mixing-render.md)
</dt> </dl>

 

 



