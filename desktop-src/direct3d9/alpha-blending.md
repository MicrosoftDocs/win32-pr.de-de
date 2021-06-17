---
description: Erfahren Sie mehr über Alphablending. Alphablending wird verwendet, um ein Bild mit transparenten oder halbtransparenten Pixeln anzuzeigen.
ms.assetid: 553b0bc8-1bd8-4282-9260-cdc5f2b8788d
title: Alphablending (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd79c622778e17c5acb9b17d52b6d5db278b1508
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262002"
---
# <a name="alpha-blending-direct3d-9"></a>Alphablending (Direct3D 9)

Alphablending wird verwendet, um ein Bild mit transparenten oder halbtransparenten Pixeln anzuzeigen. Zusätzlich zu einem roten, grünen und blauen Farbkanal verfügt jedes Pixel in einer Alphabitmap über eine Transparenzkomponente, die als Alphakanal bezeichnet wird. Der Alphakanal enthält in der Regel so viele Bits wie ein Farbkanal. Beispielsweise kann ein 8-Bit-Alphakanal 256 Transparenzebenen darstellen, von 0 (das gesamte Pixel ist transparent) bis 255 (das gesamte Pixel ist nicht transparent). Die folgende Liste zeigt einige Sondereffekte, die Sie mithilfe von Alphablending erstellen können.

Farbe kann mit oder ohne Alphawerte definiert werden. Farbe ohne Alpha ist RGB-Farbe, wobei Alpha als ARGB gespeichert wird. Scheitelpunktdaten, Materialdaten und Texturdaten können verwendet werden, um die Transparenz des Objekts zu erhöhen. Der Framepuffer kann auch verwendet werden, um Transparenzeffekte zu generieren.

-   [Vertex Alpha (Direct3D 9)](vertex-alpha.md)
-   [Material Alpha (Direct3D 9)](material-alpha.md)
-   [Textur alpha (Direct3D 9)](texture-alpha.md)
-   [Framepuffer alpha (Direct3D 9)](frame-buffer-alpha.md)
-   [Renderziel Alpha (Direct3D 9)](render-target-alpha.md)

Beispiele, die Alpha veranschaulichen, sind:

-   [Aussteigend (Direct3D 9)](billboarding.md)
-   [Clouds, Smoke und Trails (Direct3D 9)](clouds--smoke--and-vapor-trails.md)
-   [Fire, Flares und Explosionen (Direct3D 9)](fire--flares--and-explosions.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Rendering](direct3d-rendering.md)
</dt> </dl>

 

 



