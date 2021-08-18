---
title: deriv_rtx (sm4 - asm)
description: Rate der Inhaltsänderung jeder float32-Komponente von src0 (post-swizzle), in Bezug auf die RenderTarget x-Richtung (rtx) oder renderTarget y-Richtung.
ms.assetid: 2438DB36-C348-4854-AE1B-EC3C890B0B42
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c7a9697372964135e5ecb3cb5e916b0509a6a6a860ff8fa01ea0daeb1b8be4d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986650"
---
# <a name="deriv_rtx-sm4---asm"></a>deriv \_ rtx (sm4 - asm)

Rate der Inhaltsänderung jeder float32-Komponente von *src0* (post-swizzle), in Bezug auf die RenderTarget x-Richtung (rtx) oder renderTarget y-Richtung.



| deriv \_ rtx \[ \_ sat \] dest \[ .mask , \] \[ - \] src0 \[ \_ abs \] \[ .swizzle \] , |
|--------------------------------------------------------------------|



 



| Element                                                            | BESCHREIBUNG                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[in \] Die Adresse des Ergebnisses des Vorgangs.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] Die Komponente im Vorgang.<br/>             |



 

## <a name="remarks"></a>Hinweise

Für jeden 2x2-Stempel von Pixeln wird nur ein einzelnes x,y-Ableitungspaar berechnet.

Dieser Vorgang ist hardwareabhängig.

Referenz zur Rasterizerimplementierung für Dreiecke:

-   Pixel-Shader führt shader immer über 2 x 2 Quad pixel in lockstep aus (selbst durch Flusssteuerung, Maskierung deaktivierter Pixel).
-   Quads verfügen immer über gleichmäßig nummerierte Pixelkoordinaten (x und y) für pixel oben links.
-   Dummypixel laufen primitiv ab, wenn der Primitivtyp zu klein ist, um ein 2x2-Quader zu füllen.
-   **deriv \_ rtx** wird berechnet, indem zuerst 2 Pixel auswählt: das aktuelle Pixel und das andere Pixel mit der gleichen y-Koordinate aus dem Quader. Anschließend wird das Ergebnis wie folgt berechnet: *src0*(ungerade x Pixel) – *src0*(sogar x \[ Pixel) pro Komponente\]
-   [deriv \_ rty](deriv-rty--sm4---asm-.md) wird berechnet, indem zuerst 2 Pixel auswählt: das aktuelle Pixel und das andere Pixel mit der gleichen x-Koordinate aus dem Quader. Anschließend wird das Ergebnis wie folgt berechnet: *src0*(ungerades y Pixel) – *src0*(sogar y Pixel) \[ pro Komponente\]

Diese Anweisung gilt für die folgenden Shaderstufen:



| Vertexshader | Geometrie-Shader | Pixelshader |
|---------------|-----------------|--------------|
|               |                 | x            |



 

## <a name="minimum-shader-model"></a>Minimales Shadermodell

Diese Funktion wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                              | Unterstützt |
|-----------------------------------------------------------|-----------|
| [Shadermodell 5](d3d11-graphics-reference-sm5.md)        | Ja       |
| [Shadermodell 4.1](dx-graphics-hlsl-sm4.md)              | Ja       |
| [Shadermodell 4](dx-graphics-hlsl-sm4.md)                | Ja       |
| [Shadermodell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | Nein        |
| [Shadermodell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | Nein        |
| [Shadermodell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | Nein        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shader Model 4-Assembly (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





