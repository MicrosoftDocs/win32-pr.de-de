---
description: Die Beleuchtungs-Engine kombiniert Material Farbe, Vertexfarbe und Beleuchtungs Informationen, um eine pro-Vertex-Farbe zu generieren.
ms.assetid: 1e7c31cb-dc63-4f4a-9ddc-d1d1d0b69085
title: Alpha Textur Mischung (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ad394b70b96e17b2ce858f871fb869afde0d122
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106339697"
---
# <a name="alpha-texture-blending-direct3d-9"></a>Alpha Textur Mischung (Direct3D 9)

Die Beleuchtungs-Engine kombiniert Material Farbe, Vertexfarbe und Beleuchtungs Informationen, um eine pro-Vertex-Farbe zu generieren. Nach der Interpolation wird dadurch eine pro-Pixel-Farbe generiert, die in den Frame Puffer geschrieben wird. Wenn eine Anwendung Textur blending ermöglicht, wird die Pixelfarbe zu einer Kombination des aktuellen Pixels im Frame Puffer und einer Textur Farbe.

Diese Formel bestimmt die endgültige gemischte Pixelfarbe:


```
Color = TexelColor x SourceBlend + CurrentPixelColor x DestBlend
```



Hierbei gilt:

-   Color ist die Ausgabe Pixelfarbe.
-   Texelcolor ist die Eingabe Farbe nach der Textur Filterung.
-   Sourceblend ist der Prozentsatz der endgültigen Pixelfarbe, die aus der texessource-Quellfarbe besteht.
-   Currentpixelcolor ist die Farbe des aktuellen Pixels.
-   Destblend ist der Prozentsatz der endgültigen Pixelfarbe, die aus der aktuellen Pixelfarbe besteht.

Die abschließende Mischungs Gleichung wird festgelegt, indem [**IDirect3DDevice9:: setrenderstate**](/windows/desktop/api) aufgerufen und der Blend-renderzustand (D3DRS \_ blendxxx) mit einem entsprechenden Mischungs Faktor ([**D3DBLEND**](./d3dblend.md)) angegeben wird. Die Werte von sourceblend und destblend reichen von 0,0 (transparent) bis 1,0 (nicht transparent) einschließlich. Außerdem kann eine Anwendung die Transparenz eines Pixels steuern, indem der Alpha-Wert in einer Textur festgelegt wird. Verwenden Sie in diesem Fall Folgendes:


```
SourceBlend = D3DBLEND_ZERO 
DestBlend = D3DBLEND_ONE
```



Die Mischungs Gleichung bewirkt, dass das gerenderte Pixel transparent ist. Die Standardwerte lauten wie folgt:


```
SourceBlend = D3DBLEND_SRCALPHA 
DestBlend = D3DBLEND_INVSRCALPHA
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Textur Mischung](texture-blending.md)
</dt> <dt>

[Textur Filterung (Direct3D 9)](texture-filtering.md)
</dt> <dt>

[**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)
</dt> </dl>

 

 
