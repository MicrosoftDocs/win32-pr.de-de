---
description: Alpha Blending wird zum Anzeigen eines Bilds mit transparenten oder semitransparenten Pixeln verwendet.
ms.assetid: 553b0bc8-1bd8-4282-9260-cdc5f2b8788d
title: Alpha Mischung (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f4ae2883c7a9a92ba1b62306dc26bf09d0d9947
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127240"
---
# <a name="alpha-blending-direct3d-9"></a>Alpha Mischung (Direct3D 9)

Alpha Blending wird zum Anzeigen eines Bilds mit transparenten oder semitransparenten Pixeln verwendet. Zusätzlich zu einem roten, grünen und blauen Farbkanal weist jedes Pixel in einer Alpha Bitmap eine Transparenz Komponente auf, die als Alphakanal bezeichnet wird. Der Alphakanal enthält in der Regel so viele Bits wie ein Farbkanal. Ein 8-Bit-Alphakanal kann z. b. 256 Ebenen der Transparenz darstellen, von 0 (das gesamte Pixel ist transparent) bis 255 (das gesamte Pixel ist nicht transparent). Die nachstehende Liste zeigt einige besondere Effekte, die Sie mithilfe von Alpha Blending erstellen können.

Die Farbe kann mit oder ohne Alpha Werte definiert werden. Farbe ohne Alpha ist RGB-Farbe, wobei Alpha als ARGB gespeichert wird. Vertexdaten, Materialdaten und Textur Daten können verwendet werden, um die Transparenz von Objekten zu unterstützen. Der Frame Puffer kann auch zum Generieren von Transparenz Effekten verwendet werden.

-   [Vertex Alpha (Direct3D 9)](vertex-alpha.md)
-   [Material Alpha (Direct3D 9)](material-alpha.md)
-   [Textur Alpha (Direct3D 9)](texture-alpha.md)
-   [Frame-Puffer Alpha (Direct3D 9)](frame-buffer-alpha.md)
-   [Renderziel Alpha (Direct3D 9)](render-target-alpha.md)

Zu den Beispielen, die Alpha veranschaulichen, gehören:

-   [Fakboardingvorgang (Direct3D 9)](billboarding.md)
-   [Clouds, Rauch und Dampfwege (Direct3D 9)](clouds--smoke--and-vapor-trails.md)
-   [Feuer, Flares und Explosionen (Direct3D 9)](fire--flares--and-explosions.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Rendering](direct3d-rendering.md)
</dt> </dl>

 

 



