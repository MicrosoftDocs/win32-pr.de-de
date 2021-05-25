---
description: Die folgenden Flags werden verwendet, um anzugeben, welche Kanäle in einer Textur verwendet werden sollen.
ms.assetid: 0317b857-2512-4ad7-b6e3-82afdda7ea10
title: D3DX_FILTER
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c83fd0b3e12d6b5bccb13f9c5fab5e078587dbd4
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/24/2021
ms.locfileid: "110342865"
---
# <a name="d3dx_filter"></a><span data-ttu-id="fc178-103">\_D3DX-FILTER</span><span class="sxs-lookup"><span data-stu-id="fc178-103">D3DX\_FILTER</span></span>

<span data-ttu-id="fc178-104">Die folgenden Flags werden verwendet, um anzugeben, welche Kanäle in einer Textur verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="fc178-104">The following flags are used to specify which channels in a texture to operate on.</span></span>



| <span data-ttu-id="fc178-105">\#Definieren</span><span class="sxs-lookup"><span data-stu-id="fc178-105">\#define</span></span>                | <span data-ttu-id="fc178-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fc178-106">Description</span></span>                                                                                                                                                                                                 |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc178-107">D3DX \_ FILTER \_ NONE</span><span class="sxs-lookup"><span data-stu-id="fc178-107">D3DX\_FILTER\_NONE</span></span>      | <span data-ttu-id="fc178-108">Es erfolgt keine Skalierung oder Filterung.</span><span class="sxs-lookup"><span data-stu-id="fc178-108">No scaling or filtering will take place.</span></span> <span data-ttu-id="fc178-109">Pixel außerhalb der Grenzen des Quellbilds werden als transparent schwarz angenommen.</span><span class="sxs-lookup"><span data-stu-id="fc178-109">Pixels outside the bounds of the source image are assumed to be transparent black.</span></span>                                                                                 |
| <span data-ttu-id="fc178-110">\_D3DX-FILTERPUNKT \_</span><span class="sxs-lookup"><span data-stu-id="fc178-110">D3DX\_FILTER\_POINT</span></span>     | <span data-ttu-id="fc178-111">Jedes Zielpixel wird berechnet, indem das nächste Pixel aus dem Quellbild entnommen wird.</span><span class="sxs-lookup"><span data-stu-id="fc178-111">Each destination pixel is computed by sampling the nearest pixel from the source image.</span></span>                                                                                                                     |
| <span data-ttu-id="fc178-112">D3DX \_ FILTER \_ LINEAR</span><span class="sxs-lookup"><span data-stu-id="fc178-112">D3DX\_FILTER\_LINEAR</span></span>    | <span data-ttu-id="fc178-113">Jedes Zielpixel wird berechnet, indem die vier nächsten Pixel aus dem Quellbild entnommen werden.</span><span class="sxs-lookup"><span data-stu-id="fc178-113">Each destination pixel is computed by sampling the four nearest pixels from the source image.</span></span> <span data-ttu-id="fc178-114">Dieser Filter funktioniert am besten, wenn die Skala auf beiden Achsen kleiner als zwei ist.</span><span class="sxs-lookup"><span data-stu-id="fc178-114">This filter works best when the scale on both axes is less than two.</span></span>                                          |
| <span data-ttu-id="fc178-115">\_D3DX-FILTERDREIECK \_</span><span class="sxs-lookup"><span data-stu-id="fc178-115">D3DX\_FILTER\_TRIANGLE</span></span>  | <span data-ttu-id="fc178-116">Jedes Pixel im Quellbild trägt gleichermaßen zum Zielbild bei.</span><span class="sxs-lookup"><span data-stu-id="fc178-116">Every pixel in the source image contributes equally to the destination image.</span></span> <span data-ttu-id="fc178-117">Dies ist der langsamste Filter.</span><span class="sxs-lookup"><span data-stu-id="fc178-117">This is the slowest of the filters.</span></span>                                                                                           |
| <span data-ttu-id="fc178-118">\_D3DX-FILTERFELD \_</span><span class="sxs-lookup"><span data-stu-id="fc178-118">D3DX\_FILTER\_BOX</span></span>       | <span data-ttu-id="fc178-119">Jedes Pixel wird berechnet, indem der Mittelwert eines 2x2(x2)-Felds von Pixeln aus dem Quellbild berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="fc178-119">Each pixel is computed by averaging a 2x2(x2) box of pixels from the source image.</span></span> <span data-ttu-id="fc178-120">Dieser Filter funktioniert nur, wenn die Abmessungen des Ziels halb so sind wie bei Mipmaps.</span><span class="sxs-lookup"><span data-stu-id="fc178-120">This filter works only when the dimensions of the destination are half those of the source, as is the case with mipmaps.</span></span> |
| <span data-ttu-id="fc178-121">\_D3DX-FILTERSPIEGELUNG \_ \_ U</span><span class="sxs-lookup"><span data-stu-id="fc178-121">D3DX\_FILTER\_MIRROR\_U</span></span> | <span data-ttu-id="fc178-122">Pixel vom Rand der Textur auf der U-Achse sollten gespiegelt und nicht umschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="fc178-122">Pixels off the edge of the texture on the u-axis should be mirrored, not wrapped.</span></span>                                                                                                                           |
| <span data-ttu-id="fc178-123">\_D3DX-FILTERSPIEGELUNG \_ \_ V</span><span class="sxs-lookup"><span data-stu-id="fc178-123">D3DX\_FILTER\_MIRROR\_V</span></span> | <span data-ttu-id="fc178-124">Pixel vom Rand der Textur auf der V-Achse sollten gespiegelt und nicht umschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="fc178-124">Pixels off the edge of the texture on the v-axis should be mirrored, not wrapped.</span></span>                                                                                                                           |
| <span data-ttu-id="fc178-125">\_D3DX-FILTERSPIEGELUNG \_ \_ W</span><span class="sxs-lookup"><span data-stu-id="fc178-125">D3DX\_FILTER\_MIRROR\_W</span></span> | <span data-ttu-id="fc178-126">Pixel vom Rand der Textur auf der W-Achse sollten gespiegelt und nicht umschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="fc178-126">Pixels off the edge of the texture on the w-axis should be mirrored, not wrapped.</span></span>                                                                                                                           |
| <span data-ttu-id="fc178-127">\_D3DX-FILTERSPIEGELUNG \_</span><span class="sxs-lookup"><span data-stu-id="fc178-127">D3DX\_FILTER\_MIRROR</span></span>    | <span data-ttu-id="fc178-128">Die Angabe dieses Flags ist identisch mit der Angabe der Flags D3DX \_ FILTER \_ MIRROR \_ U, D3DX FILTER MIRROR V und \_ \_ \_ D3DX \_ FILTER MIRROR \_ \_ W.</span><span class="sxs-lookup"><span data-stu-id="fc178-128">Specifying this flag is the same as specifying the D3DX\_FILTER\_MIRROR\_U, D3DX\_FILTER\_MIRROR\_V, and D3DX\_FILTER\_MIRROR\_W flags.</span></span>                                                                     |
| <span data-ttu-id="fc178-129">D3DX \_ FILTER \_ DITHER</span><span class="sxs-lookup"><span data-stu-id="fc178-129">D3DX\_FILTER\_DITHER</span></span>    | <span data-ttu-id="fc178-130">Das resultierende Bild muss mithilfe eines 4x4-geordneten Ditheralgorithmus gedithert werden.</span><span class="sxs-lookup"><span data-stu-id="fc178-130">The resulting image must be dithered using a 4x4 ordered dither algorithm.</span></span>                                                                                                                                  |
| <span data-ttu-id="fc178-131">D3DX \_ FILTER \_ SRGB \_ IN</span><span class="sxs-lookup"><span data-stu-id="fc178-131">D3DX\_FILTER\_SRGB\_IN</span></span>  | <span data-ttu-id="fc178-132">Die Eingabedaten sind im sRGB-Farbraum (Gamma 2,2) gespeichert.</span><span class="sxs-lookup"><span data-stu-id="fc178-132">Input data is in sRGB (gamma 2.2) color space.</span></span>                                                                                                                                                              |
| <span data-ttu-id="fc178-133">D3DX \_ FILTER \_ SRGB \_ OUT</span><span class="sxs-lookup"><span data-stu-id="fc178-133">D3DX\_FILTER\_SRGB\_OUT</span></span> | <span data-ttu-id="fc178-134">Die Ausgabedaten werden im sRGB-Farbraum (Gamma 2.2) angezeigt.</span><span class="sxs-lookup"><span data-stu-id="fc178-134">The output data is in sRGB (gamma 2.2) color space.</span></span>                                                                                                                                                         |
| <span data-ttu-id="fc178-135">D3DX \_ FILTER \_ SRGB</span><span class="sxs-lookup"><span data-stu-id="fc178-135">D3DX\_FILTER\_SRGB</span></span>      | <span data-ttu-id="fc178-136">Identisch mit der Angabe von D3DX \_ FILTER \_ SRGB \_ IN \| D3DX \_ FILTER \_ SRGB \_ OUT.</span><span class="sxs-lookup"><span data-stu-id="fc178-136">Same as specifying D3DX\_FILTER\_SRGB\_IN \| D3DX\_FILTER\_SRGB\_OUT.</span></span>                                                                                                                                       |



 

