---
description: Definiert den unterstützten Blend-Modus.
ms.assetid: 60ff384c-15a0-4c6f-9e2c-59fdea76b7a1
title: D3DBLEND-Enumeration (D3D9Types. h)
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
ms.openlocfilehash: d8d779ad714e396f9c9a82bbbc42ddd09b76e2ac
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961568"
---
# <a name="d3dblend-enumeration"></a><span data-ttu-id="76671-103">D3DBLEND-Enumeration</span><span class="sxs-lookup"><span data-stu-id="76671-103">D3DBLEND enumeration</span></span>

<span data-ttu-id="76671-104">Definiert den unterstützten Blend-Modus.</span><span class="sxs-lookup"><span data-stu-id="76671-104">Defines the supported blend mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="76671-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="76671-105">Syntax</span></span>


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



## <a name="constants"></a><span data-ttu-id="76671-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="76671-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="76671-107"><span id="D3DBLEND_ZERO"></span><span id="d3dblend_zero"></span>**D3DBLEND \_ 0**</span><span class="sxs-lookup"><span data-stu-id="76671-107"><span id="D3DBLEND_ZERO"></span><span id="d3dblend_zero"></span>**D3DBLEND\_ZERO**</span></span>
</dt> <dd>

<span data-ttu-id="76671-108">Der Blend-Faktor ist (0, 0, 0, 0).</span><span class="sxs-lookup"><span data-stu-id="76671-108">Blend factor is (0, 0, 0, 0).</span></span>

</dd> <dt>

<span data-ttu-id="76671-109"><span id="D3DBLEND_ONE"></span><span id="d3dblend_one"></span>**D3DBLEND \_**</span><span class="sxs-lookup"><span data-stu-id="76671-109"><span id="D3DBLEND_ONE"></span><span id="d3dblend_one"></span>**D3DBLEND\_ONE**</span></span>
</dt> <dd>

<span data-ttu-id="76671-110">Der Blend-Faktor ist (1, 1, 1, 1).</span><span class="sxs-lookup"><span data-stu-id="76671-110">Blend factor is (1, 1, 1, 1).</span></span>

</dd> <dt>

<span data-ttu-id="76671-111"><span id="D3DBLEND_SRCCOLOR"></span><span id="d3dblend_srccolor"></span>**D3DBLEND \_ srccolor**</span><span class="sxs-lookup"><span data-stu-id="76671-111"><span id="D3DBLEND_SRCCOLOR"></span><span id="d3dblend_srccolor"></span>**D3DBLEND\_SRCCOLOR**</span></span>
</dt> <dd>

<span data-ttu-id="76671-112">Der Blend-Faktor ist (RS, GS, SB, as).</span><span class="sxs-lookup"><span data-stu-id="76671-112">Blend factor is (Rₛ, Gₛ, Bₛ, Aₛ).</span></span>

</dd> <dt>

<span data-ttu-id="76671-113"><span id="D3DBLEND_INVSRCCOLOR"></span><span id="d3dblend_invsrccolor"></span>**D3DBLEND- \_ invsrccolor**</span><span class="sxs-lookup"><span data-stu-id="76671-113"><span id="D3DBLEND_INVSRCCOLOR"></span><span id="d3dblend_invsrccolor"></span>**D3DBLEND\_INVSRCCOLOR**</span></span>
</dt> <dd>

<span data-ttu-id="76671-114">Der Blend-Faktor ist (1-RS, 1-GS, 1-SB, 1-AS).</span><span class="sxs-lookup"><span data-stu-id="76671-114">Blend factor is (1 - Rₛ, 1 - Gₛ, 1 - Bₛ, 1 - Aₛ).</span></span>

</dd> <dt>

<span data-ttu-id="76671-115"><span id="D3DBLEND_SRCALPHA"></span><span id="d3dblend_srcalpha"></span>**D3DBLEND \_ srcalpha**</span><span class="sxs-lookup"><span data-stu-id="76671-115"><span id="D3DBLEND_SRCALPHA"></span><span id="d3dblend_srcalpha"></span>**D3DBLEND\_SRCALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="76671-116">Der Blend-Faktor ist (AS, as, as).</span><span class="sxs-lookup"><span data-stu-id="76671-116">Blend factor is (Aₛ, Aₛ, Aₛ, Aₛ).</span></span>

</dd> <dt>

