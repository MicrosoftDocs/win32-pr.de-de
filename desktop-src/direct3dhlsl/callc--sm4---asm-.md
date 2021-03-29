---
title: callc (SM4-ASM)
description: Ruft bedingt eine durch markierte Unterroutine auf, wobei die Bezeichnung l \ im Programm angezeigt wird.
ms.assetid: 7F6E81CE-0C38-499B-B83E-FA76FA154451
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6bc8c9d1e4a99ce25f99253518482181cdb74d8
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104993071"
---
# <a name="callc-sm4---asm"></a><span data-ttu-id="855dd-103">callc (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="855dd-103">callc (sm4 - asm)</span></span>

<span data-ttu-id="855dd-104">Ruft bedingt eine durch markierte Unterroutine auf, wobei die Bezeichnung **l \#** im Programm angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="855dd-104">Conditionally calls a subroutine marked by where the label **l\#** appears in the program.</span></span>



| <span data-ttu-id="855dd-105">callc { \_ z </span><span class="sxs-lookup"><span data-stu-id="855dd-105">callc{\_z</span></span>\|<span data-ttu-id="855dd-106">\_NZ} src0. Select- \_ Komponente, l\#</span><span class="sxs-lookup"><span data-stu-id="855dd-106">\_nz} src0.select\_component, l\#</span></span> |
|----------------------------------------------|



 



| <span data-ttu-id="855dd-107">Element</span><span class="sxs-lookup"><span data-stu-id="855dd-107">Item</span></span>                                                            | <span data-ttu-id="855dd-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="855dd-108">Description</span></span>                                                     |
|-----------------------------------------------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="855dd-109"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="855dd-109"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="855dd-110">\[in \] der Komponente, für die die Bedingung getestet werden soll.</span><span class="sxs-lookup"><span data-stu-id="855dd-110">\[in\] The component on which to test the condition.</span></span><br/> |
| <span data-ttu-id="855dd-111"><span id="l_"></span><span id="L_"></span>*int\#*</span><span class="sxs-lookup"><span data-stu-id="855dd-111"><span id="l_"></span><span id="L_"></span>*l\#*</span></span><br/>      | <span data-ttu-id="855dd-112">\[in \] der Bezeichnung der Unterroutine.</span><span class="sxs-lookup"><span data-stu-id="855dd-112">\[in\] The label of the subroutine.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="855dd-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="855dd-113">Remarks</span></span>

<span data-ttu-id="855dd-114">Wenn ein [ret](ret--sm4---asm-.md) gefunden wird, wird die Ausführung an die Anweisung nach diesem-Befehl zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="855dd-114">When a [ret](ret--sm4---asm-.md) is encountered, return execution to the instruction after this call.</span></span>

<span data-ttu-id="855dd-115">Das tokenformat enthält den Offset der entsprechenden Bezeichnung im Shader.</span><span class="sxs-lookup"><span data-stu-id="855dd-115">The token format contains the offset of the corresponding label in the Shader as a convenience.</span></span>

<span data-ttu-id="855dd-116">Im folgenden Beispiel wird die-Anweisung aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="855dd-116">The following example shows the call instruction.</span></span>


```
                ...
                callc_z  r1.y, l3 // if all bits in r0.x are 0, call l3
                callc_nz r2.z, l3 // if any bit in r0.x is nonzero, call l3
                ...
                ret
                label l3
                    ...
                    retc_nz r0.x
                    ...
                ret

```



### <a name="restrictions"></a><span data-ttu-id="855dd-117">Beschränkungen</span><span class="sxs-lookup"><span data-stu-id="855dd-117">Restrictions</span></span>

-   <span data-ttu-id="855dd-118">Unterroutinen können 32 tief Schachteln.</span><span class="sxs-lookup"><span data-stu-id="855dd-118">Subroutines can nest 32 deep.</span></span>
-   <span data-ttu-id="855dd-119">Der Rückgabe Adress Stapel wird von der-Implementierung transparent verwaltet.</span><span class="sxs-lookup"><span data-stu-id="855dd-119">The return address stack is managed transparently by the implementation.</span></span>
-   <span data-ttu-id="855dd-120">Wenn im Rückgabe Adress Stapel bereits 32 Einträge vorhanden sind und ein-Befehl ausgegeben wird **, wird der** -Vorgang übersprungen.</span><span class="sxs-lookup"><span data-stu-id="855dd-120">If there are already 32 entries on the return address stack and a **call** is issued, the call is skipped over.</span></span>
-   <span data-ttu-id="855dd-121">Es ist kein automatischer Parameter Stapel vorhanden.</span><span class="sxs-lookup"><span data-stu-id="855dd-121">There is no automatic parameter stack.</span></span> <span data-ttu-id="855dd-122">Die Anwendung kann ein indizierbares temporäres Registrierungs Array (x \# \[ \] ) verwenden, um einen Stapel manuell zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="855dd-122">The application can use an indexable temporary register array (x\#\[\]) to manually implement a stack.</span></span> <span data-ttu-id="855dd-123">Allerdings sind die Rückgabe Adressen der Unterroutine Aufrufe nicht sichtbar und für jede manuelle Stapel Verwaltung, die von der Anwendung ausgeführt wird, orthogonal.</span><span class="sxs-lookup"><span data-stu-id="855dd-123">However, the subroutine call return addresses are not visible and are orthogonal to any manual stack management done by the application.</span></span>
-   <span data-ttu-id="855dd-124">Die Indizierung *des \# l* -Parameters ist nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="855dd-124">Indexing of the *l\#* parameter is not permitted.</span></span>
-   <span data-ttu-id="855dd-125">Das 32-Bit-Register, das von *src0* bereitgestellt wird, wird auf einer Bitebene getestet.</span><span class="sxs-lookup"><span data-stu-id="855dd-125">The 32-bit register supplied by *src0* is tested at a bit level.</span></span> <span data-ttu-id="855dd-126">Wenn ein Bit ungleich 0 (null) ist, führt **callc \_ NZ** den Aufruf aus.</span><span class="sxs-lookup"><span data-stu-id="855dd-126">If any bit is nonzero, **callc\_nz** will perform the call.</span></span> <span data-ttu-id="855dd-127">Wenn alle Bits NULL sind, führt **callc \_ z** den Aufruf aus.</span><span class="sxs-lookup"><span data-stu-id="855dd-127">If all bits are zero, **callc\_z** will perform the call.</span></span>
-   <span data-ttu-id="855dd-128">Rekursion ist nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="855dd-128">Recursion is not permitted.</span></span>

<span data-ttu-id="855dd-129">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="855dd-129">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="855dd-130">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="855dd-130">Vertex Shader</span></span> | <span data-ttu-id="855dd-131">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="855dd-131">Geometry Shader</span></span> | <span data-ttu-id="855dd-132">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="855dd-132">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="855dd-133">x</span><span class="sxs-lookup"><span data-stu-id="855dd-133">x</span></span>             | <span data-ttu-id="855dd-134">x</span><span class="sxs-lookup"><span data-stu-id="855dd-134">x</span></span>               | <span data-ttu-id="855dd-135">x</span><span class="sxs-lookup"><span data-stu-id="855dd-135">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="855dd-136">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="855dd-136">Minimum Shader Model</span></span>

<span data-ttu-id="855dd-137">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="855dd-137">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="855dd-138">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="855dd-138">Shader Model</span></span>                                              | <span data-ttu-id="855dd-139">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="855dd-139">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="855dd-140">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="855dd-140">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="855dd-141">ja</span><span class="sxs-lookup"><span data-stu-id="855dd-141">yes</span></span>       |
| [<span data-ttu-id="855dd-142">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="855dd-142">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="855dd-143">ja</span><span class="sxs-lookup"><span data-stu-id="855dd-143">yes</span></span>       |
| [<span data-ttu-id="855dd-144">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="855dd-144">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="855dd-145">ja</span><span class="sxs-lookup"><span data-stu-id="855dd-145">yes</span></span>       |
| [<span data-ttu-id="855dd-146">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="855dd-146">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="855dd-147">nein</span><span class="sxs-lookup"><span data-stu-id="855dd-147">no</span></span>        |
| [<span data-ttu-id="855dd-148">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="855dd-148">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="855dd-149">nein</span><span class="sxs-lookup"><span data-stu-id="855dd-149">no</span></span>        |
| [<span data-ttu-id="855dd-150">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="855dd-150">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="855dd-151">nein</span><span class="sxs-lookup"><span data-stu-id="855dd-151">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="855dd-152">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="855dd-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="855dd-153">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="855dd-153">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





