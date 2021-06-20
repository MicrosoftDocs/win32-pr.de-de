---
description: Eine Liste der D3DCAPS3-Treiberfunktionsflags finden Sie hier. Enthält die Definitionen, Werte und Beschreibungen mit Links zu APIs.
ms.assetid: d9cd7388-3413-472d-aacb-0b8c9c60031a
title: D3DCAPS3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b28614b2b2ea3c20f828b39f2b8926cb484a88c
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408263"
---
# <a name="d3dcaps3"></a><span data-ttu-id="3a5ac-104">D3DCAPS3</span><span class="sxs-lookup"><span data-stu-id="3a5ac-104">D3DCAPS3</span></span>

<span data-ttu-id="3a5ac-105">Treiberfunktionsflags.</span><span class="sxs-lookup"><span data-stu-id="3a5ac-105">Driver capability flags.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3a5ac-106">#Definieren</span><span class="sxs-lookup"><span data-stu-id="3a5ac-106">#define</span></span></td>
<td><span data-ttu-id="3a5ac-107">Wert</span><span class="sxs-lookup"><span data-stu-id="3a5ac-107">Value</span></span></td>
<td><span data-ttu-id="3a5ac-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3a5ac-108">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3a5ac-109">D3DCAPS3_ALPHA_FULLSCREEN_FLIP_OR_DISCARD</span><span class="sxs-lookup"><span data-stu-id="3a5ac-109">D3DCAPS3_ALPHA_FULLSCREEN_FLIP_OR_DISCARD</span></span></td>
<td><span data-ttu-id="3a5ac-110">0x00000020L</span><span class="sxs-lookup"><span data-stu-id="3a5ac-110">0x00000020L</span></span></td>
<td><span data-ttu-id="3a5ac-111">Gibt an, dass das Gerät den D3DRS_ALPHABLENDENABLE Im Vollbildmodus rendern kann, während der Flip- oder DISCARD-Swapeffekt verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3a5ac-111">Indicates that the device can respect the D3DRS_ALPHABLENDENABLE render state in full-screen mode while using the FLIP or DISCARD swap effect.</span></span> <span data-ttu-id="3a5ac-112">Dies gilt nur, wenn D3DRS_SRCBLEND oder D3DRS_DESTBLEND auf einen der folgenden Zustände festgelegt sind:</span><span class="sxs-lookup"><span data-stu-id="3a5ac-112">This only applies when the D3DRS_SRCBLEND or D3DRS_DESTBLEND states are set to one of the following:</span></span>
<ul>
<li><span data-ttu-id="3a5ac-113">D3DBLEND_DESTALPHA</span><span class="sxs-lookup"><span data-stu-id="3a5ac-113">D3DBLEND_DESTALPHA</span></span></li>
<li><span data-ttu-id="3a5ac-114">D3DBLEND_INVDESTALPHA</span><span class="sxs-lookup"><span data-stu-id="3a5ac-114">D3DBLEND_INVDESTALPHA</span></span></li>
<li><span data-ttu-id="3a5ac-115">D3DBLEND_DESTCOLOR</span><span class="sxs-lookup"><span data-stu-id="3a5ac-115">D3DBLEND_DESTCOLOR</span></span></li>
<li><span data-ttu-id="3a5ac-116">D3DBLEND_INVDESTCOLOR</span><span class="sxs-lookup"><span data-stu-id="3a5ac-116">D3DBLEND_INVDESTCOLOR</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3a5ac-117">D3DCAPS3_COPY_TO_VIDMEM</span><span class="sxs-lookup"><span data-stu-id="3a5ac-117">D3DCAPS3_COPY_TO_VIDMEM</span></span></td>
<td><span data-ttu-id="3a5ac-118">0x00000100L</span><span class="sxs-lookup"><span data-stu-id="3a5ac-118">0x00000100L</span></span></td>
<td><span data-ttu-id="3a5ac-119">Das Gerät kann eine Speicherkopie aus dem Systemspeicher in den lokalen Videospeicher beschleunigen.</span><span class="sxs-lookup"><span data-stu-id="3a5ac-119">Device can accelerate a memory copy from system memory to local video memory.</span></span> <span data-ttu-id="3a5ac-120">Diese Obergrenze garantiert, dass <a href="/windows/desktop/api"><strong>UpdateSurface-</strong></a> und <a href="/windows/desktop/api"><strong>UpdateTexture-Aufrufe</strong></a> hardwarebeschleunigt werden.</span><span class="sxs-lookup"><span data-stu-id="3a5ac-120">This cap guarantees that <a href="/windows/desktop/api"><strong>UpdateSurface</strong></a> and <a href="/windows/desktop/api"><strong>UpdateTexture</strong></a> calls will be hardware accelerated.</span></span> <span data-ttu-id="3a5ac-121">Wenn diese Obergrenze nicht vorhanden ist, werden diese Aufrufe erfolgreich, aber langsamer.</span><span class="sxs-lookup"><span data-stu-id="3a5ac-121">If this cap is absent, these calls will succeed but will be slower.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3a5ac-122">D3DCAPS3_COPY_TO_SYSTEMMEM</span><span class="sxs-lookup"><span data-stu-id="3a5ac-122">D3DCAPS3_COPY_TO_SYSTEMMEM</span></span></td>
<td><span data-ttu-id="3a5ac-123">0x00000200L</span><span class="sxs-lookup"><span data-stu-id="3a5ac-123">0x00000200L</span></span></td>
<td><span data-ttu-id="3a5ac-124">Das Gerät kann eine Speicherkopie aus dem lokalen Videospeicher in den Systemspeicher beschleunigen.</span><span class="sxs-lookup"><span data-stu-id="3a5ac-124">Device can accelerate a memory copy from local video memory to system memory.</span></span> <span data-ttu-id="3a5ac-125">Diese Obergrenze garantiert, dass <a href="/windows/desktop/api"><strong>GetRenderTargetData-Aufrufe</strong></a> hardwarebeschleunigt werden.</span><span class="sxs-lookup"><span data-stu-id="3a5ac-125">This cap guarantees that <a href="/windows/desktop/api"><strong>GetRenderTargetData</strong></a> calls will be hardware accelerated.</span></span> <span data-ttu-id="3a5ac-126">Wenn diese Obergrenze nicht vorhanden ist, ist dieser Aufruf erfolgreich, aber langsamer.</span><span class="sxs-lookup"><span data-stu-id="3a5ac-126">If this cap is absent, this call will succeed but will be slower.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3a5ac-127">D3DCAPS3_DXVAHD</span><span class="sxs-lookup"><span data-stu-id="3a5ac-127">D3DCAPS3_DXVAHD</span></span></td>
<td><span data-ttu-id="3a5ac-128">0x00000400L</span><span class="sxs-lookup"><span data-stu-id="3a5ac-128">0x00000400L</span></span></td>
<td><span data-ttu-id="3a5ac-129">Der Anzeigetreiber unterstützt dxva-HD DDI.</span><span class="sxs-lookup"><span data-stu-id="3a5ac-129">The display driver supports the DXVA-HD DDI.</span></span> <span data-ttu-id="3a5ac-130">Weitere Informationen zu DXVA-HD DDI finden Sie unter <a href="https://msdn.microsoft.com/library/dd835176.aspx">Processing High-Definition Video</a>.</span><span class="sxs-lookup"><span data-stu-id="3a5ac-130">For more information about DXVA-HD DDI, see <a href="https://msdn.microsoft.com/library/dd835176.aspx">Processing High-Definition Video</a>.</span></span><br/> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3a5ac-131">Unterschiede zwischen Direct3D 9 und Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="3a5ac-131">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="3a5ac-132">Dieses Flag ist nur in Direct3D 9Ex verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3a5ac-132">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3a5ac-133">D3DCAPS3_LINEAR_TO_SRGB_PRESENTATION</span><span class="sxs-lookup"><span data-stu-id="3a5ac-133">D3DCAPS3_LINEAR_TO_SRGB_PRESENTATION</span></span></td>
<td><span data-ttu-id="3a5ac-134">0x00000080L</span><span class="sxs-lookup"><span data-stu-id="3a5ac-134">0x00000080L</span></span></td>
<td><span data-ttu-id="3a5ac-135">Gibt an, dass das Gerät eine Gammakorrektur von einem Puffer mit Hintergrundfenster (mit linearem Inhalt) zu einem sRGB-Desktop ausführen kann.</span><span class="sxs-lookup"><span data-stu-id="3a5ac-135">Indicates that the device can perform gamma correction from a windowed back buffer (containing linear content) to an sRGB desktop.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3a5ac-136">D3DCAPS3_RESERVED</span><span class="sxs-lookup"><span data-stu-id="3a5ac-136">D3DCAPS3_RESERVED</span></span></td>
<td><span data-ttu-id="3a5ac-137">0x8000001fL</span><span class="sxs-lookup"><span data-stu-id="3a5ac-137">0x8000001fL</span></span></td>
<td><span data-ttu-id="3a5ac-138">Reserviert; nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="3a5ac-138">Reserved; not used.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="3a5ac-139">Diese Konstanten werden vom D3CAPS3-Member von [**D3DCAPS9 verwendet.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)</span><span class="sxs-lookup"><span data-stu-id="3a5ac-139">These constants are used by the D3CAPS3 member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

