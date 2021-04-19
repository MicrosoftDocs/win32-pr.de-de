---
description: Renderzustände definieren Setup Zustände für alle Arten von Vertex-und Pixel Verarbeitung.
ms.assetid: 2fd56388-f3bd-409f-876c-ae893840b623
title: D3DRENDERSTATETYPE-Enumeration (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DRENDERSTATETYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 2386762eaa45f1eefbccac97723c3ad71c3a76fd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106353704"
---
# <a name="d3drenderstatetype-enumeration"></a><span data-ttu-id="a6e47-103">D3DRENDERSTATETYPE-Enumeration</span><span class="sxs-lookup"><span data-stu-id="a6e47-103">D3DRENDERSTATETYPE enumeration</span></span>

<span data-ttu-id="a6e47-104">Renderzustände definieren Setup Zustände für alle Arten von Vertex-und Pixel Verarbeitung.</span><span class="sxs-lookup"><span data-stu-id="a6e47-104">Render states define set-up states for all kinds of vertex and pixel processing.</span></span> <span data-ttu-id="a6e47-105">Einige renderzustände richten die Vertexverarbeitung ein, und einige einrichten die Pixel Verarbeitung (siehe [renderzustände (Direct3D 9)](render-states.md)).</span><span class="sxs-lookup"><span data-stu-id="a6e47-105">Some render states set up vertex processing, and some set up pixel processing (see [Render States (Direct3D 9)](render-states.md)).</span></span> <span data-ttu-id="a6e47-106">Renderzustände können mithilfe von stateblocks gespeichert und wieder hergestellt werden (siehe [Status Blöcke speichern und Wiederherstellen (Direct3D 9)](state-blocks-save-and-restore-state.md)).</span><span class="sxs-lookup"><span data-stu-id="a6e47-106">Render states can be saved and restored using stateblocks (see [State Blocks Save and Restore State (Direct3D 9)](state-blocks-save-and-restore-state.md)).</span></span>

## <a name="syntax"></a><span data-ttu-id="a6e47-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a6e47-107">Syntax</span></span>


```C++
typedef enum D3DRENDERSTATETYPE { 
  D3DRS_ZENABLE                     = 7,
  D3DRS_FILLMODE                    = 8,
  D3DRS_SHADEMODE                   = 9,
  D3DRS_ZWRITEENABLE                = 14,
  D3DRS_ALPHATESTENABLE             = 15,
  D3DRS_LASTPIXEL                   = 16,
  D3DRS_SRCBLEND                    = 19,
  D3DRS_DESTBLEND                   = 20,
  D3DRS_CULLMODE                    = 22,
  D3DRS_ZFUNC                       = 23,
  D3DRS_ALPHAREF                    = 24,
  D3DRS_ALPHAFUNC                   = 25,
  D3DRS_DITHERENABLE                = 26,
  D3DRS_ALPHABLENDENABLE            = 27,
  D3DRS_FOGENABLE                   = 28,
  D3DRS_SPECULARENABLE              = 29,
  D3DRS_FOGCOLOR                    = 34,
  D3DRS_FOGTABLEMODE                = 35,
  D3DRS_FOGSTART                    = 36,
  D3DRS_FOGEND                      = 37,
  D3DRS_FOGDENSITY                  = 38,
  D3DRS_RANGEFOGENABLE              = 48,
  D3DRS_STENCILENABLE               = 52,
  D3DRS_STENCILFAIL                 = 53,
  D3DRS_STENCILZFAIL                = 54,
  D3DRS_STENCILPASS                 = 55,
  D3DRS_STENCILFUNC                 = 56,
  D3DRS_STENCILREF                  = 57,
  D3DRS_STENCILMASK                 = 58,
  D3DRS_STENCILWRITEMASK            = 59,
  D3DRS_TEXTUREFACTOR               = 60,
  D3DRS_WRAP0                       = 128,
  D3DRS_WRAP1                       = 129,
  D3DRS_WRAP2                       = 130,
  D3DRS_WRAP3                       = 131,
  D3DRS_WRAP4                       = 132,
  D3DRS_WRAP5                       = 133,
  D3DRS_WRAP6                       = 134,
  D3DRS_WRAP7                       = 135,
  D3DRS_CLIPPING                    = 136,
  D3DRS_LIGHTING                    = 137,
  D3DRS_AMBIENT                     = 139,
  D3DRS_FOGVERTEXMODE               = 140,
  D3DRS_COLORVERTEX                 = 141,
  D3DRS_LOCALVIEWER                 = 142,
  D3DRS_NORMALIZENORMALS            = 143,
  D3DRS_DIFFUSEMATERIALSOURCE       = 145,
  D3DRS_SPECULARMATERIALSOURCE      = 146,
  D3DRS_AMBIENTMATERIALSOURCE       = 147,
  D3DRS_EMISSIVEMATERIALSOURCE      = 148,
  D3DRS_VERTEXBLEND                 = 151,
  D3DRS_CLIPPLANEENABLE             = 152,
  D3DRS_POINTSIZE                   = 154,
  D3DRS_POINTSIZE_MIN               = 155,
  D3DRS_POINTSPRITEENABLE           = 156,
  D3DRS_POINTSCALEENABLE            = 157,
  D3DRS_POINTSCALE_A                = 158,
  D3DRS_POINTSCALE_B                = 159,
  D3DRS_POINTSCALE_C                = 160,
  D3DRS_MULTISAMPLEANTIALIAS        = 161,
  D3DRS_MULTISAMPLEMASK             = 162,
  D3DRS_PATCHEDGESTYLE              = 163,
  D3DRS_DEBUGMONITORTOKEN           = 165,
  D3DRS_POINTSIZE_MAX               = 166,
  D3DRS_INDEXEDVERTEXBLENDENABLE    = 167,
  D3DRS_COLORWRITEENABLE            = 168,
  D3DRS_TWEENFACTOR                 = 170,
  D3DRS_BLENDOP                     = 171,
  D3DRS_POSITIONDEGREE              = 172,
  D3DRS_NORMALDEGREE                = 173,
  D3DRS_SCISSORTESTENABLE           = 174,
  D3DRS_SLOPESCALEDEPTHBIAS         = 175,
  D3DRS_ANTIALIASEDLINEENABLE       = 176,
  D3DRS_MINTESSELLATIONLEVEL        = 178,
  D3DRS_MAXTESSELLATIONLEVEL        = 179,
  D3DRS_ADAPTIVETESS_X              = 180,
  D3DRS_ADAPTIVETESS_Y              = 181,
  D3DRS_ADAPTIVETESS_Z              = 182,
  D3DRS_ADAPTIVETESS_W              = 183,
  D3DRS_ENABLEADAPTIVETESSELLATION  = 184,
  D3DRS_TWOSIDEDSTENCILMODE         = 185,
  D3DRS_CCW_STENCILFAIL             = 186,
  D3DRS_CCW_STENCILZFAIL            = 187,
  D3DRS_CCW_STENCILPASS             = 188,
  D3DRS_CCW_STENCILFUNC             = 189,
  D3DRS_COLORWRITEENABLE1           = 190,
  D3DRS_COLORWRITEENABLE2           = 191,
  D3DRS_COLORWRITEENABLE3           = 192,
  D3DRS_BLENDFACTOR                 = 193,
  D3DRS_SRGBWRITEENABLE             = 194,
  D3DRS_DEPTHBIAS                   = 195,
  D3DRS_WRAP8                       = 198,
  D3DRS_WRAP9                       = 199,
  D3DRS_WRAP10                      = 200,
  D3DRS_WRAP11                      = 201,
  D3DRS_WRAP12                      = 202,
  D3DRS_WRAP13                      = 203,
  D3DRS_WRAP14                      = 204,
  D3DRS_WRAP15                      = 205,
  D3DRS_SEPARATEALPHABLENDENABLE    = 206,
  D3DRS_SRCBLENDALPHA               = 207,
  D3DRS_DESTBLENDALPHA              = 208,
  D3DRS_BLENDOPALPHA                = 209,
  D3DRS_FORCE_DWORD                 = 0x7fffffff
} D3DRENDERSTATETYPE, *LPD3DRENDERSTATETYPE;
```



## <a name="constants"></a><span data-ttu-id="a6e47-108">Konstanten</span><span class="sxs-lookup"><span data-stu-id="a6e47-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="a6e47-109"><span id="D3DRS_ZENABLE"></span><span id="d3drs_zenable"></span>**D3DRS \_ zenable**</span><span class="sxs-lookup"><span data-stu-id="a6e47-109"><span id="D3DRS_ZENABLE"></span><span id="d3drs_zenable"></span>**D3DRS\_ZENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="a6e47-110">Der tiefen Puffer Zustand als ein Member des [**D3DZBUFFERTYPE**](./d3dzbuffertype.md) -enumerierten Typs.</span><span class="sxs-lookup"><span data-stu-id="a6e47-110">Depth-buffering state as one member of the [**D3DZBUFFERTYPE**](./d3dzbuffertype.md) enumerated type.</span></span> <span data-ttu-id="a6e47-111">Legen Sie diesen Status auf D3DZB true fest, \_ um z-Pufferung zu aktivieren, D3DZB \_ usew, um w-buffereing zu aktivieren, oder D3DZB \_ false, um die tiefen Pufferung zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="a6e47-111">Set this state to D3DZB\_TRUE to enable z-buffering, D3DZB\_USEW to enable w-buffering, or D3DZB\_FALSE to disable depth buffering.</span></span>

<span data-ttu-id="a6e47-112">Der Standardwert für diesen renderzustand ist D3DZB \_ true, wenn eine tiefen Schablone zusammen mit der SwapChain erstellt wurde, indem der enableautodepthstencil-Member der [**D3DPRESENT \_ Parameters**](d3dpresent-parameters.md) -Struktur auf **true** festgelegt wurde, \_ andernfalls D3DZB false.</span><span class="sxs-lookup"><span data-stu-id="a6e47-112">The default value for this render state is D3DZB\_TRUE if a depth stencil was created along with the swap chain by setting the EnableAutoDepthStencil member of the [**D3DPRESENT\_PARAMETERS**](d3dpresent-parameters.md) structure to **TRUE**, and D3DZB\_FALSE otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="a6e47-113"><span id="D3DRS_FILLMODE"></span><span id="d3drs_fillmode"></span>**D3DRS \_ FillMode**</span><span class="sxs-lookup"><span data-stu-id="a6e47-113"><span id="D3DRS_FILLMODE"></span><span id="d3drs_fillmode"></span>**D3DRS\_FILLMODE**</span></span>
</dt> <dd>

<span data-ttu-id="a6e47-114">Mindestens ein Member des [**D3DFILLMODE**](./d3dfillmode.md) -Enumerationstyps.</span><span class="sxs-lookup"><span data-stu-id="a6e47-114">One or more members of the [**D3DFILLMODE**](./d3dfillmode.md) enumerated type.</span></span> <span data-ttu-id="a6e47-115">Der Standardwert ist D3DFILL \_ Solid.</span><span class="sxs-lookup"><span data-stu-id="a6e47-115">The default value is D3DFILL\_SOLID.</span></span>

</dd> <dt>

<span data-ttu-id="a6e47-116"><span id="D3DRS_SHADEMODE"></span><span id="d3drs_shademode"></span>**D3DRS \_ SHADEMODE**</span><span class="sxs-lookup"><span data-stu-id="a6e47-116"><span id="D3DRS_SHADEMODE"></span><span id="d3drs_shademode"></span>**D3DRS\_SHADEMODE**</span></span>
</dt> <dd>

<span data-ttu-id="a6e47-117">Mindestens ein Member des [**D3DSHADEMODE**](./d3dshademode.md) -Enumerationstyps.</span><span class="sxs-lookup"><span data-stu-id="a6e47-117">One or more members of the [**D3DSHADEMODE**](./d3dshademode.md) enumerated type.</span></span> <span data-ttu-id="a6e47-118">Der Standardwert ist D3DSHADE \_ Gouraud.</span><span class="sxs-lookup"><span data-stu-id="a6e47-118">The default value is D3DSHADE\_GOURAUD.</span></span>

</dd> <dt>

<span data-ttu-id="a6e47-119"><span id="D3DRS_ZWRITEENABLE"></span><span id="d3drs_zwriteenable"></span>**D3DRS \_ zbeschreib teenable**</span><span class="sxs-lookup"><span data-stu-id="a6e47-119"><span id="D3DRS_ZWRITEENABLE"></span><span id="d3drs_zwriteenable"></span>**D3DRS\_ZWRITEENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="a6e47-120">**True** , wenn die Anwendung in den tiefen Puffer schreiben soll.</span><span class="sxs-lookup"><span data-stu-id="a6e47-120">**TRUE** to enable the application to write to the depth buffer.</span></span> <span data-ttu-id="a6e47-121">Der Standardwert ist " **true**".</span><span class="sxs-lookup"><span data-stu-id="a6e47-121">The default value is **TRUE**.</span></span> <span data-ttu-id="a6e47-122">Mit diesem Member kann eine Anwendung verhindern, dass das System den tiefen Puffer mit neuen tiefen Werten aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="a6e47-122">This member enables an application to prevent the system from updating the depth buffer with new depth values.</span></span> <span data-ttu-id="a6e47-123">**False** gibt an, dass tiefe Vergleiche weiterhin gemäß dem \_ renderzustand D3DRS zfunc erfolgen, vorausgesetzt, dass die tiefen Pufferung stattfindet, aber keine tiefen Werte in den Puffer geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="a6e47-123">If **FALSE**, depth comparisons are still made according to the render state D3DRS\_ZFUNC, assuming that depth buffering is taking place, but depth values are not written to the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="a6e47-124"><span id="D3DRS_ALPHATESTENABLE"></span><span id="d3drs_alphatestenable"></span>**D3DRS \_ Alpha atestenable**</span><span class="sxs-lookup"><span data-stu-id="a6e47-124"><span id="D3DRS_ALPHATESTENABLE"></span><span id="d3drs_alphatestenable"></span>**D3DRS\_ALPHATESTENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="a6e47-125">**True** , um pro Pixel-Alpha Tests zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="a6e47-125">**TRUE** to enable per pixel alpha testing.</span></span> <span data-ttu-id="a6e47-126">Wenn der Test durchlaufen wird, wird das Pixel vom Frame Puffer verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="a6e47-126">If the test passes, the pixel is processed by the frame buffer.</span></span> <span data-ttu-id="a6e47-127">Andernfalls wird die gesamte Verarbeitung des Frame Puffers für das Pixel übersprungen.</span><span class="sxs-lookup"><span data-stu-id="a6e47-127">Otherwise, all frame-buffer processing is skipped for the pixel.</span></span>

<span data-ttu-id="a6e47-128">Der Test wird durchgeführt, indem der eingehende Alpha-Wert mit dem Reference-Alpha-Wert verglichen wird, wobei die Vergleichsfunktion des D3DRS \_ alphafunc-gerengerstatus verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a6e47-128">The test is done by comparing the incoming alpha value with the reference alpha value, using the comparison function provided by the D3DRS\_ALPHAFUNC render state.</span></span> <span data-ttu-id="a6e47-129">Der Reference Alpha-Wert wird durch den Wert bestimmt, der für D3DRS \_ Alpha Aref festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="a6e47-129">The reference alpha value is determined by the value set for D3DRS\_ALPHAREF.</span></span> <span data-ttu-id="a6e47-130">Weitere Informationen finden Sie unter [Status des Alpha Tests (Direct3D 9)](alpha-testing-state.md).</span><span class="sxs-lookup"><span data-stu-id="a6e47-130">For more information, see [Alpha Testing State (Direct3D 9)](alpha-testing-state.md).</span></span>

<span data-ttu-id="a6e47-131">Der Standardwert dieses Parameters ist **false**.</span><span class="sxs-lookup"><span data-stu-id="a6e47-131">The default value of this parameter is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="a6e47-132"><span id="D3DRS_LASTPIXEL"></span><span id="d3drs_lastpixel"></span>**D3DRS \_ lastpixel**</span><span class="sxs-lookup"><span data-stu-id="a6e47-132"><span id="D3DRS_LASTPIXEL"></span><span id="d3drs_lastpixel"></span>**D3DRS\_LASTPIXEL**</span></span>
</dt> <dd>

<span data-ttu-id="a6e47-133">Der Standardwert ist **true**, wodurch das Zeichnen des letzten Pixels in einer Zeile ermöglicht wird.</span><span class="sxs-lookup"><span data-stu-id="a6e47-133">The default value is **TRUE**, which enables drawing of the last pixel in a line.</span></span> <span data-ttu-id="a6e47-134">Legen Sie diesen Wert auf **false** fest, um das Zeichnen des letzten Pixels zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="a6e47-134">To prevent drawing of the last pixel, set this value to **FALSE**.</span></span> <span data-ttu-id="a6e47-135">Weitere Informationen finden Sie Untergliederung [und Füll Zustand (Direct3D 9)](outline-and-fill-state.md).</span><span class="sxs-lookup"><span data-stu-id="a6e47-135">For more information, see [Outline and Fill State (Direct3D 9)](outline-and-fill-state.md).</span></span>

</dd> <dt>

<span data-ttu-id="a6e47-136"><span id="D3DRS_SRCBLEND"></span><span id="d3drs_srcblend"></span>**D3DRS \_ srcblend**</span><span class="sxs-lookup"><span data-stu-id="a6e47-136"><span id="D3DRS_SRCBLEND"></span><span id="d3drs_srcblend"></span>**D3DRS\_SRCBLEND**</span></span>
</dt> <dd>

<span data-ttu-id="a6e47-137">Ein Member des [**D3DBLEND**](./d3dblend.md) -Enumerationstyps.</span><span class="sxs-lookup"><span data-stu-id="a6e47-137">One member of the [**D3DBLEND**](./d3dblend.md) enumerated type.</span></span> <span data-ttu-id="a6e47-138">Der Standardwert ist D3DBLEND \_ 1.</span><span class="sxs-lookup"><span data-stu-id="a6e47-138">The default value is D3DBLEND\_ONE.</span></span>

</dd> <dt>

<span data-ttu-id="a6e47-139"><span id="D3DRS_DESTBLEND"></span><span id="d3drs_destblend"></span>**D3DRS \_ destblend**</span><span class="sxs-lookup"><span data-stu-id="a6e47-139"><span id="D3DRS_DESTBLEND"></span><span id="d3drs_destblend"></span>**D3DRS\_DESTBLEND**</span></span>
</dt> <dd>

<span data-ttu-id="a6e47-140">Ein Member des [**D3DBLEND**](./d3dblend.md) -Enumerationstyps.</span><span class="sxs-lookup"><span data-stu-id="a6e47-140">One member of the [**D3DBLEND**](./d3dblend.md) enumerated type.</span></span> <span data-ttu-id="a6e47-141">Der Standardwert ist D3DBLEND \_ 0 (null).</span><span class="sxs-lookup"><span data-stu-id="a6e47-141">The default value is D3DBLEND\_ZERO.</span></span>

</dd> <dt>

<span data-ttu-id="a6e47-142"><span id="D3DRS_CULLMODE"></span><span id="d3drs_cullmode"></span>**D3DRS \_ CullMode**</span><span class="sxs-lookup"><span data-stu-id="a6e47-142"><span id="D3DRS_CULLMODE"></span><span id="d3drs_cullmode"></span>**D3DRS\_CULLMODE**</span></span>
</dt> <dd>

<span data-ttu-id="a6e47-143">Gibt an, wie rückwärts gerichtete Dreiecke durchgeführt werden, wenn überhaupt.</span><span class="sxs-lookup"><span data-stu-id="a6e47-143">Specifies how back-facing triangles are culled, if at all.</span></span> <span data-ttu-id="a6e47-144">Dies kann auf einen Member des [**D3DCULL**](./d3dcull.md) -enumerierten Typs festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="a6e47-144">This can be set to one member of the [**D3DCULL**](./d3dcull.md) enumerated type.</span></span> <span data-ttu-id="a6e47-145">Der Standardwert ist D3DCULL \_ CCW.</span><span class="sxs-lookup"><span data-stu-id="a6e47-145">The default value is D3DCULL\_CCW.</span></span>

</dd> <dt>

<span data-ttu-id="a6e47-146"><span id="D3DRS_ZFUNC"></span><span id="d3drs_zfunc"></span>**D3DRS \_ zfunc**</span><span class="sxs-lookup"><span data-stu-id="a6e47-146"><span id="D3DRS_ZFUNC"></span><span id="d3drs_zfunc"></span>**D3DRS\_ZFUNC**</span></span>
</dt> <dd>

<span data-ttu-id="a6e47-147">Ein Member des [**D3DCMPFUNC**](./d3dcmpfunc.md) -Enumerationstyps.</span><span class="sxs-lookup"><span data-stu-id="a6e47-147">One member of the [**D3DCMPFUNC**](./d3dcmpfunc.md) enumerated type.</span></span> <span data-ttu-id="a6e47-148">Der Standardwert ist D3DCMP \_ lessequal.</span><span class="sxs-lookup"><span data-stu-id="a6e47-148">The default value is D3DCMP\_LESSEQUAL.</span></span> <span data-ttu-id="a6e47-149">Dieser Member ermöglicht es einer Anwendung, ein Pixel basierend auf der Entfernung von der Kamera zu akzeptieren oder abzulehnen.</span><span class="sxs-lookup"><span data-stu-id="a6e47-149">This member enables an application to accept or reject a pixel, based on its distance from the camera.</span></span>

<span data-ttu-id="a6e47-150">Der tiefen Wert des Pixels wird mit dem tiefen Puffer Wert verglichen.</span><span class="sxs-lookup"><span data-stu-id="a6e47-150">The depth value of the pixel is compared with the depth-buffer value.</span></span> <span data-ttu-id="a6e47-151">Wenn der tiefen Wert des Pixels die Vergleichsfunktion übergibt, wird das Pixel geschrieben.</span><span class="sxs-lookup"><span data-stu-id="a6e47-151">If the depth value of the pixel passes the comparison function, the pixel is written.</span></span>

<span data-ttu-id="a6e47-152">Der tiefen Wert wird nur in den tiefen Puffer geschrieben, wenn der renderzustand " **true**" ist.</span><span class="sxs-lookup"><span data-stu-id="a6e47-152">The depth value is written to the depth buffer only if the render state is **TRUE**.</span></span>

<span data-ttu-id="a6e47-153">Software Rasterizer und viele Hardware Accelerators arbeiten schneller, wenn der tiefen Test fehlschlägt, da die Textur nicht gefiltert und modulieren werden muss, wenn das Pixel nicht gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="a6e47-153">Software rasterizers and many hardware accelerators work faster if the depth test fails, because there is no need to filter and modulate the texture if the pixel is not going to be rendered.</span></span>

</dd> <dt>

<span data-ttu-id="a6e47-154"><span id="D3DRS_ALPHAREF"></span><span id="d3drs_alpharef"></span>**D3DRS \_ Alpha Aref**</span><span class="sxs-lookup"><span data-stu-id="a6e47-154"><span id="D3DRS_ALPHAREF"></span><span id="d3drs_alpharef"></span>**D3DRS\_ALPHAREF**</span></span>
</dt> <dd>

<span data-ttu-id="a6e47-155">Ein Wert, der einen Alpha-Verweiswert angibt, mit dem Pixel getestet werden, wenn Alpha Tests aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="a6e47-155">Value that specifies a reference alpha value against which pixels are tested when alpha testing is enabled.</span></span> <span data-ttu-id="a6e47-156">Dabei handelt es sich um einen 8-Bit-Wert, der in die unteren 8 Bits des DWORD-Rendering-State-Werts eingefügt wird.</span><span class="sxs-lookup"><span data-stu-id="a6e47-156">This is an 8-bit value placed in the low 8 bits of the DWORD render-state value.</span></span> <span data-ttu-id="a6e47-157">Die Werte liegen im Bereich von 0x00000000 bis 0x000000ff.</span><span class="sxs-lookup"><span data-stu-id="a6e47-157">Values can range from 0x00000000 through 0x000000FF.</span></span> <span data-ttu-id="a6e47-158">Der Standardwert ist 0.</span><span class="sxs-lookup"><span data-stu-id="a6e47-158">The default value is 0.</span></span>

</dd> <dt>

<span data-ttu-id="a6e47-159"><span id="D3DRS_ALPHAFUNC"></span><span id="d3drs_alphafunc"></span>**D3DRS \_ alphafunc**</span><span class="sxs-lookup"><span data-stu-id="a6e47-159"><span id="D3DRS_ALPHAFUNC"></span><span id="d3drs_alphafunc"></span>**D3DRS\_ALPHAFUNC**</span></span>
</dt> <dd>

<span data-ttu-id="a6e47-160">Ein Member des [**D3DCMPFUNC**](./d3dcmpfunc.md) -Enumerationstyps.</span><span class="sxs-lookup"><span data-stu-id="a6e47-160">One member of the [**D3DCMPFUNC**](./d3dcmpfunc.md) enumerated type.</span></span> <span data-ttu-id="a6e47-161">Der Standardwert ist D3DCMP \_ Always.</span><span class="sxs-lookup"><span data-stu-id="a6e47-161">The default value is D3DCMP\_ALWAYS.</span></span> <span data-ttu-id="a6e47-162">Dieser Member ermöglicht es einer Anwendung, ein Pixel auf der Grundlage des Alphawerts zu akzeptieren oder abzulehnen.</span><span class="sxs-lookup"><span data-stu-id="a6e47-162">This member enables an application to accept or reject a pixel, based on its alpha value.</span></span>

</dd> <dt>

<span data-ttu-id="a6e47-163"><span id="D3DRS_DITHERENABLE"></span><span id="d3drs_ditherenable"></span>**D3DRS \_ ditherenable**</span><span class="sxs-lookup"><span data-stu-id="a6e47-163"><span id="D3DRS_DITHERENABLE"></span><span id="d3drs_ditherenable"></span>**D3DRS\_DITHERENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="a6e47-164">**True** , um Dithering zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="a6e47-164">**TRUE** to enable dithering.</span></span> <span data-ttu-id="a6e47-165">Der Standardwert ist **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="a6e47-165">The default value is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="a6e47-166"><span id="D3DRS_ALPHABLENDENABLE"></span><span id="d3drs_alphablendenable"></span>**D3DRS \_ AlphaBlendEnable**</span><span class="sxs-lookup"><span data-stu-id="a6e47-166"><span id="D3DRS_ALPHABLENDENABLE"></span><span id="d3drs_alphablendenable"></span>**D3DRS\_ALPHABLENDENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="a6e47-167">" **True** ", um eine Alpha Gemischte Transparenz zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="a6e47-167">**TRUE** to enable alpha-blended transparency.</span></span> <span data-ttu-id="a6e47-168">Der Standardwert ist **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="a6e47-168">The default value is **FALSE**.</span></span>

<span data-ttu-id="a6e47-169">Der Typ der Alpha Mischung wird durch die D3DRS \_ srcblend-und D3DRS \_ destblend-Rendering-Zustände bestimmt.</span><span class="sxs-lookup"><span data-stu-id="a6e47-169">The type of alpha blending is determined by the D3DRS\_SRCBLEND and D3DRS\_DESTBLEND render states.</span></span>

</dd> <dt>

<span data-ttu-id="a6e47-170"><span id="D3DRS_FOGENABLE"></span><span id="d3drs_fogenable"></span>**D3DRS \_ fogenable**</span><span class="sxs-lookup"><span data-stu-id="a6e47-170"><span id="D3DRS_FOGENABLE"></span><span id="d3drs_fogenable"></span>**D3DRS\_FOGENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="a6e47-171">**True** , um eine Nebel Mischung zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="a6e47-171">**TRUE** to enable fog blending.</span></span> <span data-ttu-id="a6e47-172">Der Standardwert ist **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="a6e47-172">The default value is **FALSE**.</span></span> <span data-ttu-id="a6e47-173">Weitere Informationen zur Verwendung der Nebel Mischung finden Sie unter [Nebel](fog.md).</span><span class="sxs-lookup"><span data-stu-id="a6e47-173">For more information about using fog blending, see [Fog](fog.md).</span></span>

</dd> <dt>

<span data-ttu-id="a6e47-174"><span id="D3DRS_SPECULARENABLE"></span><span id="d3drs_specularenable"></span>**D3DRS \_ specularenable**</span><span class="sxs-lookup"><span data-stu-id="a6e47-174"><span id="D3DRS_SPECULARENABLE"></span><span id="d3drs_specularenable"></span>**D3DRS\_SPECULARENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="a6e47-175">**True** , um Glanzlichter zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="a6e47-175">**TRUE** to enable specular highlights.</span></span> <span data-ttu-id="a6e47-176">Der Standardwert ist **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="a6e47-176">The default value is **FALSE**.</span></span>

<span data-ttu-id="a6e47-177">Glanzlichter werden berechnet, als wäre jeder Scheitelpunkt in dem Objekt, das beleuchtet wird, am Ursprung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="a6e47-177">Specular highlights are calculated as though every vertex in the object being lit is at the object's origin.</span></span> <span data-ttu-id="a6e47-178">Dadurch werden die erwarteten Ergebnisse generiert, solange das Objekt um den Ursprung modelliert wird und der Abstand vom Licht zum Objekt relativ groß ist.</span><span class="sxs-lookup"><span data-stu-id="a6e47-178">This gives the expected results as long as the object is modeled around the origin and the distance from the light to the object is relatively large.</span></span> <span data-ttu-id="a6e47-179">In anderen Fällen sind die Ergebnisse als nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="a6e47-179">In other cases, the results as undefined.</span></span>

<span data-ttu-id="a6e47-180">Wenn dieser Member auf **true** festgelegt ist, wird die Glanz Farbe der Basis Farbe nach der Textur kaskadierenden, aber vor dem Alpha Blending hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a6e47-180">When this member is set to **TRUE**, the specular color is added to the base color after the texture cascade but before alpha blending.</span></span>

</dd> <dt>

<span data-ttu-id="a6e47-181"><span id="D3DRS_FOGCOLOR"></span><span id="d3drs_fogcolor"></span>**D3DRS \_ fogcolor**</span><span class="sxs-lookup"><span data-stu-id="a6e47-181"><span id="D3DRS_FOGCOLOR"></span><span id="d3drs_fogcolor"></span>**D3DRS\_FOGCOLOR**</span></span>
</dt> <dd>

<span data-ttu-id="a6e47-182">Der Wert, dessen Typ " [**D3DCOLOR**](d3dcolor.md)" ist.</span><span class="sxs-lookup"><span data-stu-id="a6e47-182">Value whose type is [**D3DCOLOR**](d3dcolor.md).</span></span> <span data-ttu-id="a6e47-183">Der Standardwert ist 0.</span><span class="sxs-lookup"><span data-stu-id="a6e47-183">The default value is 0.</span></span> <span data-ttu-id="a6e47-184">Weitere Informationen zur Nebelfarbe finden Sie unter [Nebelfarbe (Direct3D 9)](fog-color.md).</span><span class="sxs-lookup"><span data-stu-id="a6e47-184">For more information about fog color, see [Fog Color (Direct3D 9)](fog-color.md).</span></span>

</dd> <dt>

<span data-ttu-id="a6e47-185"><span id="D3DRS_FOGTABLEMODE"></span><span id="d3drs_fogtablemode"></span>**D3DRS \_ fogtablemode**</span><span class="sxs-lookup"><span data-stu-id="a6e47-185"><span id="D3DRS_FOGTABLEMODE"></span><span id="d3drs_fogtablemode"></span>**D3DRS\_FOGTABLEMODE**</span></span>
</dt> <dd>

<span data-ttu-id="a6e47-186">Die für den Pixel Nebel zu verwendende Nebelformel.</span><span class="sxs-lookup"><span data-stu-id="a6e47-186">The fog formula to be used for pixel fog.</span></span> <span data-ttu-id="a6e47-187">Legen Sie auf einen der Member des [**D3DFOGMODE**](./d3dfogmode.md) -Enumerationstyps fest.</span><span class="sxs-lookup"><span data-stu-id="a6e47-187">Set to one of the members of the [**D3DFOGMODE**](./d3dfogmode.md) enumerated type.</span></span> <span data-ttu-id="a6e47-188">Der Standardwert ist D3DFOG \_ None.</span><span class="sxs-lookup"><span data-stu-id="a6e47-188">The default value is D3DFOG\_NONE.</span></span> <span data-ttu-id="a6e47-189">Weitere Informationen zu Pixel Nebel finden Sie unter [Pixel Nebel (Direct3D 9)](pixel-fog.md).</span><span class="sxs-lookup"><span data-stu-id="a6e47-189">For more information about pixel fog, see [Pixel Fog (Direct3D 9)](pixel-fog.md).</span></span>

</dd> <dt>

<span data-ttu-id="a6e47-190"><span id="D3DRS_FOGSTART"></span><span id="d3drs_fogstart"></span>**D3DRS \_ fogstart**</span><span class="sxs-lookup"><span data-stu-id="a6e47-190"><span id="D3DRS_FOGSTART"></span><span id="d3drs_fogstart"></span>**D3DRS\_FOGSTART**</span></span>
</dt> <dd>

<span data-ttu-id="a6e47-191">Die Tiefe, bei der Pixel-oder Scheitelpunkt Effekte für den linearen Nebel Modus beginnen.</span><span class="sxs-lookup"><span data-stu-id="a6e47-191">Depth at which pixel or vertex fog effects begin for linear fog mode.</span></span> <span data-ttu-id="a6e47-192">Der Standardwert ist 0,0 f.</span><span class="sxs-lookup"><span data-stu-id="a6e47-192">The default value is 0.0f.</span></span> <span data-ttu-id="a6e47-193">Die Tiefe wird im Welt Raum für den Scheitelpunkt Nebel und entweder den Geräteraum \[ 0,0, 1,0 \] oder den Raum für den Pixel Nebel angegeben.</span><span class="sxs-lookup"><span data-stu-id="a6e47-193">Depth is specified in world space for vertex fog and either device space \[0.0, 1.0\] or world space for pixel fog.</span></span> <span data-ttu-id="a6e47-194">Bei Pixel Nebel befinden sich diese Werte im Geräteraum, wenn das System z für Nebel Berechnungen und weltweiten Raum verwendet, wenn das System den Augen relativen Nebel (w-Fog) verwendet.</span><span class="sxs-lookup"><span data-stu-id="a6e47-194">For pixel fog, these values are in device space when the system uses z for fog calculations and world-world space when the system is using eye-relative fog (w-fog).</span></span> <span data-ttu-id="a6e47-195">Weitere Informationen finden Sie unter [Nebel Parameter (Direct3D 9)](fog-parameters.md) und [Eye-relative im Vergleich zu Z-basierter Tiefe](pixel-fog.md).</span><span class="sxs-lookup"><span data-stu-id="a6e47-195">For more information, see [Fog Parameters (Direct3D 9)](fog-parameters.md) and [Eye-Relative vs. Z-based Depth](pixel-fog.md).</span></span>

<span data-ttu-id="a6e47-196">Werte für diesen Rendering-Zustand sind Gleit Komma Werte.</span><span class="sxs-lookup"><span data-stu-id="a6e47-196">Values for this render state are floating-point values.</span></span> <span data-ttu-id="a6e47-197">Da die [**IDirect3DDevice9:: setrenderstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) -Methode DWORD-Werte akzeptiert, muss Ihre Anwendung eine Variable umwandeln, die den Wert enthält, wie im folgenden Codebeispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="a6e47-197">Because the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method accepts DWORD values, your application must cast a variable that contains the value, as shown in the following code example.</span></span>


```
pDevice9->SetRenderState(D3DRS_FOGSTART, 
                         *((DWORD*) (&fFogStart)));
```



</dd> <dt>

<span data-ttu-id="a6e47-198"><span id="D3DRS_FOGEND"></span><span id="d3drs_fogend"></span>**D3DRS \_ fogend**</span><span class="sxs-lookup"><span data-stu-id="a6e47-198"><span id="D3DRS_FOGEND"></span><span id="d3drs_fogend"></span>**D3DRS\_FOGEND**</span></span>
</dt> <dd>

<span data-ttu-id="a6e47-199">Die Tiefe, bei der Pixel-oder Scheitelpunkt Effekte für den linearen Nebel Modus enden.</span><span class="sxs-lookup"><span data-stu-id="a6e47-199">Depth at which pixel or vertex fog effects end for linear fog mode.</span></span> <span data-ttu-id="a6e47-200">Der Standardwert ist 1.0 f.</span><span class="sxs-lookup"><span data-stu-id="a6e47-200">The default value is 1.0f.</span></span> <span data-ttu-id="a6e47-201">Die Tiefe wird im Welt Raum für den Scheitelpunkt Nebel und entweder den Geräteraum \[ 0,0, 1,0 \] oder den Raum für den Pixel Nebel angegeben.</span><span class="sxs-lookup"><span data-stu-id="a6e47-201">Depth is specified in world space for vertex fog and either device space \[0.0, 1.0\] or world space for pixel fog.</span></span> <span data-ttu-id="a6e47-202">Bei Pixel Nebel befinden sich diese Werte im Geräteraum, wenn das System z für Nebel Berechnungen und in Welt Raum verwendet, wenn das System den Augen relativen Nebel (w-Fog) verwendet.</span><span class="sxs-lookup"><span data-stu-id="a6e47-202">For pixel fog, these values are in device space when the system uses z for fog calculations and in world space when the system is using eye-relative fog (w-fog).</span></span> <span data-ttu-id="a6e47-203">Weitere Informationen finden Sie unter [Nebel Parameter (Direct3D 9)](fog-parameters.md) und [Eye-relative im Vergleich zu Z-basierter Tiefe](pixel-fog.md).</span><span class="sxs-lookup"><span data-stu-id="a6e47-203">For more information, see [Fog Parameters (Direct3D 9)](fog-parameters.md) and [Eye-Relative vs. Z-based Depth](pixel-fog.md).</span></span>

<span data-ttu-id="a6e47-204">Werte für diesen Rendering-Zustand sind Gleit Komma Werte.</span><span class="sxs-lookup"><span data-stu-id="a6e47-204">Values for this render state are floating-point values.</span></span> <span data-ttu-id="a6e47-205">Da die [**IDirect3DDevice9:: setrenderstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) -Methode DWORD-Werte akzeptiert, muss Ihre Anwendung eine Variable umwandeln, die den Wert enthält, wie im folgenden Codebeispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="a6e47-205">Because the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method accepts DWORD values, your application must cast a variable that contains the value, as shown in the following code example.</span></span>


```
m_pDevice9->SetRenderState(D3DRS_FOGEND, *((DWORD*) (&fFogEnd)));
```



</dd> <dt>

<span data-ttu-id="a6e47-206"><span id="D3DRS_FOGDENSITY"></span><span id="d3drs_fogdensity"></span>**D3DRS- \_ fogdensity**</span><span class="sxs-lookup"><span data-stu-id="a6e47-206"><span id="D3DRS_FOGDENSITY"></span><span id="d3drs_fogdensity"></span>**D3DRS\_FOGDENSITY**</span></span>
</dt> <dd>

<span data-ttu-id="a6e47-207">In den exponentialnebelmodi (D3DFOG \_ exp und D3DFOG exp2) verwendete Nebeldichte für Pixel-oder Vertexnebel \_ .</span><span class="sxs-lookup"><span data-stu-id="a6e47-207">Fog density for pixel or vertex fog used in the exponential fog modes (D3DFOG\_EXP and D3DFOG\_EXP2).</span></span> <span data-ttu-id="a6e47-208">Gültige Dichte Werte liegen zwischen 0,0 und 1,0.</span><span class="sxs-lookup"><span data-stu-id="a6e47-208">Valid density values range from 0.0 through 1.0.</span></span> <span data-ttu-id="a6e47-209">Der Standardwert ist 1,0.</span><span class="sxs-lookup"><span data-stu-id="a6e47-209">The default value is 1.0.</span></span> <span data-ttu-id="a6e47-210">Weitere Informationen finden Sie unter " [Fog Parameters" (Direct3D 9)](fog-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="a6e47-210">For more information, see [Fog Parameters (Direct3D 9)](fog-parameters.md).</span></span>

<span data-ttu-id="a6e47-211">Werte für diesen Rendering-Zustand sind Gleit Komma Werte.</span><span class="sxs-lookup"><span data-stu-id="a6e47-211">Values for this render state are floating-point values.</span></span> <span data-ttu-id="a6e47-212">Da die [**IDirect3DDevice9:: setrenderstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) -Methode DWORD-Werte akzeptiert, muss Ihre Anwendung eine Variable umwandeln, die den Wert enthält, wie im folgenden Codebeispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="a6e47-212">Because the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method accepts DWORD values, your application must cast a variable that contains the value, as shown in the following code example.</span></span>


```
    m_pDevice9->SetRenderState(D3DRS_FOGDENSITY, *((DWORD*) (&fFogDensity)));
```



</dd> <dt>

<span data-ttu-id="a6e47-213"><span id="D3DRS_RANGEFOGENABLE"></span><span id="d3drs_rangefogenable"></span>**D3DRS \_ RANGEFOGENABLE**</span><span class="sxs-lookup"><span data-stu-id="a6e47-213"><span id="D3DRS_RANGEFOGENABLE"></span><span id="d3drs_rangefogenable"></span>**D3DRS\_RANGEFOGENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="a6e47-214">**True** , um Bereichs basierten Scheitelpunkt Nebel zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="a6e47-214">**TRUE** to enable range-based vertex fog.</span></span> <span data-ttu-id="a6e47-215">Der Standardwert ist **false**. in diesem Fall verwendet das System tiefen basierten Nebel.</span><span class="sxs-lookup"><span data-stu-id="a6e47-215">The default value is **FALSE**, in which case the system uses depth-based fog.</span></span> <span data-ttu-id="a6e47-216">Im Bereichs basierten Nebel wird der Abstand eines Objekts vom Viewer zum Berechnen von Nebeleffekten verwendet, nicht die Tiefe des Objekts (d. h. die z-Koordinate) in der Szene.</span><span class="sxs-lookup"><span data-stu-id="a6e47-216">In range-based fog, the distance of an object from the viewer is used to compute fog effects, not the depth of the object (that is, the z-coordinate) in the scene.</span></span> <span data-ttu-id="a6e47-217">Im Bereichs basierten Nebel funktionieren alle Nebel Methoden wie üblich, mit dem Unterschied, dass Sie in den Berechnungen den Bereich anstelle von Tiefe verwenden.</span><span class="sxs-lookup"><span data-stu-id="a6e47-217">In range-based fog, all fog methods work as usual, except that they use range instead of depth in the computations.</span></span>

<span data-ttu-id="a6e47-218">Range ist der richtige Faktor für die Berechnung von Nebel Berechnungen, aber die Tiefe wird häufig verwendet, da Range zeitaufwändig ist, und Tiefe ist im allgemeinen bereits verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a6e47-218">Range is the correct factor to use for fog computations, but depth is commonly used instead because range is time-consuming to compute and depth is generally already available.</span></span> <span data-ttu-id="a6e47-219">Die Verwendung der Tiefe zur Berechnung von Nebel hat den unerwünschten Effekt, dass sich das fogginess von peripheren Objekten ändert, wenn der Viewer das Auge bewegt. in diesem Fall werden die tiefen Änderungen und der Bereich konstant bleiben.</span><span class="sxs-lookup"><span data-stu-id="a6e47-219">Using depth to calculate fog has the undesirable effect of having the fogginess of peripheral objects change as the viewer's eye moves - in this case, the depth changes and the range remains constant.</span></span>

<span data-ttu-id="a6e47-220">Da derzeit keine Hardware den Bereichs basierten Nebel pro Pixel unterstützt, wird die Bereichs Korrektur nur für Scheitel Punkte angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a6e47-220">Because no hardware currently supports per-pixel range-based fog, range correction is offered only for vertex fog.</span></span>

<span data-ttu-id="a6e47-221">Weitere Informationen finden Sie unter [Scheitelpunkt Nebel (Direct3D 9)](vertex-fog.md).</span><span class="sxs-lookup"><span data-stu-id="a6e47-221">For more information, see [Vertex Fog (Direct3D 9)](vertex-fog.md).</span></span>

</dd> <dt>

<span data-ttu-id="a6e47-222"><span id="D3DRS_STENCILENABLE"></span><span id="d3drs_stencilenable"></span>**D3DRS \_ Schablone**</span><span class="sxs-lookup"><span data-stu-id="a6e47-222"><span id="D3DRS_STENCILENABLE"></span><span id="d3drs_stencilenable"></span>**D3DRS\_STENCILENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="a6e47-223">**True** zum Aktivieren der Schablone oder **false** zum Deaktivieren der Schablone.</span><span class="sxs-lookup"><span data-stu-id="a6e47-223">**TRUE** to enable stenciling, or **FALSE** to disable stenciling.</span></span> <span data-ttu-id="a6e47-224">Der Standardwert ist **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="a6e47-224">The default value is **FALSE**.</span></span> <span data-ttu-id="a6e47-225">Weitere Informationen finden Sie unter [Schablonen Puffer Techniken (Direct3D 9)](stencil-buffer-techniques.md).</span><span class="sxs-lookup"><span data-stu-id="a6e47-225">For more information, see [Stencil Buffer Techniques (Direct3D 9)](stencil-buffer-techniques.md).</span></span>

</dd> <dt>

<span data-ttu-id="a6e47-226"><span id="D3DRS_STENCILFAIL"></span><span id="d3drs_stencilfail"></span>**D3DRS \_ stencilfail**</span><span class="sxs-lookup"><span data-stu-id="a6e47-226"><span id="D3DRS_STENCILFAIL"></span><span id="d3drs_stencilfail"></span>**D3DRS\_STENCILFAIL**</span></span>
</dt> <dd>

<span data-ttu-id="a6e47-227">Der Schablonen Vorgang, der ausgeführt werden soll, wenn der Schablonen Test fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="a6e47-227">Stencil operation to perform if the stencil test fails.</span></span> <span data-ttu-id="a6e47-228">Werte stammen aus dem [**D3DSTENCILOP**](./d3dstencilop.md) -Enumerationstyp.</span><span class="sxs-lookup"><span data-stu-id="a6e47-228">Values are from the [**D3DSTENCILOP**](./d3dstencilop.md) enumerated type.</span></span> <span data-ttu-id="a6e47-229">Der Standardwert ist D3DSTENCILOP \_ Keep.</span><span class="sxs-lookup"><span data-stu-id="a6e47-229">The default value is D3DSTENCILOP\_KEEP.</span></span>

</dd> <dt>

<span data-ttu-id="a6e47-230"><span id="D3DRS_STENCILZFAIL"></span><span id="d3drs_stencilzfail"></span>**D3DRS \_ stencilzfail**</span><span class="sxs-lookup"><span data-stu-id="a6e47-230"><span id="D3DRS_STENCILZFAIL"></span><span id="d3drs_stencilzfail"></span>**D3DRS\_STENCILZFAIL**</span></span>
</dt> <dd>

<span data-ttu-id="a6e47-231">Der Schablonen Vorgang, der ausgeführt werden soll, wenn der Schablone-Test erfolgreich verläuft und der tiefen Test (z-Test) fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="a6e47-231">Stencil operation to perform if the stencil test passes and the depth test (z-test) fails.</span></span> <span data-ttu-id="a6e47-232">Werte stammen aus dem [**D3DSTENCILOP**](./d3dstencilop.md) -Enumerationstyp.</span><span class="sxs-lookup"><span data-stu-id="a6e47-232">Values are from the [**D3DSTENCILOP**](./d3dstencilop.md) enumerated type.</span></span> <span data-ttu-id="a6e47-233">Der Standardwert ist D3DSTENCILOP \_ Keep.</span><span class="sxs-lookup"><span data-stu-id="a6e47-233">The default value is D3DSTENCILOP\_KEEP.</span></span>

</dd> <dt>

<span data-ttu-id="a6e47-234"><span id="D3DRS_STENCILPASS"></span><span id="d3drs_stencilpass"></span>**D3DRS \_ stencilpass**</span><span class="sxs-lookup"><span data-stu-id="a6e47-234"><span id="D3DRS_STENCILPASS"></span><span id="d3drs_stencilpass"></span>**D3DRS\_STENCILPASS**</span></span>
</dt> <dd>

<span data-ttu-id="a6e47-235">Der Schablonen Vorgang, der ausgeführt werden soll, wenn sowohl die Schablone als auch die Tiefe (z)-Tests bestanden werden.</span><span class="sxs-lookup"><span data-stu-id="a6e47-235">Stencil operation to perform if both the stencil and the depth (z) tests pass.</span></span> <span data-ttu-id="a6e47-236">Werte stammen aus dem [**D3DSTENCILOP**](./d3dstencilop.md) -Enumerationstyp.</span><span class="sxs-lookup"><span data-stu-id="a6e47-236">Values are from the [**D3DSTENCILOP**](./d3dstencilop.md) enumerated type.</span></span> <span data-ttu-id="a6e47-237">Der Standardwert ist D3DSTENCILOP \_ Keep.</span><span class="sxs-lookup"><span data-stu-id="a6e47-237">The default value is D3DSTENCILOP\_KEEP.</span></span>

</dd> <dt>

<span data-ttu-id="a6e47-238"><span id="D3DRS_STENCILFUNC"></span><span id="d3drs_stencilfunc"></span>**D3DRS \_ stencilfunc**</span><span class="sxs-lookup"><span data-stu-id="a6e47-238"><span id="D3DRS_STENCILFUNC"></span><span id="d3drs_stencilfunc"></span>**D3DRS\_STENCILFUNC**</span></span>
</dt> <dd>

<span data-ttu-id="a6e47-239">Vergleichsfunktion für den Schablonen Test.</span><span class="sxs-lookup"><span data-stu-id="a6e47-239">Comparison function for the stencil test.</span></span> <span data-ttu-id="a6e47-240">Werte stammen aus dem [**D3DCMPFUNC**](./d3dcmpfunc.md) -Enumerationstyp.</span><span class="sxs-lookup"><span data-stu-id="a6e47-240">Values are from the [**D3DCMPFUNC**](./d3dcmpfunc.md) enumerated type.</span></span> <span data-ttu-id="a6e47-241">Der Standardwert ist D3DCMP \_ Always.</span><span class="sxs-lookup"><span data-stu-id="a6e47-241">The default value is D3DCMP\_ALWAYS.</span></span>

<span data-ttu-id="a6e47-242">Die Vergleichsfunktion wird verwendet, um den Verweis Wert mit einem Schablone-Puffer Eintrag zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="a6e47-242">The comparison function is used to compare the reference value to a stencil buffer entry.</span></span> <span data-ttu-id="a6e47-243">Dieser Vergleich gilt nur für die Bits im Verweis-und Schablonen Puffer Eintrag, die in der Schablonen Maske festgelegt sind (durch den D3DRS \_ stencilmask-Rendering festgelegt).</span><span class="sxs-lookup"><span data-stu-id="a6e47-243">This comparison applies only to the bits in the reference value and stencil buffer entry that are set in the stencil mask (set by the D3DRS\_STENCILMASK render state).</span></span> <span data-ttu-id="a6e47-244">**True** gibt an, dass der Schablone-Test durchlaufen wird.</span><span class="sxs-lookup"><span data-stu-id="a6e47-244">If **TRUE**, the stencil test passes.</span></span>

</dd> <dt>

<span data-ttu-id="a6e47-245"><span id="D3DRS_STENCILREF"></span><span id="d3drs_stencilref"></span>**D3DRS \_ stencilref**</span><span class="sxs-lookup"><span data-stu-id="a6e47-245"><span id="D3DRS_STENCILREF"></span><span id="d3drs_stencilref"></span>**D3DRS\_STENCILREF**</span></span>
</dt> <dd>

<span data-ttu-id="a6e47-246">Ein int-Verweis Wert für den Schablonen Test.</span><span class="sxs-lookup"><span data-stu-id="a6e47-246">An int reference value for the stencil test.</span></span> <span data-ttu-id="a6e47-247">Der Standardwert ist 0.</span><span class="sxs-lookup"><span data-stu-id="a6e47-247">The default value is 0.</span></span>

</dd> <dt>

<span data-ttu-id="a6e47-248"><span id="D3DRS_STENCILMASK"></span><span id="d3drs_stencilmask"></span>**D3DRS \_ stencilmask**</span><span class="sxs-lookup"><span data-stu-id="a6e47-248"><span id="D3DRS_STENCILMASK"></span><span id="d3drs_stencilmask"></span>**D3DRS\_STENCILMASK**</span></span>
</dt> <dd>

<span data-ttu-id="a6e47-249">Die auf den Verweis Wert angewendete Maske und die einzelnen Schablonen Puffer Einträge, um die signifikanten Bits für den Schablonen Test zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="a6e47-249">Mask applied to the reference value and each stencil buffer entry to determine the significant bits for the stencil test.</span></span> <span data-ttu-id="a6e47-250">Die Standard Maske ist 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="a6e47-250">The default mask is 0xFFFFFFFF.</span></span>

</dd> <dt>

<span data-ttu-id="a6e47-251"><span id="D3DRS_STENCILWRITEMASK"></span><span id="d3drs_stencilwritemask"></span>**D3DRS \_ stencilschreitefrage**</span><span class="sxs-lookup"><span data-stu-id="a6e47-251"><span id="D3DRS_STENCILWRITEMASK"></span><span id="d3drs_stencilwritemask"></span>**D3DRS\_STENCILWRITEMASK**</span></span>
</dt> <dd>

<span data-ttu-id="a6e47-252">Schreib Maske, die auf Werte angewendet wird, die in den Schablonen Puffer geschrieben wurden.</span><span class="sxs-lookup"><span data-stu-id="a6e47-252">Write mask applied to values written into the stencil buffer.</span></span> <span data-ttu-id="a6e47-253">Die Standard Maske ist 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="a6e47-253">The default mask is 0xFFFFFFFF.</span></span>

</dd> <dt>

<span data-ttu-id="a6e47-254"><span id="D3DRS_TEXTUREFACTOR"></span><span id="d3drs_texturefactor"></span>**D3DRS \_ TextureFactor**</span><span class="sxs-lookup"><span data-stu-id="a6e47-254"><span id="D3DRS_TEXTUREFACTOR"></span><span id="d3drs_texturefactor"></span>**D3DRS\_TEXTUREFACTOR**</span></span>
</dt> <dd>

<span data-ttu-id="a6e47-255">Die Farbe, die für die mehrfach Textur Mischung mit dem D3DTA \_ Tfactor-Textur Mischungs Argument oder dem D3DTOP \_ blendfactoralpha-Textur Mischungs Vorgang verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a6e47-255">Color used for multiple-texture blending with the D3DTA\_TFACTOR texture-blending argument or the D3DTOP\_BLENDFACTORALPHA texture-blending operation.</span></span> <span data-ttu-id="a6e47-256">Der zugeordnete Wert ist eine [**D3DCOLOR**](d3dcolor.md) -Variable.</span><span class="sxs-lookup"><span data-stu-id="a6e47-256">The associated value is a [**D3DCOLOR**](d3dcolor.md) variable.</span></span> <span data-ttu-id="a6e47-257">Der Standardwert ist undurchsichtig weiß (0xFFFFFFFF).</span><span class="sxs-lookup"><span data-stu-id="a6e47-257">The default value is opaque white (0xFFFFFFFF).</span></span>

</dd> <dt>

<span data-ttu-id="a6e47-258"><span id="D3DRS_WRAP0"></span><span id="d3drs_wrap0"></span>**D3DRS \_ WRAP0**</span><span class="sxs-lookup"><span data-stu-id="a6e47-258"><span id="D3DRS_WRAP0"></span><span id="d3drs_wrap0"></span>**D3DRS\_WRAP0**</span></span>
</dt> <dd>

<span data-ttu-id="a6e47-259">Textur Wrapping Verhalten für mehrere Sätze von Texturkoordinaten.</span><span class="sxs-lookup"><span data-stu-id="a6e47-259">Texture-wrapping behavior for multiple sets of texture coordinates.</span></span> <span data-ttu-id="a6e47-260">Gültige Werte für diesen Rendering-Zustand können eine beliebige Kombination aus den \_ Flags D3DWRAPCOORD 0 (oder D3DWRAP \_ U), D3DWRAPCOORD \_ 1 (oder D3DWRAP \_ V), D3DWRAPCOORD \_ 2 (oder D3DWRAP \_ W) und D3DWRAPCOORD \_ 3 sein.</span><span class="sxs-lookup"><span data-stu-id="a6e47-260">Valid values for this render state can be any combination of the D3DWRAPCOORD\_0 (or D3DWRAP\_U), D3DWRAPCOORD\_1 (or D3DWRAP\_V), D3DWRAPCOORD\_2 (or D3DWRAP\_W), and D3DWRAPCOORD\_3 flags.</span></span> <span data-ttu-id="a6e47-261">Diese bewirken, dass das System in der Richtung der ersten, zweiten, dritten und vierten Dimensionen (manchmal auch als s-, t-, r-und q-Richtung) für eine bestimmte Textur eingebunden wird.</span><span class="sxs-lookup"><span data-stu-id="a6e47-261">These cause the system to wrap in the direction of the first, second, third, and fourth dimensions, sometimes referred to as the s, t, r, and q directions, for a given texture.</span></span> <span data-ttu-id="a6e47-262">Der Standardwert für diesen Rendering-Zustand ist 0 (Wrapping in alle Richtungen deaktiviert).</span><span class="sxs-lookup"><span data-stu-id="a6e47-262">The default value for this render state is 0 (wrapping disabled in all directions).</span></span>

</dd> <dt>

<span data-ttu-id="a6e47-263"><span id="D3DRS_WRAP1"></span><span id="d3drs_wrap1"></span>**D3DRS \_ WRAP1**</span><span class="sxs-lookup"><span data-stu-id="a6e47-263"><span id="D3DRS_WRAP1"></span><span id="d3drs_wrap1"></span>**D3DRS\_WRAP1**</span></span>
</dt> <dd>

<span data-ttu-id="a6e47-264">Siehe D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="a6e47-264">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="a6e47-265"><span id="D3DRS_WRAP2"></span><span id="d3drs_wrap2"></span>**D3DRS \_ WRAP2**</span><span class="sxs-lookup"><span data-stu-id="a6e47-265"><span id="D3DRS_WRAP2"></span><span id="d3drs_wrap2"></span>**D3DRS\_WRAP2**</span></span>
</dt> <dd>

<span data-ttu-id="a6e47-266">Siehe D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="a6e47-266">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="a6e47-267"><span id="D3DRS_WRAP3"></span><span id="d3drs_wrap3"></span>**D3DRS \_ WRAP3**</span><span class="sxs-lookup"><span data-stu-id="a6e47-267"><span id="D3DRS_WRAP3"></span><span id="d3drs_wrap3"></span>**D3DRS\_WRAP3**</span></span>
</dt> <dd>

<span data-ttu-id="a6e47-268">Siehe D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="a6e47-268">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="a6e47-269"><span id="D3DRS_WRAP4"></span><span id="d3drs_wrap4"></span>**D3DRS \_ WRAP4**</span><span class="sxs-lookup"><span data-stu-id="a6e47-269"><span id="D3DRS_WRAP4"></span><span id="d3drs_wrap4"></span>**D3DRS\_WRAP4**</span></span>
</dt> <dd>

<span data-ttu-id="a6e47-270">Siehe D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="a6e47-270">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="a6e47-271"><span id="D3DRS_WRAP5"></span><span id="d3drs_wrap5"></span>**D3DRS \_ WRAP5**</span><span class="sxs-lookup"><span data-stu-id="a6e47-271"><span id="D3DRS_WRAP5"></span><span id="d3drs_wrap5"></span>**D3DRS\_WRAP5**</span></span>
</dt> <dd>

<span data-ttu-id="a6e47-272">Siehe D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="a6e47-272">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="a6e47-273"><span id="D3DRS_WRAP6"></span><span id="d3drs_wrap6"></span>**D3DRS \_ WRAP6**</span><span class="sxs-lookup"><span data-stu-id="a6e47-273"><span id="D3DRS_WRAP6"></span><span id="d3drs_wrap6"></span>**D3DRS\_WRAP6**</span></span>
</dt> <dd>

<span data-ttu-id="a6e47-274">Siehe D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="a6e47-274">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="a6e47-275"><span id="D3DRS_WRAP7"></span><span id="d3drs_wrap7"></span>**D3DRS \_ WRAP7**</span><span class="sxs-lookup"><span data-stu-id="a6e47-275"><span id="D3DRS_WRAP7"></span><span id="d3drs_wrap7"></span>**D3DRS\_WRAP7**</span></span>
</dt> <dd>

<span data-ttu-id="a6e47-276">Siehe D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="a6e47-276">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="a6e47-277"><span id="D3DRS_CLIPPING"></span><span id="d3drs_clipping"></span>**D3DRS \_ Clipping**</span><span class="sxs-lookup"><span data-stu-id="a6e47-277"><span id="D3DRS_CLIPPING"></span><span id="d3drs_clipping"></span>**D3DRS\_CLIPPING**</span></span>
</dt> <dd>

<span data-ttu-id="a6e47-278">**True** , um das primitive Clipping durch Direct3D zu aktivieren, oder **false** , um es zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="a6e47-278">**TRUE** to enable primitive clipping by Direct3D, or **FALSE** to disable it.</span></span> <span data-ttu-id="a6e47-279">Der Standardwert ist " **true**".</span><span class="sxs-lookup"><span data-stu-id="a6e47-279">The default value is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="a6e47-280"><span id="D3DRS_LIGHTING"></span><span id="d3drs_lighting"></span>**D3DRS- \_ Beleuchtung**</span><span class="sxs-lookup"><span data-stu-id="a6e47-280"><span id="D3DRS_LIGHTING"></span><span id="d3drs_lighting"></span>**D3DRS\_LIGHTING**</span></span>
</dt> <dd>

<span data-ttu-id="a6e47-281">**True** , um die Direct3D-Beleuchtung zu aktivieren, oder **false** , um Sie zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="a6e47-281">**TRUE** to enable Direct3D lighting, or **FALSE** to disable it.</span></span> <span data-ttu-id="a6e47-282">Der Standardwert ist " **true**".</span><span class="sxs-lookup"><span data-stu-id="a6e47-282">The default value is **TRUE**.</span></span> <span data-ttu-id="a6e47-283">Nur Scheitel Punkte, die eine Scheitelpunkt normale enthalten, werden ordnungsgemäß beleuchtet. Scheitel Punkte, die keine normale enthalten, verwenden in allen Beleuchtungsberechnungen ein Punktprodukt von 0.</span><span class="sxs-lookup"><span data-stu-id="a6e47-283">Only vertices that include a vertex normal are properly lit; vertices that do not contain a normal employ a dot product of 0 in all lighting calculations.</span></span>

</dd> <dt>

<span data-ttu-id="a6e47-284"><span id="D3DRS_AMBIENT"></span><span id="d3drs_ambient"></span>**D3DRS \_ AMBIENT**</span><span class="sxs-lookup"><span data-stu-id="a6e47-284"><span id="D3DRS_AMBIENT"></span><span id="d3drs_ambient"></span>**D3DRS\_AMBIENT**</span></span>
</dt> <dd>

<span data-ttu-id="a6e47-285">Helle Farbe der Umgebung.</span><span class="sxs-lookup"><span data-stu-id="a6e47-285">Ambient light color.</span></span> <span data-ttu-id="a6e47-286">Dieser Wert ist vom Typ [**D3DCOLOR**](d3dcolor.md).</span><span class="sxs-lookup"><span data-stu-id="a6e47-286">This value is of type [**D3DCOLOR**](d3dcolor.md).</span></span> <span data-ttu-id="a6e47-287">Der Standardwert ist 0.</span><span class="sxs-lookup"><span data-stu-id="a6e47-287">The default value is 0.</span></span>

</dd> <dt>

<span data-ttu-id="a6e47-288"><span id="D3DRS_FOGVERTEXMODE"></span><span id="d3drs_fogvertexmode"></span>**D3DRS \_ fogvertexmode**</span><span class="sxs-lookup"><span data-stu-id="a6e47-288"><span id="D3DRS_FOGVERTEXMODE"></span><span id="d3drs_fogvertexmode"></span>**D3DRS\_FOGVERTEXMODE**</span></span>
</dt> <dd>

<span data-ttu-id="a6e47-289">Für Scheitelpunkt Nebel zu verwendende Nebelformel.</span><span class="sxs-lookup"><span data-stu-id="a6e47-289">Fog formula to be used for vertex fog.</span></span> <span data-ttu-id="a6e47-290">Legen Sie auf einen Member des [**D3DFOGMODE**](./d3dfogmode.md) -Enumerationstyps fest.</span><span class="sxs-lookup"><span data-stu-id="a6e47-290">Set to one member of the [**D3DFOGMODE**](./d3dfogmode.md) enumerated type.</span></span> <span data-ttu-id="a6e47-291">Der Standardwert ist D3DFOG \_ None.</span><span class="sxs-lookup"><span data-stu-id="a6e47-291">The default value is D3DFOG\_NONE.</span></span>

</dd> <dt>

<span data-ttu-id="a6e47-292"><span id="D3DRS_COLORVERTEX"></span><span id="d3drs_colorvertex"></span>**D3DRS \_ ColorVertex**</span><span class="sxs-lookup"><span data-stu-id="a6e47-292"><span id="D3DRS_COLORVERTEX"></span><span id="d3drs_colorvertex"></span>**D3DRS\_COLORVERTEX**</span></span>
</dt> <dd>

<span data-ttu-id="a6e47-293">**True** , um die pro-Vertex-Farbe zu aktivieren oder **false** , um Sie zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="a6e47-293">**TRUE** to enable per-vertex color or **FALSE** to disable it.</span></span> <span data-ttu-id="a6e47-294">Der Standardwert ist " **true**".</span><span class="sxs-lookup"><span data-stu-id="a6e47-294">The default value is **TRUE**.</span></span> <span data-ttu-id="a6e47-295">Durch das Aktivieren der pro-Vertex-Farbe kann das System die Farbe, die für einzelne Scheitel Punkte in seinen Beleuchtungsberechnungen definiert ist, einschließen.</span><span class="sxs-lookup"><span data-stu-id="a6e47-295">Enabling per-vertex color allows the system to include the color defined for individual vertices in its lighting calculations.</span></span>

<span data-ttu-id="a6e47-296">Weitere Informationen finden Sie in den folgenden Rendering-Zuständen:</span><span class="sxs-lookup"><span data-stu-id="a6e47-296">For more information, see the following render states:</span></span>

-   <span data-ttu-id="a6e47-297">D3DRS \_ DiffuseMaterialSource</span><span class="sxs-lookup"><span data-stu-id="a6e47-297">D3DRS\_DIFFUSEMATERIALSOURCE</span></span>
-   <span data-ttu-id="a6e47-298">D3DRS \_ SpecularMaterialSource</span><span class="sxs-lookup"><span data-stu-id="a6e47-298">D3DRS\_SPECULARMATERIALSOURCE</span></span>
-   <span data-ttu-id="a6e47-299">D3DRS \_ AmbientMaterialSource</span><span class="sxs-lookup"><span data-stu-id="a6e47-299">D3DRS\_AMBIENTMATERIALSOURCE</span></span>
-   <span data-ttu-id="a6e47-300">D3DRS \_ emissivematerialsource</span><span class="sxs-lookup"><span data-stu-id="a6e47-300">D3DRS\_EMISSIVEMATERIALSOURCE</span></span>

</dd> <dt>

<span data-ttu-id="a6e47-301"><span id="D3DRS_LOCALVIEWER"></span><span id="d3drs_localviewer"></span>**D3DRS \_ localviewer**</span><span class="sxs-lookup"><span data-stu-id="a6e47-301"><span id="D3DRS_LOCALVIEWER"></span><span id="d3drs_localviewer"></span>**D3DRS\_LOCALVIEWER**</span></span>
</dt> <dd>

<span data-ttu-id="a6e47-302">" **True** ", um für die Kamera relative Glanzlichter zu aktivieren, oder " **false** ", um orthogonale Glanzlichter zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="a6e47-302">**TRUE** to enable camera-relative specular highlights, or **FALSE** to use orthogonal specular highlights.</span></span> <span data-ttu-id="a6e47-303">Der Standardwert ist " **true**".</span><span class="sxs-lookup"><span data-stu-id="a6e47-303">The default value is **TRUE**.</span></span> <span data-ttu-id="a6e47-304">Anwendungen, die eine orthogonale Projektion verwenden, sollten **false** angeben.</span><span class="sxs-lookup"><span data-stu-id="a6e47-304">Applications that use orthogonal projection should specify **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="a6e47-305"><span id="D3DRS_NORMALIZENORMALS"></span><span id="d3drs_normalizenormals"></span>**D3DRS \_ normalizenormals**</span><span class="sxs-lookup"><span data-stu-id="a6e47-305"><span id="D3DRS_NORMALIZENORMALS"></span><span id="d3drs_normalizenormals"></span>**D3DRS\_NORMALIZENORMALS**</span></span>
</dt> <dd>

<span data-ttu-id="a6e47-306">**True** , um die automatische Normalisierung von Scheitelpunkt normalen zu aktivieren, oder **false** , um Sie zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="a6e47-306">**TRUE** to enable automatic normalization of vertex normals, or **FALSE** to disable it.</span></span> <span data-ttu-id="a6e47-307">Der Standardwert ist **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="a6e47-307">The default value is **FALSE**.</span></span> <span data-ttu-id="a6e47-308">Wenn Sie diese Funktion aktivieren, normalisiert das System die Scheitelpunkt normale für Scheitel Punkte, nachdem Sie in einen Kamerabereich transformiert wurden, der Rechenzeit aufwändig sein kann.</span><span class="sxs-lookup"><span data-stu-id="a6e47-308">Enabling this feature causes the system to normalize the vertex normals for vertices after transforming them to camera space, which can be computationally time-consuming.</span></span>

</dd> <dt>

<span data-ttu-id="a6e47-309"><span id="D3DRS_DIFFUSEMATERIALSOURCE"></span><span id="d3drs_diffusematerialsource"></span>**D3DRS \_ DiffuseMaterialSource**</span><span class="sxs-lookup"><span data-stu-id="a6e47-309"><span id="D3DRS_DIFFUSEMATERIALSOURCE"></span><span id="d3drs_diffusematerialsource"></span>**D3DRS\_DIFFUSEMATERIALSOURCE**</span></span>
</dt> <dd>

<span data-ttu-id="a6e47-310">Diffuse Farb Quelle für Beleuchtungsberechnungen.</span><span class="sxs-lookup"><span data-stu-id="a6e47-310">Diffuse color source for lighting calculations.</span></span> <span data-ttu-id="a6e47-311">Gültige Werte sind Member des [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) -Enumerationstyps.</span><span class="sxs-lookup"><span data-stu-id="a6e47-311">Valid values are members of the [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) enumerated type.</span></span> <span data-ttu-id="a6e47-312">Der Standardwert ist D3DMCS \_ COLOR1.</span><span class="sxs-lookup"><span data-stu-id="a6e47-312">The default value is D3DMCS\_COLOR1.</span></span> <span data-ttu-id="a6e47-313">Der Wert für diesen Rendering-Zustand wird nur verwendet, wenn der D3DRS \_ ColorVertex-Rendering-Zustand auf **true** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="a6e47-313">The value for this render state is used only if the D3DRS\_COLORVERTEX render state is set to **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="a6e47-314"><span id="D3DRS_SPECULARMATERIALSOURCE"></span><span id="d3drs_specularmaterialsource"></span>**D3DRS \_ SpecularMaterialSource**</span><span class="sxs-lookup"><span data-stu-id="a6e47-314"><span id="D3DRS_SPECULARMATERIALSOURCE"></span><span id="d3drs_specularmaterialsource"></span>**D3DRS\_SPECULARMATERIALSOURCE**</span></span>
</dt> <dd>

<span data-ttu-id="a6e47-315">Glanz Farben Quelle für Beleuchtungsberechnungen.</span><span class="sxs-lookup"><span data-stu-id="a6e47-315">Specular color source for lighting calculations.</span></span> <span data-ttu-id="a6e47-316">Gültige Werte sind Member des [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) -Enumerationstyps.</span><span class="sxs-lookup"><span data-stu-id="a6e47-316">Valid values are members of the [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) enumerated type.</span></span> <span data-ttu-id="a6e47-317">Der Standardwert ist D3DMCS \_ COLOR2.</span><span class="sxs-lookup"><span data-stu-id="a6e47-317">The default value is D3DMCS\_COLOR2.</span></span>

</dd> <dt>

<span data-ttu-id="a6e47-318"><span id="D3DRS_AMBIENTMATERIALSOURCE"></span><span id="d3drs_ambientmaterialsource"></span>**D3DRS \_ AmbientMaterialSource**</span><span class="sxs-lookup"><span data-stu-id="a6e47-318"><span id="D3DRS_AMBIENTMATERIALSOURCE"></span><span id="d3drs_ambientmaterialsource"></span>**D3DRS\_AMBIENTMATERIALSOURCE**</span></span>
</dt> <dd>

<span data-ttu-id="a6e47-319">Umgebungs Farb Quelle für Beleuchtungsberechnungen.</span><span class="sxs-lookup"><span data-stu-id="a6e47-319">Ambient color source for lighting calculations.</span></span> <span data-ttu-id="a6e47-320">Gültige Werte sind Member des [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) -Enumerationstyps.</span><span class="sxs-lookup"><span data-stu-id="a6e47-320">Valid values are members of the [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) enumerated type.</span></span> <span data-ttu-id="a6e47-321">Der Standardwert ist D3DMCS \_ Material.</span><span class="sxs-lookup"><span data-stu-id="a6e47-321">The default value is D3DMCS\_MATERIAL.</span></span>

</dd> <dt>

<span data-ttu-id="a6e47-322"><span id="D3DRS_EMISSIVEMATERIALSOURCE"></span><span id="d3drs_emissivematerialsource"></span>**D3DRS \_ emissivematerialsource**</span><span class="sxs-lookup"><span data-stu-id="a6e47-322"><span id="D3DRS_EMISSIVEMATERIALSOURCE"></span><span id="d3drs_emissivematerialsource"></span>**D3DRS\_EMISSIVEMATERIALSOURCE**</span></span>
</dt> <dd>

<span data-ttu-id="a6e47-323">Emissive-Farb Quelle für Beleuchtungsberechnungen.</span><span class="sxs-lookup"><span data-stu-id="a6e47-323">Emissive color source for lighting calculations.</span></span> <span data-ttu-id="a6e47-324">Gültige Werte sind Member des [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) -Enumerationstyps.</span><span class="sxs-lookup"><span data-stu-id="a6e47-324">Valid values are members of the [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) enumerated type.</span></span> <span data-ttu-id="a6e47-325">Der Standardwert ist D3DMCS \_ Material.</span><span class="sxs-lookup"><span data-stu-id="a6e47-325">The default value is D3DMCS\_MATERIAL.</span></span>

</dd> <dt>

<span data-ttu-id="a6e47-326"><span id="D3DRS_VERTEXBLEND"></span><span id="d3drs_vertexblend"></span>**D3DRS \_ vertexblend**</span><span class="sxs-lookup"><span data-stu-id="a6e47-326"><span id="D3DRS_VERTEXBLEND"></span><span id="d3drs_vertexblend"></span>**D3DRS\_VERTEXBLEND**</span></span>
</dt> <dd>

<span data-ttu-id="a6e47-327">Anzahl von Matrizen, die zum Durchführen von Geometrie Mischungen verwendet werden sollen, sofern vorhanden.</span><span class="sxs-lookup"><span data-stu-id="a6e47-327">Number of matrices to use to perform geometry blending, if any.</span></span> <span data-ttu-id="a6e47-328">Gültige Werte sind Member des [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) -Enumerationstyps.</span><span class="sxs-lookup"><span data-stu-id="a6e47-328">Valid values are members of the [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) enumerated type.</span></span> <span data-ttu-id="a6e47-329">Der Standardwert ist D3DVBF \_ deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="a6e47-329">The default value is D3DVBF\_DISABLE.</span></span>

</dd> <dt>

<span data-ttu-id="a6e47-330"><span id="D3DRS_CLIPPLANEENABLE"></span><span id="d3drs_clipplaneenable"></span>**D3DRS \_ clipplaneenable**</span><span class="sxs-lookup"><span data-stu-id="a6e47-330"><span id="D3DRS_CLIPPLANEENABLE"></span><span id="d3drs_clipplaneenable"></span>**D3DRS\_CLIPPLANEENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="a6e47-331">Aktiviert oder deaktiviert benutzerdefinierte Clippingebenen.</span><span class="sxs-lookup"><span data-stu-id="a6e47-331">Enables or disables user-defined clipping planes.</span></span> <span data-ttu-id="a6e47-332">Gültige Werte sind ein beliebiges DWORD-Objekt, in dem der Status jedes Bits (festgelegt oder nicht festgelegt) den Aktivierungszustand einer entsprechenden benutzerdefinierten Clippingebene schaltet.</span><span class="sxs-lookup"><span data-stu-id="a6e47-332">Valid values are any DWORD in which the status of each bit (set or not set) toggles the activation state of a corresponding user-defined clipping plane.</span></span> <span data-ttu-id="a6e47-333">Das unwichtigste Bit (Bit 0) steuert die erste Clippingebene am Index 0, und nachfolgende Bits steuern die Aktivierung von Clippingebenen bei höheren Indizes.</span><span class="sxs-lookup"><span data-stu-id="a6e47-333">The least significant bit (bit 0) controls the first clipping plane at index 0, and subsequent bits control the activation of clipping planes at higher indexes.</span></span> <span data-ttu-id="a6e47-334">Wenn ein Bit festgelegt ist, wendet das System während des Szenen Rendering die entsprechende Clippingebene an.</span><span class="sxs-lookup"><span data-stu-id="a6e47-334">If a bit is set, the system applies the appropriate clipping plane during scene rendering.</span></span> <span data-ttu-id="a6e47-335">Der Standardwert ist 0.</span><span class="sxs-lookup"><span data-stu-id="a6e47-335">The default value is 0.</span></span>

<span data-ttu-id="a6e47-336">Die [**D3DCLIPPLANEn**](d3dclipplanen.md) -Makros werden definiert, um eine bequeme Möglichkeit zum Aktivieren von Clippingebenen bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="a6e47-336">The [**D3DCLIPPLANEn**](d3dclipplanen.md) macros are defined to provide a convenient way to enable clipping planes.</span></span>

</dd> <dt>

<span data-ttu-id="a6e47-337"><span id="D3DRS_POINTSIZE"></span><span id="d3drs_pointsize"></span>**D3DRS \_ pointsize**</span><span class="sxs-lookup"><span data-stu-id="a6e47-337"><span id="D3DRS_POINTSIZE"></span><span id="d3drs_pointsize"></span>**D3DRS\_POINTSIZE**</span></span>
</dt> <dd>

<span data-ttu-id="a6e47-338">Ein Gleit Komma Wert, der die Größe angibt, die für die Berechnung der Punktgröße in Fällen verwendet wird, in denen für jeden Scheitelpunkt keine Punktgröße angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="a6e47-338">A float value that specifies the size to use for point size computation in cases where point size is not specified for each vertex.</span></span> <span data-ttu-id="a6e47-339">Dieser Wert wird nicht verwendet, wenn der Scheitelpunkt die Punktgröße enthält.</span><span class="sxs-lookup"><span data-stu-id="a6e47-339">This value is not used when the vertex contains point size.</span></span> <span data-ttu-id="a6e47-340">Dieser Wert befindet sich in Bildschirmraum Einheiten, wenn D3DRS \_ pointscaleenable den Wert **false** hat. andernfalls befindet sich dieser Wert in Welt Raumeinheiten.</span><span class="sxs-lookup"><span data-stu-id="a6e47-340">This value is in screen space units if D3DRS\_POINTSCALEENABLE is **FALSE**; otherwise this value is in world space units.</span></span> <span data-ttu-id="a6e47-341">Der Standardwert ist der Wert, den ein Treiber zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="a6e47-341">The default value is the value a driver returns.</span></span> <span data-ttu-id="a6e47-342">Wenn ein Treiber 0 oder 1 zurückgibt, ist der Standardwert 64, womit die Software Punktgröße emulieren kann.</span><span class="sxs-lookup"><span data-stu-id="a6e47-342">If a driver returns 0 or 1, the default value is 64, which allows software point size emulation.</span></span> <span data-ttu-id="a6e47-343">Da die [**IDirect3DDevice9:: setrenderstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) -Methode DWORD-Werte akzeptiert, muss Ihre Anwendung eine Variable umwandeln, die den Wert enthält, wie im folgenden Codebeispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="a6e47-343">Because the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method accepts DWORD values, your application must cast a variable that contains the value, as shown in the following code example.</span></span>


```
m_pDevice9->SetRenderState(D3DRS_POINTSIZE, *((DWORD*)&pointSize));
```



</dd> <dt>

<span data-ttu-id="a6e47-344"><span id="D3DRS_POINTSIZE_MIN"></span><span id="d3drs_pointsize_min"></span>**D3DRS \_ pointsize \_ Min**</span><span class="sxs-lookup"><span data-stu-id="a6e47-344"><span id="D3DRS_POINTSIZE_MIN"></span><span id="d3drs_pointsize_min"></span>**D3DRS\_POINTSIZE\_MIN**</span></span>
</dt> <dd>

<span data-ttu-id="a6e47-345">Ein float-Wert, der die minimale Größe von Punkt primitiven angibt.</span><span class="sxs-lookup"><span data-stu-id="a6e47-345">A float value that specifies the minimum size of point primitives.</span></span> <span data-ttu-id="a6e47-346">Punkt primitiven werden während des Renderings an diese Größe gebunden.</span><span class="sxs-lookup"><span data-stu-id="a6e47-346">Point primitives are clamped to this size during rendering.</span></span> <span data-ttu-id="a6e47-347">Wenn Sie diese Einstellung auf Werte festlegen, die kleiner als 1,0 sind, werden Punkte verworfen, wenn der Punkt keine Pixel Zentrierung abdeckt und das Antialiasing deaktiviert ist oder mit reduzierter Intensität gerendert wird, wenn das Antialiasing aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="a6e47-347">Setting this to values smaller than 1.0 results in points dropping out when the point does not cover a pixel center and antialiasing is disabled or being rendered with reduced intensity when antialiasing is enabled.</span></span> <span data-ttu-id="a6e47-348">Der Standardwert ist 1.0 f.</span><span class="sxs-lookup"><span data-stu-id="a6e47-348">The default value is 1.0f.</span></span> <span data-ttu-id="a6e47-349">Der Bereich für diesen Wert ist größer als oder gleich 0,0 f.</span><span class="sxs-lookup"><span data-stu-id="a6e47-349">The range for this value is greater than or equal to 0.0f.</span></span> <span data-ttu-id="a6e47-350">Da die [**IDirect3DDevice9:: setrenderstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) -Methode DWORD-Werte akzeptiert, muss Ihre Anwendung eine Variable umwandeln, die den Wert enthält, wie im folgenden Codebeispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="a6e47-350">Because the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method accepts DWORD values, your application must cast a variable that contains the value, as shown in the following code example.</span></span>


```
m_pDevice9->SetRenderState(D3DRS_POINTSIZE_MIN, *((DWORD*)&pointSizeMin));
```



</dd> <dt>

<span data-ttu-id="a6e47-351"><span id="D3DRS_POINTSPRITEENABLE"></span><span id="d3drs_pointspriteenable"></span>**D3DRS \_ pointspriteenable**</span><span class="sxs-lookup"><span data-stu-id="a6e47-351"><span id="D3DRS_POINTSPRITEENABLE"></span><span id="d3drs_pointspriteenable"></span>**D3DRS\_POINTSPRITEENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="a6e47-352">boolescher Wert.</span><span class="sxs-lookup"><span data-stu-id="a6e47-352">bool value.</span></span> <span data-ttu-id="a6e47-353">Wenn **true**, werden Texturkoordinaten von Punkt primitiven festgelegt, sodass an jedem Punkt vollständige Texturen zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="a6e47-353">When **TRUE**, texture coordinates of point primitives are set so that full textures are mapped on each point.</span></span> <span data-ttu-id="a6e47-354">Bei " **false**" werden die Scheitelpunkt Texturkoordinaten für den gesamten Punkt verwendet.</span><span class="sxs-lookup"><span data-stu-id="a6e47-354">When **FALSE**, the vertex texture coordinates are used for the entire point.</span></span> <span data-ttu-id="a6e47-355">Der Standardwert ist **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="a6e47-355">The default value is **FALSE**.</span></span> <span data-ttu-id="a6e47-356">Sie können Einzel Pixel Punkte im DirectX 7-Stil erzielen, indem Sie D3DRS \_ pointscaleenable auf **false** und D3DRS \_ pointsize auf 1,0 festlegen. Dies sind die Standardwerte.</span><span class="sxs-lookup"><span data-stu-id="a6e47-356">You can achieve DirectX 7 style single-pixel points by setting D3DRS\_POINTSCALEENABLE to **FALSE** and D3DRS\_POINTSIZE to 1.0, which are the default values.</span></span>

</dd> <dt>

<span data-ttu-id="a6e47-357"><span id="D3DRS_POINTSCALEENABLE"></span><span id="d3drs_pointscaleenable"></span>**D3DRS \_ pointscaleenable**</span><span class="sxs-lookup"><span data-stu-id="a6e47-357"><span id="D3DRS_POINTSCALEENABLE"></span><span id="d3drs_pointscaleenable"></span>**D3DRS\_POINTSCALEENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="a6e47-358">boolescher Wert, der die Berechnung der Größe für Punkt primitive steuert.</span><span class="sxs-lookup"><span data-stu-id="a6e47-358">bool value that controls computation of size for point primitives.</span></span> <span data-ttu-id="a6e47-359">**True** gibt an, dass die Punktgröße als Wert für die Kamera Fläche interpretiert wird und durch die Entfernungs Funktion skaliert wird, und durch den Wert von "Frustum" wird die y-Achsen-Skalierung berechnet, um die endgültige Größe des Bildschirm Raums zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="a6e47-359">When **TRUE**, the point size is interpreted as a camera space value and is scaled by the distance function and the frustum to viewport y-axis scaling to compute the final screen-space point size.</span></span> <span data-ttu-id="a6e47-360">Bei " **false**" wird die Punktgröße als Bildschirmfläche interpretiert und direkt verwendet.</span><span class="sxs-lookup"><span data-stu-id="a6e47-360">When **FALSE**, the point size is interpreted as screen space and used directly.</span></span> <span data-ttu-id="a6e47-361">Der Standardwert ist **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="a6e47-361">The default value is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="a6e47-362"><span id="D3DRS_POINTSCALE_A"></span><span id="d3drs_pointscale_a"></span>**D3DRS \_ pointscale \_ A**</span><span class="sxs-lookup"><span data-stu-id="a6e47-362"><span id="D3DRS_POINTSCALE_A"></span><span id="d3drs_pointscale_a"></span>**D3DRS\_POINTSCALE\_A**</span></span>
</dt> <dd>

<span data-ttu-id="a6e47-363">Ein float-Wert, der die Entfernungs basierte Größen Dämpfung für Punkt primitive steuert.</span><span class="sxs-lookup"><span data-stu-id="a6e47-363">A float value that controls for distance-based size attenuation for point primitives.</span></span> <span data-ttu-id="a6e47-364">Nur aktiv, wenn D3DRS \_ pointscaleenable den Wert **true** hat.</span><span class="sxs-lookup"><span data-stu-id="a6e47-364">Active only when D3DRS\_POINTSCALEENABLE is **TRUE**.</span></span> <span data-ttu-id="a6e47-365">Der Standardwert ist 1.0 f.</span><span class="sxs-lookup"><span data-stu-id="a6e47-365">The default value is 1.0f.</span></span> <span data-ttu-id="a6e47-366">Der Bereich für diesen Wert ist größer als oder gleich 0,0 f.</span><span class="sxs-lookup"><span data-stu-id="a6e47-366">The range for this value is greater than or equal to 0.0f.</span></span> <span data-ttu-id="a6e47-367">Da die [**IDirect3DDevice9:: setrenderstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) -Methode DWORD-Werte akzeptiert, muss Ihre Anwendung eine Variable umwandeln, die den Wert enthält, wie im folgenden Codebeispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="a6e47-367">Because the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method accepts DWORD values, your application must cast a variable that contains the value, as shown in the following code example.</span></span>


```
m_pDevice9->SetRenderState(D3DRS_POINTSCALE_A, *((DWORD*)&pointScaleA));
```



</dd> <dt>

<span data-ttu-id="a6e47-368"><span id="D3DRS_POINTSCALE_B"></span><span id="d3drs_pointscale_b"></span>**D3DRS \_ pointscale \_ B**</span><span class="sxs-lookup"><span data-stu-id="a6e47-368"><span id="D3DRS_POINTSCALE_B"></span><span id="d3drs_pointscale_b"></span>**D3DRS\_POINTSCALE\_B**</span></span>
</dt> <dd>

<span data-ttu-id="a6e47-369">Ein float-Wert, der die Entfernungs basierte Größen Dämpfung für Punkt primitive steuert.</span><span class="sxs-lookup"><span data-stu-id="a6e47-369">A float value that controls for distance-based size attenuation for point primitives.</span></span> <span data-ttu-id="a6e47-370">Nur aktiv, wenn D3DRS \_ pointscaleenable den Wert **true** hat.</span><span class="sxs-lookup"><span data-stu-id="a6e47-370">Active only when D3DRS\_POINTSCALEENABLE is **TRUE**.</span></span> <span data-ttu-id="a6e47-371">Der Standardwert ist 0,0 f.</span><span class="sxs-lookup"><span data-stu-id="a6e47-371">The default value is 0.0f.</span></span> <span data-ttu-id="a6e47-372">Der Bereich für diesen Wert ist größer als oder gleich 0,0 f.</span><span class="sxs-lookup"><span data-stu-id="a6e47-372">The range for this value is greater than or equal to 0.0f.</span></span> <span data-ttu-id="a6e47-373">Da die [**IDirect3DDevice9:: setrenderstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) -Methode DWORD-Werte akzeptiert, muss Ihre Anwendung eine Variable umwandeln, die den Wert enthält, wie im folgenden Codebeispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="a6e47-373">Because the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method accepts DWORD values, your application must cast a variable that contains the value, as shown in the following code example.</span></span>


```
m_pDevice9->SetRenderState(D3DRS_POINTSCALE_B, *((DWORD*)&pointScaleB));
```



</dd> <dt>

<span data-ttu-id="a6e47-374"><span id="D3DRS_POINTSCALE_C"></span><span id="d3drs_pointscale_c"></span>**D3DRS \_ pointscale \_ C**</span><span class="sxs-lookup"><span data-stu-id="a6e47-374"><span id="D3DRS_POINTSCALE_C"></span><span id="d3drs_pointscale_c"></span>**D3DRS\_POINTSCALE\_C**</span></span>
</dt> <dd>

<span data-ttu-id="a6e47-375">Ein float-Wert, der die Entfernungs basierte Größen Dämpfung für Punkt primitive steuert.</span><span class="sxs-lookup"><span data-stu-id="a6e47-375">A float value that controls for distance-based size attenuation for point primitives.</span></span> <span data-ttu-id="a6e47-376">Nur aktiv, wenn D3DRS \_ pointscaleenable den Wert **true** hat.</span><span class="sxs-lookup"><span data-stu-id="a6e47-376">Active only when D3DRS\_POINTSCALEENABLE is **TRUE**.</span></span> <span data-ttu-id="a6e47-377">Der Standardwert ist 0,0 f.</span><span class="sxs-lookup"><span data-stu-id="a6e47-377">The default value is 0.0f.</span></span> <span data-ttu-id="a6e47-378">Der Bereich für diesen Wert ist größer als oder gleich 0,0 f.</span><span class="sxs-lookup"><span data-stu-id="a6e47-378">The range for this value is greater than or equal to 0.0f.</span></span> <span data-ttu-id="a6e47-379">Da die [**IDirect3DDevice9:: setrenderstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) -Methode DWORD-Werte akzeptiert, muss Ihre Anwendung eine Variable umwandeln, die den Wert enthält, wie im folgenden Codebeispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="a6e47-379">Because the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method accepts DWORD values, your application must cast a variable that contains the value, as shown in the following code example.</span></span>


```
m_pDevice9->SetRenderState(D3DRS_POINTSCALE_C, *((DWORD*)&pointScaleC));
```



</dd> <dt>

<span data-ttu-id="a6e47-380"><span id="D3DRS_MULTISAMPLEANTIALIAS"></span><span id="d3drs_multisampleantialias"></span>**D3DRS \_ multisampleantialias**</span><span class="sxs-lookup"><span data-stu-id="a6e47-380"><span id="D3DRS_MULTISAMPLEANTIALIAS"></span><span id="d3drs_multisampleantialias"></span>**D3DRS\_MULTISAMPLEANTIALIAS**</span></span>
</dt> <dd>

<span data-ttu-id="a6e47-381">boolescher Wert, der bestimmt, wie einzelne Stichproben berechnet werden, wenn ein Multisampling-Renderziel-Puffer verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a6e47-381">bool value that determines how individual samples are computed when using a multisample render-target buffer.</span></span> <span data-ttu-id="a6e47-382">Wenn diese Einstellung auf " **true**" festgelegt ist, werden mehrere Stichproben berechnet, sodass das Vollbild-Antialiasing durch Sampling an verschiedenen Beispiel Positionen für die einzelnen Stichproben durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a6e47-382">When set to **TRUE**, the multiple samples are computed so that full-scene antialiasing is performed by sampling at different sample positions for each multiple sample.</span></span> <span data-ttu-id="a6e47-383">Wenn diese Einstellung auf " **false**" festgelegt ist, werden alle Samplings mit dem gleichen Stichproben Wert geschrieben, der im Pixel Center Stichprobe ist, wodurch das Rendering von nicht-Antialiasing an einen Multisampling-Puffer ermöglicht wird.</span><span class="sxs-lookup"><span data-stu-id="a6e47-383">When set to **FALSE**, the multiple samples are all written with the same sample value, sampled at the pixel center, which allows non-antialiased rendering to a multisample buffer.</span></span> <span data-ttu-id="a6e47-384">Dieser renderzustand hat keine Auswirkung, wenn ein einzelner Beispiel Puffer gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="a6e47-384">This render state has no effect when rendering to a single sample buffer.</span></span> <span data-ttu-id="a6e47-385">Der Standardwert ist " **true**".</span><span class="sxs-lookup"><span data-stu-id="a6e47-385">The default value is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="a6e47-386"><span id="D3DRS_MULTISAMPLEMASK"></span><span id="d3drs_multisamplemask"></span>**D3DRS \_ multisamplemask**</span><span class="sxs-lookup"><span data-stu-id="a6e47-386"><span id="D3DRS_MULTISAMPLEMASK"></span><span id="d3drs_multisamplemask"></span>**D3DRS\_MULTISAMPLEMASK**</span></span>
</dt> <dd>

<span data-ttu-id="a6e47-387">Jedes Bit in dieser Maske, beginnend mit dem am wenigsten signifikanten Bit (LSB), steuert die Änderung eines der Beispiele in einem Multisampling-Renderziel.</span><span class="sxs-lookup"><span data-stu-id="a6e47-387">Each bit in this mask, starting at the least significant bit (LSB), controls modification of one of the samples in a multisample render target.</span></span> <span data-ttu-id="a6e47-388">Daher enthält das niedrige Byte bei einem 8-Stichproben-Renderziel die acht Schreibvorgänge für jedes der acht Stichproben.</span><span class="sxs-lookup"><span data-stu-id="a6e47-388">Thus, for an 8-sample render target, the low byte contains the eight write enables for each of the eight samples.</span></span> <span data-ttu-id="a6e47-389">Dieser renderzustand hat keine Auswirkung, wenn ein einzelner Beispiel Puffer gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="a6e47-389">This render state has no effect when rendering to a single sample buffer.</span></span> <span data-ttu-id="a6e47-390">Der Standardwert ist 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="a6e47-390">The default value is 0xFFFFFFFF.</span></span>

<span data-ttu-id="a6e47-391">Dieser renderzustand ermöglicht die Verwendung eines Multisampling-Puffers als Akkumulations Puffer und ermöglicht das Multipass-Rendering der Geometrie, bei der jeder Pass eine Teilmenge von Beispielen aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="a6e47-391">This render state enables use of a multisample buffer as an accumulation buffer, doing multipass rendering of geometry where each pass updates a subset of samples.</span></span>

<span data-ttu-id="a6e47-392">Wenn n multisamples-und k-aktivierte Beispiele vorhanden sind, sollte die resultierende Intensität des gerenderten Bilds k/n sein.</span><span class="sxs-lookup"><span data-stu-id="a6e47-392">If there are n multisamples and k enabled samples, the resulting intensity of the rendered image should be k/n.</span></span> <span data-ttu-id="a6e47-393">Jede Komponente RGB jedes Pixels wird von k/n berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="a6e47-393">Each component RGB of every pixel is factored by k/n.</span></span>

</dd> <dt>

<span data-ttu-id="a6e47-394"><span id="D3DRS_PATCHEDGESTYLE"></span><span id="d3drs_patchedgestyle"></span>**D3DRS \_ patchedgestyle**</span><span class="sxs-lookup"><span data-stu-id="a6e47-394"><span id="D3DRS_PATCHEDGESTYLE"></span><span id="d3drs_patchedgestyle"></span>**D3DRS\_PATCHEDGESTYLE**</span></span>
</dt> <dd>

<span data-ttu-id="a6e47-395">Legt fest, ob patchkanten den Mosaik Stil verwenden.</span><span class="sxs-lookup"><span data-stu-id="a6e47-395">Sets whether patch edges will use float style tessellation.</span></span> <span data-ttu-id="a6e47-396">Mögliche Werte werden durch den [**D3DPATCHEDGESTYLE**](./d3dpatchedgestyle.md) -enumerierten Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="a6e47-396">Possible values are defined by the [**D3DPATCHEDGESTYLE**](./d3dpatchedgestyle.md) enumerated type.</span></span> <span data-ttu-id="a6e47-397">Der Standardwert ist D3DPATCHEDGE \_ diskret.</span><span class="sxs-lookup"><span data-stu-id="a6e47-397">The default value is D3DPATCHEDGE\_DISCRETE.</span></span>

</dd> <dt>

<span data-ttu-id="a6e47-398"><span id="D3DRS_DEBUGMONITORTOKEN"></span><span id="d3drs_debugmonitortoken"></span>**D3DRS-Debug- \_ monitortoken**</span><span class="sxs-lookup"><span data-stu-id="a6e47-398"><span id="D3DRS_DEBUGMONITORTOKEN"></span><span id="d3drs_debugmonitortoken"></span>**D3DRS\_DEBUGMONITORTOKEN**</span></span>
</dt> <dd>

<span data-ttu-id="a6e47-399">Wird nur zum Debuggen des Monitors festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a6e47-399">Set only for debugging the monitor.</span></span> <span data-ttu-id="a6e47-400">Mögliche Werte werden durch den [**D3DDEBUGMONITORTOKENS**](./d3ddebugmonitortokens.md) -enumerierten Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="a6e47-400">Possible values are defined by the [**D3DDEBUGMONITORTOKENS**](./d3ddebugmonitortokens.md) enumerated type.</span></span> <span data-ttu-id="a6e47-401">Beachten Sie Folgendes: Wenn D3DRS \_ debugmonitortoken festgelegt ist, wird der-Befehl als übergeben eines Tokens an den Debug-Monitor behandelt.</span><span class="sxs-lookup"><span data-stu-id="a6e47-401">Note that if D3DRS\_DEBUGMONITORTOKEN is set, the call is treated as passing a token to the debug monitor.</span></span> <span data-ttu-id="a6e47-402">Wenn z \_ . b. nach dem übergeben von D3DDMT enable oder D3DDMT \_ Deaktivieren an D3DRS \_ debugmonitortoken-andere Tokenwerte übergeben werden, wird der Status (aktiviert oder deaktiviert) des debugmonitors weiterhin beibehalten.</span><span class="sxs-lookup"><span data-stu-id="a6e47-402">For example, if - after passing D3DDMT\_ENABLE or D3DDMT\_DISABLE to D3DRS\_DEBUGMONITORTOKEN - other token values are passed in, the state (enabled or disabled) of the debug monitor will still persist.</span></span>

<span data-ttu-id="a6e47-403">Dieser Status ist nur für Debugbuilds nützlich.</span><span class="sxs-lookup"><span data-stu-id="a6e47-403">This state is only useful for debug builds.</span></span> <span data-ttu-id="a6e47-404">Der Debugmonitor wird standardmäßig auf D3DDMT \_ enable eingestellt.</span><span class="sxs-lookup"><span data-stu-id="a6e47-404">The debug monitor defaults to D3DDMT\_ENABLE.</span></span>

</dd> <dt>

<span data-ttu-id="a6e47-405"><span id="D3DRS_POINTSIZE_MAX"></span><span id="d3drs_pointsize_max"></span>**D3DRS \_ pointsize \_ Max**</span><span class="sxs-lookup"><span data-stu-id="a6e47-405"><span id="D3DRS_POINTSIZE_MAX"></span><span id="d3drs_pointsize_max"></span>**D3DRS\_POINTSIZE\_MAX**</span></span>
</dt> <dd>

<span data-ttu-id="a6e47-406">Ein float-Wert, der die maximale Größe angibt, an die Punkt Sprites gebunden werden.</span><span class="sxs-lookup"><span data-stu-id="a6e47-406">A float value that specifies the maximum size to which point sprites will be clamped.</span></span> <span data-ttu-id="a6e47-407">Der Wert muss kleiner oder gleich dem maxpointsize-Member von [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) und größer oder gleich D3DRS \_ pointsize \_ min sein.</span><span class="sxs-lookup"><span data-stu-id="a6e47-407">The value must be less than or equal to the MaxPointSize member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) and greater than or equal to D3DRS\_POINTSIZE\_MIN.</span></span> <span data-ttu-id="a6e47-408">Der Standardwert ist 64,0.</span><span class="sxs-lookup"><span data-stu-id="a6e47-408">The default value is 64.0.</span></span> <span data-ttu-id="a6e47-409">Da die [**IDirect3DDevice9:: setrenderstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) -Methode DWORD-Werte akzeptiert, muss Ihre Anwendung eine Variable umwandeln, die den Wert enthält, wie im folgenden Codebeispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="a6e47-409">Because the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method accepts DWORD values, your application must cast a variable that contains the value, as shown in the following code example.</span></span>


