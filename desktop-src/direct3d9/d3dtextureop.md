---
description: Definiert einstufige Textur Mischungs Vorgänge.
ms.assetid: 7bfdcb15-c3c3-4e7e-b924-6ecfa350e2f3
title: D3DTEXTUREOP-Enumeration (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTEXTUREOP
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: d35e2d4b65cd41a49d8ed8edb3252295ca3baef3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354516"
---
# <a name="d3dtextureop-enumeration"></a><span data-ttu-id="0447c-103">D3DTEXTUREOP-Enumeration</span><span class="sxs-lookup"><span data-stu-id="0447c-103">D3DTEXTUREOP enumeration</span></span>

<span data-ttu-id="0447c-104">Definiert einstufige Textur Mischungs Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="0447c-104">Defines per-stage texture-blending operations.</span></span>

## <a name="syntax"></a><span data-ttu-id="0447c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0447c-105">Syntax</span></span>


```C++
typedef enum D3DTEXTUREOP { 
  D3DTOP_DISABLE                    = 1,
  D3DTOP_SELECTARG1                 = 2,
  D3DTOP_SELECTARG2                 = 3,
  D3DTOP_MODULATE                   = 4,
  D3DTOP_MODULATE2X                 = 5,
  D3DTOP_MODULATE4X                 = 6,
  D3DTOP_ADD                        = 7,
  D3DTOP_ADDSIGNED                  = 8,
  D3DTOP_ADDSIGNED2X                = 9,
  D3DTOP_SUBTRACT                   = 10,
  D3DTOP_ADDSMOOTH                  = 11,
  D3DTOP_BLENDDIFFUSEALPHA          = 12,
  D3DTOP_BLENDTEXTUREALPHA          = 13,
  D3DTOP_BLENDFACTORALPHA           = 14,
  D3DTOP_BLENDTEXTUREALPHAPM        = 15,
  D3DTOP_BLENDCURRENTALPHA          = 16,
  D3DTOP_PREMODULATE                = 17,
  D3DTOP_MODULATEALPHA_ADDCOLOR     = 18,
  D3DTOP_MODULATECOLOR_ADDALPHA     = 19,
  D3DTOP_MODULATEINVALPHA_ADDCOLOR  = 20,
  D3DTOP_MODULATEINVCOLOR_ADDALPHA  = 21,
  D3DTOP_BUMPENVMAP                 = 22,
  D3DTOP_BUMPENVMAPLUMINANCE        = 23,
  D3DTOP_DOTPRODUCT3                = 24,
  D3DTOP_MULTIPLYADD                = 25,
  D3DTOP_LERP                       = 26,
  D3DTOP_FORCE_DWORD                = 0x7fffffff
} D3DTEXTUREOP, *LPD3DTEXTUREOP;
```



## <a name="constants"></a><span data-ttu-id="0447c-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="0447c-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="0447c-107"><span id="D3DTOP_DISABLE"></span><span id="d3dtop_disable"></span>**D3DTOP \_ Deaktivieren**</span><span class="sxs-lookup"><span data-stu-id="0447c-107"><span id="D3DTOP_DISABLE"></span><span id="d3dtop_disable"></span>**D3DTOP\_DISABLE**</span></span>
</dt> <dd>

<span data-ttu-id="0447c-108">Deaktiviert die Ausgabe dieser Textur Phase und aller Stufen mit einem höheren Index.</span><span class="sxs-lookup"><span data-stu-id="0447c-108">Disables output from this texture stage and all stages with a higher index.</span></span> <span data-ttu-id="0447c-109">Um die Textur Zuordnung zu deaktivieren, legen Sie diese als Farb Vorgang für die erste Textur Phase fest (Phase 0).</span><span class="sxs-lookup"><span data-stu-id="0447c-109">To disable texture mapping, set this as the color operation for the first texture stage (stage 0).</span></span> <span data-ttu-id="0447c-110">Alpha Vorgänge können nicht deaktiviert werden, wenn Farb Vorgänge aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="0447c-110">Alpha operations cannot be disabled when color operations are enabled.</span></span> <span data-ttu-id="0447c-111">Das Festlegen des Alpha-Vorgangs auf D3DTOP \_ deaktivieren, wenn die Farbmischung aktiviert ist, verursacht ein nicht definiertes Verhalten</span><span class="sxs-lookup"><span data-stu-id="0447c-111">Setting the alpha operation to D3DTOP\_DISABLE when color blending is enabled causes undefined behavior.</span></span>

</dd> <dt>

<span data-ttu-id="0447c-112"><span id="D3DTOP_SELECTARG1"></span><span id="d3dtop_selectarg1"></span>**D3DTOP \_ SELECTARG1**</span><span class="sxs-lookup"><span data-stu-id="0447c-112"><span id="D3DTOP_SELECTARG1"></span><span id="d3dtop_selectarg1"></span>**D3DTOP\_SELECTARG1**</span></span>
</dt> <dd>

<span data-ttu-id="0447c-113">Verwenden Sie die erste Farbe oder das Alpha Argument der Textur Phase, unverändert als Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="0447c-113">Use this texture stage's first color or alpha argument, unmodified, as the output.</span></span> <span data-ttu-id="0447c-114">Dieser Vorgang wirkt sich auf das Color-Argument aus, wenn es mit dem D3DTSS \_ colorop-Textur Stufen Zustand verwendet wird, und das Alpha-Argument bei Verwendung mit D3DTSS \_ alphaop.</span><span class="sxs-lookup"><span data-stu-id="0447c-114">This operation affects the color argument when used with the D3DTSS\_COLOROP texture-stage state, and the alpha argument when used with D3DTSS\_ALPHAOP.</span></span>

![Gleichung dieses Arguments (s (RGBA) = arg1)](images/topfrm1.png)

</dd> <dt>

<span data-ttu-id="0447c-116"><span id="D3DTOP_SELECTARG2"></span><span id="d3dtop_selectarg2"></span>**D3DTOP \_ SELECTARG2**</span><span class="sxs-lookup"><span data-stu-id="0447c-116"><span id="D3DTOP_SELECTARG2"></span><span id="d3dtop_selectarg2"></span>**D3DTOP\_SELECTARG2**</span></span>
</dt> <dd>

<span data-ttu-id="0447c-117">Verwenden Sie die zweite Farbe oder das Alpha Argument der Textur Phase unverändert als Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="0447c-117">Use this texture stage's second color or alpha argument, unmodified, as the output.</span></span> <span data-ttu-id="0447c-118">Dieser Vorgang wirkt sich auf das Color-Argument aus, wenn es mit dem D3DTSS \_ colorop-Textur Stufen Zustand verwendet wird, und das Alpha-Argument bei der Verwendung mit D3DTSS \_ alphaop.</span><span class="sxs-lookup"><span data-stu-id="0447c-118">This operation affects the color argument when used with the D3DTSS\_COLOROP texture stage state, and the alpha argument when used with D3DTSS\_ALPHAOP.</span></span>

![Gleichung dieses Arguments (s (RGBA) = arg2)](images/topfrm2.png)

</dd> <dt>

<span data-ttu-id="0447c-120"><span id="D3DTOP_MODULATE"></span><span id="d3dtop_modulate"></span>**D3DTOP \_ modulate**</span><span class="sxs-lookup"><span data-stu-id="0447c-120"><span id="D3DTOP_MODULATE"></span><span id="d3dtop_modulate"></span>**D3DTOP\_MODULATE**</span></span>
</dt> <dd>

<span data-ttu-id="0447c-121">Multiplizieren Sie die Komponenten der Argumente.</span><span class="sxs-lookup"><span data-stu-id="0447c-121">Multiply the components of the arguments.</span></span>

![Gleichung der modulieren-Operation (s (RGBA) = arg1 x Arg 2)](images/topfrm3.png)

</dd> <dt>

<span data-ttu-id="0447c-123"><span id="D3DTOP_MODULATE2X"></span><span id="d3dtop_modulate2x"></span>**D3DTOP \_ MODULATE2X**</span><span class="sxs-lookup"><span data-stu-id="0447c-123"><span id="D3DTOP_MODULATE2X"></span><span id="d3dtop_modulate2x"></span>**D3DTOP\_MODULATE2X**</span></span>
</dt> <dd>

<span data-ttu-id="0447c-124">Multiplizieren Sie die Komponenten der Argumente, und verschieben Sie die Produkte auf das linke 1 Bit (wodurch Sie effektiv um 2 multipliziert werden), um die Beleuchtung zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="0447c-124">Multiply the components of the arguments, and shift the products to the left 1 bit (effectively multiplying them by 2) for brightening.</span></span>

![Gleichung der Modulate2X Operation (s (RGBA) = (arg1 x Arg 2), dann Shift Left 1)](images/topfrm4.png)

</dd> <dt>

<span data-ttu-id="0447c-126"><span id="D3DTOP_MODULATE4X"></span><span id="d3dtop_modulate4x"></span>**D3DTOP \_ MODULATE4X**</span><span class="sxs-lookup"><span data-stu-id="0447c-126"><span id="D3DTOP_MODULATE4X"></span><span id="d3dtop_modulate4x"></span>**D3DTOP\_MODULATE4X**</span></span>
</dt> <dd>

<span data-ttu-id="0447c-127">Multiplizieren Sie die Komponenten der Argumente, und verschieben Sie die Produkte auf die linken 2 Bits (wodurch Sie durch 4 multipliziert werden), um die Beleuchtung zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="0447c-127">Multiply the components of the arguments, and shift the products to the left 2 bits (effectively multiplying them by 4) for brightening.</span></span>

![Gleichung der Modulate4X Operation (s (RGBA) = (arg1 x Arg 2), UMSCHALT Left 2)](images/topfrm5.png)

</dd> <dt>

<span data-ttu-id="0447c-129"><span id="D3DTOP_ADD"></span><span id="d3dtop_add"></span>**D3DTOP \_ Hinzufügen**</span><span class="sxs-lookup"><span data-stu-id="0447c-129"><span id="D3DTOP_ADD"></span><span id="d3dtop_add"></span>**D3DTOP\_ADD**</span></span>
</dt> <dd>

<span data-ttu-id="0447c-130">Fügen Sie die Komponenten der Argumente hinzu.</span><span class="sxs-lookup"><span data-stu-id="0447c-130">Add the components of the arguments.</span></span>

![Gleichung des Add-Vorgangs (s (RGBA) = arg1 + Arg 2)](images/topfrm6.png)

</dd> <dt>

<span data-ttu-id="0447c-132"><span id="D3DTOP_ADDSIGNED"></span><span id="d3dtop_addsigned"></span>**D3DTOP \_ AddSigned**</span><span class="sxs-lookup"><span data-stu-id="0447c-132"><span id="D3DTOP_ADDSIGNED"></span><span id="d3dtop_addsigned"></span>**D3DTOP\_ADDSIGNED**</span></span>
</dt> <dd>

<span data-ttu-id="0447c-133">Fügen Sie die Komponenten der Argumente mit einem-0,5-Bias hinzu, und legen Sie den effektiven Wertebereich von-0,5 bis 0,5.</span><span class="sxs-lookup"><span data-stu-id="0447c-133">Add the components of the arguments with a - 0.5 bias, making the effective range of values from - 0.5 through 0.5.</span></span>

![Gleichung der hinzu zufügenden signierten Operation (s (RGBA) = arg1 + Arg 2 – 0,5)](images/topfrm7.png)

</dd> <dt>

<span data-ttu-id="0447c-135"><span id="D3DTOP_ADDSIGNED2X"></span><span id="d3dtop_addsigned2x"></span>**D3DTOP \_ ADDSIGNED2X**</span><span class="sxs-lookup"><span data-stu-id="0447c-135"><span id="D3DTOP_ADDSIGNED2X"></span><span id="d3dtop_addsigned2x"></span>**D3DTOP\_ADDSIGNED2X**</span></span>
</dt> <dd>

<span data-ttu-id="0447c-136">Fügen Sie die Komponenten der Argumente mit einem-0,5-Bias hinzu, und verschieben Sie die Produkte auf das linke 1-Bit.</span><span class="sxs-lookup"><span data-stu-id="0447c-136">Add the components of the arguments with a - 0.5 bias, and shift the products to the left 1 bit.</span></span>

![Gleichung des hinzu fügenden 2X-Vorgangs ((s (RGBA) = arg1 + Arg 2-0,5) und nach links 1)](images/topfrm8.png)

</dd> <dt>

<span data-ttu-id="0447c-138"><span id="D3DTOP_SUBTRACT"></span><span id="d3dtop_subtract"></span>**D3DTOP \_ subtrahieren**</span><span class="sxs-lookup"><span data-stu-id="0447c-138"><span id="D3DTOP_SUBTRACT"></span><span id="d3dtop_subtract"></span>**D3DTOP\_SUBTRACT**</span></span>
</dt> <dd>

<span data-ttu-id="0447c-139">Subtrahieren Sie die Komponenten des zweiten Arguments von denen des ersten Arguments.</span><span class="sxs-lookup"><span data-stu-id="0447c-139">Subtract the components of the second argument from those of the first argument.</span></span>

![Gleichung des subtrahieren-Vorgangs (s (RGBA) = arg1-Arg 2)](images/topfrm9.png)

</dd> <dt>

<span data-ttu-id="0447c-141"><span id="D3DTOP_ADDSMOOTH"></span><span id="d3dtop_addsmooth"></span>**D3DTOP \_ AddSmooth**</span><span class="sxs-lookup"><span data-stu-id="0447c-141"><span id="D3DTOP_ADDSMOOTH"></span><span id="d3dtop_addsmooth"></span>**D3DTOP\_ADDSMOOTH**</span></span>
</dt> <dd>

<span data-ttu-id="0447c-142">Fügen Sie das erste und zweite Argument hinzu. subtrahieren Sie dann das Produkt von der Summe.</span><span class="sxs-lookup"><span data-stu-id="0447c-142">Add the first and second arguments; then subtract their product from the sum.</span></span>

![Gleichung des hinzu fügenden Smooth-Vorgangs (s (RGBA) = arg1 + Arg 2 x (1-arg1))](images/topfrm10.png)

</dd> <dt>

<span data-ttu-id="0447c-144"><span id="D3DTOP_BLENDDIFFUSEALPHA"></span><span id="d3dtop_blenddiffusealpha"></span>**D3DTOP \_ blenddiffusealpha**</span><span class="sxs-lookup"><span data-stu-id="0447c-144"><span id="D3DTOP_BLENDDIFFUSEALPHA"></span><span id="d3dtop_blenddiffusealpha"></span>**D3DTOP\_BLENDDIFFUSEALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="0447c-145">Linear Blend diese Textur Phase, wobei das interpoliert-Alpha aus jedem Scheitelpunkt verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0447c-145">Linearly blend this texture stage, using the interpolated alpha from each vertex.</span></span>

![Gleichung der Blend-diffuses Alpha Operation (s (RGBA) = arg1 x Alpha + Arg 2 x (1-Alpha))](images/topfrm11.png)

</dd> <dt>

<span data-ttu-id="0447c-147"><span id="D3DTOP_BLENDTEXTUREALPHA"></span><span id="d3dtop_blendtexturealpha"></span>**D3DTOP \_ blendtexturealpha**</span><span class="sxs-lookup"><span data-stu-id="0447c-147"><span id="D3DTOP_BLENDTEXTUREALPHA"></span><span id="d3dtop_blendtexturealpha"></span>**D3DTOP\_BLENDTEXTUREALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="0447c-148">Linear Blend diese Textur Phase, wobei das Alpha aus der Textur dieser Stufe verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0447c-148">Linearly blend this texture stage, using the alpha from this stage's texture.</span></span>

![Gleichung der Blend-Textur Alpha Operation (s (RGBA) = arg1 x Alpha + Arg 2 x (1-Alpha))](images/topfrm11.png)

</dd> <dt>

<span data-ttu-id="0447c-150"><span id="D3DTOP_BLENDFACTORALPHA"></span><span id="d3dtop_blendfactoralpha"></span>**D3DTOP \_ blendfactor Alpha**</span><span class="sxs-lookup"><span data-stu-id="0447c-150"><span id="D3DTOP_BLENDFACTORALPHA"></span><span id="d3dtop_blendfactoralpha"></span>**D3DTOP\_BLENDFACTORALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="0447c-151">Linear Blend diese Textur Phase, wobei eine skalare Alpha Gruppe mit dem D3DRS \_ TextureFactor-Rendering-Zustand verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0447c-151">Linearly blend this texture stage, using a scalar alpha set with the D3DRS\_TEXTUREFACTOR render state.</span></span>

![Gleichung der Blend Faktor Alpha Operation (s (RGBA) = arg1 x Alpha + Arg 2 x (1-Alpha))](images/topfrm11.png)

</dd> <dt>

<span data-ttu-id="0447c-153"><span id="D3DTOP_BLENDTEXTUREALPHAPM"></span><span id="d3dtop_blendtexturealphapm"></span>**D3DTOP \_ blendtexturealphapm**</span><span class="sxs-lookup"><span data-stu-id="0447c-153"><span id="D3DTOP_BLENDTEXTUREALPHAPM"></span><span id="d3dtop_blendtexturealphapm"></span>**D3DTOP\_BLENDTEXTUREALPHAPM**</span></span>
</dt> <dd>

<span data-ttu-id="0447c-154">Linear Blend eine Textur Phase, in der ein prämultipliziertes Alpha verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0447c-154">Linearly blend a texture stage that uses a premultiplied alpha.</span></span>

![Gleichung des Blend-Textur-Alpha-pm-Vorgangs (s (RGBA) = arg1 + Arg 2 x (1-Alpha))](images/topfrm12.png)

</dd> <dt>

<span data-ttu-id="0447c-156"><span id="D3DTOP_BLENDCURRENTALPHA"></span><span id="d3dtop_blendcurrentalpha"></span>**D3DTOP \_ blendcurrentalpha**</span><span class="sxs-lookup"><span data-stu-id="0447c-156"><span id="D3DTOP_BLENDCURRENTALPHA"></span><span id="d3dtop_blendcurrentalpha"></span>**D3DTOP\_BLENDCURRENTALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="0447c-157">Linear Blend diese Textur Phase mit dem Alpha aus der vorherigen Textur Phase.</span><span class="sxs-lookup"><span data-stu-id="0447c-157">Linearly blend this texture stage, using the alpha taken from the previous texture stage.</span></span>

![Gleichung der Blend-aktuellen Alpha Operation (s (RGBA) = arg1 x Alpha + arg2 x (1-Alpha))](images/topfrm11.png)

</dd> <dt>

<span data-ttu-id="0447c-159"><span id="D3DTOP_PREMODULATE"></span><span id="d3dtop_premodulate"></span>**D3DTOP \_ PreModulate**</span><span class="sxs-lookup"><span data-stu-id="0447c-159"><span id="D3DTOP_PREMODULATE"></span><span id="d3dtop_premodulate"></span>**D3DTOP\_PREMODULATE**</span></span>
</dt> <dd>

<span data-ttu-id="0447c-160">D3DTOP \_ PreModulate wird in Phase n festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0447c-160">D3DTOP\_PREMODULATE is set in stage n.</span></span> <span data-ttu-id="0447c-161">Die Ausgabe von Phase n ist arg1.</span><span class="sxs-lookup"><span data-stu-id="0447c-161">The output of stage n is arg1.</span></span> <span data-ttu-id="0447c-162">Wenn eine Textur in der Phase n + 1 vorhanden ist, werden alle D3DTA, die \_ in Phase n + 1 aktuell sind, in der Phase n + 1 mit der Textur aufgefüllt.</span><span class="sxs-lookup"><span data-stu-id="0447c-162">Additionally, if there is a texture in stage n + 1, any D3DTA\_CURRENT in stage n + 1 is premultiplied by texture in stage n + 1.</span></span>

</dd> <dt>

<span data-ttu-id="0447c-163"><span id="D3DTOP_MODULATEALPHA_ADDCOLOR"></span><span id="d3dtop_modulatealpha_addcolor"></span>**D3DTOP \_ modulatealpha \_ addcolor**</span><span class="sxs-lookup"><span data-stu-id="0447c-163"><span id="D3DTOP_MODULATEALPHA_ADDCOLOR"></span><span id="d3dtop_modulatealpha_addcolor"></span>**D3DTOP\_MODULATEALPHA\_ADDCOLOR**</span></span>
</dt> <dd>

<span data-ttu-id="0447c-164">Gibt die Farbe des zweiten Arguments mit dem Alpha des ersten Arguments an. Fügen Sie dann das Ergebnis zu Argument 1 hinzu.</span><span class="sxs-lookup"><span data-stu-id="0447c-164">Modulate the color of the second argument, using the alpha of the first argument; then add the result to argument one.</span></span> <span data-ttu-id="0447c-165">Dieser Vorgang wird nur für Farb Vorgänge (D3DTSS \_ colorop) unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0447c-165">This operation is supported only for color operations (D3DTSS\_COLOROP).</span></span>

![Gleichung des Vorgangs zum Hinzufügen von Color modulieren Alpha (s (RGBA) = arg1 (RGB) + arg1 (a) x arg2 (RGB))](images/topfrm13.png)

</dd> <dt>

<span data-ttu-id="0447c-167"><span id="D3DTOP_MODULATECOLOR_ADDALPHA"></span><span id="d3dtop_modulatecolor_addalpha"></span>**D3DTOP \_ modulatecolor \_ addalpha**</span><span class="sxs-lookup"><span data-stu-id="0447c-167"><span id="D3DTOP_MODULATECOLOR_ADDALPHA"></span><span id="d3dtop_modulatecolor_addalpha"></span>**D3DTOP\_MODULATECOLOR\_ADDALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="0447c-168">Modulate der Argumente. Fügen Sie dann das Alpha des ersten Arguments hinzu.</span><span class="sxs-lookup"><span data-stu-id="0447c-168">Modulate the arguments; then add the alpha of the first argument.</span></span> <span data-ttu-id="0447c-169">Dieser Vorgang wird nur für Farb Vorgänge (D3DTSS \_ colorop) unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0447c-169">This operation is supported only for color operations (D3DTSS\_COLOROP).</span></span>

![Gleichung des hinzu fügenden Alpha modulieren Color-Vorgangs (s (RGBA) = arg1 (RGB) x arg2 (RGB) + arg1 (a))](images/topfrm14.png)

</dd> <dt>

<span data-ttu-id="0447c-171"><span id="D3DTOP_MODULATEINVALPHA_ADDCOLOR"></span><span id="d3dtop_modulateinvalpha_addcolor"></span>**D3DTOP \_ modulateinvalpha \_ addcolor**</span><span class="sxs-lookup"><span data-stu-id="0447c-171"><span id="D3DTOP_MODULATEINVALPHA_ADDCOLOR"></span><span id="d3dtop_modulateinvalpha_addcolor"></span>**D3DTOP\_MODULATEINVALPHA\_ADDCOLOR**</span></span>
</dt> <dd>

<span data-ttu-id="0447c-172">Vergleichbar mit D3DTOP \_ modulatealpha \_ addcolor, aber mit der Umkehrung der Alpha des ersten Arguments.</span><span class="sxs-lookup"><span data-stu-id="0447c-172">Similar to D3DTOP\_MODULATEALPHA\_ADDCOLOR, but use the inverse of the alpha of the first argument.</span></span> <span data-ttu-id="0447c-173">Dieser Vorgang wird nur für Farb Vorgänge (D3DTSS \_ colorop) unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0447c-173">This operation is supported only for color operations (D3DTSS\_COLOROP).</span></span>

![Gleichung des Vorgangs zum Hinzufügen von farbmodulen mit umgekehrtem Alpha (s (RGBA) = (1-arg1 (a)) x arg2 (RGB) + arg1 (RGB))](images/topfrm15.png)

</dd> <dt>

<span data-ttu-id="0447c-175"><span id="D3DTOP_MODULATEINVCOLOR_ADDALPHA"></span><span id="d3dtop_modulateinvcolor_addalpha"></span>**D3DTOP \_ modulateinvcolor \_ addalpha**</span><span class="sxs-lookup"><span data-stu-id="0447c-175"><span id="D3DTOP_MODULATEINVCOLOR_ADDALPHA"></span><span id="d3dtop_modulateinvcolor_addalpha"></span>**D3DTOP\_MODULATEINVCOLOR\_ADDALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="0447c-176">Vergleichbar mit D3DTOP \_ modulatecolor \_ addalpha, aber verwenden Sie die Umkehrung der Farbe des ersten Arguments.</span><span class="sxs-lookup"><span data-stu-id="0447c-176">Similar to D3DTOP\_MODULATECOLOR\_ADDALPHA, but use the inverse of the color of the first argument.</span></span> <span data-ttu-id="0447c-177">Dieser Vorgang wird nur für Farb Vorgänge (D3DTSS \_ colorop) unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0447c-177">This operation is supported only for color operations (D3DTSS\_COLOROP).</span></span>

![Gleichung des hinzu fügenden Alpha modulieren-Farb Vorgangs (s (RGBA) = (1-arg1 (RGB)) x arg2 (RGB) + arg1 (a))](images/topfrm16.png)

</dd> <dt>

<span data-ttu-id="0447c-179"><span id="D3DTOP_BUMPENVMAP"></span><span id="d3dtop_bumpenvmap"></span>**D3DTOP \_ bumpenvmap**</span><span class="sxs-lookup"><span data-stu-id="0447c-179"><span id="D3DTOP_BUMPENVMAP"></span><span id="d3dtop_bumpenvmap"></span>**D3DTOP\_BUMPENVMAP**</span></span>
</dt> <dd>

<span data-ttu-id="0447c-180">Durchführen einer pro-Pixel-Bump-Zuordnung mithilfe der Umgebungs Zuordnung in der nächsten Textur Phase ohne Leuchtkraft.</span><span class="sxs-lookup"><span data-stu-id="0447c-180">Perform per-pixel bump mapping, using the environment map in the next texture stage, without luminance.</span></span> <span data-ttu-id="0447c-181">Dieser Vorgang wird nur für Farb Vorgänge (D3DTSS \_ colorop) unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0447c-181">This operation is supported only for color operations (D3DTSS\_COLOROP).</span></span>

</dd> <dt>

<span data-ttu-id="0447c-182"><span id="D3DTOP_BUMPENVMAPLUMINANCE"></span><span id="d3dtop_bumpenvmapluminance"></span>**D3DTOP \_ bumpumvmapluminance**</span><span class="sxs-lookup"><span data-stu-id="0447c-182"><span id="D3DTOP_BUMPENVMAPLUMINANCE"></span><span id="d3dtop_bumpenvmapluminance"></span>**D3DTOP\_BUMPENVMAPLUMINANCE**</span></span>
</dt> <dd>

<span data-ttu-id="0447c-183">Durchführen einer pro-Pixel-Bump-Zuordnung mithilfe der Umgebungs Zuordnung in der nächsten Textur Phase mit Leuchtkraft.</span><span class="sxs-lookup"><span data-stu-id="0447c-183">Perform per-pixel bump mapping, using the environment map in the next texture stage, with luminance.</span></span> <span data-ttu-id="0447c-184">Dieser Vorgang wird nur für Farb Vorgänge (D3DTSS \_ colorop) unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0447c-184">This operation is supported only for color operations (D3DTSS\_COLOROP).</span></span>

</dd> <dt>

<span data-ttu-id="0447c-185"><span id="D3DTOP_DOTPRODUCT3"></span><span id="d3dtop_dotproduct3"></span>**D3DTOP \_ DOTPRODUCT3**</span><span class="sxs-lookup"><span data-stu-id="0447c-185"><span id="D3DTOP_DOTPRODUCT3"></span><span id="d3dtop_dotproduct3"></span>**D3DTOP\_DOTPRODUCT3**</span></span>
</dt> <dd>

<span data-ttu-id="0447c-186">Modulieren Sie die Komponenten der einzelnen Argumente als signierte Komponenten, und fügen Sie Ihre Produkte hinzu. Replizieren Sie die Summe dann in alle Farbkanäle, einschließlich alpha.</span><span class="sxs-lookup"><span data-stu-id="0447c-186">Modulate the components of each argument as signed components, add their products; then replicate the sum to all color channels, including alpha.</span></span> <span data-ttu-id="0447c-187">Dieser Vorgang wird für Farb-und Alpha Vorgänge unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0447c-187">This operation is supported for color and alpha operations.</span></span>

![Gleichung der Punktprodukt 3 Operation (s (RGBA) = arg1 (r) x arg2 (r) + arg1 (g) x arg2 (g) + arg1 (b) x arg2 (b))](images/topfrm17.png)

<span data-ttu-id="0447c-189">In DirectX 6 und DirectX 7 werden die oben genannten Eingaben vor der Verwendung zum simulieren signierter Daten um die Hälfte (y = x-0,5) nach unten verschoben, und das skalare Ergebnis wird automatisch an positive Werte gebunden und auf alle drei Ausgabekanäle repliziert.</span><span class="sxs-lookup"><span data-stu-id="0447c-189">In DirectX 6 and DirectX 7, multitexture operations the above inputs are all shifted down by half (y = x - 0.5) before use to simulate signed data, and the scalar result is automatically clamped to positive values and replicated to all three output channels.</span></span> <span data-ttu-id="0447c-190">Beachten Sie außerdem, dass bei einem Farb Vorgang die Alpha-Komponenten nicht aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="0447c-190">Also, note that as a color operation this does not updated the alpha it just updates the RGB components.</span></span>

<span data-ttu-id="0447c-191">In DirectX 8,1-Shadern können Sie jedoch angeben, dass die Ausgabe an die RGB-oder die. a-Komponente oder beides (Standard) weitergeleitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="0447c-191">However, in DirectX 8.1 shaders you can specify that the output be routed to the .rgb or the .a components or both (the default).</span></span> <span data-ttu-id="0447c-192">Sie können auch einen separaten skalarvorgang für den Alphakanal angeben.</span><span class="sxs-lookup"><span data-stu-id="0447c-192">You can also specify a separate scalar operation on the alpha channel.</span></span>

</dd> <dt>

<span data-ttu-id="0447c-193"><span id="D3DTOP_MULTIPLYADD"></span><span id="d3dtop_multiplyadd"></span>**D3DTOP \_ MultiplyAdd**</span><span class="sxs-lookup"><span data-stu-id="0447c-193"><span id="D3DTOP_MULTIPLYADD"></span><span id="d3dtop_multiplyadd"></span>**D3DTOP\_MULTIPLYADD**</span></span>
</dt> <dd>

<span data-ttu-id="0447c-194">Führt einen Multiplikations Vorgang aus.</span><span class="sxs-lookup"><span data-stu-id="0447c-194">Performs a multiply-accumulate operation.</span></span> <span data-ttu-id="0447c-195">Es werden die beiden letzten Argumente abgerufen, multipliziert und dem verbleibenden Eingabe-/Quellargument hinzugefügt und in das Ergebnis eingefügt.</span><span class="sxs-lookup"><span data-stu-id="0447c-195">It takes the last two arguments, multiplies them together, and adds them to the remaining input/source argument, and places that into the result.</span></span>

<span data-ttu-id="0447c-196">S<sub>RGBA</sub> = arg1 + arg2 \* arg3</span><span class="sxs-lookup"><span data-stu-id="0447c-196">S<sub>RGBA</sub> = Arg1 + Arg2 \* Arg3</span></span>

</dd> <dt>

<span data-ttu-id="0447c-197"><span id="D3DTOP_LERP"></span><span id="d3dtop_lerp"></span>**D3DTOP \_ Lerp**</span><span class="sxs-lookup"><span data-stu-id="0447c-197"><span id="D3DTOP_LERP"></span><span id="d3dtop_lerp"></span>**D3DTOP\_LERP**</span></span>
</dt> <dd>

<span data-ttu-id="0447c-198">Linearly interpoliert zwischen dem zweiten und dritten Quell Argument durch einen proportional, der im ersten Quell Argument angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="0447c-198">Linearly interpolates between the second and third source arguments by a proportion specified in the first source argument.</span></span>

<span data-ttu-id="0447c-199">S<sub>RGBA</sub> = (arg1) \* arg2 + (1-arg1) \* arg3.</span><span class="sxs-lookup"><span data-stu-id="0447c-199">S<sub>RGBA</sub> = (Arg1) \* Arg2 + (1- Arg1) \* Arg3.</span></span>

</dd> <dt>

<span data-ttu-id="0447c-200"><span id="D3DTOP_FORCE_DWORD"></span><span id="d3dtop_force_dword"></span>**D3DTOP \_ Erzwingen von \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="0447c-200"><span id="D3DTOP_FORCE_DWORD"></span><span id="d3dtop_force_dword"></span>**D3DTOP\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="0447c-201">Erzwingt die Kompilierung dieser Enumeration in 32 Bits.</span><span class="sxs-lookup"><span data-stu-id="0447c-201">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="0447c-202">Ohne diesen Wert können einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="0447c-202">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="0447c-203">Dieser Wert wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="0447c-203">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0447c-204">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0447c-204">Remarks</span></span>

<span data-ttu-id="0447c-205">Die Member dieses Typs werden verwendet, wenn Farb-oder Alpha Operationen mithilfe der D3DTSS \_ colorop-oder D3DTSS \_ alphaop-Werte mit der [**IDirect3DDevice9:: settexturestagestate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) -Methode festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="0447c-205">The members of this type are used when setting color or alpha operations by using the D3DTSS\_COLOROP or D3DTSS\_ALPHAOP values with the [**IDirect3DDevice9::SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) method.</span></span>

<span data-ttu-id="0447c-206">In den obigen Formeln ist S<sub>RGBA</sub> die von einer Textur Operation erzeugte RGBA-Farbe, und arg1, arg2 und arg3 stellen die gesamte RGBA-Farbe der Textur Argumente dar.</span><span class="sxs-lookup"><span data-stu-id="0447c-206">In the above formulas, S<sub>RGBA</sub> is the RGBA color produced by a texture operation, and Arg1, Arg2, and Arg3 represent the complete RGBA color of the texture arguments.</span></span> <span data-ttu-id="0447c-207">Einzelne Komponenten eines Arguments werden mit Indexzeichen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="0447c-207">Individual components of an argument are shown with subscripts.</span></span> <span data-ttu-id="0447c-208">Die Alpha Komponente für Argument 1 würde z. b. als arg1<sub>A</sub>angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="0447c-208">For example, the alpha component for argument 1 would be shown as Arg1<sub>A</sub>.</span></span>

## <a name="requirements"></a><span data-ttu-id="0447c-209">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0447c-209">Requirements</span></span>



| <span data-ttu-id="0447c-210">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0447c-210">Requirement</span></span> | <span data-ttu-id="0447c-211">Wert</span><span class="sxs-lookup"><span data-stu-id="0447c-211">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0447c-212">Header</span><span class="sxs-lookup"><span data-stu-id="0447c-212">Header</span></span><br/> | <dl> <span data-ttu-id="0447c-213"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="0447c-213"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0447c-214">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0447c-214">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0447c-215">Direct3D-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="0447c-215">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="0447c-216">**D3DTEXTURESTAGESTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="0447c-216">**D3DTEXTURESTAGESTATETYPE**</span></span>](./d3dtexturestagestatetype.md)
</dt> </dl>

 

 
