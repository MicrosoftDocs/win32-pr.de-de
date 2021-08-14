---
title: deriv_rty (sm4 - asm)
description: Renderziel y-Entsprechung von deriv \_ rtx.
ms.assetid: F78F2DBD-9428-4F34-85AD-276DF54C52D1
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb522076435b525252e8cab40590c649e5cc8af8a83023ebd6cace1695fbb729
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118515468"
---
# <a name="deriv_rty-sm4---asm"></a>deriv \_ rty (sm4 - asm)

Renderziel y-Entsprechung [von deriv \_ rtx](deriv-rtx--sm4---asm-.md).



| deriv \_ rty \[ \_ sat \] dest \[ .mask , \] \[ - \] src0 \[ \_ abs \] \[ .swizzle \] , |
|--------------------------------------------------------------------|



 



| Element                                                            | BESCHREIBUNG                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[in \] Die Adresse des Ergebnisses des Vorgangs.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] Die Komponente im Vorgang.<br/>             |



 

## <a name="remarks"></a>Hinweise

Für jeden 2x2-Stempel von Pixeln wird nur ein einzelnes x,y-Ableitungspaar berechnet.

Dieser Vorgang ist hardwareabhängig.

Referenz zur Rasterizerimplementierung für Dreiecke:

-   Pixel-Shader führt shader immer über 2 x 2 Quad pixel in lockstep aus (auch durch Flusssteuerung, Maskierung deaktivierter Pixel).
-   Quads verfügen immer über gleichmäßig nummerierte Pixelkoordinaten (x und y) für pixel oben links.
-   Dummypixel laufen primitiv ab, wenn der Primitivtyp zu klein ist, um ein 2x2-Quad zu füllen.
-   [deriv \_ rtx](deriv-rtx--sm4---asm-.md) wird berechnet, indem zuerst 2 Pixel angegeben werden: das aktuelle Pixel und das andere Pixel mit der gleichen y-Koordinate aus dem Quader. Anschließend wird das Ergebnis wie folgt berechnet: *src0*(ungerades x Pixel) – *src0*(sogar x \[ Pixel) pro Komponente\]
-   **deriv \_ rty** wird berechnet, indem zuerst 2 Pixel auswählt: das aktuelle Pixel und das andere Pixel mit der gleichen x-Koordinate vom Quader. Anschließend wird das Ergebnis wie folgt berechnet: *src0*(ungerades y Pixel) - *src0*(sogar y Pixel) \[ pro Komponente\]

Diese Anweisung gilt für die folgenden Shaderstufen:



| Vertexshader | Geometrie-Shader | Pixelshader |
|---------------|-----------------|--------------|
|               |                 | x            |



 

## <a name="minimum-shader-model"></a>Minimales Shadermodell

Diese Funktion wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                              | Unterstützt |
|-----------------------------------------------------------|-----------|
| [Shadermodell 5](d3d11-graphics-reference-sm5.md)        | ja       |
| [Shadermodell 4.1](dx-graphics-hlsl-sm4.md)              | ja       |
| [Shadermodell 4](dx-graphics-hlsl-sm4.md)                | ja       |
| [Shadermodell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | nein        |
| [Shadermodell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | nein        |
| [Shadermodell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | nein        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shader Model 4-Assembly (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





