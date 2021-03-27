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
# <a name="depth-bias"></a><span data-ttu-id="645e1-103">Tiefenausrichtung</span><span class="sxs-lookup"><span data-stu-id="645e1-103">Depth Bias</span></span>

<span data-ttu-id="645e1-104">Polygone, die in 3D-Raum kopiert werden, können so dargestellt werden, als wären Sie nicht durch Hinzufügen einer z-Bias (oder einer tiefen Abweichung) zu jeder Form.</span><span class="sxs-lookup"><span data-stu-id="645e1-104">Polygons that are coplanar in 3D space can be made to appear as if they are not coplanar by adding a z-bias (or depth bias) to each one.</span></span>

<span data-ttu-id="645e1-105">Dies ist eine Technik, die häufig verwendet wird, um sicherzustellen, dass Schatten in einer Szene ordnungsgemäß angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="645e1-105">This is a technique commonly used to ensure that shadows in a scene are displayed properly.</span></span> <span data-ttu-id="645e1-106">Beispielsweise hat ein Schatten auf einer Wand wahrscheinlich denselben tiefen Wert wie die Wand.</span><span class="sxs-lookup"><span data-stu-id="645e1-106">For instance, a shadow on a wall will likely have the same depth value as the wall.</span></span> <span data-ttu-id="645e1-107">Wenn eine Anwendung zuerst eine Wand und dann einen Schatten rendert, ist der Schatten möglicherweise nicht sichtbar, oder es sind keine tiefen Artefakte sichtbar.</span><span class="sxs-lookup"><span data-stu-id="645e1-107">If an application renders a wall first and then a shadow, the shadow might not be visible, or depth artifacts might be visible.</span></span>


<span data-ttu-id="645e1-108">Eine Anwendung kann sicherstellen, dass kopale Polygone ordnungsgemäß gerendert werden, indem Sie den z-Werten (aus dem **depthbias** -Member von [**D3D11 \_ Rasterizer \_ DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1)) den z-Werten hinzufügen, die das System beim Rendern der Mengen von Coplanar-Polygonen verwendet.</span><span class="sxs-lookup"><span data-stu-id="645e1-108">An application can help ensure that coplanar polygons are rendered properly by adding the bias (from the **DepthBias** member of [**D3D11\_RASTERIZER\_DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1)) to the z-values that the system uses when rendering the sets of coplanar polygons.</span></span> <span data-ttu-id="645e1-109">Polygone mit einem größeren z-Wert werden vor Polygonen mit einem kleineren z-Wert gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="645e1-109">Polygons with a larger z value will be drawn in front of polygons with a smaller z value.</span></span>

<span data-ttu-id="645e1-110">Es gibt zwei Optionen für die Berechnung der tiefen Abweichung.</span><span class="sxs-lookup"><span data-stu-id="645e1-110">There are two options for calculating depth bias.</span></span>

1.  <span data-ttu-id="645e1-111">Wenn der derzeit an die Output-Fusion-Stufe gebundene tiefen Puffer ein **unorm** -Format aufweist oder kein tiefen Puffer gebunden ist, wird der Wert für den Wert wie folgt berechnet:</span><span class="sxs-lookup"><span data-stu-id="645e1-111">If the depth buffer currently bound to the output-merger stage has a **UNORM** format or no depth buffer is bound, the bias value is calculated like this:</span></span>
    ```
    Bias = (float)DepthBias * r + SlopeScaledDepthBias * MaxDepthSlope;
    ```

    

    <span data-ttu-id="645e1-112">Dabei ist *r* der minimale darstellbare Wert > 0 im Tiefe-Puffer-Format, das in **float32** konvertiert wird.</span><span class="sxs-lookup"><span data-stu-id="645e1-112">where *r* is the minimum representable value > 0 in the depth-buffer format converted to **float32**.</span></span> <span data-ttu-id="645e1-113">Die Werte **depthbias** und **slopescaleddepthbias** sind [**D3D11 \_ Rasterizer \_ DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1) Structure Members.</span><span class="sxs-lookup"><span data-stu-id="645e1-113">The **DepthBias** and **SlopeScaledDepthBias** values are [**D3D11\_RASTERIZER\_DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1) structure members.</span></span> <span data-ttu-id="645e1-114">Der Wert **maxdepthslope** ist das Maximum der horizontalen und vertikalen Hänge des tiefen Werts auf dem Pixel.</span><span class="sxs-lookup"><span data-stu-id="645e1-114">The **MaxDepthSlope** value is the maximum of the horizontal and vertical slopes of the depth value at the pixel.</span></span>
2.  <span data-ttu-id="645e1-115">Wenn ein Gleit Komma Tiefe-Puffer an die Output-Merger-Phase gebunden ist, wird der Wert für die Ausrichtung wie folgt berechnet:</span><span class="sxs-lookup"><span data-stu-id="645e1-115">If a floating-point depth buffer is bound to the output-merger stage the bias value is calculated like this:</span></span>
    ```
    Bias = (float)DepthBias * 2**(exponent(max z in primitive) - r) +
                SlopeScaledDepthBias * MaxDepthSlope;
    ```

    

    <span data-ttu-id="645e1-116">Dabei ist *r* die Anzahl der Mantisse-Bits in der Gleit Komma Darstellung (mit Ausnahme des ausgeblendeten Bits). beispielsweise 23 für **float32**.</span><span class="sxs-lookup"><span data-stu-id="645e1-116">where *r* is the number of mantissa bits in the floating point representation (excluding the hidden bit); for example, 23 for **float32**.</span></span>

<span data-ttu-id="645e1-117">Der Wert "Bias" wird dann wie folgt gebunden:</span><span class="sxs-lookup"><span data-stu-id="645e1-117">The bias value is then clamped like this:</span></span>


