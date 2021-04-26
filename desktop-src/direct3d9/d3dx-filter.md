---
description: Die folgenden Flags werden verwendet, um anzugeben, welche Kanäle in einer Textur verwendet werden sollen.
ms.assetid: 0317b857-2512-4ad7-b6e3-82afdda7ea10
title: D3DX_FILTER
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e6e1ab3ab51a73277da685b7ac562e84d1b94a9
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997327"
---
# <a name="d3dx_filter"></a><span data-ttu-id="7dfba-103">\_D3DX-FILTER</span><span class="sxs-lookup"><span data-stu-id="7dfba-103">D3DX\_FILTER</span></span>

<span data-ttu-id="7dfba-104">Die folgenden Flags werden verwendet, um anzugeben, welche Kanäle in einer Textur verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7dfba-104">The following flags are used to specify which channels in a texture to operate on.</span></span>



| <span data-ttu-id="7dfba-105">\#Definieren</span><span class="sxs-lookup"><span data-stu-id="7dfba-105">\#define</span></span>                | <span data-ttu-id="7dfba-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7dfba-106">Description</span></span>                                                                                                                                                                                                 |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7dfba-107">D3DX \_ FILTER \_ NONE</span><span class="sxs-lookup"><span data-stu-id="7dfba-107">D3DX\_FILTER\_NONE</span></span>      | <span data-ttu-id="7dfba-108">Es erfolgt keine Skalierung oder Filterung.</span><span class="sxs-lookup"><span data-stu-id="7dfba-108">No scaling or filtering will take place.</span></span> <span data-ttu-id="7dfba-109">Pixel außerhalb der Grenzen des Quellbilds werden als transparent schwarz angenommen.</span><span class="sxs-lookup"><span data-stu-id="7dfba-109">Pixels outside the bounds of the source image are assumed to be transparent black.</span></span>                                                                                 |
| <span data-ttu-id="7dfba-110">D3DX-FILTERPUNKT \_ \_</span><span class="sxs-lookup"><span data-stu-id="7dfba-110">D3DX\_FILTER\_POINT</span></span>     | <span data-ttu-id="7dfba-111">Jedes Zielpixel wird durch Sampling des nächstgelegenen Pixels aus dem Quellbild berechnet.</span><span class="sxs-lookup"><span data-stu-id="7dfba-111">Each destination pixel is computed by sampling the nearest pixel from the source image.</span></span>                                                                                                                     |
| <span data-ttu-id="7dfba-112">D3DX-FILTER \_ \_ LINEAR</span><span class="sxs-lookup"><span data-stu-id="7dfba-112">D3DX\_FILTER\_LINEAR</span></span>    | <span data-ttu-id="7dfba-113">Jedes Zielpixel wird durch Sampling der vier nächstgelegenen Pixel aus dem Quellbild berechnet.</span><span class="sxs-lookup"><span data-stu-id="7dfba-113">Each destination pixel is computed by sampling the four nearest pixels from the source image.</span></span> <span data-ttu-id="7dfba-114">Dieser Filter funktioniert am besten, wenn die Skalierung auf beiden Achsen kleiner als zwei ist.</span><span class="sxs-lookup"><span data-stu-id="7dfba-114">This filter works best when the scale on both axes is less than two.</span></span>                                          |
| <span data-ttu-id="7dfba-115">\_D3DX-FILTERDREIECK \_</span><span class="sxs-lookup"><span data-stu-id="7dfba-115">D3DX\_FILTER\_TRIANGLE</span></span>  | <span data-ttu-id="7dfba-116">Jedes Pixel im Quellbild trägt gleichermaßen zum Zielbild bei.</span><span class="sxs-lookup"><span data-stu-id="7dfba-116">Every pixel in the source image contributes equally to the destination image.</span></span> <span data-ttu-id="7dfba-117">Dies ist die langsamste der Filter.</span><span class="sxs-lookup"><span data-stu-id="7dfba-117">This is the slowest of the filters.</span></span>                                                                                           |
| <span data-ttu-id="7dfba-118">D3DX-FILTERFELD \_ \_</span><span class="sxs-lookup"><span data-stu-id="7dfba-118">D3DX\_FILTER\_BOX</span></span>       | <span data-ttu-id="7dfba-119">Jedes Pixel wird berechnet, indem ein 2x2(x2)-Feld aus Pixeln aus dem Quellbild durchschnittlich berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="7dfba-119">Each pixel is computed by averaging a 2x2(x2) box of pixels from the source image.</span></span> <span data-ttu-id="7dfba-120">Dieser Filter funktioniert nur, wenn die Dimensionen des Ziels die Hälfte der Quelldimensionen sind, wie dies bei Mipmaps der Fall ist.</span><span class="sxs-lookup"><span data-stu-id="7dfba-120">This filter works only when the dimensions of the destination are half those of the source, as is the case with mipmaps.</span></span> |
| <span data-ttu-id="7dfba-121">D3DX-FILTERSPIEGELUNG \_ \_ \_ U</span><span class="sxs-lookup"><span data-stu-id="7dfba-121">D3DX\_FILTER\_MIRROR\_U</span></span> | <span data-ttu-id="7dfba-122">Pixel am Rand der Textur auf der U-Achse sollten gespiegelt und nicht umschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="7dfba-122">Pixels off the edge of the texture on the u-axis should be mirrored, not wrapped.</span></span>                                                                                                                           |
| <span data-ttu-id="7dfba-123">\_D3DX-FILTERSPIEGELUNG \_ \_ V</span><span class="sxs-lookup"><span data-stu-id="7dfba-123">D3DX\_FILTER\_MIRROR\_V</span></span> | <span data-ttu-id="7dfba-124">Pixel am Rand der Textur auf der V-Achse sollten gespiegelt und nicht umschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="7dfba-124">Pixels off the edge of the texture on the v-axis should be mirrored, not wrapped.</span></span>                                                                                                                           |
| <span data-ttu-id="7dfba-125">\_D3DX-FILTERSPIEGELUNG \_ \_ W</span><span class="sxs-lookup"><span data-stu-id="7dfba-125">D3DX\_FILTER\_MIRROR\_W</span></span> | <span data-ttu-id="7dfba-126">Pixel am Rand der Textur auf der W-Achse sollten gespiegelt und nicht umschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="7dfba-126">Pixels off the edge of the texture on the w-axis should be mirrored, not wrapped.</span></span>                                                                                                                           |
| <span data-ttu-id="7dfba-127">\_D3DX-FILTERSPIEGELUNG \_</span><span class="sxs-lookup"><span data-stu-id="7dfba-127">D3DX\_FILTER\_MIRROR</span></span>    | <span data-ttu-id="7dfba-128">Die Angabe dieses Flags entspricht der Angabe der W-Flags D3DX \_ FILTER \_ MIRROR \_ U, D3DX FILTER MIRROR V und \_ \_ \_ D3DX \_ FILTER \_ \_ MIRROR.</span><span class="sxs-lookup"><span data-stu-id="7dfba-128">Specifying this flag is the same as specifying the D3DX\_FILTER\_MIRROR\_U, D3DX\_FILTER\_MIRROR\_V, and D3DX\_FILTER\_MIRROR\_W flags.</span></span>                                                                     |
| <span data-ttu-id="7dfba-129">D3DX \_ FILTER \_ DITHER</span><span class="sxs-lookup"><span data-stu-id="7dfba-129">D3DX\_FILTER\_DITHER</span></span>    | <span data-ttu-id="7dfba-130">Das resultierende Bild muss mithilfe eines 4x4-geordneten Ditheralgorithmus geblendet werden.</span><span class="sxs-lookup"><span data-stu-id="7dfba-130">The resulting image must be dithered using a 4x4 ordered dither algorithm.</span></span>                                                                                                                                  |
| <span data-ttu-id="7dfba-131">D3DX \_ FILTER \_ SRGB \_ IN</span><span class="sxs-lookup"><span data-stu-id="7dfba-131">D3DX\_FILTER\_SRGB\_IN</span></span>  | <span data-ttu-id="7dfba-132">Die Eingabedaten sind im Farbraum sRGB (gamma 2.2) enthalten.</span><span class="sxs-lookup"><span data-stu-id="7dfba-132">Input data is in sRGB (gamma 2.2) color space.</span></span>                                                                                                                                                              |
| <span data-ttu-id="7dfba-133">D3DX \_ FILTER \_ SRGB \_ OUT</span><span class="sxs-lookup"><span data-stu-id="7dfba-133">D3DX\_FILTER\_SRGB\_OUT</span></span> | <span data-ttu-id="7dfba-134">Die Ausgabedaten sind im Farbraum sRGB (Gamma 2,2) enthalten.</span><span class="sxs-lookup"><span data-stu-id="7dfba-134">The output data is in sRGB (gamma 2.2) color space.</span></span>                                                                                                                                                         |
| <span data-ttu-id="7dfba-135">D3DX \_ FILTER \_ SRGB</span><span class="sxs-lookup"><span data-stu-id="7dfba-135">D3DX\_FILTER\_SRGB</span></span>      | <span data-ttu-id="7dfba-136">Entspricht der Angabe von D3DX \_ FILTER \_ SRGB \_ IN \| D3DX \_ FILTER \_ SRGB \_ OUT.</span><span class="sxs-lookup"><span data-stu-id="7dfba-136">Same as specifying D3DX\_FILTER\_SRGB\_IN \| D3DX\_FILTER\_SRGB\_OUT.</span></span>                                                                                                                                       |



 

