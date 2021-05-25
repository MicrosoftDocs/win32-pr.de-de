---
description: Renderzustände definieren Einrichtungszustände für alle Arten der Vertex- und Pixelverarbeitung.
ms.assetid: 2fd56388-f3bd-409f-876c-ae893840b623
title: D3DRENDERSTATETYPE-Enumeration (D3D9Types.h)
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
ms.openlocfilehash: 0a7ad803535032705e6e1bb5456109486c59d190
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343065"
---
# <a name="d3drenderstatetype-enumeration"></a><span data-ttu-id="70bd2-103">D3DRENDERSTATETYPE-Enumeration</span><span class="sxs-lookup"><span data-stu-id="70bd2-103">D3DRENDERSTATETYPE enumeration</span></span>

<span data-ttu-id="70bd2-104">Renderzustände definieren Einrichtungszustände für alle Arten der Vertex- und Pixelverarbeitung.</span><span class="sxs-lookup"><span data-stu-id="70bd2-104">Render states define set-up states for all kinds of vertex and pixel processing.</span></span> <span data-ttu-id="70bd2-105">Einige Renderzustände richten die Scheitelpunktverarbeitung ein, andere richten die Pixelverarbeitung ein (siehe [Renderzustände (Direct3D 9)](render-states.md)).</span><span class="sxs-lookup"><span data-stu-id="70bd2-105">Some render states set up vertex processing, and some set up pixel processing (see [Render States (Direct3D 9)](render-states.md)).</span></span> <span data-ttu-id="70bd2-106">Renderzustände können mit stateblocks gespeichert und wiederhergestellt werden (siehe [Zustandsblöcke Speichern und Wiederherstellen des Zustands (Direct3D 9)](state-blocks-save-and-restore-state.md)).</span><span class="sxs-lookup"><span data-stu-id="70bd2-106">Render states can be saved and restored using stateblocks (see [State Blocks Save and Restore State (Direct3D 9)](state-blocks-save-and-restore-state.md)).</span></span>

## <a name="syntax"></a><span data-ttu-id="70bd2-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="70bd2-107">Syntax</span></span>


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



## <a name="constants"></a><span data-ttu-id="70bd2-108">Konstanten</span><span class="sxs-lookup"><span data-stu-id="70bd2-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="70bd2-109"><span id="D3DRS_ZENABLE"></span><span id="d3drs_zenable"></span>**D3DRS \_ ZENABLE**</span><span class="sxs-lookup"><span data-stu-id="70bd2-109"><span id="D3DRS_ZENABLE"></span><span id="d3drs_zenable"></span>**D3DRS\_ZENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="70bd2-110">Tiefenpufferungszustand als member des [**D3DEINANDERUFFERTYPE-Enumerationstyps.**](./d3dzbuffertype.md)</span><span class="sxs-lookup"><span data-stu-id="70bd2-110">Depth-buffering state as one member of the [**D3DZBUFFERTYPE**](./d3dzbuffertype.md) enumerated type.</span></span> <span data-ttu-id="70bd2-111">Legen Sie diesen Zustand auf D3DFANG \_ TRUE fest, um die Z-Pufferung zu aktivieren, D3DFFE USEW zum Aktivieren der \_ W-Pufferung oder D3DFANG \_ FALSE, um die Tiefenpufferung zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="70bd2-111">Set this state to D3DZB\_TRUE to enable z-buffering, D3DZB\_USEW to enable w-buffering, or D3DZB\_FALSE to disable depth buffering.</span></span>

<span data-ttu-id="70bd2-112">Der Standardwert für diesen Renderzustand ist D3DEINANDER \_ TRUE, wenn eine Tiefenschablone zusammen mit der Swapkette erstellt wurde, indem der EnableAutoDepthStencil-Member der [**D3DPRESENT \_ PARAMETERS-Struktur**](d3dpresent-parameters.md) auf **TRUE** festgelegt wurde, andernfalls D3D \_ FALSE.</span><span class="sxs-lookup"><span data-stu-id="70bd2-112">The default value for this render state is D3DZB\_TRUE if a depth stencil was created along with the swap chain by setting the EnableAutoDepthStencil member of the [**D3DPRESENT\_PARAMETERS**](d3dpresent-parameters.md) structure to **TRUE**, and D3DZB\_FALSE otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="70bd2-113"><span id="D3DRS_FILLMODE"></span><span id="d3drs_fillmode"></span>**D3DRS \_ FILLMODE**</span><span class="sxs-lookup"><span data-stu-id="70bd2-113"><span id="D3DRS_FILLMODE"></span><span id="d3drs_fillmode"></span>**D3DRS\_FILLMODE**</span></span>
</dt> <dd>

<span data-ttu-id="70bd2-114">Mindestens ein Member des [**D3DFILLMODE-Enumerationstyps.**](./d3dfillmode.md)</span><span class="sxs-lookup"><span data-stu-id="70bd2-114">One or more members of the [**D3DFILLMODE**](./d3dfillmode.md) enumerated type.</span></span> <span data-ttu-id="70bd2-115">Der Standardwert ist D3DFILL \_ SOLID.</span><span class="sxs-lookup"><span data-stu-id="70bd2-115">The default value is D3DFILL\_SOLID.</span></span>

</dd> <dt>

<span data-ttu-id="70bd2-116"><span id="D3DRS_SHADEMODE"></span><span id="d3drs_shademode"></span>**D3DRS \_ SHADEMODE**</span><span class="sxs-lookup"><span data-stu-id="70bd2-116"><span id="D3DRS_SHADEMODE"></span><span id="d3drs_shademode"></span>**D3DRS\_SHADEMODE**</span></span>
</dt> <dd>

<span data-ttu-id="70bd2-117">Mindestens ein Member des [**D3DSHADEMODE-Enumerationstyps.**](./d3dshademode.md)</span><span class="sxs-lookup"><span data-stu-id="70bd2-117">One or more members of the [**D3DSHADEMODE**](./d3dshademode.md) enumerated type.</span></span> <span data-ttu-id="70bd2-118">Der Standardwert ist D3DSHADE \_ GOURAUD.</span><span class="sxs-lookup"><span data-stu-id="70bd2-118">The default value is D3DSHADE\_GOURAUD.</span></span>

</dd> <dt>

<span data-ttu-id="70bd2-119"><span id="D3DRS_ZWRITEENABLE"></span><span id="d3drs_zwriteenable"></span>**D3DRS \_ ZWRITEENABLE**</span><span class="sxs-lookup"><span data-stu-id="70bd2-119"><span id="D3DRS_ZWRITEENABLE"></span><span id="d3drs_zwriteenable"></span>**D3DRS\_ZWRITEENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="70bd2-120">**TRUE,** damit die Anwendung in den Tiefenpuffer schreiben kann.</span><span class="sxs-lookup"><span data-stu-id="70bd2-120">**TRUE** to enable the application to write to the depth buffer.</span></span> <span data-ttu-id="70bd2-121">Der Standardwert ist **TRUE.**</span><span class="sxs-lookup"><span data-stu-id="70bd2-121">The default value is **TRUE**.</span></span> <span data-ttu-id="70bd2-122">Mit diesem Member kann eine Anwendung verhindern, dass das System den Tiefenpuffer mit neuen Tiefenwerten aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="70bd2-122">This member enables an application to prevent the system from updating the depth buffer with new depth values.</span></span> <span data-ttu-id="70bd2-123">False **gibt** an, dass Tiefenvergleiche weiterhin gemäß dem Renderzustand D3DRSUNKUNC vorgenommen werden, vorausgesetzt, dass die Tiefenpufferung stattfindet, aber die Tiefenwerte werden nicht in den Puffer \_ geschrieben.</span><span class="sxs-lookup"><span data-stu-id="70bd2-123">If **FALSE**, depth comparisons are still made according to the render state D3DRS\_ZFUNC, assuming that depth buffering is taking place, but depth values are not written to the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="70bd2-124"><span id="D3DRS_ALPHATESTENABLE"></span><span id="d3drs_alphatestenable"></span>**D3DRS \_ ALPHATESTENABLE**</span><span class="sxs-lookup"><span data-stu-id="70bd2-124"><span id="D3DRS_ALPHATESTENABLE"></span><span id="d3drs_alphatestenable"></span>**D3DRS\_ALPHATESTENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="70bd2-125">**TRUE,** um Alphatests pro Pixel zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="70bd2-125">**TRUE** to enable per pixel alpha testing.</span></span> <span data-ttu-id="70bd2-126">Wenn der Test bestanden wird, wird das Pixel vom Framepuffer verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="70bd2-126">If the test passes, the pixel is processed by the frame buffer.</span></span> <span data-ttu-id="70bd2-127">Andernfalls wird die verarbeitung des Framepuffers für das Pixel übersprungen.</span><span class="sxs-lookup"><span data-stu-id="70bd2-127">Otherwise, all frame-buffer processing is skipped for the pixel.</span></span>

<span data-ttu-id="70bd2-128">Der Test erfolgt durch Vergleichen des eingehenden Alphawerts mit dem Alphawert des Verweises unter Verwendung der Vergleichsfunktion, die vom D3DRS \_ ALPHAFUNC-Renderzustand bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="70bd2-128">The test is done by comparing the incoming alpha value with the reference alpha value, using the comparison function provided by the D3DRS\_ALPHAFUNC render state.</span></span> <span data-ttu-id="70bd2-129">Der Alphawert des Verweises wird durch den für D3DRS \_ ALPHAREF festgelegten Wert bestimmt.</span><span class="sxs-lookup"><span data-stu-id="70bd2-129">The reference alpha value is determined by the value set for D3DRS\_ALPHAREF.</span></span> <span data-ttu-id="70bd2-130">Weitere Informationen finden Sie unter [Alpha Testing State (Direct3D 9)](alpha-testing-state.md).</span><span class="sxs-lookup"><span data-stu-id="70bd2-130">For more information, see [Alpha Testing State (Direct3D 9)](alpha-testing-state.md).</span></span>

<span data-ttu-id="70bd2-131">Der Standardwert dieses Parameters ist **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="70bd2-131">The default value of this parameter is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="70bd2-132"><span id="D3DRS_LASTPIXEL"></span><span id="d3drs_lastpixel"></span>**D3DRS \_ LASTPIXEL**</span><span class="sxs-lookup"><span data-stu-id="70bd2-132"><span id="D3DRS_LASTPIXEL"></span><span id="d3drs_lastpixel"></span>**D3DRS\_LASTPIXEL**</span></span>
</dt> <dd>

<span data-ttu-id="70bd2-133">Der Standardwert ist **TRUE,** wodurch das Zeichnen des letzten Pixels in einer Linie ermöglicht wird.</span><span class="sxs-lookup"><span data-stu-id="70bd2-133">The default value is **TRUE**, which enables drawing of the last pixel in a line.</span></span> <span data-ttu-id="70bd2-134">Um das Zeichnen des letzten Pixels zu verhindern, legen Sie diesen Wert auf **FALSE fest.**</span><span class="sxs-lookup"><span data-stu-id="70bd2-134">To prevent drawing of the last pixel, set this value to **FALSE**.</span></span> <span data-ttu-id="70bd2-135">Weitere Informationen finden Sie unter [Gliederungs- und Füllzustand (Direct3D 9).](outline-and-fill-state.md)</span><span class="sxs-lookup"><span data-stu-id="70bd2-135">For more information, see [Outline and Fill State (Direct3D 9)](outline-and-fill-state.md).</span></span>

</dd> <dt>

<span data-ttu-id="70bd2-136"><span id="D3DRS_SRCBLEND"></span><span id="d3drs_srcblend"></span>**D3DRS \_ SRCBLEND**</span><span class="sxs-lookup"><span data-stu-id="70bd2-136"><span id="D3DRS_SRCBLEND"></span><span id="d3drs_srcblend"></span>**D3DRS\_SRCBLEND**</span></span>
</dt> <dd>

<span data-ttu-id="70bd2-137">Ein Member des [**aufzählten D3DBLEND-Typs.**](./d3dblend.md)</span><span class="sxs-lookup"><span data-stu-id="70bd2-137">One member of the [**D3DBLEND**](./d3dblend.md) enumerated type.</span></span> <span data-ttu-id="70bd2-138">Der Standardwert ist D3DBLEND \_ ONE.</span><span class="sxs-lookup"><span data-stu-id="70bd2-138">The default value is D3DBLEND\_ONE.</span></span>

</dd> <dt>

<span data-ttu-id="70bd2-139"><span id="D3DRS_DESTBLEND"></span><span id="d3drs_destblend"></span>**D3DRS \_ DESTBLEND**</span><span class="sxs-lookup"><span data-stu-id="70bd2-139"><span id="D3DRS_DESTBLEND"></span><span id="d3drs_destblend"></span>**D3DRS\_DESTBLEND**</span></span>
</dt> <dd>

<span data-ttu-id="70bd2-140">Ein Member des [**aufzählten D3DBLEND-Typs.**](./d3dblend.md)</span><span class="sxs-lookup"><span data-stu-id="70bd2-140">One member of the [**D3DBLEND**](./d3dblend.md) enumerated type.</span></span> <span data-ttu-id="70bd2-141">Der Standardwert ist D3DBLEND \_ ZERO.</span><span class="sxs-lookup"><span data-stu-id="70bd2-141">The default value is D3DBLEND\_ZERO.</span></span>

</dd> <dt>

<span data-ttu-id="70bd2-142"><span id="D3DRS_CULLMODE"></span><span id="d3drs_cullmode"></span>**D3DRS \_ CULLMODE**</span><span class="sxs-lookup"><span data-stu-id="70bd2-142"><span id="D3DRS_CULLMODE"></span><span id="d3drs_cullmode"></span>**D3DRS\_CULLMODE**</span></span>
</dt> <dd>

<span data-ttu-id="70bd2-143">Gibt an, wie rückwärts gerichtete Dreiecke , wenn überhaupt, culled werden.</span><span class="sxs-lookup"><span data-stu-id="70bd2-143">Specifies how back-facing triangles are culled, if at all.</span></span> <span data-ttu-id="70bd2-144">Dieser kann auf einen Member des [**D3DCULL-Enumerationstyps**](./d3dcull.md) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="70bd2-144">This can be set to one member of the [**D3DCULL**](./d3dcull.md) enumerated type.</span></span> <span data-ttu-id="70bd2-145">Der Standardwert ist D3DCULL \_ CCW.</span><span class="sxs-lookup"><span data-stu-id="70bd2-145">The default value is D3DCULL\_CCW.</span></span>

</dd> <dt>

<span data-ttu-id="70bd2-146"><span id="D3DRS_ZFUNC"></span><span id="d3drs_zfunc"></span>**\_D3DRS–MARKEUNC**</span><span class="sxs-lookup"><span data-stu-id="70bd2-146"><span id="D3DRS_ZFUNC"></span><span id="d3drs_zfunc"></span>**D3DRS\_ZFUNC**</span></span>
</dt> <dd>

<span data-ttu-id="70bd2-147">Ein Member des [**D3DCMPFUNC-Enumerationstyps.**](./d3dcmpfunc.md)</span><span class="sxs-lookup"><span data-stu-id="70bd2-147">One member of the [**D3DCMPFUNC**](./d3dcmpfunc.md) enumerated type.</span></span> <span data-ttu-id="70bd2-148">Der Standardwert ist D3DCMP \_ LESSEQUAL.</span><span class="sxs-lookup"><span data-stu-id="70bd2-148">The default value is D3DCMP\_LESSEQUAL.</span></span> <span data-ttu-id="70bd2-149">Mit diesem Member kann eine Anwendung ein Pixel basierend auf seinem Abstand zur Kamera akzeptieren oder ablehnen.</span><span class="sxs-lookup"><span data-stu-id="70bd2-149">This member enables an application to accept or reject a pixel, based on its distance from the camera.</span></span>

<span data-ttu-id="70bd2-150">Der Tiefenwert des Pixels wird mit dem Tiefenpufferwert verglichen.</span><span class="sxs-lookup"><span data-stu-id="70bd2-150">The depth value of the pixel is compared with the depth-buffer value.</span></span> <span data-ttu-id="70bd2-151">Wenn der Tiefenwert des Pixels die Vergleichsfunktion übergibt, wird das Pixel geschrieben.</span><span class="sxs-lookup"><span data-stu-id="70bd2-151">If the depth value of the pixel passes the comparison function, the pixel is written.</span></span>

<span data-ttu-id="70bd2-152">Der Tiefenwert wird nur in den Tiefenpuffer geschrieben, wenn der Renderzustand **TRUE** ist.</span><span class="sxs-lookup"><span data-stu-id="70bd2-152">The depth value is written to the depth buffer only if the render state is **TRUE**.</span></span>

<span data-ttu-id="70bd2-153">Softwareraster und viele Hardwarebeschleunigungen funktionieren schneller, wenn der Tiefentest fehlschlägt, da die Textur nicht gefiltert und moduliert werden muss, wenn das Pixel nicht gerendert werden soll.</span><span class="sxs-lookup"><span data-stu-id="70bd2-153">Software rasterizers and many hardware accelerators work faster if the depth test fails, because there is no need to filter and modulate the texture if the pixel is not going to be rendered.</span></span>

</dd> <dt>

<span data-ttu-id="70bd2-154"><span id="D3DRS_ALPHAREF"></span><span id="d3drs_alpharef"></span>**D3DRS \_ ALPHAREF**</span><span class="sxs-lookup"><span data-stu-id="70bd2-154"><span id="D3DRS_ALPHAREF"></span><span id="d3drs_alpharef"></span>**D3DRS\_ALPHAREF**</span></span>
</dt> <dd>

<span data-ttu-id="70bd2-155">Wert, der einen Alpha-Verweiswert angibt, für den Pixel getestet werden, wenn Alphatests aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="70bd2-155">Value that specifies a reference alpha value against which pixels are tested when alpha testing is enabled.</span></span> <span data-ttu-id="70bd2-156">Dies ist ein 8-Bit-Wert, der in den unteren 8 Bits des DWORD-Renderzustandswerts platziert wird.</span><span class="sxs-lookup"><span data-stu-id="70bd2-156">This is an 8-bit value placed in the low 8 bits of the DWORD render-state value.</span></span> <span data-ttu-id="70bd2-157">Werte können zwischen 0x00000000 und 0x000000FF liegen.</span><span class="sxs-lookup"><span data-stu-id="70bd2-157">Values can range from 0x00000000 through 0x000000FF.</span></span> <span data-ttu-id="70bd2-158">Der Standardwert ist 0.</span><span class="sxs-lookup"><span data-stu-id="70bd2-158">The default value is 0.</span></span>

</dd> <dt>

<span data-ttu-id="70bd2-159"><span id="D3DRS_ALPHAFUNC"></span><span id="d3drs_alphafunc"></span>**D3DRS \_ ALPHAFUNC**</span><span class="sxs-lookup"><span data-stu-id="70bd2-159"><span id="D3DRS_ALPHAFUNC"></span><span id="d3drs_alphafunc"></span>**D3DRS\_ALPHAFUNC**</span></span>
</dt> <dd>