```
if(DepthBiasClamp > 0)
    Bias = min(DepthBiasClamp, Bias)
else if(DepthBiasClamp < 0)
    Bias = max(DepthBiasClamp, Bias)
```



<span data-ttu-id="645e1-118">Der Wert "Bias" wird dann verwendet, um die Pixel Tiefe zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="645e1-118">The bias value is then used to calculate the pixel depth.</span></span>


```
if ( (DepthBias != 0) || (SlopeScaledDepthBias != 0) )
    z = z + Bias
```



<span data-ttu-id="645e1-119">Tiefe-bidirektionoperationen werden nach dem Abschneiden in Scheitel Punkten ausgeführt. Daher hat die tiefen Abweichung keine Auswirkung auf das geometrische Clipping.</span><span class="sxs-lookup"><span data-stu-id="645e1-119">Depth-bias operations occur on vertices after clipping, therefore, depth-bias has no effect on geometric clipping.</span></span> <span data-ttu-id="645e1-120">Der Wert "Bias" ist für ein bestimmtes primitiv konstant und wird vor dem interpolatorsetup dem z-Wert für jeden Scheitelpunkt hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="645e1-120">The bias value is constant for a given primitive and is added to the z value for each vertex before interpolator setup.</span></span> <span data-ttu-id="645e1-121">Wenn Sie [featureebenen](overviews-direct3d-11-devices-downlevel-intro.md) 10,0 und höher verwenden, werden alle Bias-Berechnungen mithilfe von Gleit Komma Zahlen mit 32 Bit ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="645e1-121">When you use [feature levels](overviews-direct3d-11-devices-downlevel-intro.md) 10.0 and higher, all bias calculations are performed using 32-bit floating-point arithmetic.</span></span> <span data-ttu-id="645e1-122">Der-Wert wird auf keine Punkt-oder Zeilen primitiven angewendet, mit Ausnahme von Linien, die im Draht Modell-Modus gezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="645e1-122">Bias is not applied to any point or line primitives, except for lines drawn in wireframe mode.</span></span>

<span data-ttu-id="645e1-123">Eines der Artefakte mit Schatten Puffer basierten Schatten ist eine Schatten-Akne oder eine Oberfläche, die sich selbst aufgrund von geringfügigen Unterschieden zwischen der tiefen Berechnung in einem Shader und der Tiefe der gleichen Oberfläche im Schatten Puffer befindet.</span><span class="sxs-lookup"><span data-stu-id="645e1-123">One of the artifacts with shadow buffer based shadows is shadow acne, or a surface shadowing itself due to minor differences between the depth computation in a shader, and the depth of the same surface in the shadow buffer.</span></span> <span data-ttu-id="645e1-124">Eine Möglichkeit, dies zu umgehen, ist die Verwendung von **depthbias** und **slopescaleddepthbias** beim Rendern eines Schatten Puffers.</span><span class="sxs-lookup"><span data-stu-id="645e1-124">One way to alleviate this is to use **DepthBias** and **SlopeScaledDepthBias** when rendering a shadow buffer.</span></span> <span data-ttu-id="645e1-125">Die Idee besteht darin, die Oberflächen beim Rendern eines Schatten Puffers ausreichend zu bewegen, damit das Vergleichs Ergebnis (zwischen dem Schatten Puffer z und dem Shader z) auf der gesamten Oberfläche konsistent ist, und eine lokale selbst Shadowing vermeiden.</span><span class="sxs-lookup"><span data-stu-id="645e1-125">The idea is to push surfaces out enough while rendering a shadow buffer so that the comparison result (between the shadow buffer z and the shader z) is consistent across the surface, and avoid local self-shadowing.</span></span>

<span data-ttu-id="645e1-126">Die Verwendung von **depthbias** und **slopescaleddepthbias** kann jedoch zu neuen Renderingproblemen führen, wenn ein Polygon, das in einem extrem spitzen Winkel angezeigt wird, bewirkt, dass die Bias-Gleichung einen sehr großen z-Wert generiert.</span><span class="sxs-lookup"><span data-stu-id="645e1-126">However, using **DepthBias** and **SlopeScaledDepthBias** can introduce new rendering problems when a polygon viewed at an extremely sharp angle causes the bias equation to generate a very large z value.</span></span> <span data-ttu-id="645e1-127">Dadurch wird das Polygon extrem weit von der ursprünglichen Oberfläche in der schattenkarte entfernt.</span><span class="sxs-lookup"><span data-stu-id="645e1-127">This in effect pushes the polygon extremely far away from the original surface in the shadow map.</span></span> <span data-ttu-id="645e1-128">Eine Möglichkeit, dieses Problem zu beheben, ist die Verwendung von **depthbiasclamp**, das eine obere Grenze (positiv oder negativ) für die Größe des berechneten z-Bias bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="645e1-128">One way to help alleviate this particular problem is to use **DepthBiasClamp**, which provides an upper bound (positive or negative) on the magnitude of the z bias calculated.</span></span>

> [!Note]  
> <span data-ttu-id="645e1-129">Für [featureebenen](overviews-direct3d-11-devices-downlevel-intro.md) 9,1, 9,2, 9,3, wird **depthbiasclamp** nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="645e1-129">For [feature levels](overviews-direct3d-11-devices-downlevel-intro.md) 9.1, 9.2, 9.3, **DepthBiasClamp** is not supported.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="645e1-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="645e1-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="645e1-131">Ausgabe-Fusion-Phase</span><span class="sxs-lookup"><span data-stu-id="645e1-131">Output-Merger Stage</span></span>](d3d10-graphics-programming-guide-output-merger-stage.md)
</dt> </dl>

 

 




