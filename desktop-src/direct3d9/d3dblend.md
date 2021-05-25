---
description: Definiert den unterstützten Überblendmodus.
ms.assetid: 60ff384c-15a0-4c6f-9e2c-59fdea76b7a1
title: D3DBLEND-Enumeration (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DBLEND
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 55edb432913720f58860d4f5cb87d8da9b9a8681
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343385"
---
# <a name="d3dblend-enumeration"></a><span data-ttu-id="6bc71-103">D3DBLEND-Enumeration</span><span class="sxs-lookup"><span data-stu-id="6bc71-103">D3DBLEND enumeration</span></span>

<span data-ttu-id="6bc71-104">Definiert den unterstützten Überblendmodus.</span><span class="sxs-lookup"><span data-stu-id="6bc71-104">Defines the supported blend mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="6bc71-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6bc71-105">Syntax</span></span>


```C++
typedef enum D3DBLEND { 
  D3DBLEND_ZERO             = 1,
  D3DBLEND_ONE              = 2,
  D3DBLEND_SRCCOLOR         = 3,
  D3DBLEND_INVSRCCOLOR      = 4,
  D3DBLEND_SRCALPHA         = 5,
  D3DBLEND_INVSRCALPHA      = 6,
  D3DBLEND_DESTALPHA        = 7,
  D3DBLEND_INVDESTALPHA     = 8,
  D3DBLEND_DESTCOLOR        = 9,
  D3DBLEND_INVDESTCOLOR     = 10,
  D3DBLEND_SRCALPHASAT      = 11,
  D3DBLEND_BOTHSRCALPHA     = 12,
  D3DBLEND_BOTHINVSRCALPHA  = 13,
  D3DBLEND_BLENDFACTOR      = 14,
  D3DBLEND_INVBLENDFACTOR   = 15,
  D3DBLEND_SRCCOLOR2        = 16,
  D3DBLEND_INVSRCCOLOR2     = 17,
  D3DBLEND_FORCE_DWORD      = 0x7fffffff
} D3DBLEND, *LPD3DBLEND;
```



## <a name="constants"></a><span data-ttu-id="6bc71-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="6bc71-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="6bc71-107"><span id="D3DBLEND_ZERO"></span><span id="d3dblend_zero"></span>**D3DBLEND \_ ZERO**</span><span class="sxs-lookup"><span data-stu-id="6bc71-107"><span id="D3DBLEND_ZERO"></span><span id="d3dblend_zero"></span>**D3DBLEND\_ZERO**</span></span>
</dt> <dd>

<span data-ttu-id="6bc71-108">Der Überblendfaktor ist (0, 0, 0, 0).</span><span class="sxs-lookup"><span data-stu-id="6bc71-108">Blend factor is (0, 0, 0, 0).</span></span>

</dd> <dt>

<span data-ttu-id="6bc71-109"><span id="D3DBLEND_ONE"></span><span id="d3dblend_one"></span>**D3DBLEND \_ ONE**</span><span class="sxs-lookup"><span data-stu-id="6bc71-109"><span id="D3DBLEND_ONE"></span><span id="d3dblend_one"></span>**D3DBLEND\_ONE**</span></span>
</dt> <dd>

<span data-ttu-id="6bc71-110">Der Überblendfaktor ist (1, 1, 1, 1).</span><span class="sxs-lookup"><span data-stu-id="6bc71-110">Blend factor is (1, 1, 1, 1).</span></span>

</dd> <dt>

<span data-ttu-id="6bc71-111"><span id="D3DBLEND_SRCCOLOR"></span><span id="d3dblend_srccolor"></span>**D3DBLEND \_ SRCCOLOR**</span><span class="sxs-lookup"><span data-stu-id="6bc71-111"><span id="D3DBLEND_SRCCOLOR"></span><span id="d3dblend_srccolor"></span>**D3DBLEND\_SRCCOLOR**</span></span>
</dt> <dd>

<span data-ttu-id="6bc71-112">Der Überblendfaktor ist (Rs, Gs, Bs, As).</span><span class="sxs-lookup"><span data-stu-id="6bc71-112">Blend factor is (Rₛ, Gₛ, Bₛ, Aₛ).</span></span>

</dd> <dt>

<span data-ttu-id="6bc71-113"><span id="D3DBLEND_INVSRCCOLOR"></span><span id="d3dblend_invsrccolor"></span>**D3DBLEND \_ INVSRCCOLOR**</span><span class="sxs-lookup"><span data-stu-id="6bc71-113"><span id="D3DBLEND_INVSRCCOLOR"></span><span id="d3dblend_invsrccolor"></span>**D3DBLEND\_INVSRCCOLOR**</span></span>
</dt> <dd>

<span data-ttu-id="6bc71-114">Der Überblendfaktor ist (1 – Rs, 1 – Gs, 1 – Bs, 1 – As).</span><span class="sxs-lookup"><span data-stu-id="6bc71-114">Blend factor is (1 - Rₛ, 1 - Gₛ, 1 - Bₛ, 1 - Aₛ).</span></span>

</dd> <dt>

<span data-ttu-id="6bc71-115"><span id="D3DBLEND_SRCALPHA"></span><span id="d3dblend_srcalpha"></span>**D3DBLEND \_ SRCALPHA**</span><span class="sxs-lookup"><span data-stu-id="6bc71-115"><span id="D3DBLEND_SRCALPHA"></span><span id="d3dblend_srcalpha"></span>**D3DBLEND\_SRCALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="6bc71-116">Der Überblendfaktor ist (As, As, As, As).</span><span class="sxs-lookup"><span data-stu-id="6bc71-116">Blend factor is (Aₛ, Aₛ, Aₛ, Aₛ).</span></span>

</dd> <dt>

<span data-ttu-id="6bc71-117"><span id="D3DBLEND_INVSRCALPHA"></span><span id="d3dblend_invsrcalpha"></span>**D3DBLEND \_ INVSRCALPHA**</span><span class="sxs-lookup"><span data-stu-id="6bc71-117"><span id="D3DBLEND_INVSRCALPHA"></span><span id="d3dblend_invsrcalpha"></span>**D3DBLEND\_INVSRCALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="6bc71-118">Der Überblendfaktor ist ( 1 - As, 1 - As, 1 - As, 1 - As).</span><span class="sxs-lookup"><span data-stu-id="6bc71-118">Blend factor is ( 1 - Aₛ, 1 - Aₛ, 1 - Aₛ, 1 - Aₛ).</span></span>

</dd> <dt>

<span data-ttu-id="6bc71-119"><span id="D3DBLEND_DESTALPHA"></span><span id="d3dblend_destalpha"></span>**D3DBLEND \_ DESTALPHA**</span><span class="sxs-lookup"><span data-stu-id="6bc71-119"><span id="D3DBLEND_DESTALPHA"></span><span id="d3dblend_destalpha"></span>**D3DBLEND\_DESTALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="6bc71-120">Der Überblendfaktor ist (A<sub>d</sub> A<sub>d</sub> A<sub>d</sub> A<sub>d</sub>).</span><span class="sxs-lookup"><span data-stu-id="6bc71-120">Blend factor is (A<sub>d</sub> A<sub>d</sub> A<sub>d</sub> A<sub>d</sub>).</span></span>

</dd> <dt>

<span data-ttu-id="6bc71-121"><span id="D3DBLEND_INVDESTALPHA"></span><span id="d3dblend_invdestalpha"></span>**D3DBLEND \_ INVDESTALPHA**</span><span class="sxs-lookup"><span data-stu-id="6bc71-121"><span id="D3DBLEND_INVDESTALPHA"></span><span id="d3dblend_invdestalpha"></span>**D3DBLEND\_INVDESTALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="6bc71-122">Der Überblendfaktor ist (1 – A<sub>d</sub> 1 – A<sub>d</sub> 1 – A<sub>d</sub> 1 – A<sub>d</sub>).</span><span class="sxs-lookup"><span data-stu-id="6bc71-122">Blend factor is (1 - A<sub>d</sub> 1 - A<sub>d</sub> 1 - A<sub>d</sub> 1 - A<sub>d</sub>).</span></span>

</dd> <dt>

<span data-ttu-id="6bc71-123"><span id="D3DBLEND_DESTCOLOR"></span><span id="d3dblend_destcolor"></span>**D3DBLEND \_ DESTCOLOR**</span><span class="sxs-lookup"><span data-stu-id="6bc71-123"><span id="D3DBLEND_DESTCOLOR"></span><span id="d3dblend_destcolor"></span>**D3DBLEND\_DESTCOLOR**</span></span>
</dt> <dd>

<span data-ttu-id="6bc71-124">Der Blend-Faktor ist (R<sub>d</sub>, G<sub>d</sub>, B<sub>d</sub>, A<sub>d</sub>).</span><span class="sxs-lookup"><span data-stu-id="6bc71-124">Blend factor is (R<sub>d</sub>, G<sub>d</sub>, B<sub>d</sub>, A<sub>d</sub>).</span></span>

</dd> <dt>

<span data-ttu-id="6bc71-125"><span id="D3DBLEND_INVDESTCOLOR"></span><span id="d3dblend_invdestcolor"></span>**D3DBLEND \_ INVDESTCOLOR**</span><span class="sxs-lookup"><span data-stu-id="6bc71-125"><span id="D3DBLEND_INVDESTCOLOR"></span><span id="d3dblend_invdestcolor"></span>**D3DBLEND\_INVDESTCOLOR**</span></span>
</dt> <dd>

<span data-ttu-id="6bc71-126">Der Blend-Faktor ist (1 – R<sub>d</sub>, 1 – G<sub>d</sub>, 1 – B<sub>d</sub>, 1 – A<sub>d</sub>).</span><span class="sxs-lookup"><span data-stu-id="6bc71-126">Blend factor is (1 - R<sub>d</sub>, 1 - G<sub>d</sub>, 1 - B<sub>d</sub>, 1 - A<sub>d</sub>).</span></span>

</dd> <dt>

<span data-ttu-id="6bc71-127"><span id="D3DBLEND_SRCALPHASAT"></span><span id="d3dblend_srcalphasat"></span>**D3DBLEND \_ SRCALPHASAT**</span><span class="sxs-lookup"><span data-stu-id="6bc71-127"><span id="D3DBLEND_SRCALPHASAT"></span><span id="d3dblend_srcalphasat"></span>**D3DBLEND\_SRCALPHASAT**</span></span>
</dt> <dd>

<span data-ttu-id="6bc71-128">Der Blend-Faktor ist (f, f, f, 1); where f = min(As, 1 - A<sub>d</sub>).</span><span class="sxs-lookup"><span data-stu-id="6bc71-128">Blend factor is (f, f, f, 1); where f = min(Aₛ, 1 - A<sub>d</sub>).</span></span>

</dd> <dt>

<span data-ttu-id="6bc71-129"><span id="D3DBLEND_BOTHSRCALPHA"></span><span id="d3dblend_bothsrcalpha"></span>**D3DBLEND \_ BOTHSRCALPHA**</span><span class="sxs-lookup"><span data-stu-id="6bc71-129"><span id="D3DBLEND_BOTHSRCALPHA"></span><span id="d3dblend_bothsrcalpha"></span>**D3DBLEND\_BOTHSRCALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="6bc71-130">**Veraltete**.</span><span class="sxs-lookup"><span data-stu-id="6bc71-130">**Obsolete**.</span></span> <span data-ttu-id="6bc71-131">Ab DirectX 6 können Sie den gleichen Effekt erzielen, indem Sie die Quellen- und Zielmischungsfaktoren in separaten Aufrufen auf D3DBLEND \_ SRCALPHA und D3DBLEND \_ INVSRCALPHA festlegen.</span><span class="sxs-lookup"><span data-stu-id="6bc71-131">Starting with DirectX 6, you can achieve the same effect by setting the source and destination blend factors to D3DBLEND\_SRCALPHA and D3DBLEND\_INVSRCALPHA in separate calls.</span></span>

</dd> <dt>

<span data-ttu-id="6bc71-132"><span id="D3DBLEND_BOTHINVSRCALPHA"></span><span id="d3dblend_bothinvsrcalpha"></span>**D3DBLEND \_ BOTHINVSRCALPHA**</span><span class="sxs-lookup"><span data-stu-id="6bc71-132"><span id="D3DBLEND_BOTHINVSRCALPHA"></span><span id="d3dblend_bothinvsrcalpha"></span>**D3DBLEND\_BOTHINVSRCALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="6bc71-133">**Veraltete**.</span><span class="sxs-lookup"><span data-stu-id="6bc71-133">**Obsolete**.</span></span> <span data-ttu-id="6bc71-134">Der Quellmischungsfaktor ist (1 – As, 1 – As, 1 – As, 1 – As), und der Zielmischungsfaktor ist (As, As, As, As); Die Zielmischungsauswahl wird überschrieben.</span><span class="sxs-lookup"><span data-stu-id="6bc71-134">Source blend factor is (1 - Aₛ, 1 - Aₛ, 1 - Aₛ, 1 - Aₛ), and destination blend factor is (Aₛ, Aₛ, Aₛ, Aₛ); the destination blend selection is overridden.</span></span> <span data-ttu-id="6bc71-135">Dieser Blendmodus wird nur für den D3DRS \_ SRCBLEND-Renderzustand unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6bc71-135">This blend mode is supported only for the D3DRS\_SRCBLEND render state.</span></span>

</dd> <dt>

<span data-ttu-id="6bc71-136"><span id="D3DBLEND_BLENDFACTOR"></span><span id="d3dblend_blendfactor"></span>**D3DBLEND \_ BLENDFACTOR**</span><span class="sxs-lookup"><span data-stu-id="6bc71-136"><span id="D3DBLEND_BLENDFACTOR"></span><span id="d3dblend_blendfactor"></span>**D3DBLEND\_BLENDFACTOR**</span></span>
</dt> <dd>

<span data-ttu-id="6bc71-137">Konstanter Farbmischungsfaktor, der vom Framepufferblender verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6bc71-137">Constant color blending factor used by the frame-buffer blender.</span></span> <span data-ttu-id="6bc71-138">Dieser Blendmodus wird nur unterstützt, wenn D3DPBLENDCAPS \_ BLENDFACTOR in den **Membern SrcBlendCaps** oder **DestBlendCaps** von [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="6bc71-138">This blend mode is supported only if D3DPBLENDCAPS\_BLENDFACTOR is set in the **SrcBlendCaps** or **DestBlendCaps** members of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

</dd> <dt>

<span data-ttu-id="6bc71-139"><span id="D3DBLEND_INVBLENDFACTOR"></span><span id="d3dblend_invblendfactor"></span>**D3DBLEND \_ INVBLENDFACTOR**</span><span class="sxs-lookup"><span data-stu-id="6bc71-139"><span id="D3DBLEND_INVBLENDFACTOR"></span><span id="d3dblend_invblendfactor"></span>**D3DBLEND\_INVBLENDFACTOR**</span></span>
</dt> <dd>

<span data-ttu-id="6bc71-140">Invertierter konstanter Farbmischungsfaktor, der vom Framepufferblender verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6bc71-140">Inverted constant color-blending factor used by the frame-buffer blender.</span></span> <span data-ttu-id="6bc71-141">Dieser Blendmodus wird nur unterstützt, wenn das D3DPBLENDCAPS \_ BLENDFACTOR-Bit in den **Membern SrcBlendCaps** oder **DestBlendCaps** von [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="6bc71-141">This blend mode is supported only if the D3DPBLENDCAPS\_BLENDFACTOR bit is set in the **SrcBlendCaps** or **DestBlendCaps** members of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

</dd> <dt>

<span data-ttu-id="6bc71-142"><span id="D3DBLEND_SRCCOLOR2"></span><span id="d3dblend_srccolor2"></span>**D3DBLEND \_ SRCCOLOR2**</span><span class="sxs-lookup"><span data-stu-id="6bc71-142"><span id="D3DBLEND_SRCCOLOR2"></span><span id="d3dblend_srccolor2"></span>**D3DBLEND\_SRCCOLOR2**</span></span>
</dt> <dd>

<span data-ttu-id="6bc71-143">Der Überblendfaktor ist (PSOutColor \[ 1 \] <sub>r,</sub>PSOutColor \[ 1 \] <sub>g,</sub>PSOutColor \[ 1 \] <sub>b,</sub>nicht verwendet).</span><span class="sxs-lookup"><span data-stu-id="6bc71-143">Blend factor is (PSOutColor\[1\]<sub>r</sub>, PSOutColor\[1\]<sub>g</sub>, PSOutColor\[1\]<sub>b</sub>, not used).</span></span> <span data-ttu-id="6bc71-144">Weitere Informationen finden [Sie unter Renderzielmischung.](#render-target-blending)</span><span class="sxs-lookup"><span data-stu-id="6bc71-144">See [Render Target Blending](#render-target-blending).</span></span>

<span data-ttu-id="6bc71-145">Unterschiede zwischen Direct3D 9 und Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="6bc71-145">Differences between Direct3D 9 and Direct3D 9Ex:</span></span>

- <span data-ttu-id="6bc71-146">Dieses Flag ist nur in Direct3D 9Ex verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6bc71-146">This flag is available in Direct3D 9Ex only.</span></span>



 

</dd> <dt>

<span data-ttu-id="6bc71-147"><span id="D3DBLEND_INVSRCCOLOR2"></span><span id="d3dblend_invsrccolor2"></span>**D3DBLEND \_ INVSRCCOLOR2**</span><span class="sxs-lookup"><span data-stu-id="6bc71-147"><span id="D3DBLEND_INVSRCCOLOR2"></span><span id="d3dblend_invsrccolor2"></span>**D3DBLEND\_INVSRCCOLOR2**</span></span>
</dt> <dd>

<span data-ttu-id="6bc71-148">Der Überblendfaktor ist (1 - PSOutColor \[ 1 \] <sub>r</sub>, 1 - PSOutColor \[ 1 \] <sub>g</sub>, 1 - PSOutColor \[ 1 \] <sub>b</sub>, nicht verwendet)).</span><span class="sxs-lookup"><span data-stu-id="6bc71-148">Blend factor is (1 - PSOutColor\[1\]<sub>r</sub>, 1 - PSOutColor\[1\]<sub>g</sub>, 1 - PSOutColor\[1\]<sub>b</sub>, not used)).</span></span> <span data-ttu-id="6bc71-149">Weitere Informationen finden [Sie unter Renderzielmischung.](#render-target-blending)</span><span class="sxs-lookup"><span data-stu-id="6bc71-149">See [Render Target Blending](#render-target-blending).</span></span>


<span data-ttu-id="6bc71-150">Unterschiede zwischen Direct3D 9 und Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="6bc71-150">Differences between Direct3D 9 and Direct3D 9Ex:</span></span>

- <span data-ttu-id="6bc71-151">Dieses Flag ist nur in Direct3D 9Ex verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6bc71-151">This flag is available in Direct3D 9Ex only.</span></span>



 

</dd> <dt>

<span data-ttu-id="6bc71-152"><span id="D3DBLEND_FORCE_DWORD"></span><span id="d3dblend_force_dword"></span>**D3DBLEND \_ FORCE \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="6bc71-152"><span id="D3DBLEND_FORCE_DWORD"></span><span id="d3dblend_force_dword"></span>**D3DBLEND\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="6bc71-153">Erzwingt, dass diese Enumeration auf eine Größe von 32 Bits kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="6bc71-153">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="6bc71-154">Ohne diesen Wert würden einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="6bc71-154">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="6bc71-155">Dieser Wert wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="6bc71-155">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6bc71-156">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6bc71-156">Remarks</span></span>

<span data-ttu-id="6bc71-157">In den obigen Memberbeschreibungen werden die RGBA-Werte der Quelle und des Ziels durch die Inskripts s und d angegeben.</span><span class="sxs-lookup"><span data-stu-id="6bc71-157">In the preceding member descriptions, the RGBA values of the source and destination are indicated by the s and d subscripts.</span></span>

<span data-ttu-id="6bc71-158">Die Werte in diesem aufzählten Typ werden von den folgenden Renderzuständen verwendet:</span><span class="sxs-lookup"><span data-stu-id="6bc71-158">The values in this enumerated type are used by the following render states:</span></span>

-   <span data-ttu-id="6bc71-159">D3DRS \_ DESTBLEND</span><span class="sxs-lookup"><span data-stu-id="6bc71-159">D3DRS\_DESTBLEND</span></span>
-   <span data-ttu-id="6bc71-160">D3DRS \_ SRCBLEND</span><span class="sxs-lookup"><span data-stu-id="6bc71-160">D3DRS\_SRCBLEND</span></span>
-   <span data-ttu-id="6bc71-161">D3DRS \_ DESTBLENDALPHA</span><span class="sxs-lookup"><span data-stu-id="6bc71-161">D3DRS\_DESTBLENDALPHA</span></span>
-   <span data-ttu-id="6bc71-162">D3DRS \_ SRCBLENDALPHA</span><span class="sxs-lookup"><span data-stu-id="6bc71-162">D3DRS\_SRCBLENDALPHA</span></span>

<span data-ttu-id="6bc71-163">Siehe [ **D3DRENDERSTATETYPE**](./d3drenderstatetype.md)</span><span class="sxs-lookup"><span data-stu-id="6bc71-163">See [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)</span></span>

### <a name="render-target-blending"></a><span data-ttu-id="6bc71-164">Renderzielblending</span><span class="sxs-lookup"><span data-stu-id="6bc71-164">Render Target Blending</span></span>

<span data-ttu-id="6bc71-165">Direct3D 9Ex verfügt über verbesserte Funktionen zum Rendern von Text.</span><span class="sxs-lookup"><span data-stu-id="6bc71-165">Direct3D 9Ex has improved text rendering capabilities.</span></span> <span data-ttu-id="6bc71-166">Für das Rendern von Schriftarten vom Typ "Klartext" sind normalerweise zwei Durchläufe erforderlich.</span><span class="sxs-lookup"><span data-stu-id="6bc71-166">Rendering clear-type fonts would normally require two passes.</span></span> <span data-ttu-id="6bc71-167">Um den zweiten Durchlauf zu vermeiden, kann ein Pixel-Shader verwendet werden, um zwei Farben auszugeben, die wir ALS PSOutColor \[ 0 \] und PSOutColor 1 bezeichnen \[ \] können.</span><span class="sxs-lookup"><span data-stu-id="6bc71-167">To eliminate the second pass, a pixel shader can be used to output two colors, which we can call PSOutColor\[0\] and PSOutColor\[1\].</span></span> <span data-ttu-id="6bc71-168">Die erste Farbe würde die standardmäßigen drei Farbkomponenten (RGB) enthalten.</span><span class="sxs-lookup"><span data-stu-id="6bc71-168">The first color would contain the standard 3 color components (RGB).</span></span> <span data-ttu-id="6bc71-169">Die zweite Farbe enthält drei Alphakomponenten (eine für jede Komponente der ersten Farbe).</span><span class="sxs-lookup"><span data-stu-id="6bc71-169">The second color would contain 3 alpha components (one for each component of the first color).</span></span>

<span data-ttu-id="6bc71-170">Diese neuen Mischungsmodi werden nur für das Textrendering auf dem ersten Renderziel verwendet.</span><span class="sxs-lookup"><span data-stu-id="6bc71-170">These new blending modes are only used for text rendering on the first render target.</span></span>

## <a name="requirements"></a><span data-ttu-id="6bc71-171">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6bc71-171">Requirements</span></span>



| <span data-ttu-id="6bc71-172">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6bc71-172">Requirement</span></span> | <span data-ttu-id="6bc71-173">Wert</span><span class="sxs-lookup"><span data-stu-id="6bc71-173">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6bc71-174">Header</span><span class="sxs-lookup"><span data-stu-id="6bc71-174">Header</span></span><br/> | <dl> <span data-ttu-id="6bc71-175"><dt>D3D9Types.h</dt></span><span class="sxs-lookup"><span data-stu-id="6bc71-175"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6bc71-176">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="6bc71-176">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6bc71-177">Direct3D-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="6bc71-177">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 