<span data-ttu-id="76671-117"><span id="D3DBLEND_INVSRCALPHA"></span><span id="d3dblend_invsrcalpha"></span>**D3DBLEND- \_ invsrcalpha**</span><span class="sxs-lookup"><span data-stu-id="76671-117"><span id="D3DBLEND_INVSRCALPHA"></span><span id="d3dblend_invsrcalpha"></span>**D3DBLEND\_INVSRCALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="76671-118">Der Blend-Faktor ist (1-AS, 1-AS, 1-AS, 1-AS).</span><span class="sxs-lookup"><span data-stu-id="76671-118">Blend factor is ( 1 - Aₛ, 1 - Aₛ, 1 - Aₛ, 1 - Aₛ).</span></span>

</dd> <dt>

<span data-ttu-id="76671-119"><span id="D3DBLEND_DESTALPHA"></span><span id="d3dblend_destalpha"></span>**D3DBLEND \_ -Debug**</span><span class="sxs-lookup"><span data-stu-id="76671-119"><span id="D3DBLEND_DESTALPHA"></span><span id="d3dblend_destalpha"></span>**D3DBLEND\_DESTALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="76671-120">Der<sub>Blend-Faktor</sub>ist<sub>(a d a d</sub> <sub>a d</sub> <sub>a d</sub> ).</span><span class="sxs-lookup"><span data-stu-id="76671-120">Blend factor is (A<sub>d</sub> A<sub>d</sub> A<sub>d</sub> A<sub>d</sub>).</span></span>

</dd> <dt>

<span data-ttu-id="76671-121"><span id="D3DBLEND_INVDESTALPHA"></span><span id="d3dblend_invdestalpha"></span>**D3DBLEND- \_ invwastalpha**</span><span class="sxs-lookup"><span data-stu-id="76671-121"><span id="D3DBLEND_INVDESTALPHA"></span><span id="d3dblend_invdestalpha"></span>**D3DBLEND\_INVDESTALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="76671-122">Der Blend-Faktor ist (1-a<sub>d</sub> 1<sub>-a d 1-</sub> a<sub>d 1-</sub> <sub>a).</sub></span><span class="sxs-lookup"><span data-stu-id="76671-122">Blend factor is (1 - A<sub>d</sub> 1 - A<sub>d</sub> 1 - A<sub>d</sub> 1 - A<sub>d</sub>).</span></span>

</dd> <dt>

<span data-ttu-id="76671-123"><span id="D3DBLEND_DESTCOLOR"></span><span id="d3dblend_destcolor"></span>**D3DBLEND \_ destcolor**</span><span class="sxs-lookup"><span data-stu-id="76671-123"><span id="D3DBLEND_DESTCOLOR"></span><span id="d3dblend_destcolor"></span>**D3DBLEND\_DESTCOLOR**</span></span>
</dt> <dd>

<span data-ttu-id="76671-124">Der Blend-Faktor ist (R<sub>d</sub>, G<sub>d</sub>, B<sub>d</sub>, a<sub>d</sub>).</span><span class="sxs-lookup"><span data-stu-id="76671-124">Blend factor is (R<sub>d</sub>, G<sub>d</sub>, B<sub>d</sub>, A<sub>d</sub>).</span></span>

</dd> <dt>

<span data-ttu-id="76671-125"><span id="D3DBLEND_INVDESTCOLOR"></span><span id="d3dblend_invdestcolor"></span>**D3DBLEND \_ invdestcolor**</span><span class="sxs-lookup"><span data-stu-id="76671-125"><span id="D3DBLEND_INVDESTCOLOR"></span><span id="d3dblend_invdestcolor"></span>**D3DBLEND\_INVDESTCOLOR**</span></span>
</dt> <dd>

<span data-ttu-id="76671-126">Der Blend-Faktor ist (1-R<sub>d</sub>, 1-G<sub>d</sub>, 1-B<sub>d</sub>, 1-A<sub>d</sub>).</span><span class="sxs-lookup"><span data-stu-id="76671-126">Blend factor is (1 - R<sub>d</sub>, 1 - G<sub>d</sub>, 1 - B<sub>d</sub>, 1 - A<sub>d</sub>).</span></span>

</dd> <dt>

<span data-ttu-id="76671-127"><span id="D3DBLEND_SRCALPHASAT"></span><span id="d3dblend_srcalphasat"></span>**D3DBLEND \_ srcalphasat**</span><span class="sxs-lookup"><span data-stu-id="76671-127"><span id="D3DBLEND_SRCALPHASAT"></span><span id="d3dblend_srcalphasat"></span>**D3DBLEND\_SRCALPHASAT**</span></span>
</dt> <dd>

