---
description: Erfahren Sie mehr über alpha blending. Alphablending wird verwendet, um ein Bild mit transparenten oder halbtransparenten Pixeln anzuzeigen.
ms.assetid: 553b0bc8-1bd8-4282-9260-cdc5f2b8788d
title: Alphablending (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 081c194b9eae85dca5599f2bf9f779d1cd896c8a37641df5105bb049b4a5bc22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119751580"
---
# <a name="alpha-blending-direct3d-9"></a>Alphablending (Direct3D 9)

Alphablending wird verwendet, um ein Bild mit transparenten oder halbtransparenten Pixeln anzuzeigen. Zusätzlich zu einem roten, grünen und blauen Farbkanal verfügt jedes Pixel in einer Alphabitmap über eine Transparenzkomponente, die als Alphakanal bezeichnet wird. Der Alphakanal enthält in der Regel so viele Bits wie ein Farbkanal. Beispielsweise kann ein 8-Bit-Alphakanal 256 Transparenzebenen darstellen, von 0 (das gesamte Pixel ist transparent) bis 255 (das gesamte Pixel ist nicht transparent). Die folgende Liste zeigt einige Sondereffekte, die Sie mit alpha blending erstellen können.

Die Farbe kann mit oder ohne Alphawerte definiert werden. Farbe ohne Alpha ist RGB-Farbe, und Alpha wird als ARGB gespeichert. Vertexdaten, Materialdaten und Texturdaten können verwendet werden, um die Transparenz des Objekts zu gewährleisten. Der Framepuffer kann auch verwendet werden, um Transparenzeffekte zu generieren.

-   [Vertex Alpha (Direct3D 9)](vertex-alpha.md)
-   [Material Alpha (Direct3D 9)](material-alpha.md)
-   [Textur alpha (Direct3D 9)](texture-alpha.md)
-   [Frame Buffer Alpha (Direct3D 9)](frame-buffer-alpha.md)
-   [Renderziel alpha (Direct3D 9)](render-target-alpha.md)

Beispiele, die Alpha veranschaulichen:

-   [Beschriftung (Direct3D 9)](billboarding.md)
-   [Clouds, Smoke und Trail Trail (Direct3D 9)](clouds--smoke--and-vapor-trails.md)
-   [Fire, Flares und Explosions (Direct3D 9)](fire--flares--and-explosions.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Rendering](direct3d-rendering.md)
</dt> </dl>

 

 



