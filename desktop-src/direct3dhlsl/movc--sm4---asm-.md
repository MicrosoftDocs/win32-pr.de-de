---
title: "\"muvc\" (SM4-ASM)"
description: Bedingter Wechsel in Komponenten. | "muvc" (SM4-ASM)
ms.assetid: B7F19DF5-282F-41D4-AE2D-6ACF61A42088
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91aa3116b7bc13102386c57c9b8c63d3534147a8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995478"
---
# <a name="movc-sm4---asm"></a><span data-ttu-id="71ceb-104">"muvc" (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="71ceb-104">movc (sm4 - asm)</span></span>

<span data-ttu-id="71ceb-105">Bedingter Wechsel in Komponenten.</span><span class="sxs-lookup"><span data-stu-id="71ceb-105">Component-wise conditional move.</span></span>



| <span data-ttu-id="71ceb-106">der Pfad von "netvc" ist " \[ \_ \] dest \[ . Mask" \] , src0 \[ . Swizzle \] , \[ - \] Quelle1 \[ \_ ABS \] \[ . Swizzle \] , \[ - \] Quelle2 \[ \_ ABS \] \[ . Swizzle \] ,</span><span class="sxs-lookup"><span data-stu-id="71ceb-106">movc\[\_sat\] dest\[.mask\], src0\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\], \[-\]src2\[\_abs\]\[.swizzle\],</span></span> |
|----------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="71ceb-107">Element</span><span class="sxs-lookup"><span data-stu-id="71ceb-107">Item</span></span>                                                            | <span data-ttu-id="71ceb-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="71ceb-108">Description</span></span>                                                                                                                    |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71ceb-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="71ceb-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="71ceb-110">\[in \] der Adresse des Vorgangs Ergebnisses.</span><span class="sxs-lookup"><span data-stu-id="71ceb-110">\[in\] The address of the result of the operation.</span></span> <br/> <span data-ttu-id="71ceb-111">Wenn *src0*, dann *dest*  =  *Quelle1* Else *dest*  =  *Quelle2*</span><span class="sxs-lookup"><span data-stu-id="71ceb-111">If *src0*, then *dest* = *src1* else *dest* = *src2*</span></span><br/> |
| <span data-ttu-id="71ceb-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="71ceb-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="71ceb-113">\[in \] den Komponenten, für die die Bedingung getestet werden soll.</span><span class="sxs-lookup"><span data-stu-id="71ceb-113">\[in\] The components on which to test the condition.</span></span><br/>                                                               |
| <span data-ttu-id="71ceb-114"><span id="src1"></span><span id="SRC1"></span>*Quelle1*</span><span class="sxs-lookup"><span data-stu-id="71ceb-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="71ceb-115">\[in \] den zu Verschieb-Komponenten.</span><span class="sxs-lookup"><span data-stu-id="71ceb-115">\[in\] The components to move.</span></span> <br/>                                                                                     |
| <span data-ttu-id="71ceb-116"><span id="src2"></span><span id="SRC2"></span>*Quelle2*</span><span class="sxs-lookup"><span data-stu-id="71ceb-116"><span id="src2"></span><span id="SRC2"></span>*src2*</span></span><br/> | <span data-ttu-id="71ceb-117">\[in \] den zu Verschieb-Komponenten.</span><span class="sxs-lookup"><span data-stu-id="71ceb-117">\[in\] The components to move.</span></span><br/>                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="71ceb-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="71ceb-118">Remarks</span></span>

<span data-ttu-id="71ceb-119">Das folgende Beispiel zeigt die Verwendung dieser Anweisung.</span><span class="sxs-lookup"><span data-stu-id="71ceb-119">The following example shows how to use this instruction.</span></span>

``` syntax
                for each component in dest[.mask]
                    if the corresponding component in src0 (POS-swizzle)
                       has any bit set
                    {
                        copy this component (POS-swizzle) from src1 into dest
                    }
                    else
                    {
                        copy this component (POS-swizzle) from src2 into dest
                    }
                endfor
```

<span data-ttu-id="71ceb-120">Bei den Modifizierern auf *Quelle1* und *Quelle2*, mit Ausnahme von Swizzle, wird davon ausgegangen, dass die Daten Gleit Komma sind.</span><span class="sxs-lookup"><span data-stu-id="71ceb-120">The modifiers on *src1* and *src2*, other than swizzle, assume the data is floating point.</span></span> <span data-ttu-id="71ceb-121">Das Fehlen von Modifizierern verschiebt Daten nur, ohne Bits zu ändern.</span><span class="sxs-lookup"><span data-stu-id="71ceb-121">The absence of modifiers just moves data without altering bits.</span></span>

<span data-ttu-id="71ceb-122">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="71ceb-122">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="71ceb-123">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="71ceb-123">Vertex Shader</span></span> | <span data-ttu-id="71ceb-124">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="71ceb-124">Geometry Shader</span></span> | <span data-ttu-id="71ceb-125">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="71ceb-125">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="71ceb-126">x</span><span class="sxs-lookup"><span data-stu-id="71ceb-126">x</span></span>             | <span data-ttu-id="71ceb-127">x</span><span class="sxs-lookup"><span data-stu-id="71ceb-127">x</span></span>               | <span data-ttu-id="71ceb-128">x</span><span class="sxs-lookup"><span data-stu-id="71ceb-128">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="71ceb-129">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="71ceb-129">Minimum Shader Model</span></span>

<span data-ttu-id="71ceb-130">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="71ceb-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="71ceb-131">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="71ceb-131">Shader Model</span></span>                                              | <span data-ttu-id="71ceb-132">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="71ceb-132">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="71ceb-133">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="71ceb-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="71ceb-134">ja</span><span class="sxs-lookup"><span data-stu-id="71ceb-134">yes</span></span>       |
| [<span data-ttu-id="71ceb-135">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="71ceb-135">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="71ceb-136">ja</span><span class="sxs-lookup"><span data-stu-id="71ceb-136">yes</span></span>       |
| [<span data-ttu-id="71ceb-137">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="71ceb-137">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="71ceb-138">ja</span><span class="sxs-lookup"><span data-stu-id="71ceb-138">yes</span></span>       |
| [<span data-ttu-id="71ceb-139">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="71ceb-139">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="71ceb-140">nein</span><span class="sxs-lookup"><span data-stu-id="71ceb-140">no</span></span>        |
| [<span data-ttu-id="71ceb-141">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="71ceb-141">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="71ceb-142">nein</span><span class="sxs-lookup"><span data-stu-id="71ceb-142">no</span></span>        |
| [<span data-ttu-id="71ceb-143">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="71ceb-143">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="71ceb-144">nein</span><span class="sxs-lookup"><span data-stu-id="71ceb-144">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="71ceb-145">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="71ceb-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="71ceb-146">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="71ceb-146">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