<span data-ttu-id="76671-128">Blend-Faktor ist (f, f, f, 1); Where f = min (AS, 1-A<sub>d</sub>).</span><span class="sxs-lookup"><span data-stu-id="76671-128">Blend factor is (f, f, f, 1); where f = min(Aₛ, 1 - A<sub>d</sub>).</span></span>

</dd> <dt>

<span data-ttu-id="76671-129"><span id="D3DBLEND_BOTHSRCALPHA"></span><span id="d3dblend_bothsrcalpha"></span>**D3DBLEND \_ bothsrcalpha**</span><span class="sxs-lookup"><span data-stu-id="76671-129"><span id="D3DBLEND_BOTHSRCALPHA"></span><span id="d3dblend_bothsrcalpha"></span>**D3DBLEND\_BOTHSRCALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="76671-130">**Veraltet**.</span><span class="sxs-lookup"><span data-stu-id="76671-130">**Obsolete**.</span></span> <span data-ttu-id="76671-131">Ab DirectX 6 können Sie denselben Effekt erzielen, indem Sie die Quell-und Ziel-Blend-Faktoren auf D3DBLEND \_ srcalpha und D3DBLEND \_ invsrcalpha in separaten Aufrufen festlegen.</span><span class="sxs-lookup"><span data-stu-id="76671-131">Starting with DirectX 6, you can achieve the same effect by setting the source and destination blend factors to D3DBLEND\_SRCALPHA and D3DBLEND\_INVSRCALPHA in separate calls.</span></span>

</dd> <dt>

<span data-ttu-id="76671-132"><span id="D3DBLEND_BOTHINVSRCALPHA"></span><span id="d3dblend_bothinvsrcalpha"></span>**D3DBLEND \_ bothinvsrcalpha**</span><span class="sxs-lookup"><span data-stu-id="76671-132"><span id="D3DBLEND_BOTHINVSRCALPHA"></span><span id="d3dblend_bothinvsrcalpha"></span>**D3DBLEND\_BOTHINVSRCALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="76671-133">**Veraltet**.</span><span class="sxs-lookup"><span data-stu-id="76671-133">**Obsolete**.</span></span> <span data-ttu-id="76671-134">Der Quell Blend Faktor ist (1-AS, 1-AS, 1-AS, 1-AS), und der Ziel-Blend-Faktor ist (AS, as, as); die Ziel-Blend-Auswahl wird überschrieben.</span><span class="sxs-lookup"><span data-stu-id="76671-134">Source blend factor is (1 - Aₛ, 1 - Aₛ, 1 - Aₛ, 1 - Aₛ), and destination blend factor is (Aₛ, Aₛ, Aₛ, Aₛ); the destination blend selection is overridden.</span></span> <span data-ttu-id="76671-135">Dieser Blend-Modus wird nur für den \_ renderzustand D3DRS srcblend unterstützt.</span><span class="sxs-lookup"><span data-stu-id="76671-135">This blend mode is supported only for the D3DRS\_SRCBLEND render state.</span></span>

</dd> <dt>

<span data-ttu-id="76671-136"><span id="D3DBLEND_BLENDFACTOR"></span><span id="d3dblend_blendfactor"></span>**D3DBLEND \_ blendfactor**</span><span class="sxs-lookup"><span data-stu-id="76671-136"><span id="D3DBLEND_BLENDFACTOR"></span><span id="d3dblend_blendfactor"></span>**D3DBLEND\_BLENDFACTOR**</span></span>
</dt> <dd>