<span data-ttu-id="70bd2-160">Ein Member des [**D3DCMPFUNC-Enumerationstyps.**](./d3dcmpfunc.md)</span><span class="sxs-lookup"><span data-stu-id="70bd2-160">One member of the [**D3DCMPFUNC**](./d3dcmpfunc.md) enumerated type.</span></span> <span data-ttu-id="70bd2-161">Der Standardwert ist D3DCMP \_ ALWAYS.</span><span class="sxs-lookup"><span data-stu-id="70bd2-161">The default value is D3DCMP\_ALWAYS.</span></span> <span data-ttu-id="70bd2-162">Mit diesem Member kann eine Anwendung ein Pixel basierend auf seinem Alphawert akzeptieren oder ablehnen.</span><span class="sxs-lookup"><span data-stu-id="70bd2-162">This member enables an application to accept or reject a pixel, based on its alpha value.</span></span>

</dd> <dt>

<span data-ttu-id="70bd2-163"><span id="D3DRS_DITHERENABLE"></span><span id="d3drs_ditherenable"></span>**D3DRS \_ DITHERENABLE**</span><span class="sxs-lookup"><span data-stu-id="70bd2-163"><span id="D3DRS_DITHERENABLE"></span><span id="d3drs_ditherenable"></span>**D3DRS\_DITHERENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="70bd2-164">**TRUE,** um dithering zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="70bd2-164">**TRUE** to enable dithering.</span></span> <span data-ttu-id="70bd2-165">Der Standardwert ist **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="70bd2-165">The default value is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="70bd2-166"><span id="D3DRS_ALPHABLENDENABLE"></span><span id="d3drs_alphablendenable"></span>**D3DRS \_ ALPHABLENDENABLE**</span><span class="sxs-lookup"><span data-stu-id="70bd2-166"><span id="D3DRS_ALPHABLENDENABLE"></span><span id="d3drs_alphablendenable"></span>**D3DRS\_ALPHABLENDENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="70bd2-167">**TRUE,** um transparenz mit Alphablending zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="70bd2-167">**TRUE** to enable alpha-blended transparency.</span></span> <span data-ttu-id="70bd2-168">Der Standardwert ist **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="70bd2-168">The default value is **FALSE**.</span></span>

<span data-ttu-id="70bd2-169">Der Typ des Alphablendings wird durch die Renderzustände D3DRS \_ SRCBLEND und D3DRS \_ DESTBLEND bestimmt.</span><span class="sxs-lookup"><span data-stu-id="70bd2-169">The type of alpha blending is determined by the D3DRS\_SRCBLEND and D3DRS\_DESTBLEND render states.</span></span>

</dd> <dt>

<span data-ttu-id="70bd2-170"><span id="D3DRS_FOGENABLE"></span><span id="d3drs_fogenable"></span>**D3DRS \_ – WARTEBAR**</span><span class="sxs-lookup"><span data-stu-id="70bd2-170"><span id="D3DRS_FOGENABLE"></span><span id="d3drs_fogenable"></span>**D3DRS\_FOGENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="70bd2-171">**TRUE,** um blending zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="70bd2-171">**TRUE** to enable fog blending.</span></span> <span data-ttu-id="70bd2-172">Der Standardwert ist **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="70bd2-172">The default value is **FALSE**.</span></span> <span data-ttu-id="70bd2-173">Weitere Informationen zur Verwendung von Blending finden Sie unter [Überblenden von .](fog.md)</span><span class="sxs-lookup"><span data-stu-id="70bd2-173">For more information about using fog blending, see [Fog](fog.md).</span></span>

</dd> <dt>

<span data-ttu-id="70bd2-174"><span id="D3DRS_SPECULARENABLE"></span><span id="d3drs_specularenable"></span>**D3DRS \_ SPECULARENABLE**</span><span class="sxs-lookup"><span data-stu-id="70bd2-174"><span id="D3DRS_SPECULARENABLE"></span><span id="d3drs_specularenable"></span>**D3DRS\_SPECULARENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="70bd2-175">**TRUE,** um Glanzlichter zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="70bd2-175">**TRUE** to enable specular highlights.</span></span> <span data-ttu-id="70bd2-176">Der Standardwert ist **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="70bd2-176">The default value is **FALSE**.</span></span>

<span data-ttu-id="70bd2-177">Glanzlichter werden so berechnet, als ob sich jeder Scheitelpunkt im objektbelichteten Objekt am Ursprung des Objekts befindet.</span><span class="sxs-lookup"><span data-stu-id="70bd2-177">Specular highlights are calculated as though every vertex in the object being lit is at the object's origin.</span></span> <span data-ttu-id="70bd2-178">Dies liefert die erwarteten Ergebnisse, solange das Objekt um den Ursprung herum modelliert wird und der Abstand vom Licht zum Objekt relativ groß ist.</span><span class="sxs-lookup"><span data-stu-id="70bd2-178">This gives the expected results as long as the object is modeled around the origin and the distance from the light to the object is relatively large.</span></span> <span data-ttu-id="70bd2-179">In anderen Fällen werden die Ergebnisse als nicht definiert angezeigt.</span><span class="sxs-lookup"><span data-stu-id="70bd2-179">In other cases, the results as undefined.</span></span>

<span data-ttu-id="70bd2-180">Wenn dieser Member auf **TRUE festgelegt** ist, wird die Specularfarbe der Basisfarbe nach der Texturkaskade, aber vor dem Alphablending hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="70bd2-180">When this member is set to **TRUE**, the specular color is added to the base color after the texture cascade but before alpha blending.</span></span>

</dd> <dt>

<span data-ttu-id="70bd2-181"><span id="D3DRS_FOGCOLOR"></span><span id="d3drs_fogcolor"></span>**D3DRSCOLOR \_**</span><span class="sxs-lookup"><span data-stu-id="70bd2-181"><span id="D3DRS_FOGCOLOR"></span><span id="d3drs_fogcolor"></span>**D3DRS\_FOGCOLOR**</span></span>
</dt> <dd>

<span data-ttu-id="70bd2-182">Wert, dessen Typ [**D3DCOLOR ist.**](d3dcolor.md)</span><span class="sxs-lookup"><span data-stu-id="70bd2-182">Value whose type is [**D3DCOLOR**](d3dcolor.md).</span></span> <span data-ttu-id="70bd2-183">Der Standardwert ist 0.</span><span class="sxs-lookup"><span data-stu-id="70bd2-183">The default value is 0.</span></span> <span data-ttu-id="70bd2-184">Weitere Informationen zur Farbe des Farbtons finden Sie unter [Farbtonfarbe (Direct3D 9).](fog-color.md)</span><span class="sxs-lookup"><span data-stu-id="70bd2-184">For more information about fog color, see [Fog Color (Direct3D 9)](fog-color.md).</span></span>

</dd> <dt>

<span data-ttu-id="70bd2-185"><span id="D3DRS_FOGTABLEMODE"></span><span id="d3drs_fogtablemode"></span>**D3DRS \_ -TABLEMODE**</span><span class="sxs-lookup"><span data-stu-id="70bd2-185"><span id="D3DRS_FOGTABLEMODE"></span><span id="d3drs_fogtablemode"></span>**D3DRS\_FOGTABLEMODE**</span></span>
</dt> <dd>

<span data-ttu-id="70bd2-186">Die Formel für die Grafik, die für Pixelpixel verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="70bd2-186">The fog formula to be used for pixel fog.</span></span> <span data-ttu-id="70bd2-187">Legen Sie auf einen der Member des [**aufzählten D3DFOGMODE-Typs**](./d3dfogmode.md) fest.</span><span class="sxs-lookup"><span data-stu-id="70bd2-187">Set to one of the members of the [**D3DFOGMODE**](./d3dfogmode.md) enumerated type.</span></span> <span data-ttu-id="70bd2-188">Der Standardwert ist D3DFOG \_ NONE.</span><span class="sxs-lookup"><span data-stu-id="70bd2-188">The default value is D3DFOG\_NONE.</span></span> <span data-ttu-id="70bd2-189">Weitere Informationen zu Pixelzunge finden Sie unter [Pixel pixel pixels (Direct3D 9)](pixel-fog.md).</span><span class="sxs-lookup"><span data-stu-id="70bd2-189">For more information about pixel fog, see [Pixel Fog (Direct3D 9)](pixel-fog.md).</span></span>

</dd> <dt>

<span data-ttu-id="70bd2-190"><span id="D3DRS_FOGSTART"></span><span id="d3drs_fogstart"></span>**D3DRS- \_ UND -START**</span><span class="sxs-lookup"><span data-stu-id="70bd2-190"><span id="D3DRS_FOGSTART"></span><span id="d3drs_fogstart"></span>**D3DRS\_FOGSTART**</span></span>
</dt> <dd>

<span data-ttu-id="70bd2-191">Tiefe, ab der Pixel- oder Scheitelpunkteffekten für den linearen Linienmodus beginnen.</span><span class="sxs-lookup"><span data-stu-id="70bd2-191">Depth at which pixel or vertex fog effects begin for linear fog mode.</span></span> <span data-ttu-id="70bd2-192">Der Standardwert ist 0,0f.</span><span class="sxs-lookup"><span data-stu-id="70bd2-192">The default value is 0.0f.</span></span> <span data-ttu-id="70bd2-193">Die Tiefe wird im Weltraum für Scheitelpunkt-Knoten und entweder im Geräteraum \[ 0,0, 1,0 \] oder im Weltraum für Pixelzunge angegeben.</span><span class="sxs-lookup"><span data-stu-id="70bd2-193">Depth is specified in world space for vertex fog and either device space \[0.0, 1.0\] or world space for pixel fog.</span></span> <span data-ttu-id="70bd2-194">Bei Pixelzunge befinden sich diese Werte im Geräteraum, wenn das System z für Berechnungen von Würfen verwendet, und im Raum der Welt, wenn das System augenrelatives Licht (w-eye) verwendet.</span><span class="sxs-lookup"><span data-stu-id="70bd2-194">For pixel fog, these values are in device space when the system uses z for fog calculations and world-world space when the system is using eye-relative fog (w-fog).</span></span> <span data-ttu-id="70bd2-195">Weitere Informationen finden Sie unter Parameter für [Metriken (Direct3D 9)](fog-parameters.md) und [Eye-Relative im Vergleich zu Z-basierter Tiefe.](pixel-fog.md)</span><span class="sxs-lookup"><span data-stu-id="70bd2-195">For more information, see [Fog Parameters (Direct3D 9)](fog-parameters.md) and [Eye-Relative vs. Z-based Depth](pixel-fog.md).</span></span>

<span data-ttu-id="70bd2-196">Werte für diesen Renderzustand sind Gleitkommawerte.</span><span class="sxs-lookup"><span data-stu-id="70bd2-196">Values for this render state are floating-point values.</span></span> <span data-ttu-id="70bd2-197">Da die [**IDirect3DDevice9::SetRenderState-Methode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) DWORD-Werte akzeptiert, muss Ihre Anwendung eine Variable mit dem Wert wandeln, wie im folgenden Codebeispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="70bd2-197">Because the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method accepts DWORD values, your application must cast a variable that contains the value, as shown in the following code example.</span></span>


```
pDevice9->SetRenderState(D3DRS_FOGSTART, 
                         *((DWORD*) (&fFogStart)));
```



</dd> <dt>

<span data-ttu-id="70bd2-198"><span id="D3DRS_FOGEND"></span><span id="d3drs_fogend"></span>**D3DRS- \_ UND -END**</span><span class="sxs-lookup"><span data-stu-id="70bd2-198"><span id="D3DRS_FOGEND"></span><span id="d3drs_fogend"></span>**D3DRS\_FOGEND**</span></span>
</dt> <dd>

<span data-ttu-id="70bd2-199">Tiefe, bei der Pixel- oder Scheitelpunkteffekten für den linearen Linienmodus enden.</span><span class="sxs-lookup"><span data-stu-id="70bd2-199">Depth at which pixel or vertex fog effects end for linear fog mode.</span></span> <span data-ttu-id="70bd2-200">Der Standardwert ist 1,0f.</span><span class="sxs-lookup"><span data-stu-id="70bd2-200">The default value is 1.0f.</span></span> <span data-ttu-id="70bd2-201">Die Tiefe wird im Weltraum für Scheitelpunkt-Knoten und entweder im Geräteraum \[ 0,0, 1,0 \] oder im Weltraum für Pixelzunge angegeben.</span><span class="sxs-lookup"><span data-stu-id="70bd2-201">Depth is specified in world space for vertex fog and either device space \[0.0, 1.0\] or world space for pixel fog.</span></span> <span data-ttu-id="70bd2-202">Bei Pixelzunge befinden sich diese Werte im Geräteraum, wenn das System z für Berechnungen der Fläche verwendet, und im Raum der Welt, wenn das System augen relatives Licht (w-eye) verwendet.</span><span class="sxs-lookup"><span data-stu-id="70bd2-202">For pixel fog, these values are in device space when the system uses z for fog calculations and in world space when the system is using eye-relative fog (w-fog).</span></span> <span data-ttu-id="70bd2-203">Weitere Informationen finden Sie unter Parameter für [Metriken (Direct3D 9)](fog-parameters.md) und [Eye-Relative im Vergleich zu Z-basierter Tiefe.](pixel-fog.md)</span><span class="sxs-lookup"><span data-stu-id="70bd2-203">For more information, see [Fog Parameters (Direct3D 9)](fog-parameters.md) and [Eye-Relative vs. Z-based Depth](pixel-fog.md).</span></span>

<span data-ttu-id="70bd2-204">Werte für diesen Renderzustand sind Gleitkommawerte.</span><span class="sxs-lookup"><span data-stu-id="70bd2-204">Values for this render state are floating-point values.</span></span> <span data-ttu-id="70bd2-205">Da die [**IDirect3DDevice9::SetRenderState-Methode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) DWORD-Werte akzeptiert, muss Ihre Anwendung eine Variable mit dem Wert wandeln, wie im folgenden Codebeispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="70bd2-205">Because the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method accepts DWORD values, your application must cast a variable that contains the value, as shown in the following code example.</span></span>


```
m_pDevice9->SetRenderState(D3DRS_FOGEND, *((DWORD*) (&fFogEnd)));
```



</dd> <dt>

<span data-ttu-id="70bd2-206"><span id="D3DRS_FOGDENSITY"></span><span id="d3drs_fogdensity"></span>**\_D3DRS-EMPFINDLICHKEIT**</span><span class="sxs-lookup"><span data-stu-id="70bd2-206"><span id="D3DRS_FOGDENSITY"></span><span id="d3drs_fogdensity"></span>**D3DRS\_FOGDENSITY**</span></span>
</dt> <dd>