<span data-ttu-id="7dfba-137">Jeder gültige Filter muss genau eines der folgenden Flags enthalten: D3DX \_ FILTER \_ NONE, D3DX \_ FILTER \_ POINT, D3DX \_ FILTER \_ LINEAR, D3DX \_ FILTER TRIANGLE oder \_ D3DX \_ FILTER \_ BOX.</span><span class="sxs-lookup"><span data-stu-id="7dfba-137">Each valid filter must contain exactly one of the following flags: D3DX\_FILTER\_NONE, D3DX\_FILTER\_POINT, D3DX\_FILTER\_LINEAR, D3DX\_FILTER\_TRIANGLE, or D3DX\_FILTER\_BOX.</span></span> <span data-ttu-id="7dfba-138">Darüber hinaus können Sie den OR-Operator verwenden, um null oder mehr der folgenden optionalen Flags mit einem gültigen Filter anzugeben: D3DX \_ FILTER \_ MIRROR \_ U, D3DX \_ FILTER MIRROR \_ \_ V, D3DX \_ FILTER MIRROR \_ \_ W, D3DX \_ FILTER \_ MIRROR, D3DX \_ FILTER \_ DITHER, D3DX \_ FILTER \_ SRGB \_ IN, D3DX \_ FILTER \_ SRGB OUT oder \_ D3DX \_ FILTER \_ SRGB.</span><span class="sxs-lookup"><span data-stu-id="7dfba-138">In addition, you can use the OR operator to specify zero or more of the following optional flags with a valid filter: D3DX\_FILTER\_MIRROR\_U, D3DX\_FILTER\_MIRROR\_V, D3DX\_FILTER\_MIRROR\_W, D3DX\_FILTER\_MIRROR, D3DX\_FILTER\_DITHER, D3DX\_FILTER\_SRGB\_IN, D3DX\_FILTER\_SRGB\_OUT or D3DX\_FILTER\_SRGB.</span></span>