<span data-ttu-id="76671-137">Konstanter Farb Mischungs Faktor, der vom Frame Puffer-Blender verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="76671-137">Constant color blending factor used by the frame-buffer blender.</span></span> <span data-ttu-id="76671-138">Dieser Blend-Modus wird nur unterstützt, wenn D3DPBLENDCAPS \_ blendfactor in den **srcblendcaps** -oder **destblendcaps** -Membern von [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="76671-138">This blend mode is supported only if D3DPBLENDCAPS\_BLENDFACTOR is set in the **SrcBlendCaps** or **DestBlendCaps** members of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

</dd> <dt>

<span data-ttu-id="76671-139"><span id="D3DBLEND_INVBLENDFACTOR"></span><span id="d3dblend_invblendfactor"></span>**D3DBLEND- \_ invblendfactor**</span><span class="sxs-lookup"><span data-stu-id="76671-139"><span id="D3DBLEND_INVBLENDFACTOR"></span><span id="d3dblend_invblendfactor"></span>**D3DBLEND\_INVBLENDFACTOR**</span></span>
</dt> <dd>

<span data-ttu-id="76671-140">Der invertierte konstante Farb Mischungs Faktor, der vom Frame Puffer-Blender verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="76671-140">Inverted constant color-blending factor used by the frame-buffer blender.</span></span> <span data-ttu-id="76671-141">Dieser Blend-Modus wird nur unterstützt, wenn das D3DPBLENDCAPS \_ blendfactor-Bit in den **srcblendcaps** -oder **destblendcaps** -Membern von [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="76671-141">This blend mode is supported only if the D3DPBLENDCAPS\_BLENDFACTOR bit is set in the **SrcBlendCaps** or **DestBlendCaps** members of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

</dd> <dt>

<span data-ttu-id="76671-142"><span id="D3DBLEND_SRCCOLOR2"></span><span id="d3dblend_srccolor2"></span>**D3DBLEND \_ SRCCOLOR2**</span><span class="sxs-lookup"><span data-stu-id="76671-142"><span id="D3DBLEND_SRCCOLOR2"></span><span id="d3dblend_srccolor2"></span>**D3DBLEND\_SRCCOLOR2**</span></span>
</dt> <dd>

<span data-ttu-id="76671-143">Der Blend-Faktor ist (psoutcolor \[ 1 \] <sub>r</sub>, psoutcolor \[ 1 \] <sub>g</sub>, psoutcolor \[ 1 \] <sub>b</sub>, nicht verwendet).</span><span class="sxs-lookup"><span data-stu-id="76671-143">Blend factor is (PSOutColor\[1\]<sub>r</sub>, PSOutColor\[1\]<sub>g</sub>, PSOutColor\[1\]<sub>b</sub>, not used).</span></span> <span data-ttu-id="76671-144">Siehe [renderzielmischungs](#render-target-blending).</span><span class="sxs-lookup"><span data-stu-id="76671-144">See [Render Target Blending](#render-target-blending).</span></span>



|                                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="76671-145">Unterschiede zwischen Direct3D 9 und Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="76671-145">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="76671-146">Dieses Flag ist nur in Direct3D 9Ex verfügbar.</span><span class="sxs-lookup"><span data-stu-id="76671-146">This flag is available in Direct3D 9Ex only.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="76671-147"><span id="D3DBLEND_INVSRCCOLOR2"></span><span id="d3dblend_invsrccolor2"></span>**D3DBLEND \_ INVSRCCOLOR2**</span><span class="sxs-lookup"><span data-stu-id="76671-147"><span id="D3DBLEND_INVSRCCOLOR2"></span><span id="d3dblend_invsrccolor2"></span>**D3DBLEND\_INVSRCCOLOR2**</span></span>
</dt> <dd>

<span data-ttu-id="76671-148">Der Blend-Faktor ist (1-psoutcolor \[ 1 \] <sub>r</sub>, 1-psoutcolor \[ 1 \] <sub>g</sub>, 1-psoutcolor \[ 1 \] <sub>b</sub>, nicht verwendet)).</span><span class="sxs-lookup"><span data-stu-id="76671-148">Blend factor is (1 - PSOutColor\[1\]<sub>r</sub>, 1 - PSOutColor\[1\]<sub>g</sub>, 1 - PSOutColor\[1\]<sub>b</sub>, not used)).</span></span> <span data-ttu-id="76671-149">Siehe [renderzielmischungs](#render-target-blending).</span><span class="sxs-lookup"><span data-stu-id="76671-149">See [Render Target Blending](#render-target-blending).</span></span>



|                                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="76671-150">Unterschiede zwischen Direct3D 9 und Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="76671-150">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="76671-151">Dieses Flag ist nur in Direct3D 9Ex verfügbar.</span><span class="sxs-lookup"><span data-stu-id="76671-151">This flag is available in Direct3D 9Ex only.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="76671-152"><span id="D3DBLEND_FORCE_DWORD"></span><span id="d3dblend_force_dword"></span>**D3DBLEND \_ Erzwingen von \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="76671-152"><span id="D3DBLEND_FORCE_DWORD"></span><span id="d3dblend_force_dword"></span>**D3DBLEND\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="76671-153">Erzwingt die Kompilierung dieser Enumeration in 32 Bits.</span><span class="sxs-lookup"><span data-stu-id="76671-153">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="76671-154">Ohne diesen Wert können einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="76671-154">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="76671-155">Dieser Wert wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="76671-155">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="76671-156">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="76671-156">Remarks</span></span>

<span data-ttu-id="76671-157">In den vorstehenden Element Beschreibungen werden die RGBA-Werte der Quelle und des Ziels durch die e-und d-Indizes angegeben.</span><span class="sxs-lookup"><span data-stu-id="76671-157">In the preceding member descriptions, the RGBA values of the source and destination are indicated by the s and d subscripts.</span></span>

<span data-ttu-id="76671-158">Die Werte in diesem enumerierten Typ werden von den folgenden Rendering-Zuständen verwendet:</span><span class="sxs-lookup"><span data-stu-id="76671-158">The values in this enumerated type are used by the following render states:</span></span>

-   <span data-ttu-id="76671-159">D3DRS \_ destblend</span><span class="sxs-lookup"><span data-stu-id="76671-159">D3DRS\_DESTBLEND</span></span>
-   <span data-ttu-id="76671-160">D3DRS \_ srcblend</span><span class="sxs-lookup"><span data-stu-id="76671-160">D3DRS\_SRCBLEND</span></span>
-   <span data-ttu-id="76671-161">D3DRS \_ destblendalpha</span><span class="sxs-lookup"><span data-stu-id="76671-161">D3DRS\_DESTBLENDALPHA</span></span>
-   <span data-ttu-id="76671-162">D3DRS \_ srcblendalpha</span><span class="sxs-lookup"><span data-stu-id="76671-162">D3DRS\_SRCBLENDALPHA</span></span>

<span data-ttu-id="76671-163">Siehe [ **D3DRENDERSTATETYPE**](./d3drenderstatetype.md)</span><span class="sxs-lookup"><span data-stu-id="76671-163">See [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)</span></span>

### <a name="render-target-blending"></a><span data-ttu-id="76671-164">Mischung für Renderziel</span><span class="sxs-lookup"><span data-stu-id="76671-164">Render Target Blending</span></span>

<span data-ttu-id="76671-165">Direct3D 9Ex hat verbesserte textrenderingfunktionen.</span><span class="sxs-lookup"><span data-stu-id="76671-165">Direct3D 9Ex has improved text rendering capabilities.</span></span> <span data-ttu-id="76671-166">Das Rendern von Schriftarten mit Klartext erfordert normalerweise zwei Durchgänge.</span><span class="sxs-lookup"><span data-stu-id="76671-166">Rendering clear-type fonts would normally require two passes.</span></span> <span data-ttu-id="76671-167">Um den zweiten Durchlauf auszuschließen, kann ein Pixelshader verwendet werden, um zwei Farben auszugeben, die wir psoutcolor \[ 0 \] und psoutcolor \[ 1 \] aufrufen können.</span><span class="sxs-lookup"><span data-stu-id="76671-167">To eliminate the second pass, a pixel shader can be used to output two colors, which we can call PSOutColor\[0\] and PSOutColor\[1\].</span></span> <span data-ttu-id="76671-168">Die erste Farbe enthält die Standard-drei Farbkomponenten (RGB).</span><span class="sxs-lookup"><span data-stu-id="76671-168">The first color would contain the standard 3 color components (RGB).</span></span> <span data-ttu-id="76671-169">Die zweite Farbe würde 3 Alpha Komponenten enthalten (eine für jede Komponente der ersten Farbe).</span><span class="sxs-lookup"><span data-stu-id="76671-169">The second color would contain 3 alpha components (one for each component of the first color).</span></span>

<span data-ttu-id="76671-170">Diese neuen Mischungs Modi werden nur zum Rendern von Text auf dem ersten Renderziel verwendet.</span><span class="sxs-lookup"><span data-stu-id="76671-170">These new blending modes are only used for text rendering on the first render target.</span></span>

## <a name="requirements"></a><span data-ttu-id="76671-171">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="76671-171">Requirements</span></span>



| <span data-ttu-id="76671-172">Anforderung</span><span class="sxs-lookup"><span data-stu-id="76671-172">Requirement</span></span> | <span data-ttu-id="76671-173">Wert</span><span class="sxs-lookup"><span data-stu-id="76671-173">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="76671-174">Header</span><span class="sxs-lookup"><span data-stu-id="76671-174">Header</span></span><br/> | <dl> <span data-ttu-id="76671-175"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="76671-175"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76671-176">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="76671-176">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76671-177">Direct3D-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="76671-177">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 
