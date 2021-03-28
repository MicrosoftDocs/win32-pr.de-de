---
title: udiv (SM4-ASM)
description: Unterteilung ohne Vorzeichen.
ms.assetid: 87C81418-0F74-4C67-9D4A-DA952EFD008E
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07a3dd2f4170a3c8fe522af12d412cfae49396da
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104389536"
---
# <a name="udiv-sm4---asm"></a><span data-ttu-id="195b6-103">udiv (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="195b6-103">udiv (sm4 - asm)</span></span>

<span data-ttu-id="195b6-104">Unterteilung ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="195b6-104">Unsigned integer divide.</span></span>



| <span data-ttu-id="195b6-105">udiv destquot \[ . mask \] , de Strem \[ . mask \] , src0 \[ . Swizzle \] , Quelle1 \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="195b6-105">udiv destQUOT\[.mask\], destREM\[.mask\], src0\[.swizzle\], src1\[.swizzle\]</span></span> |
|------------------------------------------------------------------------------|



 



| <span data-ttu-id="195b6-106">Element</span><span class="sxs-lookup"><span data-stu-id="195b6-106">Item</span></span>                                                                                                   | <span data-ttu-id="195b6-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="195b6-107">Description</span></span>                                                |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="195b6-108"><span id="destQUOT"></span><span id="destquot"></span><span id="DESTQUOT"></span>*destquot*</span><span class="sxs-lookup"><span data-stu-id="195b6-108"><span id="destQUOT"></span><span id="destquot"></span><span id="DESTQUOT"></span>*destQUOT*</span></span><br/> | <span data-ttu-id="195b6-109">\[in \] der Adresse des resultierenden Quotienten.</span><span class="sxs-lookup"><span data-stu-id="195b6-109">\[in\] The address of the resulting quotient.</span></span><br/>   |
| <span data-ttu-id="195b6-110"><span id="destREM"></span><span id="destrem"></span><span id="DESTREM"></span>*"Debug"*</span><span class="sxs-lookup"><span data-stu-id="195b6-110"><span id="destREM"></span><span id="destrem"></span><span id="DESTREM"></span>*destREM*</span></span><br/>     | <span data-ttu-id="195b6-111">\[in \] der Adresse des resultierenden Restwerts.</span><span class="sxs-lookup"><span data-stu-id="195b6-111">\[in\] The address of the resulting remainder.</span></span><br/>  |
| <span data-ttu-id="195b6-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="195b6-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                        | <span data-ttu-id="195b6-113">\[in \] den Komponenten, die durch *Quelle1* dividiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="195b6-113">\[in\] The components to be divided by *src1*.</span></span><br/>  |
| <span data-ttu-id="195b6-114"><span id="src1"></span><span id="SRC1"></span>*Quelle1*</span><span class="sxs-lookup"><span data-stu-id="195b6-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/>                                        | <span data-ttu-id="195b6-115">\[in \] den Komponenten by welche to Divide *src0*.</span><span class="sxs-lookup"><span data-stu-id="195b6-115">\[in\] The components by whch to divide *src0*.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="195b6-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="195b6-116">Remarks</span></span>

<span data-ttu-id="195b6-117">Diese Anweisung führt eine Komponenten Weise unsignierte Teilung des 32-Bit-Operanden *src0* durch den 32-Bit-Operanden *Quelle1* aus.</span><span class="sxs-lookup"><span data-stu-id="195b6-117">This instruction performs a component-wise unsigned divide of the 32-bit operand *src0* by the 32-bit operand *src1*.</span></span> <span data-ttu-id="195b6-118">Die Ergebnisse der Teilungen sind die 32-Bit-Quotienten in " *destquot* " und 32-Bit-Rest-Werten, die in " *de Strem*" platziert werden.</span><span class="sxs-lookup"><span data-stu-id="195b6-118">The results of the divides are the 32-bit quotients placed in *destQUOT* and 32-bit remainders placed in *destREM*.</span></span>

<span data-ttu-id="195b6-119">Division durch Null gibt 0xFFFFFFFF für den Quotienten und den Rest zurück.</span><span class="sxs-lookup"><span data-stu-id="195b6-119">Divide by zero returns 0xffffffff for both quotient and remainder.</span></span>

<span data-ttu-id="195b6-120">Sie können entweder *destquot* oder *Destrem* als NULL angeben, anstatt ein Register anzugeben, wenn der Quotienten oder Rest nicht benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="195b6-120">You can specifiy either *destQUOT* or *destREM* as NULL instead of specifying a register, if the quotient or remainder are not needed.</span></span>

<span data-ttu-id="195b6-121">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="195b6-121">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="195b6-122">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="195b6-122">Vertex Shader</span></span> | <span data-ttu-id="195b6-123">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="195b6-123">Geometry Shader</span></span> | <span data-ttu-id="195b6-124">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="195b6-124">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="195b6-125">x</span><span class="sxs-lookup"><span data-stu-id="195b6-125">x</span></span>             | <span data-ttu-id="195b6-126">x</span><span class="sxs-lookup"><span data-stu-id="195b6-126">x</span></span>               | <span data-ttu-id="195b6-127">x</span><span class="sxs-lookup"><span data-stu-id="195b6-127">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="195b6-128">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="195b6-128">Minimum Shader Model</span></span>

<span data-ttu-id="195b6-129">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="195b6-129">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="195b6-130">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="195b6-130">Shader Model</span></span>                                              | <span data-ttu-id="195b6-131">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="195b6-131">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="195b6-132">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="195b6-132">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="195b6-133">ja</span><span class="sxs-lookup"><span data-stu-id="195b6-133">yes</span></span>       |
| [<span data-ttu-id="195b6-134">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="195b6-134">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="195b6-135">ja</span><span class="sxs-lookup"><span data-stu-id="195b6-135">yes</span></span>       |
| [<span data-ttu-id="195b6-136">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="195b6-136">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="195b6-137">ja</span><span class="sxs-lookup"><span data-stu-id="195b6-137">yes</span></span>       |
| [<span data-ttu-id="195b6-138">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="195b6-138">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="195b6-139">nein</span><span class="sxs-lookup"><span data-stu-id="195b6-139">no</span></span>        |
| [<span data-ttu-id="195b6-140">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="195b6-140">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="195b6-141">nein</span><span class="sxs-lookup"><span data-stu-id="195b6-141">no</span></span>        |
| [<span data-ttu-id="195b6-142">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="195b6-142">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="195b6-143">nein</span><span class="sxs-lookup"><span data-stu-id="195b6-143">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="195b6-144">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="195b6-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="195b6-145">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="195b6-145">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





