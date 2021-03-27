---
title: deriv_rty (SM4-ASM)
description: Renderziel-y-Entsprechung von DERIV \_ RTX.
ms.assetid: F78F2DBD-9428-4F34-85AD-276DF54C52D1
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2e4517782c687473b4789229334b4cafc94b989
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "103857751"
---
# <a name="deriv_rty-sm4---asm"></a>DERIV \_ Eigenschaft (SM4-ASM)

Renderziel-y-Entsprechung von [DERIV \_ RTX](deriv-rtx--sm4---asm-.md).



| DERIV \_ Eigenschaft \[ \_ Sat \] dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] , |
|--------------------------------------------------------------------|



 



| Element                                                            | BESCHREIBUNG                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[in \] der Adresse des Vorgangs Ergebnisses.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] der-Komponente im-Vorgang.<br/>             |



 

## <a name="remarks"></a>Bemerkungen

Nur ein einzelnes x-, y-abgeleitetes Paar wird für jeden 2 x 2-Stempel von Pixel berechnet.

Dieser Vorgang ist Hardware abhängig.

Implementierung des verweisrasterizers für Dreiecke:

-   Der Pixelshader führt den Shader immer über 2 x 2 Quad von Pixeln in Gleichschritt aus (sogar Durchfluss Steuerung, Maskierungs deaktivierte Pixel).
-   Bei den Quads sind immer sogar nummerierte Pixelkoordinaten (x und y) für das linke obere Pixel vorhanden.
-   Dummypixel werden primitiv, wenn primitiv zu klein ist, um ein 2 x 2 Quad zu füllen.
-   [DERIV \_ RTX](deriv-rtx--sm4---asm-.md) wird berechnet, indem zuerst 2 Pixel ausgewählt werden: das aktuelle Pixel und das andere Pixel mit derselben y-Koordinate aus dem Quad. Das Ergebnis wird dann wie folgt berechnet: *src0*(ungerade x Pixel)- *src0*(sogar x Pixel) \[ pro Komponente\]
-   **DERIV \_ Eigenschaft** wird berechnet, indem zuerst 2 Pixel ausgewählt werden: das aktuelle Pixel und das andere Pixel mit derselben x-Koordinate aus dem Quad. Das Ergebnis wird dann wie folgt berechnet: *src0*(ungerader y Pixel)- *src0*(sogar y Pixel) \[ pro Komponente\]

Diese Anweisung gilt für die folgenden Shader-Phasen:



| Vertexshader | Geometrie-Shader | Pixelshader |
|---------------|-----------------|--------------|
|               |                 | x            |



 

## <a name="minimum-shader-model"></a>Minimaler Shader-Modell

Diese Funktion wird in den folgenden shadermodellen unterstützt.



| Shadermodell                                              | Unterstützt |
|-----------------------------------------------------------|-----------|
| [Shader-Modell 5](d3d11-graphics-reference-sm5.md)        | ja       |
| [Shadermodell 4,1](dx-graphics-hlsl-sm4.md)              | ja       |
| [Shadermodell 4](dx-graphics-hlsl-sm4.md)                | ja       |
| [Shader-Modell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | nein        |
| [Shader-Modell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | nein        |
| [Shader-Modell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | nein        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shader Model 4-Assembly (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