```
m_pDevice9->SetRenderState(D3DRS_PONTSIZE_MAX, *((DWORD*)&pointSizeMax));
```



</dd> <dt>

<span data-ttu-id="a6e47-410"><span id="D3DRS_INDEXEDVERTEXBLENDENABLE"></span><span id="d3drs_indexedvertexblendenable"></span>**D3DRS \_ indexedvertexblendenable**</span><span class="sxs-lookup"><span data-stu-id="a6e47-410"><span id="D3DRS_INDEXEDVERTEXBLENDENABLE"></span><span id="d3drs_indexedvertexblendenable"></span>**D3DRS\_INDEXEDVERTEXBLENDENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="a6e47-411">boolescher Wert, der die indizierte Vertex-Mischung aktiviert oder deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="a6e47-411">bool value that enables or disables indexed vertex blending.</span></span> <span data-ttu-id="a6e47-412">Der Standardwert ist **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="a6e47-412">The default value is **FALSE**.</span></span> <span data-ttu-id="a6e47-413">Wenn diese Option auf **true** festgelegt ist, wird die indizierte vertexmischung aktiviert.</span><span class="sxs-lookup"><span data-stu-id="a6e47-413">When set to **TRUE**, indexed vertex blending is enabled.</span></span> <span data-ttu-id="a6e47-414">Wenn **false** festgelegt ist, wird die indizierte vertexmischung deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="a6e47-414">When set to **FALSE**, indexed vertex blending is disabled.</span></span> <span data-ttu-id="a6e47-415">Wenn dieser renderzustand aktiviert ist, muss der Benutzer Matrix Indizes als gepacktes dwordan jeden Scheitelpunkt übergeben.</span><span class="sxs-lookup"><span data-stu-id="a6e47-415">If this render state is enabled, the user must pass matrix indices as a packed DWORDwith every vertex.</span></span> <span data-ttu-id="a6e47-416">Wenn der renderzustand deaktiviert ist und Vertex-Blending über den D3DRS \_ vertexblend-Zustand aktiviert wird, entspricht er den Matrix Indizes 0, 1, 2 und 3 in jedem Scheitelpunkt.</span><span class="sxs-lookup"><span data-stu-id="a6e47-416">When the render state is disabled and vertex blending is enabled through the D3DRS\_VERTEXBLEND state, it is equivalent to having matrix indices 0, 1, 2, 3 in every vertex.</span></span>

