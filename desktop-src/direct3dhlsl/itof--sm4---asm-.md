---
title: itof (SM4-ASM)
description: Ganzzahl mit Vorzeichen für Gleit Komma Konvertierung.
ms.assetid: 60652168-25FA-4084-8CC1-73F12984ECED
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f9d262f65801cd2caa0e6432b335ce32fff0d4e
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "103857783"
---
# <a name="itof-sm4---asm"></a><span data-ttu-id="54be0-103">itof (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="54be0-103">itof (sm4 - asm)</span></span>

<span data-ttu-id="54be0-104">Ganzzahl mit Vorzeichen für Gleit Komma Konvertierung.</span><span class="sxs-lookup"><span data-stu-id="54be0-104">Signed integer to floating point conversion.</span></span>



| <span data-ttu-id="54be0-105">itof dest \[ . mask \] , \[ - \] src0 \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="54be0-105">itof dest\[.mask\], \[-\]src0\[.swizzle\]</span></span> |
|-------------------------------------------|



 



| <span data-ttu-id="54be0-106">Element</span><span class="sxs-lookup"><span data-stu-id="54be0-106">Item</span></span>                                                            | <span data-ttu-id="54be0-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="54be0-107">Description</span></span>                                             |
|-----------------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="54be0-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="54be0-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="54be0-109">\[in \] enthält das Ergebnis des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="54be0-109">\[in\] Contains the result of the operation.</span></span><br/> |
| <span data-ttu-id="54be0-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="54be0-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="54be0-111">\[in \] enthält den zu konvertierenden Wert.</span><span class="sxs-lookup"><span data-stu-id="54be0-111">\[in\] Contains the value to convert.</span></span><br/>        |



 

## <a name="remarks"></a><span data-ttu-id="54be0-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="54be0-112">Remarks</span></span>

<span data-ttu-id="54be0-113">Diese Konvertierungs Anweisung mit Vorzeichen unter Vorzeichen setzt voraus, dass *src0* 32 eine ganze Zahl mit Vorzeichen und 4-Tupel mit Vorzeichen enthält.</span><span class="sxs-lookup"><span data-stu-id="54be0-113">This signed integer-to-float conversion instruction assumes that *src0* contains a signed 32-bit integer 4-tuple.</span></span> <span data-ttu-id="54be0-114">Nachdem die Anweisung ausgeführt wurde, enthält " *dest* " ein 4-Tupel mit Gleit Komma Wert.</span><span class="sxs-lookup"><span data-stu-id="54be0-114">After the instruction executes, *dest* will contain a floating-point 4-tuple.</span></span>

<span data-ttu-id="54be0-115">Die Konvertierung erfolgt pro Komponente.</span><span class="sxs-lookup"><span data-stu-id="54be0-115">The conversion is performed per-component.</span></span>

<span data-ttu-id="54be0-116">Wenn ein ganzzahliger Eingabe Wert zu groß ist, um genau im Gleit Komma Format dargestellt zu werden, wird die Rundung auf den nächstgelegenen geraden Modus dringend empfohlen, ist aber nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="54be0-116">When an integer input value is too large in magnitude to be represented exactly in the floating point format, rounding to nearest even mode is strongly recommended but not required.</span></span>

<span data-ttu-id="54be0-117">Der optionale Negation-Modifizierer für den Quell Operanden nimmt vor dem Durchführen einer arithmetischen Operation eine Ergänzung von 2.</span><span class="sxs-lookup"><span data-stu-id="54be0-117">The optional negate modifier on source operand takes 2's complement before performing arithmetic operation.</span></span>

<span data-ttu-id="54be0-118">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="54be0-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="54be0-119">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="54be0-119">Vertex Shader</span></span> | <span data-ttu-id="54be0-120">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="54be0-120">Geometry Shader</span></span> | <span data-ttu-id="54be0-121">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="54be0-121">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="54be0-122">x</span><span class="sxs-lookup"><span data-stu-id="54be0-122">x</span></span>             | <span data-ttu-id="54be0-123">x</span><span class="sxs-lookup"><span data-stu-id="54be0-123">x</span></span>               | <span data-ttu-id="54be0-124">x</span><span class="sxs-lookup"><span data-stu-id="54be0-124">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="54be0-125">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="54be0-125">Minimum Shader Model</span></span>

<span data-ttu-id="54be0-126">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="54be0-126">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="54be0-127">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="54be0-127">Shader Model</span></span>                                              | <span data-ttu-id="54be0-128">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="54be0-128">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="54be0-129">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="54be0-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="54be0-130">ja</span><span class="sxs-lookup"><span data-stu-id="54be0-130">yes</span></span>       |
| [<span data-ttu-id="54be0-131">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="54be0-131">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="54be0-132">ja</span><span class="sxs-lookup"><span data-stu-id="54be0-132">yes</span></span>       |
| [<span data-ttu-id="54be0-133">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="54be0-133">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="54be0-134">ja</span><span class="sxs-lookup"><span data-stu-id="54be0-134">yes</span></span>       |
| [<span data-ttu-id="54be0-135">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="54be0-135">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="54be0-136">nein</span><span class="sxs-lookup"><span data-stu-id="54be0-136">no</span></span>        |
| [<span data-ttu-id="54be0-137">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="54be0-137">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="54be0-138">nein</span><span class="sxs-lookup"><span data-stu-id="54be0-138">no</span></span>        |
| [<span data-ttu-id="54be0-139">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="54be0-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="54be0-140">nein</span><span class="sxs-lookup"><span data-stu-id="54be0-140">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="54be0-141">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="54be0-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="54be0-142">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="54be0-142">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





