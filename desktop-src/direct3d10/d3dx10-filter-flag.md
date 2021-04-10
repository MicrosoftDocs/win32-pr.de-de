---
description: Textur Filterflags.
ms.assetid: bc73d916-fe18-4b15-b507-7954e157ab9a
title: D3DX10_FILTER_FLAG-Enumeration (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_FILTER_FLAG
api_type:
- HeaderDef
api_location:
- D3DX10Tex.h
ms.openlocfilehash: f12842cd07c55c33509ecfbb56fc804a6fc3b7c0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961728"
---
# <a name="d3dx10_filter_flag-enumeration"></a><span data-ttu-id="5938e-103">D3dx10 \_ - \_ filterflag-Enumeration</span><span class="sxs-lookup"><span data-stu-id="5938e-103">D3DX10\_FILTER\_FLAG enumeration</span></span>

<span data-ttu-id="5938e-104">Textur Filterflags.</span><span class="sxs-lookup"><span data-stu-id="5938e-104">Texture filtering flags.</span></span>

## <a name="syntax"></a><span data-ttu-id="5938e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5938e-105">Syntax</span></span>


```C++
typedef enum D3DX10_FILTER_FLAG { 
  D3DX10_FILTER_NONE              = (1 << 0),
  D3DX10_FILTER_POINT             = (2 << 0),
  D3DX10_FILTER_LINEAR            = (3 << 0),
  D3DX10_FILTER_TRIANGLE          = (4 << 0),
  D3DX10_FILTER_BOX               = (5 << 0),
  D3DX10_FILTER_MIRROR_U          = (1 << 16),
  D3DX10_FILTER_MIRROR_V          = (2 << 16),
  D3DX10_FILTER_MIRROR_W          = (4 << 16),
  D3DX10_FILTER_MIRROR            = (7 << 16),
  D3DX10_FILTER_DITHER            = (1 << 19),
  D3DX10_FILTER_DITHER_DIFFUSION  = (2 << 19),
  D3DX10_FILTER_SRGB_IN           = (1 << 21),
  D3DX10_FILTER_SRGB_OUT          = (2 << 21),
  D3DX10_FILTER_SRGB              = (3 << 21)
} D3DX10_FILTER_FLAG, *LPD3DX10_FILTER_FLAG;
```



## <a name="constants"></a><span data-ttu-id="5938e-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="5938e-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="5938e-107"><span id="D3DX10_FILTER_NONE"></span><span id="d3dx10_filter_none"></span>**D3dx10 \_ Filter \_ None**</span><span class="sxs-lookup"><span data-stu-id="5938e-107"><span id="D3DX10_FILTER_NONE"></span><span id="d3dx10_filter_none"></span>**D3DX10\_FILTER\_NONE**</span></span>
</dt> <dd>

<span data-ttu-id="5938e-108">Es findet keine Skalierung oder Filterung statt.</span><span class="sxs-lookup"><span data-stu-id="5938e-108">No scaling or filtering will take place.</span></span> <span data-ttu-id="5938e-109">Es wird davon ausgegangen, dass Pixel außerhalb der Begrenzungen des Quell Bilds transparent schwarz sind.</span><span class="sxs-lookup"><span data-stu-id="5938e-109">Pixels outside the bounds of the source image are assumed to be transparent black.</span></span>

</dd> <dt>

<span data-ttu-id="5938e-110"><span id="D3DX10_FILTER_POINT"></span><span id="d3dx10_filter_point"></span>**D3dx10- \_ Filter \_ Punkt**</span><span class="sxs-lookup"><span data-stu-id="5938e-110"><span id="D3DX10_FILTER_POINT"></span><span id="d3dx10_filter_point"></span>**D3DX10\_FILTER\_POINT**</span></span>
</dt> <dd>

<span data-ttu-id="5938e-111">Jedes Zielpixel wird berechnet, indem das nächste Pixel aus dem Quell Image entnommen wird.</span><span class="sxs-lookup"><span data-stu-id="5938e-111">Each destination pixel is computed by sampling the nearest pixel from the source image.</span></span>

</dd> <dt>

<span data-ttu-id="5938e-112"><span id="D3DX10_FILTER_LINEAR"></span><span id="d3dx10_filter_linear"></span>**D3dx10- \_ Filter \_ linear**</span><span class="sxs-lookup"><span data-stu-id="5938e-112"><span id="D3DX10_FILTER_LINEAR"></span><span id="d3dx10_filter_linear"></span>**D3DX10\_FILTER\_LINEAR**</span></span>
</dt> <dd>

<span data-ttu-id="5938e-113">Jedes Zielpixel wird berechnet, indem die vier nächsten Pixel aus dem Quell Image entnommen werden.</span><span class="sxs-lookup"><span data-stu-id="5938e-113">Each destination pixel is computed by sampling the four nearest pixels from the source image.</span></span> <span data-ttu-id="5938e-114">Dieser Filter funktioniert am besten, wenn die Skala auf beiden Achsen kleiner als zwei ist.</span><span class="sxs-lookup"><span data-stu-id="5938e-114">This filter works best when the scale on both axes is less than two.</span></span>

</dd> <dt>

<span data-ttu-id="5938e-115"><span id="D3DX10_FILTER_TRIANGLE"></span><span id="d3dx10_filter_triangle"></span>**D3dx10 \_ Filter \_ Dreieck**</span><span class="sxs-lookup"><span data-stu-id="5938e-115"><span id="D3DX10_FILTER_TRIANGLE"></span><span id="d3dx10_filter_triangle"></span>**D3DX10\_FILTER\_TRIANGLE**</span></span>
</dt> <dd>

<span data-ttu-id="5938e-116">Jedes Pixel im Quell Image trägt gleichermaßen dem Ziel Image bei.</span><span class="sxs-lookup"><span data-stu-id="5938e-116">Every pixel in the source image contributes equally to the destination image.</span></span> <span data-ttu-id="5938e-117">Dies ist der langsamste der Filter.</span><span class="sxs-lookup"><span data-stu-id="5938e-117">This is the slowest of the filters.</span></span>

</dd> <dt>

<span data-ttu-id="5938e-118"><span id="D3DX10_FILTER_BOX"></span><span id="d3dx10_filter_box"></span>**D3dx10 \_ Filter \_ Feld**</span><span class="sxs-lookup"><span data-stu-id="5938e-118"><span id="D3DX10_FILTER_BOX"></span><span id="d3dx10_filter_box"></span>**D3DX10\_FILTER\_BOX**</span></span>
</dt> <dd>

<span data-ttu-id="5938e-119">Jedes Pixel wird berechnet, indem das Feld 2 x 2 (x2) aus dem Quell Abbild durchläuft.</span><span class="sxs-lookup"><span data-stu-id="5938e-119">Each pixel is computed by averaging a 2x2(x2) box of pixels from the source image.</span></span> <span data-ttu-id="5938e-120">Dieser Filter kann nur verwendet werden, wenn die Abmessungen des Ziels die Hälfte der der Quelle sind, wie es bei MipMaps der Fall ist.</span><span class="sxs-lookup"><span data-stu-id="5938e-120">This filter works only when the dimensions of the destination are half those of the source, as is the case with mipmaps.</span></span>

</dd> <dt>

<span data-ttu-id="5938e-121"><span id="D3DX10_FILTER_MIRROR_U"></span><span id="d3dx10_filter_mirror_u"></span>**D3dx10 \_ Filter \_ Spiegelung \_ U**</span><span class="sxs-lookup"><span data-stu-id="5938e-121"><span id="D3DX10_FILTER_MIRROR_U"></span><span id="d3dx10_filter_mirror_u"></span>**D3DX10\_FILTER\_MIRROR\_U**</span></span>
</dt> <dd>

<span data-ttu-id="5938e-122">Pixel am Rand der Textur auf der u-Achse sollten gespiegelt, nicht umschließt werden.</span><span class="sxs-lookup"><span data-stu-id="5938e-122">Pixels off the edge of the texture on the u-axis should be mirrored, not wrapped.</span></span>

</dd> <dt>

<span data-ttu-id="5938e-123"><span id="D3DX10_FILTER_MIRROR_V"></span><span id="d3dx10_filter_mirror_v"></span>**D3dx10 \_ Filter \_ Spiegelung \_ V**</span><span class="sxs-lookup"><span data-stu-id="5938e-123"><span id="D3DX10_FILTER_MIRROR_V"></span><span id="d3dx10_filter_mirror_v"></span>**D3DX10\_FILTER\_MIRROR\_V**</span></span>
</dt> <dd>

<span data-ttu-id="5938e-124">Pixel am Rand der Textur auf der v-Achse sollten gespiegelt und nicht umschließt werden.</span><span class="sxs-lookup"><span data-stu-id="5938e-124">Pixels off the edge of the texture on the v-axis should be mirrored, not wrapped.</span></span>

</dd> <dt>

<span data-ttu-id="5938e-125"><span id="D3DX10_FILTER_MIRROR_W"></span><span id="d3dx10_filter_mirror_w"></span>**D3dx10 \_ Filter \_ Spiegelung \_**</span><span class="sxs-lookup"><span data-stu-id="5938e-125"><span id="D3DX10_FILTER_MIRROR_W"></span><span id="d3dx10_filter_mirror_w"></span>**D3DX10\_FILTER\_MIRROR\_W**</span></span>
</dt> <dd>

<span data-ttu-id="5938e-126">Pixel am Rand der Textur auf der w-Achse sollten gespiegelt, nicht umschließt werden.</span><span class="sxs-lookup"><span data-stu-id="5938e-126">Pixels off the edge of the texture on the w-axis should be mirrored, not wrapped.</span></span>

</dd> <dt>

<span data-ttu-id="5938e-127"><span id="D3DX10_FILTER_MIRROR"></span><span id="d3dx10_filter_mirror"></span>**D3dx10- \_ Filter \_ Spiegelung**</span><span class="sxs-lookup"><span data-stu-id="5938e-127"><span id="D3DX10_FILTER_MIRROR"></span><span id="d3dx10_filter_mirror"></span>**D3DX10\_FILTER\_MIRROR**</span></span>
</dt> <dd>

<span data-ttu-id="5938e-128">Die Angabe dieses Flags ist identisch mit dem Angeben der D3DX \_ Filter \_ Mirror \_ U, D3DX \_ Filter \_ Spiegel \_ V und D3DX \_ Filter \_ Mirror \_ W-Flags.</span><span class="sxs-lookup"><span data-stu-id="5938e-128">Specifying this flag is the same as specifying the D3DX\_FILTER\_MIRROR\_U, D3DX\_FILTER\_MIRROR\_V, and D3DX\_FILTER\_MIRROR\_W flags.</span></span>

</dd> <dt>

<span data-ttu-id="5938e-129"><span id="D3DX10_FILTER_DITHER"></span><span id="d3dx10_filter_dither"></span>**D3dx10 \_ Filter \_ Dither**</span><span class="sxs-lookup"><span data-stu-id="5938e-129"><span id="D3DX10_FILTER_DITHER"></span><span id="d3dx10_filter_dither"></span>**D3DX10\_FILTER\_DITHER**</span></span>
</dt> <dd>

<span data-ttu-id="5938e-130">Das resultierende Bild muss mit einem 4 x 4-geordneten Dithering-Algorithmus ausgeblendet werden.</span><span class="sxs-lookup"><span data-stu-id="5938e-130">The resulting image must be dithered using a 4x4 ordered dither algorithm.</span></span> <span data-ttu-id="5938e-131">Dies geschieht bei der Umstellung von einem Format in ein anderes.</span><span class="sxs-lookup"><span data-stu-id="5938e-131">This happens when converting from one format to another.</span></span>

</dd> <dt>

<span data-ttu-id="5938e-132"><span id="D3DX10_FILTER_DITHER_DIFFUSION"></span><span id="d3dx10_filter_dither_diffusion"></span>**D3dx10 \_ Filter \_ Dither- \_ Verbreitung**</span><span class="sxs-lookup"><span data-stu-id="5938e-132"><span id="D3DX10_FILTER_DITHER_DIFFUSION"></span><span id="d3dx10_filter_dither_diffusion"></span>**D3DX10\_FILTER\_DITHER\_DIFFUSION**</span></span>
</dt> <dd>

<span data-ttu-id="5938e-133">Verwenden Sie beim Wechsel von einem Format in ein anderes diffuses Dithering für das Bild.</span><span class="sxs-lookup"><span data-stu-id="5938e-133">Do diffuse dithering on the image when changing from one format to another.</span></span>

</dd> <dt>

<span data-ttu-id="5938e-134"><span id="D3DX10_FILTER_SRGB_IN"></span><span id="d3dx10_filter_srgb_in"></span>**D3dx10 \_ \_ sRGB Filtern \_ in**</span><span class="sxs-lookup"><span data-stu-id="5938e-134"><span id="D3DX10_FILTER_SRGB_IN"></span><span id="d3dx10_filter_srgb_in"></span>**D3DX10\_FILTER\_SRGB\_IN**</span></span>
</dt> <dd>

<span data-ttu-id="5938e-135">Eingabedaten befinden sich im Standard-RGB-Farbraum (sRGB).</span><span class="sxs-lookup"><span data-stu-id="5938e-135">Input data is in standard RGB (sRGB) color space.</span></span> <span data-ttu-id="5938e-136">Siehe Bemerkungen.</span><span class="sxs-lookup"><span data-stu-id="5938e-136">See remarks.</span></span>

</dd> <dt>

<span data-ttu-id="5938e-137"><span id="D3DX10_FILTER_SRGB_OUT"></span><span id="d3dx10_filter_srgb_out"></span>**D3dx10 \_ filtert \_ sRGB \_ out**</span><span class="sxs-lookup"><span data-stu-id="5938e-137"><span id="D3DX10_FILTER_SRGB_OUT"></span><span id="d3dx10_filter_srgb_out"></span>**D3DX10\_FILTER\_SRGB\_OUT**</span></span>
</dt> <dd>

<span data-ttu-id="5938e-138">Ausgabedaten befinden sich im Standard-RGB-Farbraum (sRGB).</span><span class="sxs-lookup"><span data-stu-id="5938e-138">Output data is in standard RGB (sRGB) color space.</span></span> <span data-ttu-id="5938e-139">Siehe Bemerkungen.</span><span class="sxs-lookup"><span data-stu-id="5938e-139">See remarks.</span></span>

</dd> <dt>

<span data-ttu-id="5938e-140"><span id="D3DX10_FILTER_SRGB"></span><span id="d3dx10_filter_srgb"></span>**D3dx10 \_ \_ sRGB Filtern**</span><span class="sxs-lookup"><span data-stu-id="5938e-140"><span id="D3DX10_FILTER_SRGB"></span><span id="d3dx10_filter_srgb"></span>**D3DX10\_FILTER\_SRGB**</span></span>
</dt> <dd>

<span data-ttu-id="5938e-141">Identisch \_ \_ mit der Angabe von D3DX Filter sRGB \_ in \| D3DX \_ Filter \_ sRGB \_ out.</span><span class="sxs-lookup"><span data-stu-id="5938e-141">Same as specifying D3DX\_FILTER\_SRGB\_IN \| D3DX\_FILTER\_SRGB\_OUT.</span></span> <span data-ttu-id="5938e-142">Siehe Bemerkungen.</span><span class="sxs-lookup"><span data-stu-id="5938e-142">See remarks.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5938e-143">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5938e-143">Remarks</span></span>

<span data-ttu-id="5938e-144">D3dx10 führt beim Laden von Textur Daten automatisch eine Gammakorrektur durch (zum Konvertieren von Farbdaten aus RGB-Raum in Standard-RGB-Speicherplatz).</span><span class="sxs-lookup"><span data-stu-id="5938e-144">D3DX10 automatically performs gamma correction (to convert color data from RGB space to standard RGB space) when loading texture data.</span></span> <span data-ttu-id="5938e-145">Dies erfolgt automatisch, wenn RGB-Daten aus einer PNG-Datei in eine sRGB-Textur geladen werden.</span><span class="sxs-lookup"><span data-stu-id="5938e-145">This is automatically done for instance when RGB data is loaded from a .png file into an sRGB texture.</span></span> <span data-ttu-id="5938e-146">Verwenden Sie die sRGB-Filterflags, um anzugeben, ob die Daten nicht in den sRGB-Speicher konvertiert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="5938e-146">Use the SRGB filter flags to indicate if the data does not need to be converted into sRGB space.</span></span>

## <a name="requirements"></a><span data-ttu-id="5938e-147">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5938e-147">Requirements</span></span>



| <span data-ttu-id="5938e-148">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5938e-148">Requirement</span></span> | <span data-ttu-id="5938e-149">Wert</span><span class="sxs-lookup"><span data-stu-id="5938e-149">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5938e-150">Header</span><span class="sxs-lookup"><span data-stu-id="5938e-150">Header</span></span><br/> | <dl> <span data-ttu-id="5938e-151"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="5938e-151"><dt>D3DX10Tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5938e-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5938e-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5938e-153">D3DX-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="5938e-153">D3DX Enumerations</span></span>](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