## <a name="constant-information"></a><span data-ttu-id="3a5ac-140">Konstante Informationen</span><span class="sxs-lookup"><span data-stu-id="3a5ac-140">Constant Information</span></span>



|  <span data-ttu-id="3a5ac-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3a5ac-141">Requirement</span></span>                        | <span data-ttu-id="3a5ac-142">Wert</span><span class="sxs-lookup"><span data-stu-id="3a5ac-142">Value</span></span>           |
|--------------------------|------------|
| <span data-ttu-id="3a5ac-143">Header</span><span class="sxs-lookup"><span data-stu-id="3a5ac-143">Header</span></span>                   | <span data-ttu-id="3a5ac-144">d3d9caps.h</span><span class="sxs-lookup"><span data-stu-id="3a5ac-144">d3d9caps.h</span></span> |
| <span data-ttu-id="3a5ac-145">Mindestbetriebssystem</span><span class="sxs-lookup"><span data-stu-id="3a5ac-145">Minimum operating system</span></span> | <span data-ttu-id="3a5ac-146">Windows 98</span><span class="sxs-lookup"><span data-stu-id="3a5ac-146">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="3a5ac-147">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3a5ac-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3a5ac-148">Direct3D-Konstanten</span><span class="sxs-lookup"><span data-stu-id="3a5ac-148">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 