<span data-ttu-id="fc178-137">Jeder gültige Filter muss genau eines der folgenden Flags enthalten: D3DX \_ FILTER \_ NONE, D3DX \_ FILTER \_ POINT, D3DX \_ FILTER \_ LINEAR, D3DX \_ FILTER TRIANGLE oder \_ D3DX \_ FILTER \_ BOX.</span><span class="sxs-lookup"><span data-stu-id="fc178-137">Each valid filter must contain exactly one of the following flags: D3DX\_FILTER\_NONE, D3DX\_FILTER\_POINT, D3DX\_FILTER\_LINEAR, D3DX\_FILTER\_TRIANGLE, or D3DX\_FILTER\_BOX.</span></span> <span data-ttu-id="fc178-138">Darüber hinaus können Sie den OR-Operator verwenden, um null oder mehr der folgenden optionalen Flags mit einem gültigen Filter anzugeben: D3DX \_ FILTER \_ MIRROR \_ U, D3DX \_ FILTER MIRROR \_ \_ V, D3DX \_ FILTER MIRROR \_ \_ W, D3DX \_ FILTER \_ MIRROR, D3DX \_ FILTER \_ DITHER, D3DX \_ FILTER \_ SRGB \_ IN, D3DX FILTER SRGB OUT oder \_ \_ \_ D3DX \_ FILTER \_ SRGB.</span><span class="sxs-lookup"><span data-stu-id="fc178-138">In addition, you can use the OR operator to specify zero or more of the following optional flags with a valid filter: D3DX\_FILTER\_MIRROR\_U, D3DX\_FILTER\_MIRROR\_V, D3DX\_FILTER\_MIRROR\_W, D3DX\_FILTER\_MIRROR, D3DX\_FILTER\_DITHER, D3DX\_FILTER\_SRGB\_IN, D3DX\_FILTER\_SRGB\_OUT or D3DX\_FILTER\_SRGB.</span></span>

