---
title: Tiefenausrichtung
description: Polygone, die im 3D-Raum koplanar sind, können so dargestellt werden, als ob sie nicht koplanar sind, indem jedem Polygon ein Z-Bias (oder Tiefenvoreingenommenheit) hinzugefügt wird.
ms.assetid: ee904316-dc6d-48a4-bdb7-0f7dcdb9d9d6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1f707a038a2da8ebe9c1adc21f6081c85f5a63fbbc1c360a4dfbbf5765d845d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118990160"
---
# <a name="depth-bias"></a>Tiefenausrichtung

Polygone, die im 3D-Raum koplanar sind, können so dargestellt werden, als ob sie nicht koplanar sind, indem jedem Polygon ein Z-Bias (oder Tiefenvoreingenommenheit) hinzugefügt wird.

Dies ist eine Technik, die häufig verwendet wird, um sicherzustellen, dass Schatten in einer Szene ordnungsgemäß angezeigt werden. Beispielsweise hat ein Schatten an einer Wand wahrscheinlich den gleichen Tiefenwert wie die Wand. Wenn eine Anwendung zuerst eine Wand und dann einen Schatten rendert, ist der Schatten möglicherweise nicht sichtbar, oder Tiefenartefakte sind möglicherweise sichtbar.


Eine Anwendung kann dazu beitragen, sicherzustellen, dass koplanare Polygone ordnungsgemäß gerendert werden, indem sie die Verzerrungen (vom **DepthBias-Member** von [**D3D11 \_ RASTERIZER \_ DESC1)**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1)zu den Z-Werten hinzufügung, die das System beim Rendern der Gruppen von coplanaren Polygonen verwendet. Polygone mit einem größeren z-Wert werden vor Polygonen mit einem kleineren z-Wert gezeichnet.

Es gibt zwei Optionen zum Berechnen des Tiefenvoreingenommenheits.

1.  Wenn der tiefen Puffer, der derzeit an die Ausgabe-Merger-Phase gebunden ist, ein **UNORM-Format** auf hat oder kein Tiefenpuffer gebunden ist, wird der Biaswert wie folgt berechnet:
    ```
    Bias = (float)DepthBias * r + SlopeScaledDepthBias * MaxDepthSlope;
    ```

    

    Wobei *r* der darstellbare Mindestwert > 0 im in **float32** konvertierten Tiefenpufferformat ist. Die **Werte DepthBias** und **SlopeScaledDepthBias** sind [**D3D11 \_ RASTERIZER \_ DESC1-Strukturmitglieder.**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1) Der **MaxDepthSxel-Wert** ist das Maximum der horizontalen und vertikalen Steigung des Tiefenwerts am Pixel.
2.  Wenn ein Gleitkommatiefenpuffer an die Ausgabe-Merger-Phase gebunden ist, wird der Biaswert wie folgt berechnet:
    ```
    Bias = (float)DepthBias * 2**(exponent(max z in primitive) - r) +
                SlopeScaledDepthBias * MaxDepthSlope;
    ```

    

    Wobei *r* die Anzahl der Mantissebits in der Gleitkommadarstellung (mit Ausnahme des ausgeblendeten Bits) ist; Beispiel: 23 für **float32**.

Der Bias-Wert wird dann wie hiergeklammert:


```
if(DepthBiasClamp > 0)
    Bias = min(DepthBiasClamp, Bias)
else if(DepthBiasClamp < 0)
    Bias = max(DepthBiasClamp, Bias)
```



Der Biaswert wird dann verwendet, um die Pixeltiefe zu berechnen.


```
if ( (DepthBias != 0) || (SlopeScaledDepthBias != 0) )
    z = z + Bias
```



Tiefenverzerrungsvorgänge treten nach dem Clipping auf Scheitelungen auf, daher hat tiefenverzerrend keine Auswirkungen auf geometrische Clippings. Der Biaswert ist für einen bestimmten Primitiven konstant und wird dem z-Wert für jeden Scheitelpunkt vor dem Interpolatorsetup hinzugefügt. Bei Verwendung [der Featureebenen](overviews-direct3d-11-devices-downlevel-intro.md) 10.0 und höher werden alle Biasberechnungen mit 32-Bit-Gleitkommaarithmetik durchgeführt. Bias wird nicht auf Punkt- oder Linienprimitiven angewendet, mit Ausnahme von Linien, die im Wireframe-Modus gezeichnet werden.

Eines der Artefakte mit Schattenpuffer-basierten Schatten ist Schattenschatten oder ein Schatten auf der Oberfläche selbst aufgrund geringfügiger Unterschiede zwischen der Tiefenberechnung in einem Shader und der Tiefe derselben Oberfläche im Schattenpuffer. Eine Möglichkeit, dies zu entschärfen, ist die Verwendung **von DepthBias** und **SlopeScaledDepthBias** beim Rendern eines Schattenpuffers. Die Idee ist, Oberflächen beim Rendern eines Schattenpuffers ausreichend zu pushen, damit das Vergleichsergebnis (zwischen dem Schattenpuffer z und dem Shader z) über die Oberfläche konsistent ist, und lokales Selbstschatten zu vermeiden.

Die **Verwendung von DepthBias** und **SlopeScaledDepthBias** kann jedoch neue Renderingprobleme verursachen, wenn ein Polygon, das in einem extrem starken Winkel angezeigt wird, dazu führt, dass die Biasgleichung einen sehr großen z-Wert generiert. Dadurch wird das Polygon extrem weit von der ursprünglichen Oberfläche in der Schattenkarte entfernt. Eine Möglichkeit, dieses spezielle Problem zu beheben, ist die **Verwendung von DepthBiasClamp,** die eine Obergrenze (positiv oder negativ) für die Größe der berechneten Z-Abweichung bietet.

> [!Note]  
> Für [die Featureebenen](overviews-direct3d-11-devices-downlevel-intro.md) 9.1, 9.2, 9.3 wird **DepthBiasClamp** nicht unterstützt.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ausgabe-Merger-Phase](d3d10-graphics-programming-guide-output-merger-stage.md)
</dt> </dl>

 

 