</dd> <dt>

<span data-ttu-id="a6e47-417"><span id="D3DRS_COLORWRITEENABLE"></span><span id="d3drs_colorwriteenable"></span>**D3DRS \_ colorschreiteenable**</span><span class="sxs-lookup"><span data-stu-id="a6e47-417"><span id="D3DRS_COLORWRITEENABLE"></span><span id="d3drs_colorwriteenable"></span>**D3DRS\_COLORWRITEENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="a6e47-418">Uint-Wert, der einen pro-Channel-Schreibvorgang für den Renderziel-Farb Puffer ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="a6e47-418">UINT value that enables a per-channel write for the render-target color buffer.</span></span> <span data-ttu-id="a6e47-419">Ein Set-Bit führt dazu, dass der Farbkanal während des 3D-Renderings aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="a6e47-419">A set bit results in the color channel being updated during 3D rendering.</span></span> <span data-ttu-id="a6e47-420">Ein Clear-Bit führt dazu, dass der Farbkanal nicht beeinträchtigt wird.</span><span class="sxs-lookup"><span data-stu-id="a6e47-420">A clear bit results in the color channel being unaffected.</span></span> <span data-ttu-id="a6e47-421">Diese Funktionalität ist verfügbar, wenn das D3DPMISCCAPS \_ colorwrite teenable-Funktionen-Bit im primitivefehlcaps-Member der [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) -Struktur für das Gerät festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="a6e47-421">This functionality is available if the D3DPMISCCAPS\_COLORWRITEENABLE capabilities bit is set in the PrimitiveMiscCaps member of the [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure for the device.</span></span> <span data-ttu-id="a6e47-422">Dieser Rendering-Zustand wirkt sich nicht auf den Löschvorgang aus.</span><span class="sxs-lookup"><span data-stu-id="a6e47-422">This render state does not affect the clear operation.</span></span> <span data-ttu-id="a6e47-423">Der Standardwert ist 0x0000000f.</span><span class="sxs-lookup"><span data-stu-id="a6e47-423">The default value is 0x0000000F.</span></span>

<span data-ttu-id="a6e47-424">Gültige Werte für diesen gerengerzustand können eine beliebige Kombination aus den \_ Flags D3DCOLORWRITEENABLE Alpha, D3DCOLORWRITEENABLE \_ Blue, D3DCOLORWRITEENABLE \_ grün oder D3DCOLORWRITEENABLE \_ Red sein.</span><span class="sxs-lookup"><span data-stu-id="a6e47-424">Valid values for this render state can be any combination of the D3DCOLORWRITEENABLE\_ALPHA, D3DCOLORWRITEENABLE\_BLUE, D3DCOLORWRITEENABLE\_GREEN, or D3DCOLORWRITEENABLE\_RED flags.</span></span>

</dd> <dt>

<span data-ttu-id="a6e47-425"><span id="D3DRS_TWEENFACTOR"></span><span id="d3drs_tweenfactor"></span>**D3DRS \_ tweumfactor**</span><span class="sxs-lookup"><span data-stu-id="a6e47-425"><span id="D3DRS_TWEENFACTOR"></span><span id="d3drs_tweenfactor"></span>**D3DRS\_TWEENFACTOR**</span></span>
</dt> <dd>

<span data-ttu-id="a6e47-426">Ein float-Wert, der den Tween-Faktor steuert.</span><span class="sxs-lookup"><span data-stu-id="a6e47-426">A float value that controls the tween factor.</span></span> <span data-ttu-id="a6e47-427">Der Standardwert ist 0,0 f.</span><span class="sxs-lookup"><span data-stu-id="a6e47-427">The default value is 0.0f.</span></span> <span data-ttu-id="a6e47-428">Da die [**IDirect3DDevice9:: setrenderstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) -Methode DWORD-Werte akzeptiert, muss Ihre Anwendung eine Variable umwandeln, die den Wert enthält, wie im folgenden Codebeispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="a6e47-428">Because the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method accepts DWORD values, your application must cast a variable that contains the value, as shown in the following code example.</span></span>


```
m_pDevice9->SetRenderState(D3DRS_TWEENFACTOR, *((DWORD*)&TweenFactor));
```



</dd> <dt>

<span data-ttu-id="a6e47-429"><span id="D3DRS_BLENDOP"></span><span id="d3drs_blendop"></span>**D3DRS \_ blendop**</span><span class="sxs-lookup"><span data-stu-id="a6e47-429"><span id="D3DRS_BLENDOP"></span><span id="d3drs_blendop"></span>**D3DRS\_BLENDOP**</span></span>
</dt> <dd>

<span data-ttu-id="a6e47-430">Der Wert, der verwendet wird, um die arithmetische Operation auszuwählen, die angewendet wird, wenn der D3DRS \_ AlphaBlendEnable-Mischungs Zustand auf **true** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="a6e47-430">Value used to select the arithmetic operation applied when the alpha blending render state, D3DRS\_ALPHABLENDENABLE, is set to **TRUE**.</span></span> <span data-ttu-id="a6e47-431">Gültige Werte werden durch den [**D3DBLENDOP**](./d3dblendop.md) -enumerierten Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="a6e47-431">Valid values are defined by the [**D3DBLENDOP**](./d3dblendop.md) enumerated type.</span></span> <span data-ttu-id="a6e47-432">Der Standardwert ist D3DBLENDOP \_ Add.</span><span class="sxs-lookup"><span data-stu-id="a6e47-432">The default value is D3DBLENDOP\_ADD.</span></span>

<span data-ttu-id="a6e47-433">Wenn die D3DPMISCCAPS \_ blendop-Geräte Funktion nicht unterstützt wird, \_ wird D3DBLENDOP Add ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a6e47-433">If the D3DPMISCCAPS\_BLENDOP device capability is not supported, then D3DBLENDOP\_ADD is performed.</span></span>

</dd> <dt>

<span data-ttu-id="a6e47-434"><span id="D3DRS_POSITIONDEGREE"></span><span id="d3drs_positiondegree"></span>**D3DRS \_ positiondegree**</span><span class="sxs-lookup"><span data-stu-id="a6e47-434"><span id="D3DRS_POSITIONDEGREE"></span><span id="d3drs_positiondegree"></span>**D3DRS\_POSITIONDEGREE**</span></span>
</dt> <dd>

<span data-ttu-id="a6e47-435">N-patchpositions-Interpolations Grad.</span><span class="sxs-lookup"><span data-stu-id="a6e47-435">N-patch position interpolation degree.</span></span> <span data-ttu-id="a6e47-436">Die Werte können D3DDEGREE \_ Cubic (Standard) oder D3DDEGREE \_ linear lauten.</span><span class="sxs-lookup"><span data-stu-id="a6e47-436">The values can be D3DDEGREE\_CUBIC (default) or D3DDEGREE\_LINEAR.</span></span> <span data-ttu-id="a6e47-437">Weitere Informationen finden Sie unter [**D3DDEGREETYPE**](./d3ddegreetype.md).</span><span class="sxs-lookup"><span data-stu-id="a6e47-437">For more information, see [**D3DDEGREETYPE**](./d3ddegreetype.md).</span></span>

</dd> <dt>

<span data-ttu-id="a6e47-438"><span id="D3DRS_NORMALDEGREE"></span><span id="d3drs_normaldegree"></span>**D3DRS \_ normaldegree**</span><span class="sxs-lookup"><span data-stu-id="a6e47-438"><span id="D3DRS_NORMALDEGREE"></span><span id="d3drs_normaldegree"></span>**D3DRS\_NORMALDEGREE**</span></span>
</dt> <dd>

<span data-ttu-id="a6e47-439">N-Patch-normaler Interpolations Grad.</span><span class="sxs-lookup"><span data-stu-id="a6e47-439">N-patch normal interpolation degree.</span></span> <span data-ttu-id="a6e47-440">Die Werte können D3DDEGREE \_ linear (Standard) oder D3DDEGREE \_ Quadratic lauten.</span><span class="sxs-lookup"><span data-stu-id="a6e47-440">The values can be D3DDEGREE\_LINEAR (default) or D3DDEGREE\_QUADRATIC.</span></span> <span data-ttu-id="a6e47-441">Weitere Informationen finden Sie unter [**D3DDEGREETYPE**](./d3ddegreetype.md).</span><span class="sxs-lookup"><span data-stu-id="a6e47-441">For more information, see [**D3DDEGREETYPE**](./d3ddegreetype.md).</span></span>

</dd> <dt>

<span data-ttu-id="a6e47-442"><span id="D3DRS_SCISSORTESTENABLE"></span><span id="d3drs_scissortestenable"></span>**D3DRS \_ scissortestenable**</span><span class="sxs-lookup"><span data-stu-id="a6e47-442"><span id="D3DRS_SCISSORTESTENABLE"></span><span id="d3drs_scissortestenable"></span>**D3DRS\_SCISSORTESTENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="a6e47-443">**True** , um das Testen von Scheren zu aktivieren und **false** zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="a6e47-443">**TRUE** to enable scissor testing and **FALSE** to disable it.</span></span> <span data-ttu-id="a6e47-444">Der Standardwert ist **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="a6e47-444">The default value is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="a6e47-445"><span id="D3DRS_SLOPESCALEDEPTHBIAS"></span><span id="d3drs_slopescaledepthbias"></span>**D3DRS \_ slopescaledepthbias**</span><span class="sxs-lookup"><span data-stu-id="a6e47-445"><span id="D3DRS_SLOPESCALEDEPTHBIAS"></span><span id="d3drs_slopescaledepthbias"></span>**D3DRS\_SLOPESCALEDEPTHBIAS**</span></span>
</dt> <dd>

<span data-ttu-id="a6e47-446">Wird verwendet, um zu bestimmen, wie viel Bias auf die Co-planaren primitiven angewendet werden kann, um die z-Bekämpfung zu verringern.</span><span class="sxs-lookup"><span data-stu-id="a6e47-446">Used to determine how much bias can be applied to co-planar primitives to reduce z-fighting.</span></span> <span data-ttu-id="a6e47-447">Der Standardwert ist 0.</span><span class="sxs-lookup"><span data-stu-id="a6e47-447">The default value is 0.</span></span>

<span data-ttu-id="a6e47-448">Bias = (Max \* D3DRS \_ slopescaledepthbias) + D3DRS \_ depthbias.</span><span class="sxs-lookup"><span data-stu-id="a6e47-448">bias = (max \* D3DRS\_SLOPESCALEDEPTHBIAS) + D3DRS\_DEPTHBIAS.</span></span>

<span data-ttu-id="a6e47-449">Dabei ist Max die maximale Tiefe Steigung des gerenderten Dreiecks.</span><span class="sxs-lookup"><span data-stu-id="a6e47-449">where max is the maximum depth slope of the triangle being rendered.</span></span>

</dd> <dt>

<span data-ttu-id="a6e47-450"><span id="D3DRS_ANTIALIASEDLINEENABLE"></span><span id="d3drs_antialiasedlineenable"></span>**D3DRS \_ antialiasedlineenable**</span><span class="sxs-lookup"><span data-stu-id="a6e47-450"><span id="D3DRS_ANTIALIASEDLINEENABLE"></span><span id="d3drs_antialiasedlineenable"></span>**D3DRS\_ANTIALIASEDLINEENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="a6e47-451">**True** , um das Zeilen-Antialiasing zu aktivieren, **false** , um das Zeilen-Antialiasing zu deaktivieren</span><span class="sxs-lookup"><span data-stu-id="a6e47-451">**TRUE** to enable line antialiasing, **FALSE** to disable line antialiasing.</span></span> <span data-ttu-id="a6e47-452">Der Standardwert ist **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="a6e47-452">The default value is **FALSE**.</span></span>

<span data-ttu-id="a6e47-453">Beim Rendern in ein Multisampling-Renderziel \_ wird D3DRS antialiasedlineenable ignoriert, und alle Zeilen werden als Alias gerendert.</span><span class="sxs-lookup"><span data-stu-id="a6e47-453">When rendering to a multisample render target, D3DRS\_ANTIALIASEDLINEENABLE is ignored and all lines are rendered aliased.</span></span> <span data-ttu-id="a6e47-454">Verwenden Sie [**ID3DXLine**](id3dxline.md) für das Zeilen Rendering mit Antialiasing in einem Multisampling-Renderziel.</span><span class="sxs-lookup"><span data-stu-id="a6e47-454">Use [**ID3DXLine**](id3dxline.md) for antialiased line rendering in a multisample render target.</span></span>

</dd> <dt>

<span data-ttu-id="a6e47-455"><span id="D3DRS_MINTESSELLATIONLEVEL"></span><span id="d3drs_mintessellationlevel"></span>**D3DRS \_ mintmeellationlevel**</span><span class="sxs-lookup"><span data-stu-id="a6e47-455"><span id="D3DRS_MINTESSELLATIONLEVEL"></span><span id="d3drs_mintessellationlevel"></span>**D3DRS\_MINTESSELLATIONLEVEL**</span></span>
</dt> <dd>

<span data-ttu-id="a6e47-456">Minimale Mosaik Ebene.</span><span class="sxs-lookup"><span data-stu-id="a6e47-456">Minimum tessellation level.</span></span> <span data-ttu-id="a6e47-457">Der Standardwert ist 1.0 f.</span><span class="sxs-lookup"><span data-stu-id="a6e47-457">The default value is 1.0f.</span></span> <span data-ttu-id="a6e47-458">Weitere Informationen finden Sie unter Mosaik [(Direct3D 9)](tessellation.md).</span><span class="sxs-lookup"><span data-stu-id="a6e47-458">See [Tessellation (Direct3D 9)](tessellation.md).</span></span>

</dd> <dt>

<span data-ttu-id="a6e47-459"><span id="D3DRS_MAXTESSELLATIONLEVEL"></span><span id="d3drs_maxtessellationlevel"></span>**D3DRS \_ maxtmeellationlevel**</span><span class="sxs-lookup"><span data-stu-id="a6e47-459"><span id="D3DRS_MAXTESSELLATIONLEVEL"></span><span id="d3drs_maxtessellationlevel"></span>**D3DRS\_MAXTESSELLATIONLEVEL**</span></span>
</dt> <dd>

<span data-ttu-id="a6e47-460">Maximale Mosaik Ebene.</span><span class="sxs-lookup"><span data-stu-id="a6e47-460">Maximum tessellation level.</span></span> <span data-ttu-id="a6e47-461">Der Standardwert ist 1.0 f.</span><span class="sxs-lookup"><span data-stu-id="a6e47-461">The default value is 1.0f.</span></span> <span data-ttu-id="a6e47-462">Weitere Informationen finden Sie unter Mosaik [(Direct3D 9)](tessellation.md).</span><span class="sxs-lookup"><span data-stu-id="a6e47-462">See [Tessellation (Direct3D 9)](tessellation.md).</span></span>

</dd> <dt>

<span data-ttu-id="a6e47-463"><span id="D3DRS_ADAPTIVETESS_X"></span><span id="d3drs_adaptivetess_x"></span>**D3DRS \_ adaptivetess \_ X**</span><span class="sxs-lookup"><span data-stu-id="a6e47-463"><span id="D3DRS_ADAPTIVETESS_X"></span><span id="d3drs_adaptivetess_x"></span>**D3DRS\_ADAPTIVETESS\_X**</span></span>
</dt> <dd>

<span data-ttu-id="a6e47-464">In der x-Richtung auf adaptiver Mosaik Wert.</span><span class="sxs-lookup"><span data-stu-id="a6e47-464">Amount to adaptively tessellate, in the x direction.</span></span> <span data-ttu-id="a6e47-465">Der Standardwert ist 0,0 f.</span><span class="sxs-lookup"><span data-stu-id="a6e47-465">Default value is 0.0f.</span></span> <span data-ttu-id="a6e47-466">Weitere [Informationen](tessellation.md)finden Sie unter Adaptive Mosaik.</span><span class="sxs-lookup"><span data-stu-id="a6e47-466">See [Adaptive Tessellation](tessellation.md).</span></span>

</dd> <dt>

<span data-ttu-id="a6e47-467"><span id="D3DRS_ADAPTIVETESS_Y"></span><span id="d3drs_adaptivetess_y"></span>**D3DRS \_ adaptivetess \_ Y**</span><span class="sxs-lookup"><span data-stu-id="a6e47-467"><span id="D3DRS_ADAPTIVETESS_Y"></span><span id="d3drs_adaptivetess_y"></span>**D3DRS\_ADAPTIVETESS\_Y**</span></span>
</dt> <dd>

<span data-ttu-id="a6e47-468">In der y-Richtung auf adaptiver Mosaik Wert.</span><span class="sxs-lookup"><span data-stu-id="a6e47-468">Amount to adaptively tessellate, in the y direction.</span></span> <span data-ttu-id="a6e47-469">Der Standardwert ist 0,0 f.</span><span class="sxs-lookup"><span data-stu-id="a6e47-469">Default value is 0.0f.</span></span> <span data-ttu-id="a6e47-470">Weitere [ \_ Informationen](tessellation.md)finden Sie unter Adaptive Mosaik.</span><span class="sxs-lookup"><span data-stu-id="a6e47-470">See [Adaptive\_Tessellation](tessellation.md).</span></span>

</dd> <dt>

<span data-ttu-id="a6e47-471"><span id="D3DRS_ADAPTIVETESS_Z"></span><span id="d3drs_adaptivetess_z"></span>**D3DRS \_ adaptivetess \_ Z**</span><span class="sxs-lookup"><span data-stu-id="a6e47-471"><span id="D3DRS_ADAPTIVETESS_Z"></span><span id="d3drs_adaptivetess_z"></span>**D3DRS\_ADAPTIVETESS\_Z**</span></span>
</dt> <dd>

<span data-ttu-id="a6e47-472">Zu adaptiver Mosaik Wert in der z-Richtung.</span><span class="sxs-lookup"><span data-stu-id="a6e47-472">Amount to adaptively tessellate, in the z direction.</span></span> <span data-ttu-id="a6e47-473">Der Standardwert ist 1.0 f.</span><span class="sxs-lookup"><span data-stu-id="a6e47-473">Default value is 1.0f.</span></span> <span data-ttu-id="a6e47-474">Weitere [ \_ Informationen](tessellation.md)finden Sie unter Adaptive Mosaik.</span><span class="sxs-lookup"><span data-stu-id="a6e47-474">See [Adaptive\_Tessellation](tessellation.md).</span></span>

</dd> <dt>

<span data-ttu-id="a6e47-475"><span id="D3DRS_ADAPTIVETESS_W"></span><span id="d3drs_adaptivetess_w"></span>**D3DRS \_ adaptivetess \_ W**</span><span class="sxs-lookup"><span data-stu-id="a6e47-475"><span id="D3DRS_ADAPTIVETESS_W"></span><span id="d3drs_adaptivetess_w"></span>**D3DRS\_ADAPTIVETESS\_W**</span></span>
</dt> <dd>

<span data-ttu-id="a6e47-476">In der w-Richtung auf adaptiver Mosaik Wert.</span><span class="sxs-lookup"><span data-stu-id="a6e47-476">Amount to adaptively tessellate, in the w direction.</span></span> <span data-ttu-id="a6e47-477">Der Standardwert ist 0,0 f.</span><span class="sxs-lookup"><span data-stu-id="a6e47-477">Default value is 0.0f.</span></span> <span data-ttu-id="a6e47-478">Weitere [ \_ Informationen](tessellation.md)finden Sie unter Adaptive Mosaik.</span><span class="sxs-lookup"><span data-stu-id="a6e47-478">See [Adaptive\_Tessellation](tessellation.md).</span></span>

</dd> <dt>

<span data-ttu-id="a6e47-479"><span id="D3DRS_ENABLEADAPTIVETESSELLATION"></span><span id="d3drs_enableadaptivetessellation"></span>**D3DRS \_ enableadaptivetess**</span><span class="sxs-lookup"><span data-stu-id="a6e47-479"><span id="D3DRS_ENABLEADAPTIVETESSELLATION"></span><span id="d3drs_enableadaptivetessellation"></span>**D3DRS\_ENABLEADAPTIVETESSELLATION**</span></span>
</dt> <dd>

<span data-ttu-id="a6e47-480">" **True** ", um das adaptive Mosaik zu aktivieren, " **false** ", um es zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="a6e47-480">**TRUE** to enable adaptive tessellation, **FALSE** to disable it.</span></span> <span data-ttu-id="a6e47-481">Der Standardwert ist **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="a6e47-481">The default value is **FALSE**.</span></span> <span data-ttu-id="a6e47-482">Weitere [ \_ Informationen](tessellation.md)finden Sie unter Adaptive Mosaik.</span><span class="sxs-lookup"><span data-stu-id="a6e47-482">See [Adaptive\_Tessellation](tessellation.md).</span></span>

</dd> <dt>

<span data-ttu-id="a6e47-483"><span id="D3DRS_TWOSIDEDSTENCILMODE"></span><span id="d3drs_twosidedstencilmode"></span>**D3DRS \_ twosidedstencilmode**</span><span class="sxs-lookup"><span data-stu-id="a6e47-483"><span id="D3DRS_TWOSIDEDSTENCILMODE"></span><span id="d3drs_twosidedstencilmode"></span>**D3DRS\_TWOSIDEDSTENCILMODE**</span></span>
</dt> <dd>

<span data-ttu-id="a6e47-484">**True** aktiviert die zweiseitige Schablone, **false** deaktiviert sie.</span><span class="sxs-lookup"><span data-stu-id="a6e47-484">**TRUE** enables two-sided stenciling, **FALSE** disables it.</span></span> <span data-ttu-id="a6e47-485">Der Standardwert ist **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="a6e47-485">The default value is **FALSE**.</span></span> <span data-ttu-id="a6e47-486">Die Anwendung sollte D3DRS \_ CullMode auf D3DCULL \_ None festlegen, um den zweiseitigen Schablonen Modus zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="a6e47-486">The application should set D3DRS\_CULLMODE to D3DCULL\_NONE to enable two-sided stencil mode.</span></span> <span data-ttu-id="a6e47-487">Wenn die dreieckige Reihenfolge im Uhrzeigersinn liegt, werden die D3DRS \_ Stencil- \* Vorgänge verwendet.</span><span class="sxs-lookup"><span data-stu-id="a6e47-487">If the triangle winding order is clockwise, the D3DRS\_STENCIL\* operations will be used.</span></span> <span data-ttu-id="a6e47-488">Wenn die Sortierreihenfolge gegen den Uhrzeigersinn steht, werden die D3DRS \_ CCW- \_ Schablone- \* Vorgänge verwendet.</span><span class="sxs-lookup"><span data-stu-id="a6e47-488">If the winding order is counterclockwise, the D3DRS\_CCW\_STENCIL\* operations will be used.</span></span>

<span data-ttu-id="a6e47-489">Um festzustellen, ob zweiseitige Schablonen unterstützt werden, überprüfen Sie das Schablone-Element von [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) für D3DSTENCILCAPS \_ twotional.</span><span class="sxs-lookup"><span data-stu-id="a6e47-489">To see if two-sided stencil is supported, check the StencilCaps member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) for D3DSTENCILCAPS\_TWOSIDED.</span></span> <span data-ttu-id="a6e47-490">Siehe auch [D3DSTENCILCAPS](d3dstencilcaps.md).</span><span class="sxs-lookup"><span data-stu-id="a6e47-490">See also [D3DSTENCILCAPS](d3dstencilcaps.md).</span></span>