<span data-ttu-id="fc178-139">Die Angabe von D3DX DEFAULT für diesen Parameter entspricht normalerweise der Angabe von \_ D3DX \_ FILTER \_ TRIANGLE \| D3DX \_ FILTER \_ DITHER.</span><span class="sxs-lookup"><span data-stu-id="fc178-139">Specifying D3DX\_DEFAULT for this parameter is usually the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span> <span data-ttu-id="fc178-140">D3DX DEFAULT kann jedoch unterschiedliche Bedeutungen haben, je \_ nachdem, welche Methode den Filter verwendet.</span><span class="sxs-lookup"><span data-stu-id="fc178-140">However, D3DX\_DEFAULT can have different meanings, depending on which method uses the filter.</span></span> <span data-ttu-id="fc178-141">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="fc178-141">For example:</span></span>

-   <span data-ttu-id="fc178-142">Bei Verwendung [**von D3DXCreateTextureFromFileEx**](d3dxcreatetexturefromfileex.md)wird D3DX \_ DEFAULT D3DX \_ FILTER TRIANGLE \_ \| D3DX \_ FILTER \_ DITHERzugestellt.</span><span class="sxs-lookup"><span data-stu-id="fc178-142">When using [**D3DXCreateTextureFromFileEx**](d3dxcreatetexturefromfileex.md), D3DX\_DEFAULT maps to D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>
-   <span data-ttu-id="fc178-143">Bei Verwendung von [**D3DXFilterTexture**](d3dxfiltertexture.md)wird D3DX \_ DEFAULT D3DX \_ FILTER BOX \_ zugeordnet, wenn die Texturgröße eine Potenz von zwei hat, und D3DX \_ FILTER BOX \_ \| D3DX \_ FILTER \_ DITHER andernfalls .</span><span class="sxs-lookup"><span data-stu-id="fc178-143">When using [**D3DXFilterTexture**](d3dxfiltertexture.md), D3DX\_DEFAULT maps to D3DX\_FILTER\_BOX if the texture size is a power of two, and D3DX\_FILTER\_BOX \| D3DX\_FILTER\_DITHER otherwise.</span></span>

<span data-ttu-id="fc178-144">Verweisen Sie auf jede Methode, um nach Informationen zur Zuordnung des D3DX \_ DEFAULT-Filters zu suchen.</span><span class="sxs-lookup"><span data-stu-id="fc178-144">Reference each method to check for information about how D3DX\_DEFAULT filter is mapped.</span></span>

## <a name="constant-information"></a><span data-ttu-id="fc178-145">Konstanteninformationen</span><span class="sxs-lookup"><span data-stu-id="fc178-145">Constant Information</span></span>



| <span data-ttu-id="fc178-146">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fc178-146">Requirement</span></span>                         | <span data-ttu-id="fc178-147">Wert</span><span class="sxs-lookup"><span data-stu-id="fc178-147">Value</span></span>           |
|--------------------------|------------|
| <span data-ttu-id="fc178-148">Header</span><span class="sxs-lookup"><span data-stu-id="fc178-148">Header</span></span>                   | <span data-ttu-id="fc178-149">d3dx9tex.h</span><span class="sxs-lookup"><span data-stu-id="fc178-149">d3dx9tex.h</span></span> |
| <span data-ttu-id="fc178-150">Mindestbetriebssystem</span><span class="sxs-lookup"><span data-stu-id="fc178-150">Minimum operating system</span></span> | <span data-ttu-id="fc178-151">Windows 98</span><span class="sxs-lookup"><span data-stu-id="fc178-151">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="fc178-152">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="fc178-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fc178-153">D3DX-Konstanten</span><span class="sxs-lookup"><span data-stu-id="fc178-153">D3DX Constants</span></span>](dx9-graphics-reference-d3dx-constants.md)
</dt> </dl>

 

 



