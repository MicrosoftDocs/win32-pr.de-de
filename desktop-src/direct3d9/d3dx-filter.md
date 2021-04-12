---
description: Die folgenden Flags werden verwendet, um anzugeben, auf welchen Kanälen in einer Textur gearbeitet werden soll.
ms.assetid: 0317b857-2512-4ad7-b6e3-82afdda7ea10
title: D3DX_FILTER
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 128525de2e403c11239c300372b79bd8ee8c1277
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481307"
---
# <a name="d3dx_filter"></a><span data-ttu-id="f8491-103">D3DX- \_ Filter</span><span class="sxs-lookup"><span data-stu-id="f8491-103">D3DX\_FILTER</span></span>

<span data-ttu-id="f8491-104">Die folgenden Flags werden verwendet, um anzugeben, auf welchen Kanälen in einer Textur gearbeitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f8491-104">The following flags are used to specify which channels in a texture to operate on.</span></span>



|                         |                                                                                                                                                                                                             |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8491-105">\#definieren</span><span class="sxs-lookup"><span data-stu-id="f8491-105">\#define</span></span>                | <span data-ttu-id="f8491-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f8491-106">Description</span></span>                                                                                                                                                                                                 |
| <span data-ttu-id="f8491-107">D3DX \_ Filter \_ None</span><span class="sxs-lookup"><span data-stu-id="f8491-107">D3DX\_FILTER\_NONE</span></span>      | <span data-ttu-id="f8491-108">Es findet keine Skalierung oder Filterung statt.</span><span class="sxs-lookup"><span data-stu-id="f8491-108">No scaling or filtering will take place.</span></span> <span data-ttu-id="f8491-109">Es wird davon ausgegangen, dass Pixel außerhalb der Begrenzungen des Quell Bilds transparent schwarz sind.</span><span class="sxs-lookup"><span data-stu-id="f8491-109">Pixels outside the bounds of the source image are assumed to be transparent black.</span></span>                                                                                 |
| <span data-ttu-id="f8491-110">D3DX- \_ Filter \_ Punkt</span><span class="sxs-lookup"><span data-stu-id="f8491-110">D3DX\_FILTER\_POINT</span></span>     | <span data-ttu-id="f8491-111">Jedes Zielpixel wird berechnet, indem das nächste Pixel aus dem Quell Image entnommen wird.</span><span class="sxs-lookup"><span data-stu-id="f8491-111">Each destination pixel is computed by sampling the nearest pixel from the source image.</span></span>                                                                                                                     |
| <span data-ttu-id="f8491-112">D3DX- \_ Filter \_ linear</span><span class="sxs-lookup"><span data-stu-id="f8491-112">D3DX\_FILTER\_LINEAR</span></span>    | <span data-ttu-id="f8491-113">Jedes Zielpixel wird berechnet, indem die vier nächsten Pixel aus dem Quell Image entnommen werden.</span><span class="sxs-lookup"><span data-stu-id="f8491-113">Each destination pixel is computed by sampling the four nearest pixels from the source image.</span></span> <span data-ttu-id="f8491-114">Dieser Filter funktioniert am besten, wenn die Skala auf beiden Achsen kleiner als zwei ist.</span><span class="sxs-lookup"><span data-stu-id="f8491-114">This filter works best when the scale on both axes is less than two.</span></span>                                          |
| <span data-ttu-id="f8491-115">D3DX \_ Filter \_ Dreieck</span><span class="sxs-lookup"><span data-stu-id="f8491-115">D3DX\_FILTER\_TRIANGLE</span></span>  | <span data-ttu-id="f8491-116">Jedes Pixel im Quell Image trägt gleichermaßen dem Ziel Image bei.</span><span class="sxs-lookup"><span data-stu-id="f8491-116">Every pixel in the source image contributes equally to the destination image.</span></span> <span data-ttu-id="f8491-117">Dies ist der langsamste der Filter.</span><span class="sxs-lookup"><span data-stu-id="f8491-117">This is the slowest of the filters.</span></span>                                                                                           |
| <span data-ttu-id="f8491-118">D3DX \_ Filter \_ Feld</span><span class="sxs-lookup"><span data-stu-id="f8491-118">D3DX\_FILTER\_BOX</span></span>       | <span data-ttu-id="f8491-119">Jedes Pixel wird berechnet, indem das Feld 2 x 2 (x2) aus dem Quell Abbild durchläuft.</span><span class="sxs-lookup"><span data-stu-id="f8491-119">Each pixel is computed by averaging a 2x2(x2) box of pixels from the source image.</span></span> <span data-ttu-id="f8491-120">Dieser Filter kann nur verwendet werden, wenn die Abmessungen des Ziels die Hälfte der der Quelle sind, wie es bei MipMaps der Fall ist.</span><span class="sxs-lookup"><span data-stu-id="f8491-120">This filter works only when the dimensions of the destination are half those of the source, as is the case with mipmaps.</span></span> |
| <span data-ttu-id="f8491-121">D3DX \_ Filter \_ Spiegelung \_ U</span><span class="sxs-lookup"><span data-stu-id="f8491-121">D3DX\_FILTER\_MIRROR\_U</span></span> | <span data-ttu-id="f8491-122">Pixel am Rand der Textur auf der u-Achse sollten gespiegelt, nicht umschließt werden.</span><span class="sxs-lookup"><span data-stu-id="f8491-122">Pixels off the edge of the texture on the u-axis should be mirrored, not wrapped.</span></span>                                                                                                                           |
| <span data-ttu-id="f8491-123">D3DX \_ Filter \_ Spiegelung \_ V</span><span class="sxs-lookup"><span data-stu-id="f8491-123">D3DX\_FILTER\_MIRROR\_V</span></span> | <span data-ttu-id="f8491-124">Pixel am Rand der Textur auf der v-Achse sollten gespiegelt und nicht umschließt werden.</span><span class="sxs-lookup"><span data-stu-id="f8491-124">Pixels off the edge of the texture on the v-axis should be mirrored, not wrapped.</span></span>                                                                                                                           |
| <span data-ttu-id="f8491-125">D3DX \_ Filter \_ Spiegelung \_</span><span class="sxs-lookup"><span data-stu-id="f8491-125">D3DX\_FILTER\_MIRROR\_W</span></span> | <span data-ttu-id="f8491-126">Pixel am Rand der Textur auf der w-Achse sollten gespiegelt, nicht umschließt werden.</span><span class="sxs-lookup"><span data-stu-id="f8491-126">Pixels off the edge of the texture on the w-axis should be mirrored, not wrapped.</span></span>                                                                                                                           |
| <span data-ttu-id="f8491-127">D3DX- \_ Filter \_ Spiegelung</span><span class="sxs-lookup"><span data-stu-id="f8491-127">D3DX\_FILTER\_MIRROR</span></span>    | <span data-ttu-id="f8491-128">Die Angabe dieses Flags ist identisch mit dem Angeben der D3DX \_ Filter \_ Mirror \_ U, D3DX \_ Filter \_ Spiegel \_ V und D3DX \_ Filter \_ Mirror \_ W-Flags.</span><span class="sxs-lookup"><span data-stu-id="f8491-128">Specifying this flag is the same as specifying the D3DX\_FILTER\_MIRROR\_U, D3DX\_FILTER\_MIRROR\_V, and D3DX\_FILTER\_MIRROR\_W flags.</span></span>                                                                     |
| <span data-ttu-id="f8491-129">D3DX \_ Filter \_ Dither</span><span class="sxs-lookup"><span data-stu-id="f8491-129">D3DX\_FILTER\_DITHER</span></span>    | <span data-ttu-id="f8491-130">Das resultierende Bild muss mit einem 4 x 4-geordneten Dithering-Algorithmus ausgeblendet werden.</span><span class="sxs-lookup"><span data-stu-id="f8491-130">The resulting image must be dithered using a 4x4 ordered dither algorithm.</span></span>                                                                                                                                  |
| <span data-ttu-id="f8491-131">D3DX \_ \_ sRGB Filtern \_ in</span><span class="sxs-lookup"><span data-stu-id="f8491-131">D3DX\_FILTER\_SRGB\_IN</span></span>  | <span data-ttu-id="f8491-132">Die Eingabedaten befinden sich im sRGB-Farbraum (Gamma 2,2).</span><span class="sxs-lookup"><span data-stu-id="f8491-132">Input data is in sRGB (gamma 2.2) color space.</span></span>                                                                                                                                                              |
| <span data-ttu-id="f8491-133">D3DX \_ filtert \_ sRGB \_ out</span><span class="sxs-lookup"><span data-stu-id="f8491-133">D3DX\_FILTER\_SRGB\_OUT</span></span> | <span data-ttu-id="f8491-134">Die Ausgabedaten befinden sich im sRGB-Farbraum (Gamma 2,2).</span><span class="sxs-lookup"><span data-stu-id="f8491-134">The output data is in sRGB (gamma 2.2) color space.</span></span>                                                                                                                                                         |
| <span data-ttu-id="f8491-135">D3DX \_ \_ sRGB Filtern</span><span class="sxs-lookup"><span data-stu-id="f8491-135">D3DX\_FILTER\_SRGB</span></span>      | <span data-ttu-id="f8491-136">Identisch \_ \_ mit der Angabe von D3DX Filter sRGB \_ in \| D3DX \_ Filter \_ sRGB \_ out.</span><span class="sxs-lookup"><span data-stu-id="f8491-136">Same as specifying D3DX\_FILTER\_SRGB\_IN \| D3DX\_FILTER\_SRGB\_OUT.</span></span>                                                                                                                                       |



 