</dd> <dt>

<span data-ttu-id="a6e47-491"><span id="D3DRS_CCW_STENCILFAIL"></span><span id="d3drs_ccw_stencilfail"></span>**D3DRS \_ CCW \_ stencilfail**</span><span class="sxs-lookup"><span data-stu-id="a6e47-491"><span id="D3DRS_CCW_STENCILFAIL"></span><span id="d3drs_ccw_stencilfail"></span>**D3DRS\_CCW\_STENCILFAIL**</span></span>
</dt> <dd>

<span data-ttu-id="a6e47-492">Der Schablonen Vorgang, der ausgeführt werden soll, wenn der CCW-Schablonen Test fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="a6e47-492">Stencil operation to perform if CCW stencil test fails.</span></span> <span data-ttu-id="a6e47-493">Werte stammen aus dem [**D3DSTENCILOP**](./d3dstencilop.md) -Enumerationstyp.</span><span class="sxs-lookup"><span data-stu-id="a6e47-493">Values are from the [**D3DSTENCILOP**](./d3dstencilop.md) enumerated type.</span></span> <span data-ttu-id="a6e47-494">Der Standardwert ist D3DSTENCILOP \_ Keep.</span><span class="sxs-lookup"><span data-stu-id="a6e47-494">The default value is D3DSTENCILOP\_KEEP.</span></span>

