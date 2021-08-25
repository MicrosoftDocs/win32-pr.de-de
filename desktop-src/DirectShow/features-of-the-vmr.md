---
description: Features der VMR
ms.assetid: a809045b-b60d-4092-bc4d-0e70e17d2913
title: Features der VMR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66c78fc34be3097beedb73ac3989bc468cff0851143355902e3236f672797a83
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117819552"
---
# <a name="features-of-the-vmr"></a>Features der VMR

Der Video Mixing Renderer 7 (VMR-7) unterstützt die folgenden neuen Features:

-   Echte Mischung mehrerer Videostreams mithilfe der Alphablendingfunktionen von Direct3D-Hardwaregeräten.
-   Die Möglichkeit, Ihre eigene Compositing-Komponente zu verbinden, um Effekte und Übergänge zwischen mehreren Videostreams zu implementieren, die in die VMR eintreten.
-   Echtes fensterloses Rendering. Es ist nicht mehr erforderlich, das Videowiedergabefenster als untergeordnetes Fenster des Anwendungsfensters zu verwenden, um die Videowiedergabe zu enthalten. Der neue fensterlose Renderingmodus des virtuellen Computers ermöglicht Anwendungen das einfache Hosten der Videowiedergabe in jedem Fenster, ohne dass Fenstermeldungen zur rendererspezifischen Verarbeitung an den Renderer weitergeleitet werden müssen.
-   Ein neuer renderloser Wiedergabemodus, in dem Anwendungen ihre eigene Zuweisungskomponente zur Verfügung stellen können, um Zugriff auf das decodierte Videobild zu erhalten, bevor es auf dem Bildschirm angezeigt wird.
-   Verbesserte Unterstützung für PCs, die mit mehreren Monitoren ausgestattet sind.
-   Unterstützung für die neue DirectX-Videobeschleunigungsarchitektur von Microsoft.
-   Unterstützung für qualitativ hochwertige Videowiedergabe gleichzeitig in mehreren Fenstern.
-   Unterstützung für den exklusiven DirectDraw-Modus
-   100 % Abwärtskompatibilität mit vorhandenen Anwendungen.
-   Unterstützung für Frameschritte und eine zuverlässige Möglichkeit, das aktuell angezeigte Bild zu erfassen.
-   Die Möglichkeit, dass Anwendungen ihre eigenen statischen Bilddaten (z. B. Kanallogos oder Benutzeroberflächenkomponenten) problemlos mit dem Video auf eine nahtlose flackerfreie Weise überblenden können.

VMR-9 unterstützt alle oben aufgeführten Features sowie:

-   Die Möglichkeit, Videodaten direkt mit Direct3D-APIs wie Pixel-Shadern zu verarbeiten.
-   Verbesserte Unterstützung für Interlacing von Videoinhalten.
-   Unterstützung auf allen Plattformen, die von DirectX unterstützt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zum Rendern von Videos](about-the-video-mixing-render.md)
</dt> </dl>

 

 