<span data-ttu-id="f8491-137">Jeder gültige Filter muss genau eines der folgenden Flags enthalten: D3DX \_ Filter \_ None, D3DX \_ Filter \_ Point, D3DX \_ Filter \_ linear, D3DX \_ Filter \_ Dreieck oder D3DX \_ Filter \_ Box.</span><span class="sxs-lookup"><span data-stu-id="f8491-137">Each valid filter must contain exactly one of the following flags: D3DX\_FILTER\_NONE, D3DX\_FILTER\_POINT, D3DX\_FILTER\_LINEAR, D3DX\_FILTER\_TRIANGLE, or D3DX\_FILTER\_BOX.</span></span> <span data-ttu-id="f8491-138">Außerdem können Sie mit dem-Operator oder dem-Operator NULL oder mehr der folgenden optionalen Flags mit einem gültigen Filter angeben: D3DX \_ Filter \_ Mirror \_ U, D3DX \_ Filter \_ Mirror \_ V, D3DX \_ Filter \_ Mirror \_ W, D3DX \_ Filter \_ Mirror, D3DX \_ Filter \_ Dither, D3DX \_ Filter \_ sRGB \_ in, D3DX \_ Filter \_ sRGB \_ out oder D3DX \_ Filter \_ sRGB.</span><span class="sxs-lookup"><span data-stu-id="f8491-138">In addition, you can use the OR operator to specify zero or more of the following optional flags with a valid filter: D3DX\_FILTER\_MIRROR\_U, D3DX\_FILTER\_MIRROR\_V, D3DX\_FILTER\_MIRROR\_W, D3DX\_FILTER\_MIRROR, D3DX\_FILTER\_DITHER, D3DX\_FILTER\_SRGB\_IN, D3DX\_FILTER\_SRGB\_OUT or D3DX\_FILTER\_SRGB.</span></span>

