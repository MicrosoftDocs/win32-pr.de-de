---
title: -Rückruf (SM4-ASM)
description: Ruft eine von markierte Unterroutine auf, wobei die Bezeichnung l \ im Programm angezeigt wird.
ms.assetid: D6B7C52D-2CF7-44DB-81E3-2945477EF94A
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dac86fa52140968443f01050cebc57718fea420
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "103719398"
---
# <a name="call-sm4---asm"></a><span data-ttu-id="9c203-103">-Rückruf (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="9c203-103">call (sm4 - asm)</span></span>

<span data-ttu-id="9c203-104">Ruft eine von markierte Unterroutine auf, wobei die Bezeichnung **l \#** im Programm angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="9c203-104">Calls a subroutine marked by where the label **l\#** appears in the program.</span></span>



| <span data-ttu-id="9c203-105">l anrufen\#</span><span class="sxs-lookup"><span data-stu-id="9c203-105">call l\#</span></span> |
|----------|



 



| <span data-ttu-id="9c203-106">Element</span><span class="sxs-lookup"><span data-stu-id="9c203-106">Item</span></span>                                                       | <span data-ttu-id="9c203-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9c203-107">Description</span></span>                                    |
|------------------------------------------------------------|------------------------------------------------|
| <span data-ttu-id="9c203-108"><span id="l_"></span><span id="L_"></span>*int\#*</span><span class="sxs-lookup"><span data-stu-id="9c203-108"><span id="l_"></span><span id="L_"></span>*l\#*</span></span><br/> | <span data-ttu-id="9c203-109">\[in \] der Bezeichnung der Unterroutine.</span><span class="sxs-lookup"><span data-stu-id="9c203-109">\[in\] The label of the subroutine.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="9c203-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9c203-110">Remarks</span></span>

<span data-ttu-id="9c203-111">Wenn ein [ret](ret--sm4---asm-.md) gefunden wird, wird die Ausführung an die Anweisung nach diesem-Befehl zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9c203-111">When a [ret](ret--sm4---asm-.md) is encountered, return execution to the instruction after this call.</span></span>

<span data-ttu-id="9c203-112">Das tokenformat enthält den Offset der entsprechenden Bezeichnung im Shader.</span><span class="sxs-lookup"><span data-stu-id="9c203-112">The token format contains the offset of the corresponding label in the Shader as a convenience.</span></span>

<span data-ttu-id="9c203-113">Im folgenden Beispiel wird die-Anweisung aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="9c203-113">The following example shows the call instruction.</span></span>


```
                ...
                call l3
                ...
                ret
                label l3
                    ...
                    retc_nz r0.x
                    ...
                ret
```



### <a name="restrictions"></a><span data-ttu-id="9c203-114">Beschränkungen</span><span class="sxs-lookup"><span data-stu-id="9c203-114">Restrictions</span></span>

-   <span data-ttu-id="9c203-115">Unterroutinen können 32 tief Schachteln.</span><span class="sxs-lookup"><span data-stu-id="9c203-115">Subroutines can nest 32 deep.</span></span>
-   <span data-ttu-id="9c203-116">Der Rückgabe Adress Stapel wird von der-Implementierung transparent verwaltet.</span><span class="sxs-lookup"><span data-stu-id="9c203-116">The return address stack is managed transparently by the implementation.</span></span>
-   <span data-ttu-id="9c203-117">Wenn im Rückgabe Adress Stapel bereits 32 Einträge vorhanden sind und ein-Befehl ausgegeben wird **, wird der** -Vorgang übersprungen.</span><span class="sxs-lookup"><span data-stu-id="9c203-117">If there are already 32 entries on the return address stack and a **call** is issued, the call is skipped over.</span></span>
-   <span data-ttu-id="9c203-118">Es ist kein automatischer Parameter Stapel vorhanden.</span><span class="sxs-lookup"><span data-stu-id="9c203-118">There is no automatic parameter stack.</span></span> <span data-ttu-id="9c203-119">Die Anwendung kann ein indizierbares temporäres Registrierungs Array (x \# \[ \] ) verwenden, um einen Stapel manuell zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="9c203-119">The application can use an indexable temporary register array (x\#\[\]) to manually implement a stack.</span></span> <span data-ttu-id="9c203-120">Allerdings sind die Rückgabe Adressen der Unterroutine Aufrufe nicht sichtbar und für jede manuelle Stapel Verwaltung, die von der Anwendung ausgeführt wird, orthogonal.</span><span class="sxs-lookup"><span data-stu-id="9c203-120">However, the subroutine call return addresses are not visible and are orthogonal to any manual stack management done by the application.</span></span>
-   <span data-ttu-id="9c203-121">Die Indizierung *des \# l* -Parameters ist nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="9c203-121">Indexing of the *l\#* parameter is not permitted.</span></span>
-   <span data-ttu-id="9c203-122">Rekursion ist nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="9c203-122">Recursion is not permitted.</span></span>

<span data-ttu-id="9c203-123">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="9c203-123">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="9c203-124">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="9c203-124">Vertex Shader</span></span> | <span data-ttu-id="9c203-125">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="9c203-125">Geometry Shader</span></span> | <span data-ttu-id="9c203-126">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="9c203-126">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="9c203-127">x</span><span class="sxs-lookup"><span data-stu-id="9c203-127">x</span></span>             | <span data-ttu-id="9c203-128">x</span><span class="sxs-lookup"><span data-stu-id="9c203-128">x</span></span>               | <span data-ttu-id="9c203-129">x</span><span class="sxs-lookup"><span data-stu-id="9c203-129">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="9c203-130">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="9c203-130">Minimum Shader Model</span></span>

<span data-ttu-id="9c203-131">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9c203-131">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="9c203-132">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="9c203-132">Shader Model</span></span>                                              | <span data-ttu-id="9c203-133">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="9c203-133">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="9c203-134">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="9c203-134">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="9c203-135">ja</span><span class="sxs-lookup"><span data-stu-id="9c203-135">yes</span></span>       |
| [<span data-ttu-id="9c203-136">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="9c203-136">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="9c203-137">ja</span><span class="sxs-lookup"><span data-stu-id="9c203-137">yes</span></span>       |
| [<span data-ttu-id="9c203-138">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="9c203-138">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="9c203-139">ja</span><span class="sxs-lookup"><span data-stu-id="9c203-139">yes</span></span>       |
| [<span data-ttu-id="9c203-140">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9c203-140">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="9c203-141">nein</span><span class="sxs-lookup"><span data-stu-id="9c203-141">no</span></span>        |
| [<span data-ttu-id="9c203-142">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9c203-142">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="9c203-143">nein</span><span class="sxs-lookup"><span data-stu-id="9c203-143">no</span></span>        |
| [<span data-ttu-id="9c203-144">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9c203-144">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="9c203-145">nein</span><span class="sxs-lookup"><span data-stu-id="9c203-145">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="9c203-146">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9c203-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9c203-147">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9c203-147">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





