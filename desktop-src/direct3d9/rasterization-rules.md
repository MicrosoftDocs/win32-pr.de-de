---
description: Häufig Stimmen die für Scheitel Punkte angegebenen Punkte nicht exakt mit den Pixeln auf dem Bildschirm identisch. In diesem Fall wendet Direct3D Dreiecks rasterisierungsregeln an, um zu entscheiden, welche Pixel für ein bestimmtes Dreieck gelten.
ms.assetid: 919b36f1-d4de-4d5d-ba1a-0605bf59a6cd
title: Rasterisierungsregeln (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5115b2f12e0064202fcbca58f52cb163166d0a82
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/04/2021
ms.locfileid: "104218910"
---
# <a name="rasterization-rules-direct3d-9"></a><span data-ttu-id="901f0-104">Rasterisierungsregeln (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="901f0-104">Rasterization Rules (Direct3D 9)</span></span>

<span data-ttu-id="901f0-105">Häufig Stimmen die für Scheitel Punkte angegebenen Punkte nicht exakt mit den Pixeln auf dem Bildschirm identisch.</span><span class="sxs-lookup"><span data-stu-id="901f0-105">Often, the points specified for vertices do not precisely match the pixels on the screen.</span></span> <span data-ttu-id="901f0-106">In diesem Fall wendet Direct3D Dreiecks rasterisierungsregeln an, um zu entscheiden, welche Pixel für ein bestimmtes Dreieck gelten.</span><span class="sxs-lookup"><span data-stu-id="901f0-106">When this happens, Direct3D applies triangle rasterization rules to decide which pixels apply to a given triangle.</span></span>

-   [<span data-ttu-id="901f0-107">Dreiecks rasterisierungsregeln</span><span class="sxs-lookup"><span data-stu-id="901f0-107">Triangle Rasterization Rules</span></span>](#triangle-rasterization-rules)
-   [<span data-ttu-id="901f0-108">Punkt-und Linien Regeln</span><span class="sxs-lookup"><span data-stu-id="901f0-108">Point and Line Rules</span></span>](#point-and-line-rules)
-   [<span data-ttu-id="901f0-109">Punkt Sprite-Regeln</span><span class="sxs-lookup"><span data-stu-id="901f0-109">Point Sprite Rules</span></span>](#point-sprite-rules)

## <a name="triangle-rasterization-rules"></a><span data-ttu-id="901f0-110">Dreiecks rasterisierungsregeln</span><span class="sxs-lookup"><span data-stu-id="901f0-110">Triangle Rasterization Rules</span></span>

<span data-ttu-id="901f0-111">Direct3D verwendet zum Auffüllen der Geometrie eine obere linke Füllungs Konvention.</span><span class="sxs-lookup"><span data-stu-id="901f0-111">Direct3D uses a top-left filling convention for filling geometry.</span></span> <span data-ttu-id="901f0-112">Dabei handelt es sich um dieselbe Konvention, die für Rechtecke in GDI und OpenGL verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="901f0-112">This is the same convention that is used for rectangles in GDI and OpenGL.</span></span> <span data-ttu-id="901f0-113">In Direct3D ist der Mittelpunkt des Pixels der entscheidende Punkt.</span><span class="sxs-lookup"><span data-stu-id="901f0-113">In Direct3D, the center of the pixel is the decisive point.</span></span> <span data-ttu-id="901f0-114">Wenn sich das Zentrum in einem Dreieck befindet, ist das Pixel Teil des Dreiecks.</span><span class="sxs-lookup"><span data-stu-id="901f0-114">If the center is inside a triangle, the pixel is part of the triangle.</span></span> <span data-ttu-id="901f0-115">Pixel Center sind an ganzzahligen Koordinaten.</span><span class="sxs-lookup"><span data-stu-id="901f0-115">Pixel centers are at integer coordinates.</span></span>

<span data-ttu-id="901f0-116">Diese Beschreibung der von Direct3D verwendeten Dreiecks rasterisierungsregeln gilt nicht notwendigerweise für alle verfügbaren Hardware.</span><span class="sxs-lookup"><span data-stu-id="901f0-116">This description of triangle-rasterization rules used by Direct3D does not necessarily apply to all available hardware.</span></span> <span data-ttu-id="901f0-117">Die Tests können kleinere Abweichungen in der Implementierung dieser Regeln aufdecken.</span><span class="sxs-lookup"><span data-stu-id="901f0-117">Your testing may uncover minor variations in the implementation of these rules.</span></span>

<span data-ttu-id="901f0-118">Die folgende Abbildung zeigt ein Rechteck, dessen linke obere Ecke bei (0,0) liegt und dessen untere rechte Ecke um (5, 5) liegt.</span><span class="sxs-lookup"><span data-stu-id="901f0-118">The following illustration shows a rectangle whose upper-left corner is at (0, 0) and whose lower-right corner is at (5, 5).</span></span> <span data-ttu-id="901f0-119">Dieses Rechteck füllt 25 Pixel wie erwartet aus.</span><span class="sxs-lookup"><span data-stu-id="901f0-119">This rectangle fills 25 pixels, just as you would expect.</span></span> <span data-ttu-id="901f0-120">Die Breite des Rechtecks wird als rechts minus Links definiert.</span><span class="sxs-lookup"><span data-stu-id="901f0-120">The width of the rectangle is defined as right minus left.</span></span> <span data-ttu-id="901f0-121">Die Höhe ist als "Bottom minus Top" definiert.</span><span class="sxs-lookup"><span data-stu-id="901f0-121">The height is defined as bottom minus top.</span></span>

![Abbildung eines nummerierten Quadrats, das in sechs Zeilen und Spalten aufgeteilt ist](images/pixmap.png)

<span data-ttu-id="901f0-123">In der oberen linken Füllungs Konvention verweist *Top* auf die vertikale Position horizontaler spannen, und *left* bezieht sich auf die horizontale Position der Pixel innerhalb einer Spanne.</span><span class="sxs-lookup"><span data-stu-id="901f0-123">In the top-left filling convention, *top* refers to the vertical location of horizontal spans, and *left* refers to the horizontal location of pixels within a span.</span></span> <span data-ttu-id="901f0-124">Ein Edge darf kein oberer Rand sein, es sei denn, er ist horizontal.</span><span class="sxs-lookup"><span data-stu-id="901f0-124">An edge cannot be a top edge unless it is horizontal.</span></span> <span data-ttu-id="901f0-125">Im Allgemeinen haben die meisten Dreiecke nur den linken und rechten Rand.</span><span class="sxs-lookup"><span data-stu-id="901f0-125">In general, most triangles have only left and right edges.</span></span> <span data-ttu-id="901f0-126">Die folgende Abbildung zeigt einen oberen und einen rechten Rand.</span><span class="sxs-lookup"><span data-stu-id="901f0-126">The following illustration shows a top edge and a right edge.</span></span>

![Abbildung eines nummerierten Quadrats, das zwei Dreiecke enthält](images/triedge.png)

<span data-ttu-id="901f0-128">Die obere linke Füllungs Konvention bestimmt die Aktion, die von Direct3D ausgeführt wird, wenn ein Dreieck den Mittelpunkt eines Pixels durchläuft.</span><span class="sxs-lookup"><span data-stu-id="901f0-128">The top-left filling convention determines the action taken by Direct3D when a triangle passes through the center of a pixel.</span></span> <span data-ttu-id="901f0-129">Die folgende Abbildung zeigt zwei Dreiecke: eins bei (0,0), (5, 0) und (5, 5) und das andere bei (0,0), (0, 0) und (5, 5).</span><span class="sxs-lookup"><span data-stu-id="901f0-129">The following illustration shows two triangles, one at (0, 0), (5, 0), and (5, 5), and the other at (0, 5), (0, 0), and (5, 5).</span></span> <span data-ttu-id="901f0-130">Das erste Dreieck in diesem Fall erhält 15 Pixel (schwarz dargestellt), während das zweite nur 10 Pixel (grau dargestellt) erhält, da der freigegebene Rand der linke Rand des ersten Dreiecks ist.</span><span class="sxs-lookup"><span data-stu-id="901f0-130">The first triangle in this case gets 15 pixels (shown in black), whereas the second gets only 10 pixels (shown in gray) because the shared edge is the left edge of the first triangle.</span></span>

![Abbildung eines nummerierten Quadrats, das zwei Dreiecke anzeigt](images/twotris.png)

<span data-ttu-id="901f0-132">Wenn Sie ein Rechteck mit der linken oberen Ecke bei (0,5, 0,5) und der unteren rechten Ecke um (2,5, 4,5) definieren, befindet sich der Mittelpunkt dieses Rechtecks bei (1,5, 2,5).</span><span class="sxs-lookup"><span data-stu-id="901f0-132">If you define a rectangle with its upper-left corner at (0.5, 0.5) and its lower-right corner at (2.5, 4.5), the center point of this rectangle is at (1.5, 2.5).</span></span> <span data-ttu-id="901f0-133">Wenn das Direct3D Raster-Element dieses Rechteck durchläuft, ist die Mitte der einzelnen Pixel eindeutig innerhalb der vier Dreiecke, und die obere linke Füllungs Konvention ist nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="901f0-133">When the Direct3D rasterizer tessellates this rectangle, the center of each pixel is unambiguously inside each of the four triangles, and the top-left filling convention is not needed.</span></span> <span data-ttu-id="901f0-134">Dies wird in der folgenden Abbildung veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="901f0-134">The following illustration shows this.</span></span> <span data-ttu-id="901f0-135">Die Pixel im Rechteck sind entsprechend dem Dreieck gekennzeichnet, in dem Direct3D Sie enthält.</span><span class="sxs-lookup"><span data-stu-id="901f0-135">The pixels in the rectangle are labeled according to the triangle in which Direct3D includes them.</span></span>

![Zeigt ein nummeriertes Quadrat an, das ein Rechteck enthält, das in vier Dreiecke aufgeteilt ist.](images/noambig.png)

<span data-ttu-id="901f0-137">Wenn Sie das Rechteck in der obigen Abbildung verschieben, sodass sich die obere linke Ecke bei (1,0, 1,0), der unteren rechten Ecke bei (3,0, 5,0) und dem zugehörigen Mittelpunkt bei (2,0, 3,0) befindet, wendet Direct3D die obere Füllungs Konvention an.</span><span class="sxs-lookup"><span data-stu-id="901f0-137">If you move the rectangle in the preceding illustration so that its upper-left corner is at (1.0, 1.0), its lower-right corner at (3.0, 5.0), and its center point at (2.0, 3.0), Direct3D applies the top-left filling convention.</span></span> <span data-ttu-id="901f0-138">Die meisten Pixel dieses Rechtecks verspannen den Rahmen zwischen zwei oder mehr Dreiecken, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="901f0-138">Most pixels in this rectangle straddle the border between two or more triangles, as the following illustration shows.</span></span>

![Abbildung eines nummerierten Quadrats, das ein Rechteck enthält, das in vier Dreiecke aufgeteilt ist](images/fillrule.png)

<span data-ttu-id="901f0-140">Bei beiden Rechtecke sind die gleichen Pixel betroffen, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="901f0-140">For both rectangles, the same pixels are affected, as shown in the following illustration.</span></span>

![Abbildung von Pixeln, die von den vorangehenden zwei nummerierten Quadraten betroffen sind](images/samepix.png)

## <a name="point-and-line-rules"></a><span data-ttu-id="901f0-142">Punkt-und Linien Regeln</span><span class="sxs-lookup"><span data-stu-id="901f0-142">Point and Line Rules</span></span>

<span data-ttu-id="901f0-143">Punkte werden genauso wie Punkt Sprite gerendert, die beide als Bildschirm ausgerichtete vierpunkte gerendert werden und somit denselben Regeln wie das Polygon Rendering entsprechen.</span><span class="sxs-lookup"><span data-stu-id="901f0-143">Points are rendered the same as point sprites, which are both rendered as screen-aligned quadrilaterals and thus adhere to the same rules as polygon rendering.</span></span>

<span data-ttu-id="901f0-144">Zeilen Rendering-Regeln mit nicht-Antialiasing sind identisch mit denen für [GDI-Zeilen](../gdi/lines.md).</span><span class="sxs-lookup"><span data-stu-id="901f0-144">Non-antialiased line rendering rules are exactly the same as those for [GDI lines](../gdi/lines.md).</span></span>

<span data-ttu-id="901f0-145">Weitere Informationen zum Rendern von Zeilen mit Antialiasing finden Sie unter [**ID3DXLine**](id3dxline.md).</span><span class="sxs-lookup"><span data-stu-id="901f0-145">For information about antialiased line rendering, see [**ID3DXLine**](id3dxline.md).</span></span>

## <a name="point-sprite-rules"></a><span data-ttu-id="901f0-146">Punkt Sprite-Regeln</span><span class="sxs-lookup"><span data-stu-id="901f0-146">Point Sprite Rules</span></span>

<span data-ttu-id="901f0-147">Punkt Sprite und patchprimitiver werden so rasterisiert, als ob die primitiven zuerst in Dreiecke und die resultierenden Dreiecke in Dreiecke unterteilt wurden.</span><span class="sxs-lookup"><span data-stu-id="901f0-147">Point sprites and patch primitives are rasterized as if the primitives were first tessellated into triangles and the resulting triangles rasterized.</span></span> <span data-ttu-id="901f0-148">Weitere Informationen finden Sie unter [Punkt Sprites (Direct3D 9)](point-sprites.md).</span><span class="sxs-lookup"><span data-stu-id="901f0-148">For more information, see [Point Sprites (Direct3D 9)](point-sprites.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="901f0-149">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="901f0-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="901f0-150">Koordinatensysteme und Geometrie</span><span class="sxs-lookup"><span data-stu-id="901f0-150">Coordinate Systems and Geometry</span></span>](coordinate-systems-and-geometry.md)
</dt> </dl>

 

 