<span data-ttu-id="70bd2-207">Die Dichte der Dichte von Pixeln oder Scheitelpunkten, die in den exponentiellen Verzweigungsmodi (D3DFOG \_ EXP und D3DFOG \_ EXP2) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="70bd2-207">Fog density for pixel or vertex fog used in the exponential fog modes (D3DFOG\_EXP and D3DFOG\_EXP2).</span></span> <span data-ttu-id="70bd2-208">Gültige Dichtewerte liegen zwischen 0,0 und 1,0.</span><span class="sxs-lookup"><span data-stu-id="70bd2-208">Valid density values range from 0.0 through 1.0.</span></span> <span data-ttu-id="70bd2-209">Der Standardwert ist 1,0.</span><span class="sxs-lookup"><span data-stu-id="70bd2-209">The default value is 1.0.</span></span> <span data-ttu-id="70bd2-210">Weitere Informationen finden Sie unter [Parameters (Direct3D 9)](fog-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="70bd2-210">For more information, see [Fog Parameters (Direct3D 9)](fog-parameters.md).</span></span>

<span data-ttu-id="70bd2-211">Werte für diesen Renderzustand sind Gleitkommawerte.</span><span class="sxs-lookup"><span data-stu-id="70bd2-211">Values for this render state are floating-point values.</span></span> <span data-ttu-id="70bd2-212">Da die [**IDirect3DDevice9::SetRenderState-Methode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) DWORD-Werte akzeptiert, muss Ihre Anwendung eine Variable, die den Wert enthält, wie im folgenden Codebeispiel gezeigt, casten.</span><span class="sxs-lookup"><span data-stu-id="70bd2-212">Because the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method accepts DWORD values, your application must cast a variable that contains the value, as shown in the following code example.</span></span>


```
    m_pDevice9->SetRenderState(D3DRS_FOGDENSITY, *((DWORD*) (&fFogDensity)));
```



</dd> <dt>

<span data-ttu-id="70bd2-213"><span id="D3DRS_RANGEFOGENABLE"></span><span id="d3drs_rangefogenable"></span>**D3DRS \_ RANGEFOGENABLE**</span><span class="sxs-lookup"><span data-stu-id="70bd2-213"><span id="D3DRS_RANGEFOGENABLE"></span><span id="d3drs_rangefogenable"></span>**D3DRS\_RANGEFOGENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="70bd2-214">**TRUE,** um bereichsbasierte Scheitelpunktverschluss zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="70bd2-214">**TRUE** to enable range-based vertex fog.</span></span> <span data-ttu-id="70bd2-215">Der Standardwert ist **FALSE.** In diesem Fall verwendet das System tiefenbasierte Ausfälle.</span><span class="sxs-lookup"><span data-stu-id="70bd2-215">The default value is **FALSE**, in which case the system uses depth-based fog.</span></span> <span data-ttu-id="70bd2-216">In bereichsbasierten Abständen wird der Abstand eines Objekts vom Viewer verwendet, um Effekten zu berechnen, nicht die Tiefe des Objekts (d. h. die Z-Koordinate) in der Szene.</span><span class="sxs-lookup"><span data-stu-id="70bd2-216">In range-based fog, the distance of an object from the viewer is used to compute fog effects, not the depth of the object (that is, the z-coordinate) in the scene.</span></span> <span data-ttu-id="70bd2-217">In bereichsbasierten 1:0-Methoden funktionieren alle Methoden wie gewohnt, mit der Ausnahme, dass sie "range" anstelle von "depth" in den Berechnungen verwenden.</span><span class="sxs-lookup"><span data-stu-id="70bd2-217">In range-based fog, all fog methods work as usual, except that they use range instead of depth in the computations.</span></span>

<span data-ttu-id="70bd2-218">Der Bereich ist der richtige Faktor, der für Berechnungsberechnungen verwendet werden kann, aber die Tiefe wird häufig verwendet, da der Bereich zeitaufwändig für die Berechnung ist und die Tiefe allgemein bereits verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="70bd2-218">Range is the correct factor to use for fog computations, but depth is commonly used instead because range is time-consuming to compute and depth is generally already available.</span></span> <span data-ttu-id="70bd2-219">Die Verwendung der Tiefe zum Berechnen von Brillen hat den unerwünschten Effekt, dass sich die Freundlichkeit von Peripherieobjekten ändert, wenn sich das Auge des Betrachters bewegt. In diesem Fall ändert sich die Tiefe, und der Bereich bleibt konstant.</span><span class="sxs-lookup"><span data-stu-id="70bd2-219">Using depth to calculate fog has the undesirable effect of having the fogginess of peripheral objects change as the viewer's eye moves - in this case, the depth changes and the range remains constant.</span></span>

<span data-ttu-id="70bd2-220">Da derzeit keine Hardware bereichsbasierte Spanne pro Pixel unterstützt, wird die Bereichskorrektur nur für Scheitelpunktsyntwinden angeboten.</span><span class="sxs-lookup"><span data-stu-id="70bd2-220">Because no hardware currently supports per-pixel range-based fog, range correction is offered only for vertex fog.</span></span>

<span data-ttu-id="70bd2-221">Weitere Informationen finden Sie unter [Vertex- (Direct3D 9)](vertex-fog.md).</span><span class="sxs-lookup"><span data-stu-id="70bd2-221">For more information, see [Vertex Fog (Direct3D 9)](vertex-fog.md).</span></span>

</dd> <dt>

<span data-ttu-id="70bd2-222"><span id="D3DRS_STENCILENABLE"></span><span id="d3drs_stencilenable"></span>**D3DRS \_ STENCILENABLE**</span><span class="sxs-lookup"><span data-stu-id="70bd2-222"><span id="D3DRS_STENCILENABLE"></span><span id="d3drs_stencilenable"></span>**D3DRS\_STENCILENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="70bd2-223">**TRUE,** um schablonieren zu aktivieren, oder **FALSE,** um schablonieren zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="70bd2-223">**TRUE** to enable stenciling, or **FALSE** to disable stenciling.</span></span> <span data-ttu-id="70bd2-224">Der Standardwert ist **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="70bd2-224">The default value is **FALSE**.</span></span> <span data-ttu-id="70bd2-225">Weitere Informationen finden Sie unter [Schablonenpuffertechniken (Direct3D 9).](stencil-buffer-techniques.md)</span><span class="sxs-lookup"><span data-stu-id="70bd2-225">For more information, see [Stencil Buffer Techniques (Direct3D 9)](stencil-buffer-techniques.md).</span></span>

</dd> <dt>

<span data-ttu-id="70bd2-226"><span id="D3DRS_STENCILFAIL"></span><span id="d3drs_stencilfail"></span>**D3DRS \_ STENCILFAIL**</span><span class="sxs-lookup"><span data-stu-id="70bd2-226"><span id="D3DRS_STENCILFAIL"></span><span id="d3drs_stencilfail"></span>**D3DRS\_STENCILFAIL**</span></span>
</dt> <dd>

<span data-ttu-id="70bd2-227">Schablonenvorgang, der durchgeführt werden soll, wenn der Schablonentest fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="70bd2-227">Stencil operation to perform if the stencil test fails.</span></span> <span data-ttu-id="70bd2-228">Werte werden vom [**aufzählten D3DSTENCILOP-Typ**](./d3dstencilop.md) verwendet.</span><span class="sxs-lookup"><span data-stu-id="70bd2-228">Values are from the [**D3DSTENCILOP**](./d3dstencilop.md) enumerated type.</span></span> <span data-ttu-id="70bd2-229">Der Standardwert ist D3DSTENCILOP \_ KEEP.</span><span class="sxs-lookup"><span data-stu-id="70bd2-229">The default value is D3DSTENCILOP\_KEEP.</span></span>

</dd> <dt>

<span data-ttu-id="70bd2-230"><span id="D3DRS_STENCILZFAIL"></span><span id="d3drs_stencilzfail"></span>**D3DRS \_ STENCILZFAIL**</span><span class="sxs-lookup"><span data-stu-id="70bd2-230"><span id="D3DRS_STENCILZFAIL"></span><span id="d3drs_stencilzfail"></span>**D3DRS\_STENCILZFAIL**</span></span>
</dt> <dd>

<span data-ttu-id="70bd2-231">Schablonenvorgang, der ausgeführt werden soll, wenn der Schablonentest erfolgreich war und der Tiefentest (z-test) fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="70bd2-231">Stencil operation to perform if the stencil test passes and the depth test (z-test) fails.</span></span> <span data-ttu-id="70bd2-232">Werte stammen vom [**D3DSTENCILOP-Enumerationstyp.**](./d3dstencilop.md)</span><span class="sxs-lookup"><span data-stu-id="70bd2-232">Values are from the [**D3DSTENCILOP**](./d3dstencilop.md) enumerated type.</span></span> <span data-ttu-id="70bd2-233">Der Standardwert ist D3DSTENCILOP \_ KEEP.</span><span class="sxs-lookup"><span data-stu-id="70bd2-233">The default value is D3DSTENCILOP\_KEEP.</span></span>

</dd> <dt>

<span data-ttu-id="70bd2-234"><span id="D3DRS_STENCILPASS"></span><span id="d3drs_stencilpass"></span>**D3DRS \_ STENCILPASS**</span><span class="sxs-lookup"><span data-stu-id="70bd2-234"><span id="D3DRS_STENCILPASS"></span><span id="d3drs_stencilpass"></span>**D3DRS\_STENCILPASS**</span></span>
</dt> <dd>

<span data-ttu-id="70bd2-235">Schablonenvorgang, der ausgeführt werden soll, wenn sowohl die Schablone als auch die Tiefentests (z) erfolgreich sind.</span><span class="sxs-lookup"><span data-stu-id="70bd2-235">Stencil operation to perform if both the stencil and the depth (z) tests pass.</span></span> <span data-ttu-id="70bd2-236">Werte stammen vom [**D3DSTENCILOP-Enumerationstyp.**](./d3dstencilop.md)</span><span class="sxs-lookup"><span data-stu-id="70bd2-236">Values are from the [**D3DSTENCILOP**](./d3dstencilop.md) enumerated type.</span></span> <span data-ttu-id="70bd2-237">Der Standardwert ist D3DSTENCILOP \_ KEEP.</span><span class="sxs-lookup"><span data-stu-id="70bd2-237">The default value is D3DSTENCILOP\_KEEP.</span></span>

</dd> <dt>

<span data-ttu-id="70bd2-238"><span id="D3DRS_STENCILFUNC"></span><span id="d3drs_stencilfunc"></span>**D3DRS \_ STENCILFUNC**</span><span class="sxs-lookup"><span data-stu-id="70bd2-238"><span id="D3DRS_STENCILFUNC"></span><span id="d3drs_stencilfunc"></span>**D3DRS\_STENCILFUNC**</span></span>
</dt> <dd>

<span data-ttu-id="70bd2-239">Vergleichsfunktion für den Schablonentest.</span><span class="sxs-lookup"><span data-stu-id="70bd2-239">Comparison function for the stencil test.</span></span> <span data-ttu-id="70bd2-240">Werte stammen vom [**D3DCMPFUNC-Enumerationstyp.**](./d3dcmpfunc.md)</span><span class="sxs-lookup"><span data-stu-id="70bd2-240">Values are from the [**D3DCMPFUNC**](./d3dcmpfunc.md) enumerated type.</span></span> <span data-ttu-id="70bd2-241">Der Standardwert ist D3DCMP \_ ALWAYS.</span><span class="sxs-lookup"><span data-stu-id="70bd2-241">The default value is D3DCMP\_ALWAYS.</span></span>

<span data-ttu-id="70bd2-242">Die Vergleichsfunktion wird verwendet, um den Verweiswert mit einem Schablonenpuffereintrag zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="70bd2-242">The comparison function is used to compare the reference value to a stencil buffer entry.</span></span> <span data-ttu-id="70bd2-243">Dieser Vergleich gilt nur für die Bits im Verweiswert und den Schablonenpuffereintrag, die in der Schablonenmaske festgelegt sind (festgelegt durch den \_ D3DRS-STENCILMASK-Renderzustand).</span><span class="sxs-lookup"><span data-stu-id="70bd2-243">This comparison applies only to the bits in the reference value and stencil buffer entry that are set in the stencil mask (set by the D3DRS\_STENCILMASK render state).</span></span> <span data-ttu-id="70bd2-244">True gibt an, dass der Schablonentest erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="70bd2-244">If **TRUE**, the stencil test passes.</span></span>

</dd> <dt>

<span data-ttu-id="70bd2-245"><span id="D3DRS_STENCILREF"></span><span id="d3drs_stencilref"></span>**D3DRS \_ STENCILREF**</span><span class="sxs-lookup"><span data-stu-id="70bd2-245"><span id="D3DRS_STENCILREF"></span><span id="d3drs_stencilref"></span>**D3DRS\_STENCILREF**</span></span>
</dt> <dd>

<span data-ttu-id="70bd2-246">Ein int-Verweiswert für den Schablonentest.</span><span class="sxs-lookup"><span data-stu-id="70bd2-246">An int reference value for the stencil test.</span></span> <span data-ttu-id="70bd2-247">Der Standardwert ist 0.</span><span class="sxs-lookup"><span data-stu-id="70bd2-247">The default value is 0.</span></span>

</dd> <dt>

<span data-ttu-id="70bd2-248"><span id="D3DRS_STENCILMASK"></span><span id="d3drs_stencilmask"></span>**D3DRS \_ STENCILMASK**</span><span class="sxs-lookup"><span data-stu-id="70bd2-248"><span id="D3DRS_STENCILMASK"></span><span id="d3drs_stencilmask"></span>**D3DRS\_STENCILMASK**</span></span>
</dt> <dd>

<span data-ttu-id="70bd2-249">Maske, die auf den Verweiswert und jeden Schablonenpuffereintrag angewendet wird, um die signifikanten Bits für den Schablonentest zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="70bd2-249">Mask applied to the reference value and each stencil buffer entry to determine the significant bits for the stencil test.</span></span> <span data-ttu-id="70bd2-250">Die Standardmaske ist 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="70bd2-250">The default mask is 0xFFFFFFFF.</span></span>

</dd> <dt>

<span data-ttu-id="70bd2-251"><span id="D3DRS_STENCILWRITEMASK"></span><span id="d3drs_stencilwritemask"></span>**D3DRS \_ STENCILWRITEMASK**</span><span class="sxs-lookup"><span data-stu-id="70bd2-251"><span id="D3DRS_STENCILWRITEMASK"></span><span id="d3drs_stencilwritemask"></span>**D3DRS\_STENCILWRITEMASK**</span></span>
</dt> <dd>

<span data-ttu-id="70bd2-252">Schreibmaske, die auf Werte angewendet wird, die in den Schablonenpuffer geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="70bd2-252">Write mask applied to values written into the stencil buffer.</span></span> <span data-ttu-id="70bd2-253">Die Standardmaske ist 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="70bd2-253">The default mask is 0xFFFFFFFF.</span></span>

</dd> <dt>

<span data-ttu-id="70bd2-254"><span id="D3DRS_TEXTUREFACTOR"></span><span id="d3drs_texturefactor"></span>**D3DRS \_ TEXTUREFACTOR**</span><span class="sxs-lookup"><span data-stu-id="70bd2-254"><span id="D3DRS_TEXTUREFACTOR"></span><span id="d3drs_texturefactor"></span>**D3DRS\_TEXTUREFACTOR**</span></span>
</dt> <dd>

<span data-ttu-id="70bd2-255">Farbe, die für das Mischen mehrerer Texturen mit dem D3DTA \_ TFACTOR-Texturmischungsargument oder dem D3DTOP \_ BLENDFACTORALPHA-Texturmischungsvorgang verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="70bd2-255">Color used for multiple-texture blending with the D3DTA\_TFACTOR texture-blending argument or the D3DTOP\_BLENDFACTORALPHA texture-blending operation.</span></span> <span data-ttu-id="70bd2-256">Der zugeordnete Wert ist eine [**D3DCOLOR-Variable.**](d3dcolor.md)</span><span class="sxs-lookup"><span data-stu-id="70bd2-256">The associated value is a [**D3DCOLOR**](d3dcolor.md) variable.</span></span> <span data-ttu-id="70bd2-257">Der Standardwert ist nicht transparent weiß (0xFFFFFFFF).</span><span class="sxs-lookup"><span data-stu-id="70bd2-257">The default value is opaque white (0xFFFFFFFF).</span></span>

</dd> <dt>

<span data-ttu-id="70bd2-258"><span id="D3DRS_WRAP0"></span><span id="d3drs_wrap0"></span>**D3DRS \_ WRAP0**</span><span class="sxs-lookup"><span data-stu-id="70bd2-258"><span id="D3DRS_WRAP0"></span><span id="d3drs_wrap0"></span>**D3DRS\_WRAP0**</span></span>
</dt> <dd>

<span data-ttu-id="70bd2-259">Texturumbruchverhalten für mehrere Sätze von Texturkoordinaten.</span><span class="sxs-lookup"><span data-stu-id="70bd2-259">Texture-wrapping behavior for multiple sets of texture coordinates.</span></span> <span data-ttu-id="70bd2-260">Gültige Werte für diesen Renderzustand können eine beliebige Kombination der Flags D3DWRAPCOORD \_ 0 (oder D3DWRAP \_ U), D3DWRAPCOORD \_ 1 (oder D3DWRAP \_ V), D3DWRAPCOORD \_ 2 (oder D3DWRAP W) und \_ D3DWRAPCOORD \_ 3 sein.</span><span class="sxs-lookup"><span data-stu-id="70bd2-260">Valid values for this render state can be any combination of the D3DWRAPCOORD\_0 (or D3DWRAP\_U), D3DWRAPCOORD\_1 (or D3DWRAP\_V), D3DWRAPCOORD\_2 (or D3DWRAP\_W), and D3DWRAPCOORD\_3 flags.</span></span> <span data-ttu-id="70bd2-261">Diese bewirken, dass das System in Richtung der ersten, zweiten, dritten und vierten Dimension, manchmal auch als s-, t-, r- und q-Richtung bezeichnet, für eine bestimmte Textur umschließt.</span><span class="sxs-lookup"><span data-stu-id="70bd2-261">These cause the system to wrap in the direction of the first, second, third, and fourth dimensions, sometimes referred to as the s, t, r, and q directions, for a given texture.</span></span> <span data-ttu-id="70bd2-262">Der Standardwert für diesen Renderzustand ist 0 (umschließen in alle Richtungen deaktiviert).</span><span class="sxs-lookup"><span data-stu-id="70bd2-262">The default value for this render state is 0 (wrapping disabled in all directions).</span></span>

</dd> <dt>

<span data-ttu-id="70bd2-263"><span id="D3DRS_WRAP1"></span><span id="d3drs_wrap1"></span>**D3DRS \_ WRAP1**</span><span class="sxs-lookup"><span data-stu-id="70bd2-263"><span id="D3DRS_WRAP1"></span><span id="d3drs_wrap1"></span>**D3DRS\_WRAP1**</span></span>
</dt> <dd>

<span data-ttu-id="70bd2-264">Siehe D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="70bd2-264">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="70bd2-265"><span id="D3DRS_WRAP2"></span><span id="d3drs_wrap2"></span>**D3DRS \_ WRAP2**</span><span class="sxs-lookup"><span data-stu-id="70bd2-265"><span id="D3DRS_WRAP2"></span><span id="d3drs_wrap2"></span>**D3DRS\_WRAP2**</span></span>
</dt> <dd>

<span data-ttu-id="70bd2-266">Siehe D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="70bd2-266">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="70bd2-267"><span id="D3DRS_WRAP3"></span><span id="d3drs_wrap3"></span>**D3DRS \_ WRAP3**</span><span class="sxs-lookup"><span data-stu-id="70bd2-267"><span id="D3DRS_WRAP3"></span><span id="d3drs_wrap3"></span>**D3DRS\_WRAP3**</span></span>
</dt> <dd>

<span data-ttu-id="70bd2-268">Siehe D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="70bd2-268">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="70bd2-269"><span id="D3DRS_WRAP4"></span><span id="d3drs_wrap4"></span>**D3DRS \_ WRAP4**</span><span class="sxs-lookup"><span data-stu-id="70bd2-269"><span id="D3DRS_WRAP4"></span><span id="d3drs_wrap4"></span>**D3DRS\_WRAP4**</span></span>
</dt> <dd>

<span data-ttu-id="70bd2-270">Siehe D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="70bd2-270">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="70bd2-271"><span id="D3DRS_WRAP5"></span><span id="d3drs_wrap5"></span>**D3DRS \_ WRAP5**</span><span class="sxs-lookup"><span data-stu-id="70bd2-271"><span id="D3DRS_WRAP5"></span><span id="d3drs_wrap5"></span>**D3DRS\_WRAP5**</span></span>
</dt> <dd>

<span data-ttu-id="70bd2-272">Siehe D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="70bd2-272">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="70bd2-273"><span id="D3DRS_WRAP6"></span><span id="d3drs_wrap6"></span>**D3DRS \_ WRAP6**</span><span class="sxs-lookup"><span data-stu-id="70bd2-273"><span id="D3DRS_WRAP6"></span><span id="d3drs_wrap6"></span>**D3DRS\_WRAP6**</span></span>
</dt> <dd>

<span data-ttu-id="70bd2-274">Siehe D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="70bd2-274">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="70bd2-275"><span id="D3DRS_WRAP7"></span><span id="d3drs_wrap7"></span>**D3DRS \_ WRAP7**</span><span class="sxs-lookup"><span data-stu-id="70bd2-275"><span id="D3DRS_WRAP7"></span><span id="d3drs_wrap7"></span>**D3DRS\_WRAP7**</span></span>
</dt> <dd>

<span data-ttu-id="70bd2-276">Siehe D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="70bd2-276">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="70bd2-277"><span id="D3DRS_CLIPPING"></span><span id="d3drs_clipping"></span>**D3DRS \_ CLIPPING**</span><span class="sxs-lookup"><span data-stu-id="70bd2-277"><span id="D3DRS_CLIPPING"></span><span id="d3drs_clipping"></span>**D3DRS\_CLIPPING**</span></span>
</dt> <dd>

<span data-ttu-id="70bd2-278">**TRUE,** um primitives Clipping durch Direct3D zu aktivieren, oder **FALSE,** um es zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="70bd2-278">**TRUE** to enable primitive clipping by Direct3D, or **FALSE** to disable it.</span></span> <span data-ttu-id="70bd2-279">Der Standardwert ist **TRUE.**</span><span class="sxs-lookup"><span data-stu-id="70bd2-279">The default value is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="70bd2-280"><span id="D3DRS_LIGHTING"></span><span id="d3drs_lighting"></span>**\_D3DRS-BELEUCHTUNG**</span><span class="sxs-lookup"><span data-stu-id="70bd2-280"><span id="D3DRS_LIGHTING"></span><span id="d3drs_lighting"></span>**D3DRS\_LIGHTING**</span></span>
</dt> <dd>

<span data-ttu-id="70bd2-281">**TRUE,** um direct3D-Beleuchtung zu aktivieren, oder **FALSE,** um sie zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="70bd2-281">**TRUE** to enable Direct3D lighting, or **FALSE** to disable it.</span></span> <span data-ttu-id="70bd2-282">Der Standardwert ist **TRUE.**</span><span class="sxs-lookup"><span data-stu-id="70bd2-282">The default value is **TRUE**.</span></span> <span data-ttu-id="70bd2-283">Nur Scheitelpunkte, die einen Scheitelpunkt normal enthalten, werden ordnungsgemäß ausgelichtet. Scheitelpunkte, die kein normales enthalten, verwenden in allen Beleuchtungsberechnungen ein Punktprodukt von 0.</span><span class="sxs-lookup"><span data-stu-id="70bd2-283">Only vertices that include a vertex normal are properly lit; vertices that do not contain a normal employ a dot product of 0 in all lighting calculations.</span></span>

</dd> <dt>

<span data-ttu-id="70bd2-284"><span id="D3DRS_AMBIENT"></span><span id="d3drs_ambient"></span>**D3DRS \_ AMBIENT**</span><span class="sxs-lookup"><span data-stu-id="70bd2-284"><span id="D3DRS_AMBIENT"></span><span id="d3drs_ambient"></span>**D3DRS\_AMBIENT**</span></span>
</dt> <dd>

<span data-ttu-id="70bd2-285">Umgebungslichtfarbe.</span><span class="sxs-lookup"><span data-stu-id="70bd2-285">Ambient light color.</span></span> <span data-ttu-id="70bd2-286">Dieser Wert ist vom Typ [**D3DCOLOR.**](d3dcolor.md)</span><span class="sxs-lookup"><span data-stu-id="70bd2-286">This value is of type [**D3DCOLOR**](d3dcolor.md).</span></span> <span data-ttu-id="70bd2-287">Der Standardwert ist 0.</span><span class="sxs-lookup"><span data-stu-id="70bd2-287">The default value is 0.</span></span>

</dd> <dt>

<span data-ttu-id="70bd2-288"><span id="D3DRS_FOGVERTEXMODE"></span><span id="d3drs_fogvertexmode"></span>**\_D3DRS-VERTEXMODE**</span><span class="sxs-lookup"><span data-stu-id="70bd2-288"><span id="D3DRS_FOGVERTEXMODE"></span><span id="d3drs_fogvertexmode"></span>**D3DRS\_FOGVERTEXMODE**</span></span>
</dt> <dd>

<span data-ttu-id="70bd2-289">Formel für Die Formel, die für Scheitelpunkt-Scheitelpunkte verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="70bd2-289">Fog formula to be used for vertex fog.</span></span> <span data-ttu-id="70bd2-290">Legen Sie auf einen Member des [**D3DFOGMODE-Enumerationstyps**](./d3dfogmode.md) fest.</span><span class="sxs-lookup"><span data-stu-id="70bd2-290">Set to one member of the [**D3DFOGMODE**](./d3dfogmode.md) enumerated type.</span></span> <span data-ttu-id="70bd2-291">Der Standardwert ist D3DFOG \_ NONE.</span><span class="sxs-lookup"><span data-stu-id="70bd2-291">The default value is D3DFOG\_NONE.</span></span>

</dd> <dt>

<span data-ttu-id="70bd2-292"><span id="D3DRS_COLORVERTEX"></span><span id="d3drs_colorvertex"></span>**D3DRS \_ COLORVERTEX**</span><span class="sxs-lookup"><span data-stu-id="70bd2-292"><span id="D3DRS_COLORVERTEX"></span><span id="d3drs_colorvertex"></span>**D3DRS\_COLORVERTEX**</span></span>
</dt> <dd>

<span data-ttu-id="70bd2-293">**TRUE,** um die Farbe pro Scheitelpunkt zu aktivieren, oder **FALSE,** um sie zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="70bd2-293">**TRUE** to enable per-vertex color or **FALSE** to disable it.</span></span> <span data-ttu-id="70bd2-294">Der Standardwert ist **TRUE.**</span><span class="sxs-lookup"><span data-stu-id="70bd2-294">The default value is **TRUE**.</span></span> <span data-ttu-id="70bd2-295">Wenn Sie die Farbe pro Scheitelpunkt aktivieren, kann das System die für einzelne Scheitelpunkte definierte Farbe in seine Beleuchtungsberechnungen einplanen.</span><span class="sxs-lookup"><span data-stu-id="70bd2-295">Enabling per-vertex color allows the system to include the color defined for individual vertices in its lighting calculations.</span></span>

<span data-ttu-id="70bd2-296">Weitere Informationen finden Sie in den folgenden Renderzuständen:</span><span class="sxs-lookup"><span data-stu-id="70bd2-296">For more information, see the following render states:</span></span>

-   <span data-ttu-id="70bd2-297">D3DRS \_ DIFFUSEMATERIALSOURCE</span><span class="sxs-lookup"><span data-stu-id="70bd2-297">D3DRS\_DIFFUSEMATERIALSOURCE</span></span>
-   <span data-ttu-id="70bd2-298">D3DRS \_ SPECULARMATERIALSOURCE</span><span class="sxs-lookup"><span data-stu-id="70bd2-298">D3DRS\_SPECULARMATERIALSOURCE</span></span>
-   <span data-ttu-id="70bd2-299">D3DRS \_ AMBIENTMATERIALSOURCE</span><span class="sxs-lookup"><span data-stu-id="70bd2-299">D3DRS\_AMBIENTMATERIALSOURCE</span></span>
-   <span data-ttu-id="70bd2-300">D3DRS- \_ UND SIVEMATERIALSOURCE</span><span class="sxs-lookup"><span data-stu-id="70bd2-300">D3DRS\_EMISSIVEMATERIALSOURCE</span></span>

</dd> <dt>

<span data-ttu-id="70bd2-301"><span id="D3DRS_LOCALVIEWER"></span><span id="d3drs_localviewer"></span>**D3DRS \_ LOCALVIEWER**</span><span class="sxs-lookup"><span data-stu-id="70bd2-301"><span id="D3DRS_LOCALVIEWER"></span><span id="d3drs_localviewer"></span>**D3DRS\_LOCALVIEWER**</span></span>
</dt> <dd>

<span data-ttu-id="70bd2-302">**TRUE,** um kamera relative Glanzlichter zu aktivieren, oder **FALSE,** um orthogonale Glanzlichter zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="70bd2-302">**TRUE** to enable camera-relative specular highlights, or **FALSE** to use orthogonal specular highlights.</span></span> <span data-ttu-id="70bd2-303">Der Standardwert ist **TRUE.**</span><span class="sxs-lookup"><span data-stu-id="70bd2-303">The default value is **TRUE**.</span></span> <span data-ttu-id="70bd2-304">Anwendungen, die die orthogonale Projektion verwenden, sollten **FALSE angeben.**</span><span class="sxs-lookup"><span data-stu-id="70bd2-304">Applications that use orthogonal projection should specify **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="70bd2-305"><span id="D3DRS_NORMALIZENORMALS"></span><span id="d3drs_normalizenormals"></span>**D3DRS \_ NORMALIZENORMALS**</span><span class="sxs-lookup"><span data-stu-id="70bd2-305"><span id="D3DRS_NORMALIZENORMALS"></span><span id="d3drs_normalizenormals"></span>**D3DRS\_NORMALIZENORMALS**</span></span>
</dt> <dd>

<span data-ttu-id="70bd2-306">**TRUE,** um die automatische Normalisierung von Scheitelpunktnormals zu aktivieren, oder **FALSE,** um sie zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="70bd2-306">**TRUE** to enable automatic normalization of vertex normals, or **FALSE** to disable it.</span></span> <span data-ttu-id="70bd2-307">Der Standardwert ist **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="70bd2-307">The default value is **FALSE**.</span></span> <span data-ttu-id="70bd2-308">Die Aktivierung dieses Features bewirkt, dass das System die Scheitelpunktnorm normalisiert, nachdem sie in den Kameraraum transformiert wurden, was rechenintensiv sein kann.</span><span class="sxs-lookup"><span data-stu-id="70bd2-308">Enabling this feature causes the system to normalize the vertex normals for vertices after transforming them to camera space, which can be computationally time-consuming.</span></span>

</dd> <dt>

<span data-ttu-id="70bd2-309"><span id="D3DRS_DIFFUSEMATERIALSOURCE"></span><span id="d3drs_diffusematerialsource"></span>**D3DRS \_ DIFFUSEMATERIALSOURCE**</span><span class="sxs-lookup"><span data-stu-id="70bd2-309"><span id="D3DRS_DIFFUSEMATERIALSOURCE"></span><span id="d3drs_diffusematerialsource"></span>**D3DRS\_DIFFUSEMATERIALSOURCE**</span></span>
</dt> <dd>

<span data-ttu-id="70bd2-310">Diffuse Farbquelle für Beleuchtungsberechnungen.</span><span class="sxs-lookup"><span data-stu-id="70bd2-310">Diffuse color source for lighting calculations.</span></span> <span data-ttu-id="70bd2-311">Gültige Werte sind Member des [**aufzählten D3DMATERIALCOLORSOURCE-Typs.**](./d3dmaterialcolorsource.md)</span><span class="sxs-lookup"><span data-stu-id="70bd2-311">Valid values are members of the [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) enumerated type.</span></span> <span data-ttu-id="70bd2-312">Der Standardwert ist D3DMCS \_ COLOR1.</span><span class="sxs-lookup"><span data-stu-id="70bd2-312">The default value is D3DMCS\_COLOR1.</span></span> <span data-ttu-id="70bd2-313">Der Wert für diesen Renderzustand wird nur verwendet, wenn der D3DRS \_ COLORVERTEX-Renderzustand auf TRUE festgelegt **ist.**</span><span class="sxs-lookup"><span data-stu-id="70bd2-313">The value for this render state is used only if the D3DRS\_COLORVERTEX render state is set to **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="70bd2-314"><span id="D3DRS_SPECULARMATERIALSOURCE"></span><span id="d3drs_specularmaterialsource"></span>**D3DRS \_ SPECULARMATERIALSOURCE**</span><span class="sxs-lookup"><span data-stu-id="70bd2-314"><span id="D3DRS_SPECULARMATERIALSOURCE"></span><span id="d3drs_specularmaterialsource"></span>**D3DRS\_SPECULARMATERIALSOURCE**</span></span>
</dt> <dd>

<span data-ttu-id="70bd2-315">Glanzfarbenquelle für Beleuchtungsberechnungen.</span><span class="sxs-lookup"><span data-stu-id="70bd2-315">Specular color source for lighting calculations.</span></span> <span data-ttu-id="70bd2-316">Gültige Werte sind Member des [**D3DMATERIALCOLORSOURCE-Enumerationstyps.**](./d3dmaterialcolorsource.md)</span><span class="sxs-lookup"><span data-stu-id="70bd2-316">Valid values are members of the [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) enumerated type.</span></span> <span data-ttu-id="70bd2-317">Der Standardwert ist D3DMCS \_ COLOR2.</span><span class="sxs-lookup"><span data-stu-id="70bd2-317">The default value is D3DMCS\_COLOR2.</span></span>

</dd> <dt>

<span data-ttu-id="70bd2-318"><span id="D3DRS_AMBIENTMATERIALSOURCE"></span><span id="d3drs_ambientmaterialsource"></span>**D3DRS \_ AMBIENTMATERIALSOURCE**</span><span class="sxs-lookup"><span data-stu-id="70bd2-318"><span id="D3DRS_AMBIENTMATERIALSOURCE"></span><span id="d3drs_ambientmaterialsource"></span>**D3DRS\_AMBIENTMATERIALSOURCE**</span></span>
</dt> <dd>

<span data-ttu-id="70bd2-319">Umgebungsfarbquelle für Beleuchtungsberechnungen.</span><span class="sxs-lookup"><span data-stu-id="70bd2-319">Ambient color source for lighting calculations.</span></span> <span data-ttu-id="70bd2-320">Gültige Werte sind Member des [**D3DMATERIALCOLORSOURCE-Enumerationstyps.**](./d3dmaterialcolorsource.md)</span><span class="sxs-lookup"><span data-stu-id="70bd2-320">Valid values are members of the [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) enumerated type.</span></span> <span data-ttu-id="70bd2-321">Der Standardwert ist D3DMCS \_ MATERIAL.</span><span class="sxs-lookup"><span data-stu-id="70bd2-321">The default value is D3DMCS\_MATERIAL.</span></span>

</dd> <dt>

<span data-ttu-id="70bd2-322"><span id="D3DRS_EMISSIVEMATERIALSOURCE"></span><span id="d3drs_emissivematerialsource"></span>**D3DRS \_ EMISSIVEMATERIALSOURCE**</span><span class="sxs-lookup"><span data-stu-id="70bd2-322"><span id="D3DRS_EMISSIVEMATERIALSOURCE"></span><span id="d3drs_emissivematerialsource"></span>**D3DRS\_EMISSIVEMATERIALSOURCE**</span></span>
</dt> <dd>

<span data-ttu-id="70bd2-323">Eine freizügige Farbquelle für Beleuchtungsberechnungen.</span><span class="sxs-lookup"><span data-stu-id="70bd2-323">Emissive color source for lighting calculations.</span></span> <span data-ttu-id="70bd2-324">Gültige Werte sind Member des [**D3DMATERIALCOLORSOURCE-Enumerationstyps.**](./d3dmaterialcolorsource.md)</span><span class="sxs-lookup"><span data-stu-id="70bd2-324">Valid values are members of the [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) enumerated type.</span></span> <span data-ttu-id="70bd2-325">Der Standardwert ist D3DMCS \_ MATERIAL.</span><span class="sxs-lookup"><span data-stu-id="70bd2-325">The default value is D3DMCS\_MATERIAL.</span></span>

</dd> <dt>

<span data-ttu-id="70bd2-326"><span id="D3DRS_VERTEXBLEND"></span><span id="d3drs_vertexblend"></span>**D3DRS \_ VERTEXBLEND**</span><span class="sxs-lookup"><span data-stu-id="70bd2-326"><span id="D3DRS_VERTEXBLEND"></span><span id="d3drs_vertexblend"></span>**D3DRS\_VERTEXBLEND**</span></span>
</dt> <dd>

<span data-ttu-id="70bd2-327">Anzahl von Matrizen, die zum Durchführen von Geometrieblending verwendet werden sollen( falls vorhanden).</span><span class="sxs-lookup"><span data-stu-id="70bd2-327">Number of matrices to use to perform geometry blending, if any.</span></span> <span data-ttu-id="70bd2-328">Gültige Werte sind Member des [**D3DVERTEXBLENDFLAGS-Enumerationstyps.**](./d3dvertexblendflags.md)</span><span class="sxs-lookup"><span data-stu-id="70bd2-328">Valid values are members of the [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) enumerated type.</span></span> <span data-ttu-id="70bd2-329">Der Standardwert ist D3DVBF \_ DISABLE.</span><span class="sxs-lookup"><span data-stu-id="70bd2-329">The default value is D3DVBF\_DISABLE.</span></span>

</dd> <dt>

<span data-ttu-id="70bd2-330"><span id="D3DRS_CLIPPLANEENABLE"></span><span id="d3drs_clipplaneenable"></span>**D3DRS \_ CLIPPLANEENABLE**</span><span class="sxs-lookup"><span data-stu-id="70bd2-330"><span id="D3DRS_CLIPPLANEENABLE"></span><span id="d3drs_clipplaneenable"></span>**D3DRS\_CLIPPLANEENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="70bd2-331">Aktiviert oder deaktiviert benutzerdefinierte Clippingebenen.</span><span class="sxs-lookup"><span data-stu-id="70bd2-331">Enables or disables user-defined clipping planes.</span></span> <span data-ttu-id="70bd2-332">Gültige Werte sind alle DWORD-Werte, bei denen der Status jedes Bits (festgelegt oder nicht festgelegt) den Aktivierungszustand einer entsprechenden benutzerdefinierten Clippingebene umschaltet.</span><span class="sxs-lookup"><span data-stu-id="70bd2-332">Valid values are any DWORD in which the status of each bit (set or not set) toggles the activation state of a corresponding user-defined clipping plane.</span></span> <span data-ttu-id="70bd2-333">Das am wenigsten signifikante Bit (Bit 0) steuert die erste Clippingebene bei Index 0, und nachfolgende Bits steuern die Aktivierung von Clippingebenen bei höheren Indizes.</span><span class="sxs-lookup"><span data-stu-id="70bd2-333">The least significant bit (bit 0) controls the first clipping plane at index 0, and subsequent bits control the activation of clipping planes at higher indexes.</span></span> <span data-ttu-id="70bd2-334">Wenn ein Bit festgelegt ist, wendet das System während des Szenenrenderings die entsprechende Clippingebene an.</span><span class="sxs-lookup"><span data-stu-id="70bd2-334">If a bit is set, the system applies the appropriate clipping plane during scene rendering.</span></span> <span data-ttu-id="70bd2-335">Der Standardwert ist 0.</span><span class="sxs-lookup"><span data-stu-id="70bd2-335">The default value is 0.</span></span>

<span data-ttu-id="70bd2-336">Die [**D3DCLIPPLANEn-Makros**](d3dclipplanen.md) sind definiert, um eine bequeme Möglichkeit zum Aktivieren von Clippingebenen zu bieten.</span><span class="sxs-lookup"><span data-stu-id="70bd2-336">The [**D3DCLIPPLANEn**](d3dclipplanen.md) macros are defined to provide a convenient way to enable clipping planes.</span></span>

</dd> <dt>

<span data-ttu-id="70bd2-337"><span id="D3DRS_POINTSIZE"></span><span id="d3drs_pointsize"></span>**D3DRS \_ POINTSIZE**</span><span class="sxs-lookup"><span data-stu-id="70bd2-337"><span id="D3DRS_POINTSIZE"></span><span id="d3drs_pointsize"></span>**D3DRS\_POINTSIZE**</span></span>
</dt> <dd>

<span data-ttu-id="70bd2-338">Ein float-Wert, der die Größe angibt, die für die Berechnung der Punktgröße in Fällen verwendet werden soll, in denen die Punktgröße nicht für jeden Scheitelpunkt angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="70bd2-338">A float value that specifies the size to use for point size computation in cases where point size is not specified for each vertex.</span></span> <span data-ttu-id="70bd2-339">Dieser Wert wird nicht verwendet, wenn der Scheitelpunkt punktgröße enthält.</span><span class="sxs-lookup"><span data-stu-id="70bd2-339">This value is not used when the vertex contains point size.</span></span> <span data-ttu-id="70bd2-340">Dieser Wert befindet sich in Bildschirmbereichseinheiten, wenn D3DRS \_ POINTSCALEENABLE **auf FALSE** festgelegt ist; andernfalls ist dieser Wert in Weltraumeinheiten.</span><span class="sxs-lookup"><span data-stu-id="70bd2-340">This value is in screen space units if D3DRS\_POINTSCALEENABLE is **FALSE**; otherwise this value is in world space units.</span></span> <span data-ttu-id="70bd2-341">Der Standardwert ist der Wert, den ein Treiber zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="70bd2-341">The default value is the value a driver returns.</span></span> <span data-ttu-id="70bd2-342">Wenn ein Treiber 0 oder 1 zurückgibt, ist der Standardwert 64, was eine Emulation der Softwarepunktgröße zulässt.</span><span class="sxs-lookup"><span data-stu-id="70bd2-342">If a driver returns 0 or 1, the default value is 64, which allows software point size emulation.</span></span> <span data-ttu-id="70bd2-343">Da die [**IDirect3DDevice9::SetRenderState-Methode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) DWORD-Werte akzeptiert, muss Ihre Anwendung eine Variable, die den Wert enthält, wie im folgenden Codebeispiel gezeigt, casten.</span><span class="sxs-lookup"><span data-stu-id="70bd2-343">Because the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method accepts DWORD values, your application must cast a variable that contains the value, as shown in the following code example.</span></span>


```
m_pDevice9->SetRenderState(D3DRS_POINTSIZE, *((DWORD*)&pointSize));
```



</dd> <dt>

<span data-ttu-id="70bd2-344"><span id="D3DRS_POINTSIZE_MIN"></span><span id="d3drs_pointsize_min"></span>**D3DRS \_ POINTSIZE \_ MIN**</span><span class="sxs-lookup"><span data-stu-id="70bd2-344"><span id="D3DRS_POINTSIZE_MIN"></span><span id="d3drs_pointsize_min"></span>**D3DRS\_POINTSIZE\_MIN**</span></span>
</dt> <dd>

<span data-ttu-id="70bd2-345">Ein float-Wert, der die Mindestgröße von Punktprimitiven angibt.</span><span class="sxs-lookup"><span data-stu-id="70bd2-345">A float value that specifies the minimum size of point primitives.</span></span> <span data-ttu-id="70bd2-346">Punktprimitiven werden während des Renderings an diese Größe klammern.</span><span class="sxs-lookup"><span data-stu-id="70bd2-346">Point primitives are clamped to this size during rendering.</span></span> <span data-ttu-id="70bd2-347">Wenn sie auf Werte kleiner als 1,0 festlegen, werden Punkte entfernt, wenn der Punkt keinen Pixelmittelpunkt verdeckt und Antialiasing deaktiviert oder mit geringerer Intensität gerendert wird, wenn Antialiasing aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="70bd2-347">Setting this to values smaller than 1.0 results in points dropping out when the point does not cover a pixel center and antialiasing is disabled or being rendered with reduced intensity when antialiasing is enabled.</span></span> <span data-ttu-id="70bd2-348">Der Standardwert ist 1,0f.</span><span class="sxs-lookup"><span data-stu-id="70bd2-348">The default value is 1.0f.</span></span> <span data-ttu-id="70bd2-349">Der Bereich für diesen Wert ist größer oder gleich 0,0f.</span><span class="sxs-lookup"><span data-stu-id="70bd2-349">The range for this value is greater than or equal to 0.0f.</span></span> <span data-ttu-id="70bd2-350">Da die [**IDirect3DDevice9::SetRenderState-Methode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) DWORD-Werte akzeptiert, muss Ihre Anwendung eine Variable, die den Wert enthält, wie im folgenden Codebeispiel gezeigt, casten.</span><span class="sxs-lookup"><span data-stu-id="70bd2-350">Because the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method accepts DWORD values, your application must cast a variable that contains the value, as shown in the following code example.</span></span>


```
m_pDevice9->SetRenderState(D3DRS_POINTSIZE_MIN, *((DWORD*)&pointSizeMin));
```



</dd> <dt>

<span data-ttu-id="70bd2-351"><span id="D3DRS_POINTSPRITEENABLE"></span><span id="d3drs_pointspriteenable"></span>**D3DRS \_ POINTSPRITEENABLE**</span><span class="sxs-lookup"><span data-stu-id="70bd2-351"><span id="D3DRS_POINTSPRITEENABLE"></span><span id="d3drs_pointspriteenable"></span>**D3DRS\_POINTSPRITEENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="70bd2-352">bool-Wert.</span><span class="sxs-lookup"><span data-stu-id="70bd2-352">bool value.</span></span> <span data-ttu-id="70bd2-353">True **gibt** an, dass Texturkoordinaten von Punktprimitiven so festgelegt werden, dass vollständige Texturen auf jedem Punkt zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="70bd2-353">When **TRUE**, texture coordinates of point primitives are set so that full textures are mapped on each point.</span></span> <span data-ttu-id="70bd2-354">False **gibt** an, dass die Scheitelpunkttexturkoordinaten für den gesamten Punkt verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="70bd2-354">When **FALSE**, the vertex texture coordinates are used for the entire point.</span></span> <span data-ttu-id="70bd2-355">Der Standardwert ist **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="70bd2-355">The default value is **FALSE**.</span></span> <span data-ttu-id="70bd2-356">Sie können DirectX 7-Stilpunkte im Einzelpixelformat erreichen, indem Sie D3DRS \_ POINTSCALEENABLE auf **FALSE** und D3DRS \_ POINTSIZE auf 1.0 festlegen. Dies sind die Standardwerte.</span><span class="sxs-lookup"><span data-stu-id="70bd2-356">You can achieve DirectX 7 style single-pixel points by setting D3DRS\_POINTSCALEENABLE to **FALSE** and D3DRS\_POINTSIZE to 1.0, which are the default values.</span></span>

</dd> <dt>

<span data-ttu-id="70bd2-357"><span id="D3DRS_POINTSCALEENABLE"></span><span id="d3drs_pointscaleenable"></span>**D3DRS \_ POINTSCALEENABLE**</span><span class="sxs-lookup"><span data-stu-id="70bd2-357"><span id="D3DRS_POINTSCALEENABLE"></span><span id="d3drs_pointscaleenable"></span>**D3DRS\_POINTSCALEENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="70bd2-358">bool-Wert, der die Berechnung der Größe für Punktprimitive steuert.</span><span class="sxs-lookup"><span data-stu-id="70bd2-358">bool value that controls computation of size for point primitives.</span></span> <span data-ttu-id="70bd2-359">True gibt an, dass die Punktgröße als Kameraraumwert interpretiert wird und von der Distance-Funktion und dem Frustum zum Skalieren der Viewport-y-Achse skaliert wird, um die endgültige Bildschirmbereichspunktgröße zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="70bd2-359">When **TRUE**, the point size is interpreted as a camera space value and is scaled by the distance function and the frustum to viewport y-axis scaling to compute the final screen-space point size.</span></span> <span data-ttu-id="70bd2-360">False gibt an, dass die Punktgröße als Bildschirmbereich interpretiert und direkt verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="70bd2-360">When **FALSE**, the point size is interpreted as screen space and used directly.</span></span> <span data-ttu-id="70bd2-361">Der Standardwert ist **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="70bd2-361">The default value is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="70bd2-362"><span id="D3DRS_POINTSCALE_A"></span><span id="d3drs_pointscale_a"></span>**D3DRS \_ POINTSCALE \_ A**</span><span class="sxs-lookup"><span data-stu-id="70bd2-362"><span id="D3DRS_POINTSCALE_A"></span><span id="d3drs_pointscale_a"></span>**D3DRS\_POINTSCALE\_A**</span></span>
</dt> <dd>

<span data-ttu-id="70bd2-363">Ein float-Wert, der die abstandsbasierte Größendämpfung für Punktprimitive steuert.</span><span class="sxs-lookup"><span data-stu-id="70bd2-363">A float value that controls for distance-based size attenuation for point primitives.</span></span> <span data-ttu-id="70bd2-364">Nur aktiv, wenn D3DRS \_ POINTSCALEENABLE **TRUE** ist.</span><span class="sxs-lookup"><span data-stu-id="70bd2-364">Active only when D3DRS\_POINTSCALEENABLE is **TRUE**.</span></span> <span data-ttu-id="70bd2-365">Der Standardwert ist 1,0f.</span><span class="sxs-lookup"><span data-stu-id="70bd2-365">The default value is 1.0f.</span></span> <span data-ttu-id="70bd2-366">Der Bereich für diesen Wert ist größer oder gleich 0,0f.</span><span class="sxs-lookup"><span data-stu-id="70bd2-366">The range for this value is greater than or equal to 0.0f.</span></span> <span data-ttu-id="70bd2-367">Da die [**IDirect3DDevice9::SetRenderState-Methode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) DWORD-Werte akzeptiert, muss Ihre Anwendung eine Variable mit dem Wert wandeln, wie im folgenden Codebeispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="70bd2-367">Because the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method accepts DWORD values, your application must cast a variable that contains the value, as shown in the following code example.</span></span>


```
m_pDevice9->SetRenderState(D3DRS_POINTSCALE_A, *((DWORD*)&pointScaleA));
```



</dd> <dt>

<span data-ttu-id="70bd2-368"><span id="D3DRS_POINTSCALE_B"></span><span id="d3drs_pointscale_b"></span>**D3DRS \_ POINTSCALE \_ B**</span><span class="sxs-lookup"><span data-stu-id="70bd2-368"><span id="D3DRS_POINTSCALE_B"></span><span id="d3drs_pointscale_b"></span>**D3DRS\_POINTSCALE\_B**</span></span>
</dt> <dd>

<span data-ttu-id="70bd2-369">Ein float-Wert, der die abstandsbasierte Größendämpfung für Punktprimitive steuert.</span><span class="sxs-lookup"><span data-stu-id="70bd2-369">A float value that controls for distance-based size attenuation for point primitives.</span></span> <span data-ttu-id="70bd2-370">Nur aktiv, wenn D3DRS \_ POINTSCALEENABLE **TRUE** ist.</span><span class="sxs-lookup"><span data-stu-id="70bd2-370">Active only when D3DRS\_POINTSCALEENABLE is **TRUE**.</span></span> <span data-ttu-id="70bd2-371">Der Standardwert ist 0,0f.</span><span class="sxs-lookup"><span data-stu-id="70bd2-371">The default value is 0.0f.</span></span> <span data-ttu-id="70bd2-372">Der Bereich für diesen Wert ist größer oder gleich 0,0f.</span><span class="sxs-lookup"><span data-stu-id="70bd2-372">The range for this value is greater than or equal to 0.0f.</span></span> <span data-ttu-id="70bd2-373">Da die [**IDirect3DDevice9::SetRenderState-Methode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) DWORD-Werte akzeptiert, muss Ihre Anwendung eine Variable mit dem Wert wandeln, wie im folgenden Codebeispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="70bd2-373">Because the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method accepts DWORD values, your application must cast a variable that contains the value, as shown in the following code example.</span></span>


```
m_pDevice9->SetRenderState(D3DRS_POINTSCALE_B, *((DWORD*)&pointScaleB));
```



</dd> <dt>

<span data-ttu-id="70bd2-374"><span id="D3DRS_POINTSCALE_C"></span><span id="d3drs_pointscale_c"></span>**D3DRS \_ POINTSCALE \_ C**</span><span class="sxs-lookup"><span data-stu-id="70bd2-374"><span id="D3DRS_POINTSCALE_C"></span><span id="d3drs_pointscale_c"></span>**D3DRS\_POINTSCALE\_C**</span></span>
</dt> <dd>

<span data-ttu-id="70bd2-375">Ein float-Wert, der die abstandsbasierte Größendämpfung für Punktprimitive steuert.</span><span class="sxs-lookup"><span data-stu-id="70bd2-375">A float value that controls for distance-based size attenuation for point primitives.</span></span> <span data-ttu-id="70bd2-376">Nur aktiv, wenn D3DRS \_ POINTSCALEENABLE **TRUE** ist.</span><span class="sxs-lookup"><span data-stu-id="70bd2-376">Active only when D3DRS\_POINTSCALEENABLE is **TRUE**.</span></span> <span data-ttu-id="70bd2-377">Der Standardwert ist 0,0f.</span><span class="sxs-lookup"><span data-stu-id="70bd2-377">The default value is 0.0f.</span></span> <span data-ttu-id="70bd2-378">Der Bereich für diesen Wert ist größer oder gleich 0,0f.</span><span class="sxs-lookup"><span data-stu-id="70bd2-378">The range for this value is greater than or equal to 0.0f.</span></span> <span data-ttu-id="70bd2-379">Da die [**IDirect3DDevice9::SetRenderState-Methode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) DWORD-Werte akzeptiert, muss Ihre Anwendung eine Variable, die den Wert enthält, wie im folgenden Codebeispiel gezeigt, casten.</span><span class="sxs-lookup"><span data-stu-id="70bd2-379">Because the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method accepts DWORD values, your application must cast a variable that contains the value, as shown in the following code example.</span></span>


```
m_pDevice9->SetRenderState(D3DRS_POINTSCALE_C, *((DWORD*)&pointScaleC));
```



</dd> <dt>

<span data-ttu-id="70bd2-380"><span id="D3DRS_MULTISAMPLEANTIALIAS"></span><span id="d3drs_multisampleantialias"></span>**D3DRS \_ MULTISAMPLEANTIALIAS**</span><span class="sxs-lookup"><span data-stu-id="70bd2-380"><span id="D3DRS_MULTISAMPLEANTIALIAS"></span><span id="d3drs_multisampleantialias"></span>**D3DRS\_MULTISAMPLEANTIALIAS**</span></span>
</dt> <dd>

<span data-ttu-id="70bd2-381">bool-Wert, der bestimmt, wie einzelne Stichproben berechnet werden, wenn ein Multisample-Renderzielpuffer verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="70bd2-381">bool value that determines how individual samples are computed when using a multisample render-target buffer.</span></span> <span data-ttu-id="70bd2-382">Wenn dies **auf TRUE** festgelegt ist, werden die mehreren Stichproben berechnet, sodass das Antialiasing in der gesamten Szene durch Stichprobenentnahme an verschiedenen Beispielpositionen für jede stichprobebasierte Stichprobe durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="70bd2-382">When set to **TRUE**, the multiple samples are computed so that full-scene antialiasing is performed by sampling at different sample positions for each multiple sample.</span></span> <span data-ttu-id="70bd2-383">Wenn diese Option auf **FALSE** festgelegt ist, werden die verschiedenen Stichproben alle mit demselben Beispielwert geschrieben, der in der Pixelmitte entnommen wird, wodurch nicht antialiasiertes Rendering in einen Multisamplepuffer ermöglicht wird.</span><span class="sxs-lookup"><span data-stu-id="70bd2-383">When set to **FALSE**, the multiple samples are all written with the same sample value, sampled at the pixel center, which allows non-antialiased rendering to a multisample buffer.</span></span> <span data-ttu-id="70bd2-384">Dieser Renderzustand hat keine Auswirkungen beim Rendern in einen einzelnen Beispielpuffer.</span><span class="sxs-lookup"><span data-stu-id="70bd2-384">This render state has no effect when rendering to a single sample buffer.</span></span> <span data-ttu-id="70bd2-385">Der Standardwert ist **TRUE.**</span><span class="sxs-lookup"><span data-stu-id="70bd2-385">The default value is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="70bd2-386"><span id="D3DRS_MULTISAMPLEMASK"></span><span id="d3drs_multisamplemask"></span>**D3DRS \_ MULTISAMPLEMASK**</span><span class="sxs-lookup"><span data-stu-id="70bd2-386"><span id="D3DRS_MULTISAMPLEMASK"></span><span id="d3drs_multisamplemask"></span>**D3DRS\_MULTISAMPLEMASK**</span></span>
</dt> <dd>

<span data-ttu-id="70bd2-387">Jedes Bit in dieser Maske, beginnend mit dem am wenigsten signifikanten Bit (LSB), steuert die Änderung eines der Beispiele in einem Multisample-Renderziel.</span><span class="sxs-lookup"><span data-stu-id="70bd2-387">Each bit in this mask, starting at the least significant bit (LSB), controls modification of one of the samples in a multisample render target.</span></span> <span data-ttu-id="70bd2-388">Daher enthält das untere Byte für ein Renderziel mit acht Stichproben die acht Schreibberechtigungen für jede der acht Stichproben.</span><span class="sxs-lookup"><span data-stu-id="70bd2-388">Thus, for an 8-sample render target, the low byte contains the eight write enables for each of the eight samples.</span></span> <span data-ttu-id="70bd2-389">Dieser Renderzustand hat keine Auswirkungen beim Rendern in einen einzelnen Beispielpuffer.</span><span class="sxs-lookup"><span data-stu-id="70bd2-389">This render state has no effect when rendering to a single sample buffer.</span></span> <span data-ttu-id="70bd2-390">Der Standardwert ist 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="70bd2-390">The default value is 0xFFFFFFFF.</span></span>

<span data-ttu-id="70bd2-391">Dieser Renderzustand ermöglicht die Verwendung eines Multisamplepuffers als Akkumulationspuffer, wobei multipass-Rendering der Geometrie durchgeführt wird, wobei jeder Durchlauf eine Teilmenge von Stichproben aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="70bd2-391">This render state enables use of a multisample buffer as an accumulation buffer, doing multipass rendering of geometry where each pass updates a subset of samples.</span></span>

<span data-ttu-id="70bd2-392">Wenn es n Multisamples und k aktivierte Stichproben gibt, sollte die resultierende Intensität des gerenderten Bilds k/n sein.</span><span class="sxs-lookup"><span data-stu-id="70bd2-392">If there are n multisamples and k enabled samples, the resulting intensity of the rendered image should be k/n.</span></span> <span data-ttu-id="70bd2-393">Jede Komponente RGB jedes Pixels wird durch k/n faktor.</span><span class="sxs-lookup"><span data-stu-id="70bd2-393">Each component RGB of every pixel is factored by k/n.</span></span>

</dd> <dt>

<span data-ttu-id="70bd2-394"><span id="D3DRS_PATCHEDGESTYLE"></span><span id="d3drs_patchedgestyle"></span>**D3DRS \_ PATCHEDGESTYLE**</span><span class="sxs-lookup"><span data-stu-id="70bd2-394"><span id="D3DRS_PATCHEDGESTYLE"></span><span id="d3drs_patchedgestyle"></span>**D3DRS\_PATCHEDGESTYLE**</span></span>
</dt> <dd>

<span data-ttu-id="70bd2-395">Legt fest, ob Patchränder das Mosaik im Float-Stil verwenden.</span><span class="sxs-lookup"><span data-stu-id="70bd2-395">Sets whether patch edges will use float style tessellation.</span></span> <span data-ttu-id="70bd2-396">Mögliche Werte werden durch den [**aufzählten D3DPATCHEDGESTYLE-Typ**](./d3dpatchedgestyle.md) definiert.</span><span class="sxs-lookup"><span data-stu-id="70bd2-396">Possible values are defined by the [**D3DPATCHEDGESTYLE**](./d3dpatchedgestyle.md) enumerated type.</span></span> <span data-ttu-id="70bd2-397">Der Standardwert ist D3DPATCHEDGE \_ DISCRETE.</span><span class="sxs-lookup"><span data-stu-id="70bd2-397">The default value is D3DPATCHEDGE\_DISCRETE.</span></span>

</dd> <dt>

<span data-ttu-id="70bd2-398"><span id="D3DRS_DEBUGMONITORTOKEN"></span><span id="d3drs_debugmonitortoken"></span>**D3DRS \_ DEBUGMONITORTOKEN**</span><span class="sxs-lookup"><span data-stu-id="70bd2-398"><span id="D3DRS_DEBUGMONITORTOKEN"></span><span id="d3drs_debugmonitortoken"></span>**D3DRS\_DEBUGMONITORTOKEN**</span></span>
</dt> <dd>

<span data-ttu-id="70bd2-399">Legen Sie nur für das Debuggen des Monitors fest.</span><span class="sxs-lookup"><span data-stu-id="70bd2-399">Set only for debugging the monitor.</span></span> <span data-ttu-id="70bd2-400">Mögliche Werte werden durch den [**D3DDEBUGMONITORTOKENS-Enumerationstyp**](./d3ddebugmonitortokens.md) definiert.</span><span class="sxs-lookup"><span data-stu-id="70bd2-400">Possible values are defined by the [**D3DDEBUGMONITORTOKENS**](./d3ddebugmonitortokens.md) enumerated type.</span></span> <span data-ttu-id="70bd2-401">Beachten Sie Folgendes: Wenn D3DRS \_ DEBUGMONITORTOKEN festgelegt ist, wird der Aufruf als Übergabe eines Tokens an den Debugmonitor behandelt.</span><span class="sxs-lookup"><span data-stu-id="70bd2-401">Note that if D3DRS\_DEBUGMONITORTOKEN is set, the call is treated as passing a token to the debug monitor.</span></span> <span data-ttu-id="70bd2-402">Wenn beispielsweise – nach der Übergabe von D3DDMT \_ ENABLE oder D3DDMT \_ DISABLE an D3DRS \_ DEBUGMONITORTOKEN – andere Tokenwerte übergeben werden, bleibt der Zustand (aktiviert oder deaktiviert) des Debugmonitors erhalten.</span><span class="sxs-lookup"><span data-stu-id="70bd2-402">For example, if - after passing D3DDMT\_ENABLE or D3DDMT\_DISABLE to D3DRS\_DEBUGMONITORTOKEN - other token values are passed in, the state (enabled or disabled) of the debug monitor will still persist.</span></span>

<span data-ttu-id="70bd2-403">Dieser Zustand ist nur für Debugbuilds nützlich.</span><span class="sxs-lookup"><span data-stu-id="70bd2-403">This state is only useful for debug builds.</span></span> <span data-ttu-id="70bd2-404">Der Debugmonitor ist standardmäßig auf D3DDMT \_ ENABLE eingestellt.</span><span class="sxs-lookup"><span data-stu-id="70bd2-404">The debug monitor defaults to D3DDMT\_ENABLE.</span></span>

</dd> <dt>

<span data-ttu-id="70bd2-405"><span id="D3DRS_POINTSIZE_MAX"></span><span id="d3drs_pointsize_max"></span>**D3DRS \_ POINTSIZE \_ MAX**</span><span class="sxs-lookup"><span data-stu-id="70bd2-405"><span id="D3DRS_POINTSIZE_MAX"></span><span id="d3drs_pointsize_max"></span>**D3DRS\_POINTSIZE\_MAX**</span></span>
</dt> <dd>

<span data-ttu-id="70bd2-406">Ein float-Wert, der die maximale Größe angibt, bis zu der Punkt-Sprites klammern werden.</span><span class="sxs-lookup"><span data-stu-id="70bd2-406">A float value that specifies the maximum size to which point sprites will be clamped.</span></span> <span data-ttu-id="70bd2-407">Der Wert muss kleiner oder gleich dem MaxPointSize-Member von [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) und größer oder gleich D3DRS \_ POINTSIZE \_ MIN sein.</span><span class="sxs-lookup"><span data-stu-id="70bd2-407">The value must be less than or equal to the MaxPointSize member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) and greater than or equal to D3DRS\_POINTSIZE\_MIN.</span></span> <span data-ttu-id="70bd2-408">Der Standardwert ist 64,0.</span><span class="sxs-lookup"><span data-stu-id="70bd2-408">The default value is 64.0.</span></span> <span data-ttu-id="70bd2-409">Da die [**IDirect3DDevice9::SetRenderState-Methode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) DWORD-Werte akzeptiert, muss Ihre Anwendung eine Variable mit dem Wert wandeln, wie im folgenden Codebeispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="70bd2-409">Because the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method accepts DWORD values, your application must cast a variable that contains the value, as shown in the following code example.</span></span>