</dd> <dt>

<span data-ttu-id="a6e47-495"><span id="D3DRS_CCW_STENCILZFAIL"></span><span id="d3drs_ccw_stencilzfail"></span>**D3DRS \_ CCW \_ stencilzfail**</span><span class="sxs-lookup"><span data-stu-id="a6e47-495"><span id="D3DRS_CCW_STENCILZFAIL"></span><span id="d3drs_ccw_stencilzfail"></span>**D3DRS\_CCW\_STENCILZFAIL**</span></span>
</dt> <dd>

<span data-ttu-id="a6e47-496">Der Schablonen Vorgang, der ausgeführt werden soll, wenn der CCW-Schablonen Test erfolgreich verläuft und z-Test fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="a6e47-496">Stencil operation to perform if CCW stencil test passes and z-test fails.</span></span> <span data-ttu-id="a6e47-497">Werte stammen aus dem [**D3DSTENCILOP**](./d3dstencilop.md) -Enumerationstyp.</span><span class="sxs-lookup"><span data-stu-id="a6e47-497">Values are from the [**D3DSTENCILOP**](./d3dstencilop.md) enumerated type.</span></span> <span data-ttu-id="a6e47-498">Der Standardwert ist D3DSTENCILOP \_ Keep.</span><span class="sxs-lookup"><span data-stu-id="a6e47-498">The default value is D3DSTENCILOP\_KEEP.</span></span>

