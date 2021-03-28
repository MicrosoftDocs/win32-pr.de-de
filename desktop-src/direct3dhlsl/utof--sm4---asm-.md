---
title: utof (SM4-ASM)
description: Ganzzahl ohne Vorzeichen für Gleit Komma Konvertierung.
ms.assetid: 5A52C959-7B4C-4FA1-B29C-BCAF448419F8
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9283857df12a85819f0d191d13450e0311fdade
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104038366"
---
# <a name="utof-sm4---asm"></a><span data-ttu-id="46242-103">utof (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="46242-103">utof (sm4 - asm)</span></span>

<span data-ttu-id="46242-104">Ganzzahl ohne Vorzeichen für Gleit Komma Konvertierung.</span><span class="sxs-lookup"><span data-stu-id="46242-104">Unsigned integer to floating point conversion.</span></span>



| <span data-ttu-id="46242-105">utof dest \[ . mask \] , src0 \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="46242-105">utof dest\[.mask\], src0\[.swizzle\]</span></span> |
|--------------------------------------|



 



| <span data-ttu-id="46242-106">Element</span><span class="sxs-lookup"><span data-stu-id="46242-106">Item</span></span>                                                            | <span data-ttu-id="46242-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="46242-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="46242-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="46242-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="46242-109">\[in \] der Adresse des Vorgangs Ergebnisses.</span><span class="sxs-lookup"><span data-stu-id="46242-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="46242-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="46242-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="46242-111">\[in \] den zu konvertierenden Komponenten.</span><span class="sxs-lookup"><span data-stu-id="46242-111">\[in\] The components to convert.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="46242-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="46242-112">Remarks</span></span>

<span data-ttu-id="46242-113">*src0* muss einen ganzzahligen 32-Bit-ganzzahligen 4-Tupel enthalten.</span><span class="sxs-lookup"><span data-stu-id="46242-113">*src0* must contain an unsigned 32-bit integer 4-tuple.</span></span> <span data-ttu-id="46242-114">Nachdem die Anweisung ausgeführt wurde, enthält " *dest* " ein 4-Tupel mit Gleit Komma Wert.</span><span class="sxs-lookup"><span data-stu-id="46242-114">After the instruction executes, *dest* will contain a floating-point 4-tuple.</span></span> <span data-ttu-id="46242-115">Die Konvertierung erfolgt pro Komponente.</span><span class="sxs-lookup"><span data-stu-id="46242-115">The conversion is performed per-component.</span></span>

<span data-ttu-id="46242-116">Wenn ein ganzzahliger Eingabe Wert zu groß ist, um genau im Gleit Komma Format dargestellt zu werden, runden Sie auf den nächstgelegenen geraden-Modus.</span><span class="sxs-lookup"><span data-stu-id="46242-116">When an integer input value is too large to be represented exactly in the floating point format, round to nearest even mode.</span></span>

<span data-ttu-id="46242-117">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="46242-117">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="46242-118">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="46242-118">Vertex Shader</span></span> | <span data-ttu-id="46242-119">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="46242-119">Geometry Shader</span></span> | <span data-ttu-id="46242-120">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="46242-120">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="46242-121">x</span><span class="sxs-lookup"><span data-stu-id="46242-121">x</span></span>             | <span data-ttu-id="46242-122">x</span><span class="sxs-lookup"><span data-stu-id="46242-122">x</span></span>               | <span data-ttu-id="46242-123">x</span><span class="sxs-lookup"><span data-stu-id="46242-123">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="46242-124">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="46242-124">Minimum Shader Model</span></span>

<span data-ttu-id="46242-125">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="46242-125">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="46242-126">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="46242-126">Shader Model</span></span>                                              | <span data-ttu-id="46242-127">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="46242-127">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="46242-128">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="46242-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="46242-129">ja</span><span class="sxs-lookup"><span data-stu-id="46242-129">yes</span></span>       |
| [<span data-ttu-id="46242-130">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="46242-130">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="46242-131">ja</span><span class="sxs-lookup"><span data-stu-id="46242-131">yes</span></span>       |
| [<span data-ttu-id="46242-132">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="46242-132">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="46242-133">ja</span><span class="sxs-lookup"><span data-stu-id="46242-133">yes</span></span>       |
| [<span data-ttu-id="46242-134">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="46242-134">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="46242-135">nein</span><span class="sxs-lookup"><span data-stu-id="46242-135">no</span></span>        |
| [<span data-ttu-id="46242-136">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="46242-136">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="46242-137">nein</span><span class="sxs-lookup"><span data-stu-id="46242-137">no</span></span>        |
| [<span data-ttu-id="46242-138">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="46242-138">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="46242-139">nein</span><span class="sxs-lookup"><span data-stu-id="46242-139">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="46242-140">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="46242-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="46242-141">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="46242-141">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