```
m_pDevice9->SetRenderState(D3DRS_PONTSIZE_MAX, *((DWORD*)&pointSizeMax));
```



</dd> <dt>

<span data-ttu-id="70bd2-410"><span id="D3DRS_INDEXEDVERTEXBLENDENABLE"></span><span id="d3drs_indexedvertexblendenable"></span>**D3DRS \_ INDEXEDVERTEXBLENDENABLE**</span><span class="sxs-lookup"><span data-stu-id="70bd2-410"><span id="D3DRS_INDEXEDVERTEXBLENDENABLE"></span><span id="d3drs_indexedvertexblendenable"></span>**D3DRS\_INDEXEDVERTEXBLENDENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="70bd2-411">bool-Wert, der indizierte Vertexmischung aktiviert oder deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="70bd2-411">bool value that enables or disables indexed vertex blending.</span></span> <span data-ttu-id="70bd2-412">Der Standardwert ist **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="70bd2-412">The default value is **FALSE**.</span></span> <span data-ttu-id="70bd2-413">Wenn auf **TRUE** festgelegt ist, ist die vertexvermischung indiziert aktiviert.</span><span class="sxs-lookup"><span data-stu-id="70bd2-413">When set to **TRUE**, indexed vertex blending is enabled.</span></span> <span data-ttu-id="70bd2-414">Wenn **false** festgelegt ist, ist die indizierte Scheitelpunktmischung deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="70bd2-414">When set to **FALSE**, indexed vertex blending is disabled.</span></span> <span data-ttu-id="70bd2-415">Wenn dieser Renderzustand aktiviert ist, muss der Benutzer Matrixindizes als gepacktes DWORD mit jedem Scheitelpunkt übergeben.</span><span class="sxs-lookup"><span data-stu-id="70bd2-415">If this render state is enabled, the user must pass matrix indices as a packed DWORDwith every vertex.</span></span> <span data-ttu-id="70bd2-416">Wenn der Renderzustand deaktiviert ist und vertex blending über den D3DRS \_ VERTEXBLEND-Zustand aktiviert ist, entspricht dies matrixindizes 0, 1, 2, 3 in jedem Scheitelpunkt.</span><span class="sxs-lookup"><span data-stu-id="70bd2-416">When the render state is disabled and vertex blending is enabled through the D3DRS\_VERTEXBLEND state, it is equivalent to having matrix indices 0, 1, 2, 3 in every vertex.</span></span>