</dd> <dt>

<span data-ttu-id="a6e47-499"><span id="D3DRS_CCW_STENCILPASS"></span><span id="d3drs_ccw_stencilpass"></span>**D3DRS \_ CCW \_ stencilpass**</span><span class="sxs-lookup"><span data-stu-id="a6e47-499"><span id="D3DRS_CCW_STENCILPASS"></span><span id="d3drs_ccw_stencilpass"></span>**D3DRS\_CCW\_STENCILPASS**</span></span>
</dt> <dd>

<span data-ttu-id="a6e47-500">Der Schablonen Vorgang, der ausgeführt werden soll, wenn die CCW-Schablone und die z-Tests bestanden werden.</span><span class="sxs-lookup"><span data-stu-id="a6e47-500">Stencil operation to perform if both CCW stencil and z-tests pass.</span></span> <span data-ttu-id="a6e47-501">Werte stammen aus dem [**D3DSTENCILOP**](./d3dstencilop.md) -Enumerationstyp.</span><span class="sxs-lookup"><span data-stu-id="a6e47-501">Values are from the [**D3DSTENCILOP**](./d3dstencilop.md) enumerated type.</span></span> <span data-ttu-id="a6e47-502">Der Standardwert ist D3DSTENCILOP \_ Keep.</span><span class="sxs-lookup"><span data-stu-id="a6e47-502">The default value is D3DSTENCILOP\_KEEP.</span></span>