<span data-ttu-id="7dfba-139">Die Angabe von D3DX \_ DEFAULT für diesen Parameter entspricht in der Regel der Angabe von D3DX FILTER TRIANGLE \_ \_ \| D3DX \_ FILTER \_ DITHER.</span><span class="sxs-lookup"><span data-stu-id="7dfba-139">Specifying D3DX\_DEFAULT for this parameter is usually the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span> <span data-ttu-id="7dfba-140">D3DX DEFAULT kann jedoch \_ unterschiedliche Bedeutungen haben, je nachdem, welche Methode den Filter verwendet.</span><span class="sxs-lookup"><span data-stu-id="7dfba-140">However, D3DX\_DEFAULT can have different meanings, depending on which method uses the filter.</span></span> <span data-ttu-id="7dfba-141">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="7dfba-141">For example:</span></span>

-   <span data-ttu-id="7dfba-142">Bei Verwendung von [**D3DXCreateTextureFromFileEx**](d3dxcreatetexturefromfileex.md)wird D3DX \_ DEFAULT D3DX \_ FILTER TRIANGLE \_ \| D3DX \_ FILTER \_ DITHER zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="7dfba-142">When using [**D3DXCreateTextureFromFileEx**](d3dxcreatetexturefromfileex.md), D3DX\_DEFAULT maps to D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>
-   <span data-ttu-id="7dfba-143">Bei Verwendung von [**D3DXFilterTexture**](d3dxfiltertexture.md)wird D3DX DEFAULT D3DX FILTER BOX zugestellt, wenn die Texturgröße eine Zweierleistung hat, andernfalls \_ \_ \_ D3DX \_ FILTER BOX \_ \| D3DX \_ FILTER \_ DITHER.</span><span class="sxs-lookup"><span data-stu-id="7dfba-143">When using [**D3DXFilterTexture**](d3dxfiltertexture.md), D3DX\_DEFAULT maps to D3DX\_FILTER\_BOX if the texture size is a power of two, and D3DX\_FILTER\_BOX \| D3DX\_FILTER\_DITHER otherwise.</span></span>

<span data-ttu-id="7dfba-144">Verweisen Sie auf jede Methode, um nach Informationen zur Zuordnung des D3DX \_ DEFAULT-Filters zu prüfen.</span><span class="sxs-lookup"><span data-stu-id="7dfba-144">Reference each method to check for information about how D3DX\_DEFAULT filter is mapped.</span></span>

## <a name="constant-information"></a><span data-ttu-id="7dfba-145">Konstante Informationen</span><span class="sxs-lookup"><span data-stu-id="7dfba-145">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="7dfba-146">Header</span><span class="sxs-lookup"><span data-stu-id="7dfba-146">Header</span></span>                   | <span data-ttu-id="7dfba-147">d3dx9tex.h</span><span class="sxs-lookup"><span data-stu-id="7dfba-147">d3dx9tex.h</span></span> |
| <span data-ttu-id="7dfba-148">Mindestbetriebssystem</span><span class="sxs-lookup"><span data-stu-id="7dfba-148">Minimum operating system</span></span> | <span data-ttu-id="7dfba-149">Windows 98</span><span class="sxs-lookup"><span data-stu-id="7dfba-149">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="7dfba-150">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7dfba-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7dfba-151">D3DX-Konstanten</span><span class="sxs-lookup"><span data-stu-id="7dfba-151">D3DX Constants</span></span>](dx9-graphics-reference-d3dx-constants.md)
</dt> </dl>

 

 