</dd> <dt>

<span data-ttu-id="70bd2-417"><span id="D3DRS_COLORWRITEENABLE"></span><span id="d3drs_colorwriteenable"></span>**D3DRS \_ COLORWRITEENABLE**</span><span class="sxs-lookup"><span data-stu-id="70bd2-417"><span id="D3DRS_COLORWRITEENABLE"></span><span id="d3drs_colorwriteenable"></span>**D3DRS\_COLORWRITEENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="70bd2-418">UINT-Wert, der einen kanalbezogenen Schreibvorgang für den Renderzielfarbpuffer ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="70bd2-418">UINT value that enables a per-channel write for the render-target color buffer.</span></span> <span data-ttu-id="70bd2-419">Ein festgelegtes Bit führt zu einer Aktualisierung des Farbkanals während des 3D-Renderings.</span><span class="sxs-lookup"><span data-stu-id="70bd2-419">A set bit results in the color channel being updated during 3D rendering.</span></span> <span data-ttu-id="70bd2-420">Ein klares Bit führt zu einer Nichtbeeinflussung des Farbkanals.</span><span class="sxs-lookup"><span data-stu-id="70bd2-420">A clear bit results in the color channel being unaffected.</span></span> <span data-ttu-id="70bd2-421">Diese Funktionalität ist verfügbar, wenn das D3DPMISCCAPS \_ COLORWRITEENABLE-Funktionsbit im PrimitiveMiscCaps-Member der [**D3DCAPS9-Struktur**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) für das Gerät festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="70bd2-421">This functionality is available if the D3DPMISCCAPS\_COLORWRITEENABLE capabilities bit is set in the PrimitiveMiscCaps member of the [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure for the device.</span></span> <span data-ttu-id="70bd2-422">Dieser Renderzustand wirkt sich nicht auf den Clear-Vorgang aus.</span><span class="sxs-lookup"><span data-stu-id="70bd2-422">This render state does not affect the clear operation.</span></span> <span data-ttu-id="70bd2-423">Der Standardwert ist 0x0000000F.</span><span class="sxs-lookup"><span data-stu-id="70bd2-423">The default value is 0x0000000F.</span></span>

<span data-ttu-id="70bd2-424">Gültige Werte für diesen Renderzustand können eine beliebige Kombination der Flags D3DCOLORWRITEENABLE \_ ALPHA, D3DCOLORWRITEENABLE \_ BLUE, D3DCOLORWRITEENABLE GREEN oder \_ D3DCOLORWRITEENABLE \_ RED sein.</span><span class="sxs-lookup"><span data-stu-id="70bd2-424">Valid values for this render state can be any combination of the D3DCOLORWRITEENABLE\_ALPHA, D3DCOLORWRITEENABLE\_BLUE, D3DCOLORWRITEENABLE\_GREEN, or D3DCOLORWRITEENABLE\_RED flags.</span></span>

</dd> <dt>

<span data-ttu-id="70bd2-425"><span id="D3DRS_TWEENFACTOR"></span><span id="d3drs_tweenfactor"></span>**D3DRS \_ TWEENFACTOR**</span><span class="sxs-lookup"><span data-stu-id="70bd2-425"><span id="D3DRS_TWEENFACTOR"></span><span id="d3drs_tweenfactor"></span>**D3DRS\_TWEENFACTOR**</span></span>
</dt> <dd>

<span data-ttu-id="70bd2-426">Ein float-Wert, der den Tweenfaktor steuert.</span><span class="sxs-lookup"><span data-stu-id="70bd2-426">A float value that controls the tween factor.</span></span> <span data-ttu-id="70bd2-427">Der Standardwert ist 0,0f.</span><span class="sxs-lookup"><span data-stu-id="70bd2-427">The default value is 0.0f.</span></span> <span data-ttu-id="70bd2-428">Da die [**IDirect3DDevice9::SetRenderState-Methode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) DWORD-Werte akzeptiert, muss Ihre Anwendung eine Variable, die den Wert enthält, wie im folgenden Codebeispiel gezeigt, casten.</span><span class="sxs-lookup"><span data-stu-id="70bd2-428">Because the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method accepts DWORD values, your application must cast a variable that contains the value, as shown in the following code example.</span></span>


```
m_pDevice9->SetRenderState(D3DRS_TWEENFACTOR, *((DWORD*)&TweenFactor));
```



</dd> <dt>

<span data-ttu-id="70bd2-429"><span id="D3DRS_BLENDOP"></span><span id="d3drs_blendop"></span>**D3DRS \_ BLENDOP**</span><span class="sxs-lookup"><span data-stu-id="70bd2-429"><span id="D3DRS_BLENDOP"></span><span id="d3drs_blendop"></span>**D3DRS\_BLENDOP**</span></span>
</dt> <dd>

<span data-ttu-id="70bd2-430">Der Wert, der verwendet wird, um die arithmetische Operation auszuwählen, die angewendet wird, wenn der Alphablending-Renderzustand D3DRS \_ ALPHABLENDENABLE auf TRUE festgelegt **ist.**</span><span class="sxs-lookup"><span data-stu-id="70bd2-430">Value used to select the arithmetic operation applied when the alpha blending render state, D3DRS\_ALPHABLENDENABLE, is set to **TRUE**.</span></span> <span data-ttu-id="70bd2-431">Gültige Werte werden durch den [**aufzählten D3DBLENDOP-Typ**](./d3dblendop.md) definiert.</span><span class="sxs-lookup"><span data-stu-id="70bd2-431">Valid values are defined by the [**D3DBLENDOP**](./d3dblendop.md) enumerated type.</span></span> <span data-ttu-id="70bd2-432">Der Standardwert ist D3DBLENDOP \_ ADD.</span><span class="sxs-lookup"><span data-stu-id="70bd2-432">The default value is D3DBLENDOP\_ADD.</span></span>

<span data-ttu-id="70bd2-433">Wenn die D3DPMISCCAPS BLENDOP-Gerätefunktion nicht \_ unterstützt wird, wird D3DBLENDOP \_ ADD ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="70bd2-433">If the D3DPMISCCAPS\_BLENDOP device capability is not supported, then D3DBLENDOP\_ADD is performed.</span></span>

</dd> <dt>

<span data-ttu-id="70bd2-434"><span id="D3DRS_POSITIONDEGREE"></span><span id="d3drs_positiondegree"></span>**D3DRS \_ POSITIONDEGREE**</span><span class="sxs-lookup"><span data-stu-id="70bd2-434"><span id="D3DRS_POSITIONDEGREE"></span><span id="d3drs_positiondegree"></span>**D3DRS\_POSITIONDEGREE**</span></span>
</dt> <dd>

<span data-ttu-id="70bd2-435">N-Patchpositionsinterpolationsgrad.</span><span class="sxs-lookup"><span data-stu-id="70bd2-435">N-patch position interpolation degree.</span></span> <span data-ttu-id="70bd2-436">Die Werte können D3DDEGREE \_ CUBIC (Standard) oder D3DDEGREE \_ LINEAR sein.</span><span class="sxs-lookup"><span data-stu-id="70bd2-436">The values can be D3DDEGREE\_CUBIC (default) or D3DDEGREE\_LINEAR.</span></span> <span data-ttu-id="70bd2-437">Weitere Informationen finden Sie unter [**D3DDEGREETYPE**](./d3ddegreetype.md).</span><span class="sxs-lookup"><span data-stu-id="70bd2-437">For more information, see [**D3DDEGREETYPE**](./d3ddegreetype.md).</span></span>

</dd> <dt>

<span data-ttu-id="70bd2-438"><span id="D3DRS_NORMALDEGREE"></span><span id="d3drs_normaldegree"></span>**D3DRS \_ NORMALDEGREE**</span><span class="sxs-lookup"><span data-stu-id="70bd2-438"><span id="D3DRS_NORMALDEGREE"></span><span id="d3drs_normaldegree"></span>**D3DRS\_NORMALDEGREE**</span></span>
</dt> <dd>

<span data-ttu-id="70bd2-439">N-Patch Normal Interpolation Degree.</span><span class="sxs-lookup"><span data-stu-id="70bd2-439">N-patch normal interpolation degree.</span></span> <span data-ttu-id="70bd2-440">Die Werte können D3DDEGREE \_ LINEAR (Standard) oder D3DDEGREE \_ QUADRATIC sein.</span><span class="sxs-lookup"><span data-stu-id="70bd2-440">The values can be D3DDEGREE\_LINEAR (default) or D3DDEGREE\_QUADRATIC.</span></span> <span data-ttu-id="70bd2-441">Weitere Informationen finden Sie unter [**D3DDEGREETYPE.**](./d3ddegreetype.md)</span><span class="sxs-lookup"><span data-stu-id="70bd2-441">For more information, see [**D3DDEGREETYPE**](./d3ddegreetype.md).</span></span>

</dd> <dt>

<span data-ttu-id="70bd2-442"><span id="D3DRS_SCISSORTESTENABLE"></span><span id="d3drs_scissortestenable"></span>**D3DRS \_ SCISSORTESTENABLE**</span><span class="sxs-lookup"><span data-stu-id="70bd2-442"><span id="D3DRS_SCISSORTESTENABLE"></span><span id="d3drs_scissortestenable"></span>**D3DRS\_SCISSORTESTENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="70bd2-443">**TRUE** zum Aktivieren von Scissortests und **FALSE** zum Deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="70bd2-443">**TRUE** to enable scissor testing and **FALSE** to disable it.</span></span> <span data-ttu-id="70bd2-444">Der Standardwert ist **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="70bd2-444">The default value is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="70bd2-445"><span id="D3DRS_SLOPESCALEDEPTHBIAS"></span><span id="d3drs_slopescaledepthbias"></span>**D3DRS \_ IM 3DRS-REGLERCALEDEPTHBIAS**</span><span class="sxs-lookup"><span data-stu-id="70bd2-445"><span id="D3DRS_SLOPESCALEDEPTHBIAS"></span><span id="d3drs_slopescaledepthbias"></span>**D3DRS\_SLOPESCALEDEPTHBIAS**</span></span>
</dt> <dd>

<span data-ttu-id="70bd2-446">Wird verwendet, um zu bestimmen, wie viel Voreingenommenheit auf co-planare Primitive angewendet werden kann, um Z-Fighting zu reduzieren.</span><span class="sxs-lookup"><span data-stu-id="70bd2-446">Used to determine how much bias can be applied to co-planar primitives to reduce z-fighting.</span></span> <span data-ttu-id="70bd2-447">Der Standardwert ist 0.</span><span class="sxs-lookup"><span data-stu-id="70bd2-447">The default value is 0.</span></span>

<span data-ttu-id="70bd2-448">bias = \* (max. D3DRS \_ VERALTUNGSEDEPTHBIAS) + D3DRS \_ DEPTHBIAS.</span><span class="sxs-lookup"><span data-stu-id="70bd2-448">bias = (max \* D3DRS\_SLOPESCALEDEPTHBIAS) + D3DRS\_DEPTHBIAS.</span></span>

<span data-ttu-id="70bd2-449">dabei ist max die maximale Tiefenpiste des gerenderten Dreiecks.</span><span class="sxs-lookup"><span data-stu-id="70bd2-449">where max is the maximum depth slope of the triangle being rendered.</span></span>

</dd> <dt>

<span data-ttu-id="70bd2-450"><span id="D3DRS_ANTIALIASEDLINEENABLE"></span><span id="d3drs_antialiasedlineenable"></span>**D3DRS \_ ANTIALIASEDLINEENABLE**</span><span class="sxs-lookup"><span data-stu-id="70bd2-450"><span id="D3DRS_ANTIALIASEDLINEENABLE"></span><span id="d3drs_antialiasedlineenable"></span>**D3DRS\_ANTIALIASEDLINEENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="70bd2-451">**TRUE** zum Aktivieren von Zeilen antialiasing, **FALSE** zum Deaktivieren von Zeilen antialiasing.</span><span class="sxs-lookup"><span data-stu-id="70bd2-451">**TRUE** to enable line antialiasing, **FALSE** to disable line antialiasing.</span></span> <span data-ttu-id="70bd2-452">Der Standardwert ist **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="70bd2-452">The default value is **FALSE**.</span></span>

<span data-ttu-id="70bd2-453">Beim Rendern in ein Multisample-Renderziel wird D3DRS \_ ANTIALIASEDLINEENABLE ignoriert, und alle Zeilen werden als Alias gerendert.</span><span class="sxs-lookup"><span data-stu-id="70bd2-453">When rendering to a multisample render target, D3DRS\_ANTIALIASEDLINEENABLE is ignored and all lines are rendered aliased.</span></span> <span data-ttu-id="70bd2-454">Verwenden Sie [**ID3DXLine**](id3dxline.md) für antialiasiertes Zeilenrendering in einem Multisample-Renderziel.</span><span class="sxs-lookup"><span data-stu-id="70bd2-454">Use [**ID3DXLine**](id3dxline.md) for antialiased line rendering in a multisample render target.</span></span>

</dd> <dt>

<span data-ttu-id="70bd2-455"><span id="D3DRS_MINTESSELLATIONLEVEL"></span><span id="d3drs_mintessellationlevel"></span>**D3DRS \_ MINTESSELLATIONLEVEL**</span><span class="sxs-lookup"><span data-stu-id="70bd2-455"><span id="D3DRS_MINTESSELLATIONLEVEL"></span><span id="d3drs_mintessellationlevel"></span>**D3DRS\_MINTESSELLATIONLEVEL**</span></span>
</dt> <dd>

<span data-ttu-id="70bd2-456">Minimale Mosaikebene.</span><span class="sxs-lookup"><span data-stu-id="70bd2-456">Minimum tessellation level.</span></span> <span data-ttu-id="70bd2-457">Der Standardwert ist 1,0f.</span><span class="sxs-lookup"><span data-stu-id="70bd2-457">The default value is 1.0f.</span></span> <span data-ttu-id="70bd2-458">Siehe [Mosaik (Direct3D 9)](tessellation.md).</span><span class="sxs-lookup"><span data-stu-id="70bd2-458">See [Tessellation (Direct3D 9)](tessellation.md).</span></span>

</dd> <dt>

<span data-ttu-id="70bd2-459"><span id="D3DRS_MAXTESSELLATIONLEVEL"></span><span id="d3drs_maxtessellationlevel"></span>**D3DRS \_ MAXTESSELLATIONLEVEL**</span><span class="sxs-lookup"><span data-stu-id="70bd2-459"><span id="D3DRS_MAXTESSELLATIONLEVEL"></span><span id="d3drs_maxtessellationlevel"></span>**D3DRS\_MAXTESSELLATIONLEVEL**</span></span>
</dt> <dd>

<span data-ttu-id="70bd2-460">Maximale Mosaikebene.</span><span class="sxs-lookup"><span data-stu-id="70bd2-460">Maximum tessellation level.</span></span> <span data-ttu-id="70bd2-461">Der Standardwert ist 1,0f.</span><span class="sxs-lookup"><span data-stu-id="70bd2-461">The default value is 1.0f.</span></span> <span data-ttu-id="70bd2-462">Weitere [Informationen finden Sie unter Mosaik (Direct3D 9).](tessellation.md)</span><span class="sxs-lookup"><span data-stu-id="70bd2-462">See [Tessellation (Direct3D 9)](tessellation.md).</span></span>

</dd> <dt>

<span data-ttu-id="70bd2-463"><span id="D3DRS_ADAPTIVETESS_X"></span><span id="d3drs_adaptivetess_x"></span>**D3DRS \_ ADAPTIVETESS \_ X**</span><span class="sxs-lookup"><span data-stu-id="70bd2-463"><span id="D3DRS_ADAPTIVETESS_X"></span><span id="d3drs_adaptivetess_x"></span>**D3DRS\_ADAPTIVETESS\_X**</span></span>
</dt> <dd>

<span data-ttu-id="70bd2-464">Betrag bis zum adaptiven Mosaik in x-Richtung.</span><span class="sxs-lookup"><span data-stu-id="70bd2-464">Amount to adaptively tessellate, in the x direction.</span></span> <span data-ttu-id="70bd2-465">Der Standardwert ist 0,0f.</span><span class="sxs-lookup"><span data-stu-id="70bd2-465">Default value is 0.0f.</span></span> <span data-ttu-id="70bd2-466">Weitere Informationen [finden Sie unter Adaptive Mosaik](tessellation.md).</span><span class="sxs-lookup"><span data-stu-id="70bd2-466">See [Adaptive Tessellation](tessellation.md).</span></span>

</dd> <dt>

<span data-ttu-id="70bd2-467"><span id="D3DRS_ADAPTIVETESS_Y"></span><span id="d3drs_adaptivetess_y"></span>**D3DRS \_ ADAPTIVETESS \_ Y**</span><span class="sxs-lookup"><span data-stu-id="70bd2-467"><span id="D3DRS_ADAPTIVETESS_Y"></span><span id="d3drs_adaptivetess_y"></span>**D3DRS\_ADAPTIVETESS\_Y**</span></span>
</dt> <dd>

<span data-ttu-id="70bd2-468">Betrag bis zum adaptiven Mosaik in y-Richtung.</span><span class="sxs-lookup"><span data-stu-id="70bd2-468">Amount to adaptively tessellate, in the y direction.</span></span> <span data-ttu-id="70bd2-469">Der Standardwert ist 0,0f.</span><span class="sxs-lookup"><span data-stu-id="70bd2-469">Default value is 0.0f.</span></span> <span data-ttu-id="70bd2-470">Weitere Informationen [finden Sie unter Adaptive \_ Mosaik](tessellation.md).</span><span class="sxs-lookup"><span data-stu-id="70bd2-470">See [Adaptive\_Tessellation](tessellation.md).</span></span>

</dd> <dt>

<span data-ttu-id="70bd2-471"><span id="D3DRS_ADAPTIVETESS_Z"></span><span id="d3drs_adaptivetess_z"></span>**D3DRS \_ ADAPTIVETESS \_ Z**</span><span class="sxs-lookup"><span data-stu-id="70bd2-471"><span id="D3DRS_ADAPTIVETESS_Z"></span><span id="d3drs_adaptivetess_z"></span>**D3DRS\_ADAPTIVETESS\_Z**</span></span>
</dt> <dd>

<span data-ttu-id="70bd2-472">Betrag bis zum adaptiven Mosaik in z-Richtung.</span><span class="sxs-lookup"><span data-stu-id="70bd2-472">Amount to adaptively tessellate, in the z direction.</span></span> <span data-ttu-id="70bd2-473">Der Standardwert ist 1,0f.</span><span class="sxs-lookup"><span data-stu-id="70bd2-473">Default value is 1.0f.</span></span> <span data-ttu-id="70bd2-474">Weitere Informationen [finden Sie unter Adaptive \_ Mosaik](tessellation.md).</span><span class="sxs-lookup"><span data-stu-id="70bd2-474">See [Adaptive\_Tessellation](tessellation.md).</span></span>

</dd> <dt>

<span data-ttu-id="70bd2-475"><span id="D3DRS_ADAPTIVETESS_W"></span><span id="d3drs_adaptivetess_w"></span>**D3DRS \_ ADAPTIVETESS \_ W**</span><span class="sxs-lookup"><span data-stu-id="70bd2-475"><span id="D3DRS_ADAPTIVETESS_W"></span><span id="d3drs_adaptivetess_w"></span>**D3DRS\_ADAPTIVETESS\_W**</span></span>
</dt> <dd>

<span data-ttu-id="70bd2-476">Betrag bis zum adaptiven Mosaik in w-Richtung.</span><span class="sxs-lookup"><span data-stu-id="70bd2-476">Amount to adaptively tessellate, in the w direction.</span></span> <span data-ttu-id="70bd2-477">Der Standardwert ist 0,0f.</span><span class="sxs-lookup"><span data-stu-id="70bd2-477">Default value is 0.0f.</span></span> <span data-ttu-id="70bd2-478">Weitere Informationen [finden Sie unter Adaptive \_ Mosaik](tessellation.md).</span><span class="sxs-lookup"><span data-stu-id="70bd2-478">See [Adaptive\_Tessellation](tessellation.md).</span></span>

</dd> <dt>

<span data-ttu-id="70bd2-479"><span id="D3DRS_ENABLEADAPTIVETESSELLATION"></span><span id="d3drs_enableadaptivetessellation"></span>**D3DRS \_ ENABLEADAPTIVETESSELLATION**</span><span class="sxs-lookup"><span data-stu-id="70bd2-479"><span id="D3DRS_ENABLEADAPTIVETESSELLATION"></span><span id="d3drs_enableadaptivetessellation"></span>**D3DRS\_ENABLEADAPTIVETESSELLATION**</span></span>
</dt> <dd>

<span data-ttu-id="70bd2-480">**TRUE,** um das adaptive Mosaik zu aktivieren, **FALSE,** um es zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="70bd2-480">**TRUE** to enable adaptive tessellation, **FALSE** to disable it.</span></span> <span data-ttu-id="70bd2-481">Der Standardwert ist **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="70bd2-481">The default value is **FALSE**.</span></span> <span data-ttu-id="70bd2-482">Weitere Informationen [finden Sie unter Adaptive \_ Mosaik](tessellation.md).</span><span class="sxs-lookup"><span data-stu-id="70bd2-482">See [Adaptive\_Tessellation](tessellation.md).</span></span>

</dd> <dt>

<span data-ttu-id="70bd2-483"><span id="D3DRS_TWOSIDEDSTENCILMODE"></span><span id="d3drs_twosidedstencilmode"></span>**D3DRS \_ TWOSIDEDSTENCILMODE**</span><span class="sxs-lookup"><span data-stu-id="70bd2-483"><span id="D3DRS_TWOSIDEDSTENCILMODE"></span><span id="d3drs_twosidedstencilmode"></span>**D3DRS\_TWOSIDEDSTENCILMODE**</span></span>
</dt> <dd>

<span data-ttu-id="70bd2-484">**TRUE** aktiviert die zweiseitige Schablonierung, **FALSE** deaktiviert sie.</span><span class="sxs-lookup"><span data-stu-id="70bd2-484">**TRUE** enables two-sided stenciling, **FALSE** disables it.</span></span> <span data-ttu-id="70bd2-485">Der Standardwert ist **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="70bd2-485">The default value is **FALSE**.</span></span> <span data-ttu-id="70bd2-486">Die Anwendung sollte D3DRS \_ CULLMODE auf D3DCULL \_ NONE festlegen, um den zweiseitigen Schablonenmodus zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="70bd2-486">The application should set D3DRS\_CULLMODE to D3DCULL\_NONE to enable two-sided stencil mode.</span></span> <span data-ttu-id="70bd2-487">Wenn die Dreieckswindungsreihenfolge im Uhrzeigersinn erfolgt, werden die \_ D3DRS-STENCIL-Vorgänge \* verwendet.</span><span class="sxs-lookup"><span data-stu-id="70bd2-487">If the triangle winding order is clockwise, the D3DRS\_STENCIL\* operations will be used.</span></span> <span data-ttu-id="70bd2-488">Wenn die Ziehreihenfolge gegen den Uhrzeigersinn lautet, werden die D3DRS \_ \_ CCW-STENCIL-Vorgänge \* verwendet.</span><span class="sxs-lookup"><span data-stu-id="70bd2-488">If the winding order is counterclockwise, the D3DRS\_CCW\_STENCIL\* operations will be used.</span></span>

<span data-ttu-id="70bd2-489">Überprüfen Sie den StencilCaps-Member von [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) für D3DSTENCILCAPS TWOSIDED, um festzustellen, ob die zweiseitige Schablone unterstützt \_ wird.</span><span class="sxs-lookup"><span data-stu-id="70bd2-489">To see if two-sided stencil is supported, check the StencilCaps member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) for D3DSTENCILCAPS\_TWOSIDED.</span></span> <span data-ttu-id="70bd2-490">Siehe auch [D3DSTENCILCAPS](d3dstencilcaps.md).</span><span class="sxs-lookup"><span data-stu-id="70bd2-490">See also [D3DSTENCILCAPS](d3dstencilcaps.md).</span></span>

