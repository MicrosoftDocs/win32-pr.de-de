---
description: Auswählen des richtigen Videorenderers
ms.assetid: c57c4c68-ea1c-4198-94b4-e9b6e53bb625
title: Auswählen des richtigen Videorenderers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38a334fec59f6e3631217d48df7f0e8c83d87462
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106346207"
---
# <a name="choosing-the-right-video-renderer"></a>Auswählen des richtigen Videorenderers

DirectShow stellt verschiedene Videorendererfilter bereit, die in der folgenden Tabelle zusammengefasst sind.



| Filter                                                                  | Bemerkungen                                           |
|-------------------------------------------------------------------------|---------------------------------------------------|
| [**Erweiterter Videorenderer**](enhanced-video-renderer-filter.md) (EVR) | Verwendet Direct3D 9. Erfordert Windows Vista oder höher. |
| [Video Mischungs-Renderer 9](video-mixing-renderer-filter-9.md) (VMR-9)   | Verwendet Direct3D 9. Erfordert Windows XP oder höher.    |
| [Video Mischungs Filter 7](video-mixing-renderer-filter-7.md) (VMR-7)     | Verwendet DirectDraw. Erfordert Windows XP oder höher.    |
| [Überlagerungs Mixer](using-the-overlay-mixer-in-video-capture.md)           | Unterstützt Hardware Überlagerungen durch DirectDraw.    |
| Der Legacy- [Videorenderer](video-renderer-filter.md) -Filter.              | Verwendet DirectDraw oder (selten) GDI                   |



 

Welcher Renderer verwendet werden soll, hängt größtenteils davon ab, welche Versionen von Windows unterstützt werden müssen.

-   In Windows Vista und höher sollten Anwendungen den EVR verwenden, wenn Sie von der Hardware unterstützt werden. Andernfalls greifen Sie auf VMR-9 oder VMR-7 zurück. Der EVR bietet eine bessere Leistung und bessere Videoqualität als vorherige Renderer. Außerdem ist er für die Verwendung mit dem Desktopfenster-Manager (DWM) konzipiert.
-   Verwenden Sie vor Windows Vista VMR-9, wenn dies von der Hardware unterstützt wird und keine Video Port Funktionen erforderlich sind. Verwenden Sie andernfalls VMR-7.
-   Auf älteren Systemen müssen Sie möglicherweise den Overlay-Mixer (für den Videoport oder die Unterstützung der Hardware Überlagerung) oder den Legacy-Videorendererfilter verwenden.

Die [**igraphbuilder:: Rendering**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) -Methode und die [**RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) -Methode verwenden standardmäßig VMR-7. Wenn die Hardware VMR-7 nicht unterstützt, greifen diese Methoden auf den Legacy-Videorendererfilter zurück. Der EVR und VMR-9 sind nie die Standardrenderer.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Videorendering](video-rendering.md)
</dt> </dl>

 

 