<span data-ttu-id="f8491-139">Das angeben \_ von D3DX default für diesen Parameter entspricht in der Regel der Angabe von D3DX \_ Filter \_ Dreieck \| D3DX \_ Filter \_ Dither.</span><span class="sxs-lookup"><span data-stu-id="f8491-139">Specifying D3DX\_DEFAULT for this parameter is usually the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span> <span data-ttu-id="f8491-140">D3DX \_ Default kann jedoch unterschiedliche Bedeutungen haben, je nachdem, welche Methode den Filter verwendet.</span><span class="sxs-lookup"><span data-stu-id="f8491-140">However, D3DX\_DEFAULT can have different meanings, depending on which method uses the filter.</span></span> <span data-ttu-id="f8491-141">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="f8491-141">For example:</span></span>

-   <span data-ttu-id="f8491-142">Bei Verwendung von [**D3DXCreateTextureFromFileEx**](d3dxcreatetexturefromfileex.md)wird D3DX \_ standardmäßig D3DX \_ Filter \_ Dreieck \| D3DX \_ Filter \_ Dither zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="f8491-142">When using [**D3DXCreateTextureFromFileEx**](d3dxcreatetexturefromfileex.md), D3DX\_DEFAULT maps to D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>
-   <span data-ttu-id="f8491-143">Wenn Sie [**D3DXFilterTexture**](d3dxfiltertexture.md)verwenden, \_ wird D3DX standardmäßig D3DX \_ Filter Box zugeordnet, \_ Wenn die Textur Größe eine Potenz von zwei ist, und D3DX \_ Filter \_ Box \| D3DX \_ Filter \_ anderenfalls.</span><span class="sxs-lookup"><span data-stu-id="f8491-143">When using [**D3DXFilterTexture**](d3dxfiltertexture.md), D3DX\_DEFAULT maps to D3DX\_FILTER\_BOX if the texture size is a power of two, and D3DX\_FILTER\_BOX \| D3DX\_FILTER\_DITHER otherwise.</span></span>

<span data-ttu-id="f8491-144">Verweisen Sie auf jede Methode, um Informationen dazu zu finden, wie D3DX \_ default Filter zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="f8491-144">Reference each method to check for information about how D3DX\_DEFAULT filter is mapped.</span></span>

## <a name="constant-information"></a><span data-ttu-id="f8491-145">Konstante Informationen</span><span class="sxs-lookup"><span data-stu-id="f8491-145">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="f8491-146">Header</span><span class="sxs-lookup"><span data-stu-id="f8491-146">Header</span></span>                   | <span data-ttu-id="f8491-147">d3dx9tex. h</span><span class="sxs-lookup"><span data-stu-id="f8491-147">d3dx9tex.h</span></span> |
| <span data-ttu-id="f8491-148">Mindestens Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="f8491-148">Minimum operating system</span></span> | <span data-ttu-id="f8491-149">Windows 98</span><span class="sxs-lookup"><span data-stu-id="f8491-149">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="f8491-150">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f8491-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f8491-151">D3DX-Konstanten</span><span class="sxs-lookup"><span data-stu-id="f8491-151">D3DX Constants</span></span>](dx9-graphics-reference-d3dx-constants.md)
</dt> </dl>

 

 