</dd> <dt>

<span data-ttu-id="70bd2-491"><span id="D3DRS_CCW_STENCILFAIL"></span><span id="d3drs_ccw_stencilfail"></span>**D3DRS \_ CCW \_ STENCILFAIL**</span><span class="sxs-lookup"><span data-stu-id="70bd2-491"><span id="D3DRS_CCW_STENCILFAIL"></span><span id="d3drs_ccw_stencilfail"></span>**D3DRS\_CCW\_STENCILFAIL**</span></span>
</dt> <dd>

<span data-ttu-id="70bd2-492">Schablonenvorgang, der ausgeführt werden soll, wenn der CCW-Schablonentest fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="70bd2-492">Stencil operation to perform if CCW stencil test fails.</span></span> <span data-ttu-id="70bd2-493">Werte stammen vom [**D3DSTENCILOP-Enumerationstyp.**](./d3dstencilop.md)</span><span class="sxs-lookup"><span data-stu-id="70bd2-493">Values are from the [**D3DSTENCILOP**](./d3dstencilop.md) enumerated type.</span></span> <span data-ttu-id="70bd2-494">Der Standardwert ist D3DSTENCILOP \_ KEEP.</span><span class="sxs-lookup"><span data-stu-id="70bd2-494">The default value is D3DSTENCILOP\_KEEP.</span></span>