</dd> <dt>

<span data-ttu-id="a6e47-503"><span id="D3DRS_CCW_STENCILFUNC"></span><span id="d3drs_ccw_stencilfunc"></span>**D3DRS \_ CCW \_ stencilfunc**</span><span class="sxs-lookup"><span data-stu-id="a6e47-503"><span id="D3DRS_CCW_STENCILFUNC"></span><span id="d3drs_ccw_stencilfunc"></span>**D3DRS\_CCW\_STENCILFUNC**</span></span>
</dt> <dd>

<span data-ttu-id="a6e47-504">Die Vergleichsfunktion.</span><span class="sxs-lookup"><span data-stu-id="a6e47-504">The comparison function.</span></span> <span data-ttu-id="a6e47-505">Der CCW-Schablone-Test wird durchgeführt, wenn ((Ref & Mask) die Schablone-Funktion (Schablone & Mask)) " **true**" ist.</span><span class="sxs-lookup"><span data-stu-id="a6e47-505">CCW stencil test passes if ((ref & mask) stencil function (stencil & mask)) is **TRUE**.</span></span> <span data-ttu-id="a6e47-506">Werte stammen aus dem [**D3DCMPFUNC**](./d3dcmpfunc.md) -Enumerationstyp.</span><span class="sxs-lookup"><span data-stu-id="a6e47-506">Values are from the [**D3DCMPFUNC**](./d3dcmpfunc.md) enumerated type.</span></span> <span data-ttu-id="a6e47-507">Der Standardwert ist D3DCMP \_ Always.</span><span class="sxs-lookup"><span data-stu-id="a6e47-507">The default value is D3DCMP\_ALWAYS.</span></span>

</dd> <dt>

<span data-ttu-id="a6e47-508"><span id="D3DRS_COLORWRITEENABLE1"></span><span id="d3drs_colorwriteenable1"></span>**D3DRS \_ COLORWRITEENABLE1**</span><span class="sxs-lookup"><span data-stu-id="a6e47-508"><span id="D3DRS_COLORWRITEENABLE1"></span><span id="d3drs_colorwriteenable1"></span>**D3DRS\_COLORWRITEENABLE1**</span></span>
</dt> <dd>

