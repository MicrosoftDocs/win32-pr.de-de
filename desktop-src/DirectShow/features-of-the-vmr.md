---
description: Features von VMR
ms.assetid: a809045b-b60d-4092-bc4d-0e70e17d2913
title: Features von VMR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7c4a5a34be9fb3b3bb08df18091b88fbe7d7432
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106339674"
---
# <a name="features-of-the-vmr"></a>Features von VMR

Der Video Mischungs-Renderer 7 (VMR-7) unterstützt die folgenden neuen Features:

-   Echte Mischung mehrerer Videostreams mithilfe der Alpha Mischungs Funktionen von Direct3D-Hardware Geräten.
-   Die Möglichkeit zum Einbinden Ihrer eigenen Zusammensetzung-Komponente, um Effekte und Übergänge zwischen mehreren Videostreams zu implementieren, die in die VMR eingegeben werden.
-   Echtes fensterloses Rendering. Es ist nicht mehr erforderlich, das Videowiedergabe Fenster zu einem untergeordneten Element des Anwendungsfensters zu machen, um die Videowiedergabe zu enthalten. Der neue fensterlose Renderingmodus von VMR ermöglicht Anwendungen das einfache Hosten der Videowiedergabe innerhalb eines beliebigen Fensters, ohne Fenster Meldungen an den Renderer für die Rendererspezifische Verarbeitung weiterleiten zu müssen.
-   Ein neuer renderloser Wiedergabemodus, in dem Anwendungen eine eigene zuordnerkomponente bereitstellen können, um Zugriff auf das decodierte Video Bild zu erhalten, bevor es auf dem Bildschirm angezeigt wird.
-   Verbesserte Unterstützung für PCs, die mit mehreren Monitoren ausgestattet sind.
-   Unterstützung für die neue DirectX-Video Beschleunigung-Architektur von Microsoft.
-   Unterstützung für hochwertige Videowiedergabe gleichzeitig auf mehreren Fenstern.
-   Unterstützung für den exklusiven DirectDraw-Modus
-   100% Abwärtskompatibilität mit vorhandenen Anwendungen.
-   Unterstützung für Frame Step und eine zuverlässige Möglichkeit, das aktuelle Bild zu erfassen, das angezeigt wird.
-   Die Möglichkeit für Anwendungen, ihre eigenen statischen Bilddaten (z. b. Kanal Logos oder UI-Komponenten) problemlos mit dem Video in eine reibungslose flimmerfreie Weise zu mischen.

VMR-9 unterstützt alle oben aufgeführten Features sowie die folgenden:

-   Die Möglichkeit zum Verarbeiten von Videodaten direkt mit Direct3D-APIs wie z. b. Pixel-Shadern.
-   Verbesserte Unterstützung für Zeilen Sprung Videoinhalte.
-   Unterstützung für alle von DirectX unterstützten Plattformen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zum Video Mischungs Rendering](about-the-video-mixing-render.md)
</dt> </dl>

 

 



