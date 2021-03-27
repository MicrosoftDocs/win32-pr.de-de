---
title: Tiefenausrichtung
description: Polygone, die in 3D-Raum kopiert werden, können so dargestellt werden, als wären Sie nicht durch Hinzufügen einer z-Bias (oder einer tiefen Abweichung) zu jeder Form.
ms.assetid: ee904316-dc6d-48a4-bdb7-0f7dcdb9d9d6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d6f9a3850b03e033a90b358d0c6ffd1ceef830f
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "103734936"
---
# <a name="depth-bias"></a>Tiefenausrichtung

Polygone, die in 3D-Raum kopiert werden, können so dargestellt werden, als wären Sie nicht durch Hinzufügen einer z-Bias (oder einer tiefen Abweichung) zu jeder Form.

Dies ist eine Technik, die häufig verwendet wird, um sicherzustellen, dass Schatten in einer Szene ordnungsgemäß angezeigt werden. Beispielsweise hat ein Schatten auf einer Wand wahrscheinlich denselben tiefen Wert wie die Wand. Wenn eine Anwendung zuerst eine Wand und dann einen Schatten rendert, ist der Schatten möglicherweise nicht sichtbar, oder es sind keine tiefen Artefakte sichtbar.


Eine Anwendung kann sicherstellen, dass kopale Polygone ordnungsgemäß gerendert werden, indem Sie den z-Werten (aus dem **depthbias** -Member von [**D3D11 \_ Rasterizer \_ DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1)) den z-Werten hinzufügen, die das System beim Rendern der Mengen von Coplanar-Polygonen verwendet. Polygone mit einem größeren z-Wert werden vor Polygonen mit einem kleineren z-Wert gezeichnet.

Es gibt zwei Optionen für die Berechnung der tiefen Abweichung.

1.  Wenn der derzeit an die Output-Fusion-Stufe gebundene tiefen Puffer ein **unorm** -Format aufweist oder kein tiefen Puffer gebunden ist, wird der Wert für den Wert wie folgt berechnet:
    ```
    Bias = (float)DepthBias * r + SlopeScaledDepthBias * MaxDepthSlope;
    ```

    

    Dabei ist *r* der minimale darstellbare Wert > 0 im Tiefe-Puffer-Format, das in **float32** konvertiert wird. Die Werte **depthbias** und **slopescaleddepthbias** sind [**D3D11 \_ Rasterizer \_ DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1) Structure Members. Der Wert **maxdepthslope** ist das Maximum der horizontalen und vertikalen Hänge des tiefen Werts auf dem Pixel.
2.  Wenn ein Gleit Komma Tiefe-Puffer an die Output-Merger-Phase gebunden ist, wird der Wert für die Ausrichtung wie folgt berechnet:
    ```
    Bias = (float)DepthBias * 2**(exponent(max z in primitive) - r) +
                SlopeScaledDepthBias * MaxDepthSlope;
    ```

    

    Dabei ist *r* die Anzahl der Mantisse-Bits in der Gleit Komma Darstellung (mit Ausnahme des ausgeblendeten Bits). beispielsweise 23 für **float32**.

Der Wert "Bias" wird dann wie folgt gebunden:


```
if(DepthBiasClamp > 0)
    Bias = min(DepthBiasClamp, Bias)
else if(DepthBiasClamp < 0)
    Bias = max(DepthBiasClamp, Bias)
```



Der Wert "Bias" wird dann verwendet, um die Pixel Tiefe zu berechnen.


```
if ( (DepthBias != 0) || (SlopeScaledDepthBias != 0) )
    z = z + Bias
```



Tiefe-bidirektionoperationen werden nach dem Abschneiden in Scheitel Punkten ausgeführt. Daher hat die tiefen Abweichung keine Auswirkung auf das geometrische Clipping. Der Wert "Bias" ist für ein bestimmtes primitiv konstant und wird vor dem interpolatorsetup dem z-Wert für jeden Scheitelpunkt hinzugefügt. Wenn Sie [featureebenen](overviews-direct3d-11-devices-downlevel-intro.md) 10,0 und höher verwenden, werden alle Bias-Berechnungen mithilfe von Gleit Komma Zahlen mit 32 Bit ausgeführt. Der-Wert wird auf keine Punkt-oder Zeilen primitiven angewendet, mit Ausnahme von Linien, die im Draht Modell-Modus gezeichnet werden.

Eines der Artefakte mit Schatten Puffer basierten Schatten ist eine Schatten-Akne oder eine Oberfläche, die sich selbst aufgrund von geringfügigen Unterschieden zwischen der tiefen Berechnung in einem Shader und der Tiefe der gleichen Oberfläche im Schatten Puffer befindet. Eine Möglichkeit, dies zu umgehen, ist die Verwendung von **depthbias** und **slopescaleddepthbias** beim Rendern eines Schatten Puffers. Die Idee besteht darin, die Oberflächen beim Rendern eines Schatten Puffers ausreichend zu bewegen, damit das Vergleichs Ergebnis (zwischen dem Schatten Puffer z und dem Shader z) auf der gesamten Oberfläche konsistent ist, und eine lokale selbst Shadowing vermeiden.

Die Verwendung von **depthbias** und **slopescaleddepthbias** kann jedoch zu neuen Renderingproblemen führen, wenn ein Polygon, das in einem extrem spitzen Winkel angezeigt wird, bewirkt, dass die Bias-Gleichung einen sehr großen z-Wert generiert. Dadurch wird das Polygon extrem weit von der ursprünglichen Oberfläche in der schattenkarte entfernt. Eine Möglichkeit, dieses Problem zu beheben, ist die Verwendung von **depthbiasclamp**, das eine obere Grenze (positiv oder negativ) für die Größe des berechneten z-Bias bereitstellt.

> [!Note]  
> Für [featureebenen](overviews-direct3d-11-devices-downlevel-intro.md) 9,1, 9,2, 9,3, wird **depthbiasclamp** nicht unterstützt.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ausgabe-Fusion-Phase](d3d10-graphics-programming-guide-output-merger-stage.md)
</dt> </dl>

 

 




