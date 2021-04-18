---
description: Treiberfunktionsflags.
ms.assetid: d9cd7388-3413-472d-aacb-0b8c9c60031a
title: D3DCAPS3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a165ff1d550612ba302c94a0b8181affe040921
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106341148"
---
# <a name="d3dcaps3"></a><span data-ttu-id="3202f-103">D3DCAPS3</span><span class="sxs-lookup"><span data-stu-id="3202f-103">D3DCAPS3</span></span>

<span data-ttu-id="3202f-104">Treiberfunktionsflags.</span><span class="sxs-lookup"><span data-stu-id="3202f-104">Driver capability flags.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3202f-105">#definieren</span><span class="sxs-lookup"><span data-stu-id="3202f-105">#define</span></span></td>
<td><span data-ttu-id="3202f-106">Wert</span><span class="sxs-lookup"><span data-stu-id="3202f-106">Value</span></span></td>
<td><span data-ttu-id="3202f-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3202f-107">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3202f-108">D3DCAPS3_ALPHA_FULLSCREEN_FLIP_OR_DISCARD</span><span class="sxs-lookup"><span data-stu-id="3202f-108">D3DCAPS3_ALPHA_FULLSCREEN_FLIP_OR_DISCARD</span></span></td>
<td><span data-ttu-id="3202f-109">0x00000020l</span><span class="sxs-lookup"><span data-stu-id="3202f-109">0x00000020L</span></span></td>
<td><span data-ttu-id="3202f-110">Gibt an, dass das Gerät den D3DRS_ALPHABLENDENABLE renderzustand im Vollbildmodus berücksichtigen kann, während er den Swap-oder Verwerfungs Effekt verwendet.</span><span class="sxs-lookup"><span data-stu-id="3202f-110">Indicates that the device can respect the D3DRS_ALPHABLENDENABLE render state in full-screen mode while using the FLIP or DISCARD swap effect.</span></span> <span data-ttu-id="3202f-111">Dies gilt nur, wenn die D3DRS_SRCBLEND oder D3DRS_DESTBLEND Zustände auf einen der folgenden Werte festgelegt sind:</span><span class="sxs-lookup"><span data-stu-id="3202f-111">This only applies when the D3DRS_SRCBLEND or D3DRS_DESTBLEND states are set to one of the following:</span></span>
<ul>
<li><span data-ttu-id="3202f-112">D3DBLEND_DESTALPHA</span><span class="sxs-lookup"><span data-stu-id="3202f-112">D3DBLEND_DESTALPHA</span></span></li>
<li><span data-ttu-id="3202f-113">D3DBLEND_INVDESTALPHA</span><span class="sxs-lookup"><span data-stu-id="3202f-113">D3DBLEND_INVDESTALPHA</span></span></li>
<li><span data-ttu-id="3202f-114">D3DBLEND_DESTCOLOR</span><span class="sxs-lookup"><span data-stu-id="3202f-114">D3DBLEND_DESTCOLOR</span></span></li>
<li><span data-ttu-id="3202f-115">D3DBLEND_INVDESTCOLOR</span><span class="sxs-lookup"><span data-stu-id="3202f-115">D3DBLEND_INVDESTCOLOR</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3202f-116">D3DCAPS3_COPY_TO_VIDMEM</span><span class="sxs-lookup"><span data-stu-id="3202f-116">D3DCAPS3_COPY_TO_VIDMEM</span></span></td>
<td><span data-ttu-id="3202f-117">0x00000100l</span><span class="sxs-lookup"><span data-stu-id="3202f-117">0x00000100L</span></span></td>
<td><span data-ttu-id="3202f-118">Das Gerät kann eine Speicher Kopie aus dem Systemspeicher in den lokalen Videospeicher beschleunigen.</span><span class="sxs-lookup"><span data-stu-id="3202f-118">Device can accelerate a memory copy from system memory to local video memory.</span></span> <span data-ttu-id="3202f-119">Dadurch wird sichergestellt, dass <a href="/windows/desktop/api"><strong>updatesurface</strong></a> -und <a href="/windows/desktop/api"><strong>UpdateTexture</strong></a> -Aufrufe Hardware beschleunigt werden.</span><span class="sxs-lookup"><span data-stu-id="3202f-119">This cap guarantees that <a href="/windows/desktop/api"><strong>UpdateSurface</strong></a> and <a href="/windows/desktop/api"><strong>UpdateTexture</strong></a> calls will be hardware accelerated.</span></span> <span data-ttu-id="3202f-120">Wenn diese Obergrenze fehlt, sind diese Aufrufe zwar erfolgreich, aber langsamer.</span><span class="sxs-lookup"><span data-stu-id="3202f-120">If this cap is absent, these calls will succeed but will be slower.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3202f-121">D3DCAPS3_COPY_TO_SYSTEMMEM</span><span class="sxs-lookup"><span data-stu-id="3202f-121">D3DCAPS3_COPY_TO_SYSTEMMEM</span></span></td>
<td><span data-ttu-id="3202f-122">0x00000200l</span><span class="sxs-lookup"><span data-stu-id="3202f-122">0x00000200L</span></span></td>
<td><span data-ttu-id="3202f-123">Das Gerät kann eine Speicher Kopie aus lokalem Videospeicher in den Systemspeicher beschleunigen.</span><span class="sxs-lookup"><span data-stu-id="3202f-123">Device can accelerate a memory copy from local video memory to system memory.</span></span> <span data-ttu-id="3202f-124">Diese Obergrenze gewährleistet, dass <a href="/windows/desktop/api"><strong>GetRenderTargetData</strong></a> -Aufrufe Hardware beschleunigt werden.</span><span class="sxs-lookup"><span data-stu-id="3202f-124">This cap guarantees that <a href="/windows/desktop/api"><strong>GetRenderTargetData</strong></a> calls will be hardware accelerated.</span></span> <span data-ttu-id="3202f-125">Wenn diese Obergrenze fehlt, wird dieser Vorgang zwar erfolgreich ausgeführt, wird jedoch langsamer.</span><span class="sxs-lookup"><span data-stu-id="3202f-125">If this cap is absent, this call will succeed but will be slower.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3202f-126">D3DCAPS3_DXVAHD</span><span class="sxs-lookup"><span data-stu-id="3202f-126">D3DCAPS3_DXVAHD</span></span></td>
<td><span data-ttu-id="3202f-127">0x00000400l</span><span class="sxs-lookup"><span data-stu-id="3202f-127">0x00000400L</span></span></td>
<td><span data-ttu-id="3202f-128">Der Anzeigetreiber unterstützt den DXVA-HD-DDI.</span><span class="sxs-lookup"><span data-stu-id="3202f-128">The display driver supports the DXVA-HD DDI.</span></span> <span data-ttu-id="3202f-129">Weitere Informationen zu DXVA-HD DDI finden Sie unter <a href="https://msdn.microsoft.com/library/dd835176.aspx">verarbeiten High-Definition Videos</a>.</span><span class="sxs-lookup"><span data-stu-id="3202f-129">For more information about DXVA-HD DDI, see <a href="https://msdn.microsoft.com/library/dd835176.aspx">Processing High-Definition Video</a>.</span></span><br/> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3202f-130">Unterschiede zwischen Direct3D 9 und Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="3202f-130">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="3202f-131">Dieses Flag ist nur in Direct3D 9Ex verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3202f-131">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3202f-132">D3DCAPS3_LINEAR_TO_SRGB_PRESENTATION</span><span class="sxs-lookup"><span data-stu-id="3202f-132">D3DCAPS3_LINEAR_TO_SRGB_PRESENTATION</span></span></td>
<td><span data-ttu-id="3202f-133">0x00000080l</span><span class="sxs-lookup"><span data-stu-id="3202f-133">0x00000080L</span></span></td>
<td><span data-ttu-id="3202f-134">Gibt an, dass das Gerät eine Gammakorrektur von einem Fenster Hintergrund Puffer (mit linearem Inhalt) zu einem sRGB-Desktop ausführen kann.</span><span class="sxs-lookup"><span data-stu-id="3202f-134">Indicates that the device can perform gamma correction from a windowed back buffer (containing linear content) to an sRGB desktop.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3202f-135">D3DCAPS3_RESERVED</span><span class="sxs-lookup"><span data-stu-id="3202f-135">D3DCAPS3_RESERVED</span></span></td>
<td><span data-ttu-id="3202f-136">0x8000001fl</span><span class="sxs-lookup"><span data-stu-id="3202f-136">0x8000001fL</span></span></td>
<td><span data-ttu-id="3202f-137">Bleiben nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="3202f-137">Reserved; not used.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="3202f-138">Diese Konstanten werden vom D3CAPS3-Member von [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)verwendet.</span><span class="sxs-lookup"><span data-stu-id="3202f-138">These constants are used by the D3CAPS3 member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

## <a name="constant-information"></a><span data-ttu-id="3202f-139">Konstante Informationen</span><span class="sxs-lookup"><span data-stu-id="3202f-139">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="3202f-140">Header</span><span class="sxs-lookup"><span data-stu-id="3202f-140">Header</span></span>                   | <span data-ttu-id="3202f-141">d3d9caps. h</span><span class="sxs-lookup"><span data-stu-id="3202f-141">d3d9caps.h</span></span> |
| <span data-ttu-id="3202f-142">Mindestens Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="3202f-142">Minimum operating system</span></span> | <span data-ttu-id="3202f-143">Windows 98</span><span class="sxs-lookup"><span data-stu-id="3202f-143">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="3202f-144">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3202f-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3202f-145">Direct3D-Konstanten</span><span class="sxs-lookup"><span data-stu-id="3202f-145">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 