</dd> <dt>

<span data-ttu-id="70bd2-495"><span id="D3DRS_CCW_STENCILZFAIL"></span><span id="d3drs_ccw_stencilzfail"></span>**D3DRS \_ CCW \_ STENCILZFAIL**</span><span class="sxs-lookup"><span data-stu-id="70bd2-495"><span id="D3DRS_CCW_STENCILZFAIL"></span><span id="d3drs_ccw_stencilzfail"></span>**D3DRS\_CCW\_STENCILZFAIL**</span></span>
</dt> <dd>

<span data-ttu-id="70bd2-496">Schablonenvorgang, der ausgeführt werden soll, wenn der CCW-Schablonentest erfolgreich war und z-test fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="70bd2-496">Stencil operation to perform if CCW stencil test passes and z-test fails.</span></span> <span data-ttu-id="70bd2-497">Werte stammen vom [**D3DSTENCILOP-Enumerationstyp.**](./d3dstencilop.md)</span><span class="sxs-lookup"><span data-stu-id="70bd2-497">Values are from the [**D3DSTENCILOP**](./d3dstencilop.md) enumerated type.</span></span> <span data-ttu-id="70bd2-498">Der Standardwert ist D3DSTENCILOP \_ KEEP.</span><span class="sxs-lookup"><span data-stu-id="70bd2-498">The default value is D3DSTENCILOP\_KEEP.</span></span>

</dd> <dt>

<span data-ttu-id="70bd2-499"><span id="D3DRS_CCW_STENCILPASS"></span><span id="d3drs_ccw_stencilpass"></span>**D3DRS \_ CCW \_ STENCILPASS**</span><span class="sxs-lookup"><span data-stu-id="70bd2-499"><span id="D3DRS_CCW_STENCILPASS"></span><span id="d3drs_ccw_stencilpass"></span>**D3DRS\_CCW\_STENCILPASS**</span></span>
</dt> <dd>

<span data-ttu-id="70bd2-500">Schablonenvorgang, der ausgeführt werden soll, wenn sowohl CCW-Schablone als auch Z-Tests erfolgreich sind.</span><span class="sxs-lookup"><span data-stu-id="70bd2-500">Stencil operation to perform if both CCW stencil and z-tests pass.</span></span> <span data-ttu-id="70bd2-501">Werte stammen vom [**D3DSTENCILOP-Enumerationstyp.**](./d3dstencilop.md)</span><span class="sxs-lookup"><span data-stu-id="70bd2-501">Values are from the [**D3DSTENCILOP**](./d3dstencilop.md) enumerated type.</span></span> <span data-ttu-id="70bd2-502">Der Standardwert ist D3DSTENCILOP \_ KEEP.</span><span class="sxs-lookup"><span data-stu-id="70bd2-502">The default value is D3DSTENCILOP\_KEEP.</span></span>

</dd> <dt>

<span data-ttu-id="70bd2-503"><span id="D3DRS_CCW_STENCILFUNC"></span><span id="d3drs_ccw_stencilfunc"></span>**D3DRS \_ CCW \_ STENCILFUNC**</span><span class="sxs-lookup"><span data-stu-id="70bd2-503"><span id="D3DRS_CCW_STENCILFUNC"></span><span id="d3drs_ccw_stencilfunc"></span>**D3DRS\_CCW\_STENCILFUNC**</span></span>
</dt> <dd>

<span data-ttu-id="70bd2-504">Die Vergleichsfunktion.</span><span class="sxs-lookup"><span data-stu-id="70bd2-504">The comparison function.</span></span> <span data-ttu-id="70bd2-505">Der CCW-Schablonentest besteht, wenn die Schablonenfunktion ((ref & mask) (Schablonen- & maske)) **TRUE ist.**</span><span class="sxs-lookup"><span data-stu-id="70bd2-505">CCW stencil test passes if ((ref & mask) stencil function (stencil & mask)) is **TRUE**.</span></span> <span data-ttu-id="70bd2-506">Werte werden vom [**aufzählten D3DCMPFUNC-Typ**](./d3dcmpfunc.md) verwendet.</span><span class="sxs-lookup"><span data-stu-id="70bd2-506">Values are from the [**D3DCMPFUNC**](./d3dcmpfunc.md) enumerated type.</span></span> <span data-ttu-id="70bd2-507">Der Standardwert ist D3DCMP \_ ALWAYS.</span><span class="sxs-lookup"><span data-stu-id="70bd2-507">The default value is D3DCMP\_ALWAYS.</span></span>

</dd> <dt>

<span data-ttu-id="70bd2-508"><span id="D3DRS_COLORWRITEENABLE1"></span><span id="d3drs_colorwriteenable1"></span>**D3DRS \_ COLORWRITEENABLE1**</span><span class="sxs-lookup"><span data-stu-id="70bd2-508"><span id="D3DRS_COLORWRITEENABLE1"></span><span id="d3drs_colorwriteenable1"></span>**D3DRS\_COLORWRITEENABLE1**</span></span>
</dt> <dd>