<span data-ttu-id="a6e47-509">Zusätzliche colorschreiteenable-Werte für die Geräte.</span><span class="sxs-lookup"><span data-stu-id="a6e47-509">Additional ColorWriteEnable values for the devices.</span></span> <span data-ttu-id="a6e47-510">Weitere Informationen finden Sie unter D3DRS \_ colorschreiteenable.</span><span class="sxs-lookup"><span data-stu-id="a6e47-510">See D3DRS\_COLORWRITEENABLE.</span></span> <span data-ttu-id="a6e47-511">Diese Funktionalität ist verfügbar, wenn das D3DPMISCCAPS \_ independentwrite temasks-Funktionen-Bit im primitivefehlcaps-Member der [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) -Struktur für das Gerät festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="a6e47-511">This functionality is available if the D3DPMISCCAPS\_INDEPENDENTWRITEMASKS capabilities bit is set in the PrimitiveMiscCaps member of the [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure for the device.</span></span> <span data-ttu-id="a6e47-512">Der Standardwert ist 0x0000000f.</span><span class="sxs-lookup"><span data-stu-id="a6e47-512">The default value is 0x0000000f.</span></span>

</dd> <dt>

<span data-ttu-id="a6e47-513"><span id="D3DRS_COLORWRITEENABLE2"></span><span id="d3drs_colorwriteenable2"></span>**D3DRS \_ COLORWRITEENABLE2**</span><span class="sxs-lookup"><span data-stu-id="a6e47-513"><span id="D3DRS_COLORWRITEENABLE2"></span><span id="d3drs_colorwriteenable2"></span>**D3DRS\_COLORWRITEENABLE2**</span></span>
</dt> <dd>

<span data-ttu-id="a6e47-514">Zusätzliche colorschreiteenable-Werte für die Geräte.</span><span class="sxs-lookup"><span data-stu-id="a6e47-514">Additional ColorWriteEnable values for the devices.</span></span> <span data-ttu-id="a6e47-515">Weitere Informationen finden Sie unter D3DRS \_ colorschreiteenable.</span><span class="sxs-lookup"><span data-stu-id="a6e47-515">See D3DRS\_COLORWRITEENABLE.</span></span> <span data-ttu-id="a6e47-516">Diese Funktionalität ist verfügbar, wenn das D3DPMISCCAPS \_ independentwrite temasks-Funktionen-Bit im primitivefehlcaps-Member der [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) -Struktur für das Gerät festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="a6e47-516">This functionality is available if the D3DPMISCCAPS\_INDEPENDENTWRITEMASKS capabilities bit is set in the PrimitiveMiscCaps member of the [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure for the device.</span></span> <span data-ttu-id="a6e47-517">Der Standardwert ist 0x0000000f.</span><span class="sxs-lookup"><span data-stu-id="a6e47-517">The default value is 0x0000000f.</span></span>

</dd> <dt>

<span data-ttu-id="a6e47-518"><span id="D3DRS_COLORWRITEENABLE3"></span><span id="d3drs_colorwriteenable3"></span>**D3DRS \_ COLORWRITEENABLE3**</span><span class="sxs-lookup"><span data-stu-id="a6e47-518"><span id="D3DRS_COLORWRITEENABLE3"></span><span id="d3drs_colorwriteenable3"></span>**D3DRS\_COLORWRITEENABLE3**</span></span>
</dt> <dd>

<span data-ttu-id="a6e47-519">Zusätzliche colorschreiteenable-Werte für die Geräte.</span><span class="sxs-lookup"><span data-stu-id="a6e47-519">Additional ColorWriteEnable values for the devices.</span></span> <span data-ttu-id="a6e47-520">Weitere Informationen finden Sie unter D3DRS \_ colorschreiteenable.</span><span class="sxs-lookup"><span data-stu-id="a6e47-520">See D3DRS\_COLORWRITEENABLE.</span></span> <span data-ttu-id="a6e47-521">Diese Funktionalität ist verfügbar, wenn das D3DPMISCCAPS \_ independentwrite temasks-Funktionen-Bit im primitivefehlcaps-Member der [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) -Struktur für das Gerät festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="a6e47-521">This functionality is available if the D3DPMISCCAPS\_INDEPENDENTWRITEMASKS capabilities bit is set in the PrimitiveMiscCaps member of the [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure for the device.</span></span> <span data-ttu-id="a6e47-522">Der Standardwert ist 0x0000000f.</span><span class="sxs-lookup"><span data-stu-id="a6e47-522">The default value is 0x0000000f.</span></span>

</dd> <dt>

<span data-ttu-id="a6e47-523"><span id="D3DRS_BLENDFACTOR"></span><span id="d3drs_blendfactor"></span>**D3DRS \_ blendfactor**</span><span class="sxs-lookup"><span data-stu-id="a6e47-523"><span id="D3DRS_BLENDFACTOR"></span><span id="d3drs_blendfactor"></span>**D3DRS\_BLENDFACTOR**</span></span>
</dt> <dd>

<span data-ttu-id="a6e47-524">[**D3DCOLOR**](d3dcolor.md) wird für einen konstanten Blend-Faktor während der Alpha Mischung verwendet.</span><span class="sxs-lookup"><span data-stu-id="a6e47-524">[**D3DCOLOR**](d3dcolor.md) used for a constant blend-factor during alpha blending.</span></span> <span data-ttu-id="a6e47-525">Diese Funktionalität ist verfügbar, wenn das D3DPBLENDCAPS \_ blendfactor-Funktionen-Bit im srcblendcaps-Member von [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) oder dem destblendcaps-Member von **D3DCAPS9** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="a6e47-525">This functionality is available if the D3DPBLENDCAPS\_BLENDFACTOR capabilities bit is set in the SrcBlendCaps member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) or the DestBlendCaps member of **D3DCAPS9**.</span></span> <span data-ttu-id="a6e47-526">Siehe [**D3DRENDERSTATETYPE**]().</span><span class="sxs-lookup"><span data-stu-id="a6e47-526">See [**D3DRENDERSTATETYPE**]().</span></span> <span data-ttu-id="a6e47-527">Der Standardwert ist 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="a6e47-527">The default value is 0xffffffff.</span></span>

</dd> <dt>

<span data-ttu-id="a6e47-528"><span id="D3DRS_SRGBWRITEENABLE"></span><span id="d3drs_srgbwriteenable"></span>**D3DRS \_ srgbschreiteenable**</span><span class="sxs-lookup"><span data-stu-id="a6e47-528"><span id="D3DRS_SRGBWRITEENABLE"></span><span id="d3drs_srgbwriteenable"></span>**D3DRS\_SRGBWRITEENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="a6e47-529">Renderziel-Schreibvorgänge für die Gammakorrektur in sRGB aktivieren.</span><span class="sxs-lookup"><span data-stu-id="a6e47-529">Enable render-target writes to be gamma corrected to sRGB.</span></span> <span data-ttu-id="a6e47-530">Das Format muss D3DUSAGE \_ srgbwrite verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="a6e47-530">The format must expose D3DUSAGE\_SRGBWRITE.</span></span> <span data-ttu-id="a6e47-531">Der Standardwert ist 0.</span><span class="sxs-lookup"><span data-stu-id="a6e47-531">The default value is 0.</span></span>

</dd> <dt>

<span data-ttu-id="a6e47-532"><span id="D3DRS_DEPTHBIAS"></span><span id="d3drs_depthbias"></span>**D3DRS \_ depthbias**</span><span class="sxs-lookup"><span data-stu-id="a6e47-532"><span id="D3DRS_DEPTHBIAS"></span><span id="d3drs_depthbias"></span>**D3DRS\_DEPTHBIAS**</span></span>
</dt> <dd>

<span data-ttu-id="a6e47-533">Ein Gleit Komma Wert, der für den Vergleich von tiefen Werten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a6e47-533">A floating-point value that is used for comparison of depth values.</span></span> <span data-ttu-id="a6e47-534">Siehe [tiefen Bias (Direct3D 9)](depth-bias.md).</span><span class="sxs-lookup"><span data-stu-id="a6e47-534">See [Depth Bias (Direct3D 9)](depth-bias.md).</span></span> <span data-ttu-id="a6e47-535">Der Standardwert ist 0.</span><span class="sxs-lookup"><span data-stu-id="a6e47-535">The default value is 0.</span></span>

</dd> <dt>

<span data-ttu-id="a6e47-536"><span id="D3DRS_WRAP8"></span><span id="d3drs_wrap8"></span>**D3DRS \_ WRAP8**</span><span class="sxs-lookup"><span data-stu-id="a6e47-536"><span id="D3DRS_WRAP8"></span><span id="d3drs_wrap8"></span>**D3DRS\_WRAP8**</span></span>
</dt> <dd>

<span data-ttu-id="a6e47-537">Siehe D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="a6e47-537">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="a6e47-538"><span id="D3DRS_WRAP9"></span><span id="d3drs_wrap9"></span>**D3DRS \_ WRAP9**</span><span class="sxs-lookup"><span data-stu-id="a6e47-538"><span id="D3DRS_WRAP9"></span><span id="d3drs_wrap9"></span>**D3DRS\_WRAP9**</span></span>
</dt> <dd>

<span data-ttu-id="a6e47-539">Siehe D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="a6e47-539">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="a6e47-540"><span id="D3DRS_WRAP10"></span><span id="d3drs_wrap10"></span>**D3DRS \_ WRAP10**</span><span class="sxs-lookup"><span data-stu-id="a6e47-540"><span id="D3DRS_WRAP10"></span><span id="d3drs_wrap10"></span>**D3DRS\_WRAP10**</span></span>
</dt> <dd>

<span data-ttu-id="a6e47-541">Siehe D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="a6e47-541">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="a6e47-542"><span id="D3DRS_WRAP11"></span><span id="d3drs_wrap11"></span>**D3DRS \_ WRAP11**</span><span class="sxs-lookup"><span data-stu-id="a6e47-542"><span id="D3DRS_WRAP11"></span><span id="d3drs_wrap11"></span>**D3DRS\_WRAP11**</span></span>
</dt> <dd>

<span data-ttu-id="a6e47-543">Siehe D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="a6e47-543">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="a6e47-544"><span id="D3DRS_WRAP12"></span><span id="d3drs_wrap12"></span>**D3DRS \_ WRAP12**</span><span class="sxs-lookup"><span data-stu-id="a6e47-544"><span id="D3DRS_WRAP12"></span><span id="d3drs_wrap12"></span>**D3DRS\_WRAP12**</span></span>
</dt> <dd>

<span data-ttu-id="a6e47-545">Siehe D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="a6e47-545">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="a6e47-546"><span id="D3DRS_WRAP13"></span><span id="d3drs_wrap13"></span>**D3DRS \_ WRAP13**</span><span class="sxs-lookup"><span data-stu-id="a6e47-546"><span id="D3DRS_WRAP13"></span><span id="d3drs_wrap13"></span>**D3DRS\_WRAP13**</span></span>
</dt> <dd>

<span data-ttu-id="a6e47-547">Siehe D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="a6e47-547">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="a6e47-548"><span id="D3DRS_WRAP14"></span><span id="d3drs_wrap14"></span>**D3DRS \_ WRAP14**</span><span class="sxs-lookup"><span data-stu-id="a6e47-548"><span id="D3DRS_WRAP14"></span><span id="d3drs_wrap14"></span>**D3DRS\_WRAP14**</span></span>
</dt> <dd>

<span data-ttu-id="a6e47-549">Siehe D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="a6e47-549">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="a6e47-550"><span id="D3DRS_WRAP15"></span><span id="d3drs_wrap15"></span>**D3DRS \_ WRAP15**</span><span class="sxs-lookup"><span data-stu-id="a6e47-550"><span id="D3DRS_WRAP15"></span><span id="d3drs_wrap15"></span>**D3DRS\_WRAP15**</span></span>
</dt> <dd>

<span data-ttu-id="a6e47-551">Siehe D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="a6e47-551">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="a6e47-552"><span id="D3DRS_SEPARATEALPHABLENDENABLE"></span><span id="d3drs_separatealphablendenable"></span>**D3DRS \_ separatealphablendenable**</span><span class="sxs-lookup"><span data-stu-id="a6e47-552"><span id="D3DRS_SEPARATEALPHABLENDENABLE"></span><span id="d3drs_separatealphablendenable"></span>**D3DRS\_SEPARATEALPHABLENDENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="a6e47-553">**True** aktiviert den separaten Blend-Modus für den Alphakanal.</span><span class="sxs-lookup"><span data-stu-id="a6e47-553">**TRUE** enables the separate blend mode for the alpha channel.</span></span> <span data-ttu-id="a6e47-554">Der Standardwert ist **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="a6e47-554">The default value is **FALSE**.</span></span>

<span data-ttu-id="a6e47-555">Wenn diese Einstellung auf " **false**" festgelegt ist, werden die auf Alpha angewendeten Mischungs Ziel Faktoren und-Vorgänge mit den für die Farbe definierten Vorgängen erzwungen.</span><span class="sxs-lookup"><span data-stu-id="a6e47-555">When set to **FALSE**, the render-target blending factors and operations applied to alpha are forced to be the same as those defined for color.</span></span> <span data-ttu-id="a6e47-556">Dieser Modus ist für Implementierungen, die nicht die Cap-D3DPMISCCAPS-Trennzeichen festgelegt haben, auf **false** festgelegt \_ .</span><span class="sxs-lookup"><span data-stu-id="a6e47-556">This mode is effectively hardwired to **FALSE** on implementations that don't set the cap D3DPMISCCAPS\_SEPARATEALPHABLEND.</span></span> <span data-ttu-id="a6e47-557">Siehe [D3DPMISCCAPS](d3dpmisccaps.md).</span><span class="sxs-lookup"><span data-stu-id="a6e47-557">See [D3DPMISCCAPS](d3dpmisccaps.md).</span></span>

<span data-ttu-id="a6e47-558">Der Typ der separaten Alpha Mischung wird durch die \_ Rendering-Zustände D3DRS srcblendalpha und D3DRS \_ destblendalpha bestimmt.</span><span class="sxs-lookup"><span data-stu-id="a6e47-558">The type of separate alpha blending is determined by the D3DRS\_SRCBLENDALPHA and D3DRS\_DESTBLENDALPHA render states.</span></span>

</dd> <dt>

<span data-ttu-id="a6e47-559"><span id="D3DRS_SRCBLENDALPHA"></span><span id="d3drs_srcblendalpha"></span>**D3DRS \_ srcblendalpha**</span><span class="sxs-lookup"><span data-stu-id="a6e47-559"><span id="D3DRS_SRCBLENDALPHA"></span><span id="d3drs_srcblendalpha"></span>**D3DRS\_SRCBLENDALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="a6e47-560">Ein Member des [**D3DBLEND**](./d3dblend.md) -Enumerationstyps.</span><span class="sxs-lookup"><span data-stu-id="a6e47-560">One member of the [**D3DBLEND**](./d3dblend.md) enumerated type.</span></span> <span data-ttu-id="a6e47-561">Dieser Wert wird ignoriert, es sei denn, D3DRS \_ separatealphablendenable ist " **true**".</span><span class="sxs-lookup"><span data-stu-id="a6e47-561">This value is ignored unless D3DRS\_SEPARATEALPHABLENDENABLE is **TRUE**.</span></span> <span data-ttu-id="a6e47-562">Der Standardwert ist D3DBLEND \_ 1.</span><span class="sxs-lookup"><span data-stu-id="a6e47-562">The default value is D3DBLEND\_ONE.</span></span>

</dd> <dt>

<span data-ttu-id="a6e47-563"><span id="D3DRS_DESTBLENDALPHA"></span><span id="d3drs_destblendalpha"></span>**D3DRS \_ destblendalpha**</span><span class="sxs-lookup"><span data-stu-id="a6e47-563"><span id="D3DRS_DESTBLENDALPHA"></span><span id="d3drs_destblendalpha"></span>**D3DRS\_DESTBLENDALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="a6e47-564">Ein Member des [**D3DBLEND**](./d3dblend.md) -Enumerationstyps.</span><span class="sxs-lookup"><span data-stu-id="a6e47-564">One member of the [**D3DBLEND**](./d3dblend.md) enumerated type.</span></span> <span data-ttu-id="a6e47-565">Dieser Wert wird ignoriert, es sei denn, D3DRS \_ separatealphablendenable ist " **true**".</span><span class="sxs-lookup"><span data-stu-id="a6e47-565">This value is ignored unless D3DRS\_SEPARATEALPHABLENDENABLE is **TRUE**.</span></span> <span data-ttu-id="a6e47-566">Der Standardwert ist D3DBLEND \_ 0 (null).</span><span class="sxs-lookup"><span data-stu-id="a6e47-566">The default value is D3DBLEND\_ZERO.</span></span>

</dd> <dt>

<span data-ttu-id="a6e47-567"><span id="D3DRS_BLENDOPALPHA"></span><span id="d3drs_blendopalpha"></span>**D3DRS \_ blendopalpha**</span><span class="sxs-lookup"><span data-stu-id="a6e47-567"><span id="D3DRS_BLENDOPALPHA"></span><span id="d3drs_blendopalpha"></span>**D3DRS\_BLENDOPALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="a6e47-568">Der Wert, der zum Auswählen der arithmetischen Operation verwendet wird, die auf separate Alpha Blending angewendet wird, wenn der Rendering-Zustand, D3DRS \_ separatealphablendenable, auf **true** festgelegt ist</span><span class="sxs-lookup"><span data-stu-id="a6e47-568">Value used to select the arithmetic operation applied to separate alpha blending when the render state, D3DRS\_SEPARATEALPHABLENDENABLE, is set to **TRUE**.</span></span>

<span data-ttu-id="a6e47-569">Gültige Werte werden durch den [**D3DBLENDOP**](./d3dblendop.md) -enumerierten Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="a6e47-569">Valid values are defined by the [**D3DBLENDOP**](./d3dblendop.md) enumerated type.</span></span> <span data-ttu-id="a6e47-570">Der Standardwert ist D3DBLENDOP \_ Add.</span><span class="sxs-lookup"><span data-stu-id="a6e47-570">The default value is D3DBLENDOP\_ADD.</span></span>

<span data-ttu-id="a6e47-571">Wenn die D3DPMISCCAPS \_ blendop-Geräte Funktion nicht unterstützt wird, \_ wird D3DBLENDOP Add ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a6e47-571">If the D3DPMISCCAPS\_BLENDOP device capability is not supported, then D3DBLENDOP\_ADD is performed.</span></span> <span data-ttu-id="a6e47-572">Siehe [D3DPMISCCAPS](d3dpmisccaps.md).</span><span class="sxs-lookup"><span data-stu-id="a6e47-572">See [D3DPMISCCAPS](d3dpmisccaps.md).</span></span>

</dd> <dt>

<span data-ttu-id="a6e47-573"><span id="D3DRS_FORCE_DWORD"></span><span id="d3drs_force_dword"></span>**D3DRS \_ Erzwingen von \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="a6e47-573"><span id="D3DRS_FORCE_DWORD"></span><span id="d3drs_force_dword"></span>**D3DRS\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="a6e47-574">Erzwingt die Kompilierung dieser Enumeration in 32 Bits.</span><span class="sxs-lookup"><span data-stu-id="a6e47-574">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="a6e47-575">Ohne diesen Wert können einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="a6e47-575">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="a6e47-576">Dieser Wert wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="a6e47-576">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a6e47-577">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a6e47-577">Remarks</span></span>



| <span data-ttu-id="a6e47-578">Rendering-Zustände</span><span class="sxs-lookup"><span data-stu-id="a6e47-578">Render States</span></span>        |                    |
|----------------------|--------------------|
| <span data-ttu-id="a6e47-579">PS \_ 1 1 \_ bis PS \_ 1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="a6e47-579">ps\_1\_1 to ps\_1\_3</span></span> | <span data-ttu-id="a6e47-580">vier Textur-Samplern</span><span class="sxs-lookup"><span data-stu-id="a6e47-580">4 texture samplers</span></span> |



 

<span data-ttu-id="a6e47-581">Direct3D definiert die D3DRENDERSTATE \_ wrapbias-Konstante als praktische Möglichkeit für Anwendungen, um die Textur Umbrüche basierend auf der NULL basierten Ganzzahl eines Texturkoordinaten Satzes (anstatt explizit einen der D3DRS Wrap n-Zustands Werte zu verwenden) zu aktivieren oder zu deaktivieren \_ .</span><span class="sxs-lookup"><span data-stu-id="a6e47-581">Direct3D defines the D3DRENDERSTATE\_WRAPBIAS constant as a convenience for applications to enable or disable texture wrapping, based on the zero-based integer of a texture coordinate set (rather than explicitly using one of the D3DRS\_WRAP n state values).</span></span> <span data-ttu-id="a6e47-582">Fügen Sie dem \_ NULL basierten Index eines Texturkoordinaten Satzes den D3DRENDERSTATE wrapbias-Wert hinzu, um den D3DRS \_ Wrap n-Wert zu berechnen, der diesem Index entspricht, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="a6e47-582">Add the D3DRENDERSTATE\_WRAPBIAS value to the zero-based index of a texture coordinate set to calculate the D3DRS\_WRAP n value that corresponds to that index, as shown in the following example.</span></span>


```
// Enable U/V wrapping for textures that use the texture 
// coordinate set at the index within the dwIndex variable
    
HRESULT hr = pd3dDevice->SetRenderState(
dwIndex + D3DRENDERSTATE_WRAPBIAS,  
D3DWRAPCOORD_0 | D3DWRAPCOORD_1);
     
// If dwIndex is 3, the value that results from 
// the addition equals D3DRS_WRAP3 (131)
```



## <a name="requirements"></a><span data-ttu-id="a6e47-583">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a6e47-583">Requirements</span></span>



| <span data-ttu-id="a6e47-584">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a6e47-584">Requirement</span></span> | <span data-ttu-id="a6e47-585">Wert</span><span class="sxs-lookup"><span data-stu-id="a6e47-585">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a6e47-586">Header</span><span class="sxs-lookup"><span data-stu-id="a6e47-586">Header</span></span><br/> | <dl> <span data-ttu-id="a6e47-587"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="a6e47-587"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6e47-588">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a6e47-588">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6e47-589">Direct3D-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="a6e47-589">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="a6e47-590">**IDirect3DDevice9::GetRenderState**</span><span class="sxs-lookup"><span data-stu-id="a6e47-590">**IDirect3DDevice9::GetRenderState**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getrenderstate)
</dt> <dt>

[<span data-ttu-id="a6e47-591">**IDirect3DDevice9:: \* Trend List State**</span><span class="sxs-lookup"><span data-stu-id="a6e47-591">**IDirect3DDevice9::SetRenderState**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate)
</dt> </dl>

 

 