<span data-ttu-id="70bd2-509">Zusätzliche ColorWriteEnable-Werte für die Geräte.</span><span class="sxs-lookup"><span data-stu-id="70bd2-509">Additional ColorWriteEnable values for the devices.</span></span> <span data-ttu-id="70bd2-510">Siehe D3DRS \_ COLORWRITEENABLE.</span><span class="sxs-lookup"><span data-stu-id="70bd2-510">See D3DRS\_COLORWRITEENABLE.</span></span> <span data-ttu-id="70bd2-511">Diese Funktionalität ist verfügbar, wenn das D3DPMISCCAPS \_ INDEPENDENTWRITEMASKS-Funktionsbit im PrimitiveMiscCaps-Member der [**D3DCAPS9-Struktur**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) für das Gerät festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="70bd2-511">This functionality is available if the D3DPMISCCAPS\_INDEPENDENTWRITEMASKS capabilities bit is set in the PrimitiveMiscCaps member of the [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure for the device.</span></span> <span data-ttu-id="70bd2-512">Der Standardwert ist 0x0000000f.</span><span class="sxs-lookup"><span data-stu-id="70bd2-512">The default value is 0x0000000f.</span></span>

</dd> <dt>

<span data-ttu-id="70bd2-513"><span id="D3DRS_COLORWRITEENABLE2"></span><span id="d3drs_colorwriteenable2"></span>**D3DRS \_ COLORWRITEENABLE2**</span><span class="sxs-lookup"><span data-stu-id="70bd2-513"><span id="D3DRS_COLORWRITEENABLE2"></span><span id="d3drs_colorwriteenable2"></span>**D3DRS\_COLORWRITEENABLE2**</span></span>
</dt> <dd>

<span data-ttu-id="70bd2-514">Zusätzliche ColorWriteEnable-Werte für die Geräte.</span><span class="sxs-lookup"><span data-stu-id="70bd2-514">Additional ColorWriteEnable values for the devices.</span></span> <span data-ttu-id="70bd2-515">Siehe D3DRS \_ COLORWRITEENABLE.</span><span class="sxs-lookup"><span data-stu-id="70bd2-515">See D3DRS\_COLORWRITEENABLE.</span></span> <span data-ttu-id="70bd2-516">Diese Funktionalität ist verfügbar, wenn das D3DPMISCCAPS \_ INDEPENDENTWRITEMASKS-Funktionsbit im PrimitiveMiscCaps-Member der [**D3DCAPS9-Struktur**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) für das Gerät festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="70bd2-516">This functionality is available if the D3DPMISCCAPS\_INDEPENDENTWRITEMASKS capabilities bit is set in the PrimitiveMiscCaps member of the [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure for the device.</span></span> <span data-ttu-id="70bd2-517">Der Standardwert ist 0x0000000f.</span><span class="sxs-lookup"><span data-stu-id="70bd2-517">The default value is 0x0000000f.</span></span>

</dd> <dt>

<span data-ttu-id="70bd2-518"><span id="D3DRS_COLORWRITEENABLE3"></span><span id="d3drs_colorwriteenable3"></span>**D3DRS \_ COLORWRITEENABLE3**</span><span class="sxs-lookup"><span data-stu-id="70bd2-518"><span id="D3DRS_COLORWRITEENABLE3"></span><span id="d3drs_colorwriteenable3"></span>**D3DRS\_COLORWRITEENABLE3**</span></span>
</dt> <dd>

<span data-ttu-id="70bd2-519">Zusätzliche ColorWriteEnable-Werte für die Geräte.</span><span class="sxs-lookup"><span data-stu-id="70bd2-519">Additional ColorWriteEnable values for the devices.</span></span> <span data-ttu-id="70bd2-520">Siehe D3DRS \_ COLORWRITEENABLE.</span><span class="sxs-lookup"><span data-stu-id="70bd2-520">See D3DRS\_COLORWRITEENABLE.</span></span> <span data-ttu-id="70bd2-521">Diese Funktionalität ist verfügbar, wenn das D3DPMISCCAPS \_ INDEPENDENTWRITEMASKS-Funktionsbit im PrimitiveMiscCaps-Member der [**D3DCAPS9-Struktur**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) für das Gerät festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="70bd2-521">This functionality is available if the D3DPMISCCAPS\_INDEPENDENTWRITEMASKS capabilities bit is set in the PrimitiveMiscCaps member of the [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure for the device.</span></span> <span data-ttu-id="70bd2-522">Der Standardwert ist 0x0000000f.</span><span class="sxs-lookup"><span data-stu-id="70bd2-522">The default value is 0x0000000f.</span></span>

</dd> <dt>

<span data-ttu-id="70bd2-523"><span id="D3DRS_BLENDFACTOR"></span><span id="d3drs_blendfactor"></span>**D3DRS \_ BLENDFACTOR**</span><span class="sxs-lookup"><span data-stu-id="70bd2-523"><span id="D3DRS_BLENDFACTOR"></span><span id="d3drs_blendfactor"></span>**D3DRS\_BLENDFACTOR**</span></span>
</dt> <dd>

<span data-ttu-id="70bd2-524">[**D3DCOLOR**](d3dcolor.md) wird für einen konstanten Mischungsfaktor während der Alphamischung verwendet.</span><span class="sxs-lookup"><span data-stu-id="70bd2-524">[**D3DCOLOR**](d3dcolor.md) used for a constant blend-factor during alpha blending.</span></span> <span data-ttu-id="70bd2-525">Diese Funktionalität ist verfügbar, wenn das D3DPBLENDCAPS \_ BLENDFACTOR-Funktionsbit im SrcBlendCaps-Member von [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) oder im DestBlendCaps-Member von **D3DCAPS9** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="70bd2-525">This functionality is available if the D3DPBLENDCAPS\_BLENDFACTOR capabilities bit is set in the SrcBlendCaps member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) or the DestBlendCaps member of **D3DCAPS9**.</span></span> <span data-ttu-id="70bd2-526">Siehe [**D3DRENDERSTATETYPE.**]()</span><span class="sxs-lookup"><span data-stu-id="70bd2-526">See [**D3DRENDERSTATETYPE**]().</span></span> <span data-ttu-id="70bd2-527">Der Standardwert ist 0xffffffff.</span><span class="sxs-lookup"><span data-stu-id="70bd2-527">The default value is 0xffffffff.</span></span>

</dd> <dt>

<span data-ttu-id="70bd2-528"><span id="D3DRS_SRGBWRITEENABLE"></span><span id="d3drs_srgbwriteenable"></span>**D3DRS \_ SRGBWRITEENABLE**</span><span class="sxs-lookup"><span data-stu-id="70bd2-528"><span id="D3DRS_SRGBWRITEENABLE"></span><span id="d3drs_srgbwriteenable"></span>**D3DRS\_SRGBWRITEENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="70bd2-529">Aktivieren Sie render-target-Schreibvorgänge, damit gamma in sRGB korrigiert wird.</span><span class="sxs-lookup"><span data-stu-id="70bd2-529">Enable render-target writes to be gamma corrected to sRGB.</span></span> <span data-ttu-id="70bd2-530">Das Format muss D3DUSAGE \_ SRGBWRITE verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="70bd2-530">The format must expose D3DUSAGE\_SRGBWRITE.</span></span> <span data-ttu-id="70bd2-531">Der Standardwert ist 0.</span><span class="sxs-lookup"><span data-stu-id="70bd2-531">The default value is 0.</span></span>

</dd> <dt>

<span data-ttu-id="70bd2-532"><span id="D3DRS_DEPTHBIAS"></span><span id="d3drs_depthbias"></span>**D3DRS \_ DEPTHBIAS**</span><span class="sxs-lookup"><span data-stu-id="70bd2-532"><span id="D3DRS_DEPTHBIAS"></span><span id="d3drs_depthbias"></span>**D3DRS\_DEPTHBIAS**</span></span>
</dt> <dd>

<span data-ttu-id="70bd2-533">Ein Gleitkommawert, der für den Vergleich von Tiefenwerten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="70bd2-533">A floating-point value that is used for comparison of depth values.</span></span> <span data-ttu-id="70bd2-534">Weitere Informationen finden Sie unter [Tiefenabweichung (Direct3D 9).](depth-bias.md)</span><span class="sxs-lookup"><span data-stu-id="70bd2-534">See [Depth Bias (Direct3D 9)](depth-bias.md).</span></span> <span data-ttu-id="70bd2-535">Der Standardwert ist 0.</span><span class="sxs-lookup"><span data-stu-id="70bd2-535">The default value is 0.</span></span>

</dd> <dt>

<span data-ttu-id="70bd2-536"><span id="D3DRS_WRAP8"></span><span id="d3drs_wrap8"></span>**D3DRS \_ WRAP8**</span><span class="sxs-lookup"><span data-stu-id="70bd2-536"><span id="D3DRS_WRAP8"></span><span id="d3drs_wrap8"></span>**D3DRS\_WRAP8**</span></span>
</dt> <dd>

<span data-ttu-id="70bd2-537">Siehe D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="70bd2-537">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="70bd2-538"><span id="D3DRS_WRAP9"></span><span id="d3drs_wrap9"></span>**D3DRS \_ WRAP9**</span><span class="sxs-lookup"><span data-stu-id="70bd2-538"><span id="D3DRS_WRAP9"></span><span id="d3drs_wrap9"></span>**D3DRS\_WRAP9**</span></span>
</dt> <dd>

<span data-ttu-id="70bd2-539">Siehe D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="70bd2-539">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="70bd2-540"><span id="D3DRS_WRAP10"></span><span id="d3drs_wrap10"></span>**D3DRS \_ WRAP10**</span><span class="sxs-lookup"><span data-stu-id="70bd2-540"><span id="D3DRS_WRAP10"></span><span id="d3drs_wrap10"></span>**D3DRS\_WRAP10**</span></span>
</dt> <dd>

<span data-ttu-id="70bd2-541">Siehe D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="70bd2-541">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="70bd2-542"><span id="D3DRS_WRAP11"></span><span id="d3drs_wrap11"></span>**D3DRS \_ WRAP11**</span><span class="sxs-lookup"><span data-stu-id="70bd2-542"><span id="D3DRS_WRAP11"></span><span id="d3drs_wrap11"></span>**D3DRS\_WRAP11**</span></span>
</dt> <dd>

<span data-ttu-id="70bd2-543">Siehe D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="70bd2-543">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="70bd2-544"><span id="D3DRS_WRAP12"></span><span id="d3drs_wrap12"></span>**D3DRS \_ WRAP12**</span><span class="sxs-lookup"><span data-stu-id="70bd2-544"><span id="D3DRS_WRAP12"></span><span id="d3drs_wrap12"></span>**D3DRS\_WRAP12**</span></span>
</dt> <dd>

<span data-ttu-id="70bd2-545">Siehe D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="70bd2-545">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="70bd2-546"><span id="D3DRS_WRAP13"></span><span id="d3drs_wrap13"></span>**D3DRS \_ WRAP13**</span><span class="sxs-lookup"><span data-stu-id="70bd2-546"><span id="D3DRS_WRAP13"></span><span id="d3drs_wrap13"></span>**D3DRS\_WRAP13**</span></span>
</dt> <dd>

<span data-ttu-id="70bd2-547">Siehe D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="70bd2-547">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="70bd2-548"><span id="D3DRS_WRAP14"></span><span id="d3drs_wrap14"></span>**D3DRS \_ WRAP14**</span><span class="sxs-lookup"><span data-stu-id="70bd2-548"><span id="D3DRS_WRAP14"></span><span id="d3drs_wrap14"></span>**D3DRS\_WRAP14**</span></span>
</dt> <dd>

<span data-ttu-id="70bd2-549">Siehe D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="70bd2-549">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="70bd2-550"><span id="D3DRS_WRAP15"></span><span id="d3drs_wrap15"></span>**D3DRS \_ WRAP15**</span><span class="sxs-lookup"><span data-stu-id="70bd2-550"><span id="D3DRS_WRAP15"></span><span id="d3drs_wrap15"></span>**D3DRS\_WRAP15**</span></span>
</dt> <dd>

<span data-ttu-id="70bd2-551">Siehe D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="70bd2-551">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="70bd2-552"><span id="D3DRS_SEPARATEALPHABLENDENABLE"></span><span id="d3drs_separatealphablendenable"></span>**D3DRS \_ SEPARATEALPHABLENDENABLE**</span><span class="sxs-lookup"><span data-stu-id="70bd2-552"><span id="D3DRS_SEPARATEALPHABLENDENABLE"></span><span id="d3drs_separatealphablendenable"></span>**D3DRS\_SEPARATEALPHABLENDENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="70bd2-553">**TRUE** aktiviert den separaten Überblendmodus für den Alphakanal.</span><span class="sxs-lookup"><span data-stu-id="70bd2-553">**TRUE** enables the separate blend mode for the alpha channel.</span></span> <span data-ttu-id="70bd2-554">Der Standardwert ist **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="70bd2-554">The default value is **FALSE**.</span></span>

<span data-ttu-id="70bd2-555">Wenn false festgelegt **ist,** müssen die auf alpha angewendeten Renderzielblendingfaktoren und -vorgänge mit denen identisch sein, die für die Farbe definiert sind.</span><span class="sxs-lookup"><span data-stu-id="70bd2-555">When set to **FALSE**, the render-target blending factors and operations applied to alpha are forced to be the same as those defined for color.</span></span> <span data-ttu-id="70bd2-556">Dieser Modus wird bei  Implementierungen, die die Obergrenze D3DPMISCCAPS SEPARATEALPHABLEND nicht festlegen, effektiv auf \_ FALSE festgelegt.</span><span class="sxs-lookup"><span data-stu-id="70bd2-556">This mode is effectively hardwired to **FALSE** on implementations that don't set the cap D3DPMISCCAPS\_SEPARATEALPHABLEND.</span></span> <span data-ttu-id="70bd2-557">Siehe [D3DPMISCCAPS](d3dpmisccaps.md).</span><span class="sxs-lookup"><span data-stu-id="70bd2-557">See [D3DPMISCCAPS](d3dpmisccaps.md).</span></span>

<span data-ttu-id="70bd2-558">Der Typ des separaten Alphablendings wird durch die Renderzustände D3DRS \_ SRCBLENDALPHA und D3DRS \_ DESTBLENDALPHA bestimmt.</span><span class="sxs-lookup"><span data-stu-id="70bd2-558">The type of separate alpha blending is determined by the D3DRS\_SRCBLENDALPHA and D3DRS\_DESTBLENDALPHA render states.</span></span>

</dd> <dt>

<span data-ttu-id="70bd2-559"><span id="D3DRS_SRCBLENDALPHA"></span><span id="d3drs_srcblendalpha"></span>**D3DRS \_ SRCBLENDALPHA**</span><span class="sxs-lookup"><span data-stu-id="70bd2-559"><span id="D3DRS_SRCBLENDALPHA"></span><span id="d3drs_srcblendalpha"></span>**D3DRS\_SRCBLENDALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="70bd2-560">Ein Member des [**aufzählten D3DBLEND-Typs.**](./d3dblend.md)</span><span class="sxs-lookup"><span data-stu-id="70bd2-560">One member of the [**D3DBLEND**](./d3dblend.md) enumerated type.</span></span> <span data-ttu-id="70bd2-561">Dieser Wert wird ignoriert, es sei denn, D3DRS \_ SEPARATEALPHABLENDENABLE ist **TRUE.**</span><span class="sxs-lookup"><span data-stu-id="70bd2-561">This value is ignored unless D3DRS\_SEPARATEALPHABLENDENABLE is **TRUE**.</span></span> <span data-ttu-id="70bd2-562">Der Standardwert ist D3DBLEND \_ ONE.</span><span class="sxs-lookup"><span data-stu-id="70bd2-562">The default value is D3DBLEND\_ONE.</span></span>

</dd> <dt>

<span data-ttu-id="70bd2-563"><span id="D3DRS_DESTBLENDALPHA"></span><span id="d3drs_destblendalpha"></span>**D3DRS \_ DESTBLENDALPHA**</span><span class="sxs-lookup"><span data-stu-id="70bd2-563"><span id="D3DRS_DESTBLENDALPHA"></span><span id="d3drs_destblendalpha"></span>**D3DRS\_DESTBLENDALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="70bd2-564">Ein Member des [**aufzählten D3DBLEND-Typs.**](./d3dblend.md)</span><span class="sxs-lookup"><span data-stu-id="70bd2-564">One member of the [**D3DBLEND**](./d3dblend.md) enumerated type.</span></span> <span data-ttu-id="70bd2-565">Dieser Wert wird ignoriert, es sei denn, D3DRS \_ SEPARATEALPHABLENDENABLE ist **TRUE.**</span><span class="sxs-lookup"><span data-stu-id="70bd2-565">This value is ignored unless D3DRS\_SEPARATEALPHABLENDENABLE is **TRUE**.</span></span> <span data-ttu-id="70bd2-566">Der Standardwert ist D3DBLEND \_ ZERO.</span><span class="sxs-lookup"><span data-stu-id="70bd2-566">The default value is D3DBLEND\_ZERO.</span></span>

</dd> <dt>

<span data-ttu-id="70bd2-567"><span id="D3DRS_BLENDOPALPHA"></span><span id="d3drs_blendopalpha"></span>**D3DRS \_ BLENDOPALPHA**</span><span class="sxs-lookup"><span data-stu-id="70bd2-567"><span id="D3DRS_BLENDOPALPHA"></span><span id="d3drs_blendopalpha"></span>**D3DRS\_BLENDOPALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="70bd2-568">Der Wert, der verwendet wird, um die arithmetische Operation auszuwählen, die auf separate Alphamischung angewendet wird, wenn der Renderzustand D3DRS \_ SEPARATEALPHABLENDENABLE auf **TRUE** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="70bd2-568">Value used to select the arithmetic operation applied to separate alpha blending when the render state, D3DRS\_SEPARATEALPHABLENDENABLE, is set to **TRUE**.</span></span>

<span data-ttu-id="70bd2-569">Gültige Werte werden vom [**D3DBLENDOP-Enumerationstyp**](./d3dblendop.md) definiert.</span><span class="sxs-lookup"><span data-stu-id="70bd2-569">Valid values are defined by the [**D3DBLENDOP**](./d3dblendop.md) enumerated type.</span></span> <span data-ttu-id="70bd2-570">Der Standardwert ist D3DBLENDOP \_ ADD.</span><span class="sxs-lookup"><span data-stu-id="70bd2-570">The default value is D3DBLENDOP\_ADD.</span></span>

<span data-ttu-id="70bd2-571">Wenn die D3DPMISCCAPS \_ BLENDOP-Gerätefunktion nicht unterstützt wird, wird D3DBLENDOP \_ ADD ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="70bd2-571">If the D3DPMISCCAPS\_BLENDOP device capability is not supported, then D3DBLENDOP\_ADD is performed.</span></span> <span data-ttu-id="70bd2-572">Siehe [D3DPMISCCAPS](d3dpmisccaps.md).</span><span class="sxs-lookup"><span data-stu-id="70bd2-572">See [D3DPMISCCAPS](d3dpmisccaps.md).</span></span>

</dd> <dt>

<span data-ttu-id="70bd2-573"><span id="D3DRS_FORCE_DWORD"></span><span id="d3drs_force_dword"></span>**D3DRS \_ FORCE \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="70bd2-573"><span id="D3DRS_FORCE_DWORD"></span><span id="d3drs_force_dword"></span>**D3DRS\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="70bd2-574">Erzwingt, dass diese Enumeration in eine Größe von 32 Bits kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="70bd2-574">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="70bd2-575">Ohne diesen Wert würden einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="70bd2-575">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="70bd2-576">Dieser Wert wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="70bd2-576">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="70bd2-577">Hinweise</span><span class="sxs-lookup"><span data-stu-id="70bd2-577">Remarks</span></span>



| <span data-ttu-id="70bd2-578">Renderzustände</span><span class="sxs-lookup"><span data-stu-id="70bd2-578">Render states</span></span>        |   <span data-ttu-id="70bd2-579">Textur-Sampler</span><span class="sxs-lookup"><span data-stu-id="70bd2-579">Texture sampler</span></span>                 |
|----------------------|--------------------|
| <span data-ttu-id="70bd2-580">ps \_ 1 \_ 1 bis ps \_ 1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="70bd2-580">ps\_1\_1 to ps\_1\_3</span></span> | <span data-ttu-id="70bd2-581">4 Textur-Sampler</span><span class="sxs-lookup"><span data-stu-id="70bd2-581">4 texture samplers</span></span> |



 

<span data-ttu-id="70bd2-582">Direct3D definiert die D3DRENDERSTATE \_ WRAPBIAS-Konstante, um Anwendungen das Aktivieren oder Deaktivieren des Texturumbruchs basierend auf der nullbasierten ganzen Zahl eines Texturkoordinatensatzes zu ermöglichen (anstatt explizit einen der D3DRS \_ WRAP n-Zustandswerte zu verwenden).</span><span class="sxs-lookup"><span data-stu-id="70bd2-582">Direct3D defines the D3DRENDERSTATE\_WRAPBIAS constant as a convenience for applications to enable or disable texture wrapping, based on the zero-based integer of a texture coordinate set (rather than explicitly using one of the D3DRS\_WRAP n state values).</span></span> <span data-ttu-id="70bd2-583">Fügen Sie den D3DRENDERSTATE \_ WRAPBIAS-Wert dem nullbasierten Index eines Texturkoordinatensatzes hinzu, um den D3DRS \_ WRAP n-Wert zu berechnen, der diesem Index entspricht, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="70bd2-583">Add the D3DRENDERSTATE\_WRAPBIAS value to the zero-based index of a texture coordinate set to calculate the D3DRS\_WRAP n value that corresponds to that index, as shown in the following example.</span></span>


```
// Enable U/V wrapping for textures that use the texture 
// coordinate set at the index within the dwIndex variable
    
HRESULT hr = pd3dDevice->SetRenderState(
dwIndex + D3DRENDERSTATE_WRAPBIAS,  
D3DWRAPCOORD_0 | D3DWRAPCOORD_1);
     
// If dwIndex is 3, the value that results from 
// the addition equals D3DRS_WRAP3 (131)
```



## <a name="requirements"></a><span data-ttu-id="70bd2-584">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="70bd2-584">Requirements</span></span>



| <span data-ttu-id="70bd2-585">Anforderung</span><span class="sxs-lookup"><span data-stu-id="70bd2-585">Requirement</span></span> | <span data-ttu-id="70bd2-586">Wert</span><span class="sxs-lookup"><span data-stu-id="70bd2-586">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="70bd2-587">Header</span><span class="sxs-lookup"><span data-stu-id="70bd2-587">Header</span></span><br/> | <dl> <span data-ttu-id="70bd2-588"><dt>D3D9Types.h</dt></span><span class="sxs-lookup"><span data-stu-id="70bd2-588"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70bd2-589">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="70bd2-589">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70bd2-590">Direct3D-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="70bd2-590">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="70bd2-591">**IDirect3DDevice9::GetRenderState**</span><span class="sxs-lookup"><span data-stu-id="70bd2-591">**IDirect3DDevice9::GetRenderState**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getrenderstate)
</dt> <dt>

[<span data-ttu-id="70bd2-592">**IDirect3DDevice9::SetRenderState**</span><span class="sxs-lookup"><span data-stu-id="70bd2-592">**IDirect3DDevice9::SetRenderState**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate)
</dt> </dl>

 

 
