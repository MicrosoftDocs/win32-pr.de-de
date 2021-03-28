---
title: ftou (SM4-ASM)
description: Gleit Komma Wert Konvertierung ohne Vorzeichen.
ms.assetid: 0E3E090B-72C0-4CED-AFA5-2DDCF67D7263
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4a5e65e4bb9d4e71e4a2000f00861cf63e7c181
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104313644"
---
# <a name="ftou-sm4---asm"></a><span data-ttu-id="847a8-103">ftou (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="847a8-103">ftou (sm4 - asm)</span></span>

<span data-ttu-id="847a8-104">Gleit Komma Wert Konvertierung ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="847a8-104">Floating point to unsigned integer conversion.</span></span>



| <span data-ttu-id="847a8-105">ftou dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="847a8-105">ftou dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|----------------------------------------------------|



 



| <span data-ttu-id="847a8-106">f: dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="847a8-106">ftoi dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|----------------------------------------------------|



 



| <span data-ttu-id="847a8-107">Element</span><span class="sxs-lookup"><span data-stu-id="847a8-107">Item</span></span>                                                            | <span data-ttu-id="847a8-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="847a8-108">Description</span></span>                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="847a8-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="847a8-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="847a8-110">\[in \] der Adresse des Vorgangs Ergebnisses.</span><span class="sxs-lookup"><span data-stu-id="847a8-110">\[in\] The address of the result of the operation.</span></span> <br/> |
| <span data-ttu-id="847a8-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="847a8-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="847a8-112">\[in \] dem zu konvertierenden Wert.</span><span class="sxs-lookup"><span data-stu-id="847a8-112">\[in\] The value to convert.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="847a8-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="847a8-113">Remarks</span></span>

<span data-ttu-id="847a8-114">Die Konvertierung erfolgt pro Komponente.</span><span class="sxs-lookup"><span data-stu-id="847a8-114">The conversion is performed per-component.</span></span> <span data-ttu-id="847a8-115">Die Rundung erfolgt immer in Richtung 0 (null) und folgt der C-Konvention für Umwandlungen von float in int.</span><span class="sxs-lookup"><span data-stu-id="847a8-115">Rounding is always performed towards zero, following the C convention for casts from float to int.</span></span>

<span data-ttu-id="847a8-116">Anwendungen, die eine andere Rundungs Semantik erfordern, können die **runden** Anweisungen vor dem umwandeln in eine ganze Zahl aufrufen.</span><span class="sxs-lookup"><span data-stu-id="847a8-116">Applications that require different rounding semantics can invoke the **round** instructions before casting to integer.</span></span>

<span data-ttu-id="847a8-117">Eingaben werden an den Bereich \[ 0,0 f... 4294967295.999 f \] vor der Konvertierung, und Eingabe-NaN-Werte führen zu einem Ergebnis von NULL.</span><span class="sxs-lookup"><span data-stu-id="847a8-117">Inputs are clamped to the range \[0.0f ... 4294967295.999f\] prior to conversion, and input NaN values produce a zero result.</span></span>

<span data-ttu-id="847a8-118">Optionale Modifizierer Negation und absolute Werte werden vor der Konvertierung auf die Quell Werte angewendet.</span><span class="sxs-lookup"><span data-stu-id="847a8-118">Optional negate and absolute value modifiers are applied to the source values before conversion.</span></span>

<span data-ttu-id="847a8-119">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="847a8-119">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="847a8-120">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="847a8-120">Vertex Shader</span></span> | <span data-ttu-id="847a8-121">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="847a8-121">Geometry Shader</span></span> | <span data-ttu-id="847a8-122">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="847a8-122">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="847a8-123">x</span><span class="sxs-lookup"><span data-stu-id="847a8-123">x</span></span>             | <span data-ttu-id="847a8-124">x</span><span class="sxs-lookup"><span data-stu-id="847a8-124">x</span></span>               | <span data-ttu-id="847a8-125">x</span><span class="sxs-lookup"><span data-stu-id="847a8-125">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="847a8-126">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="847a8-126">Minimum Shader Model</span></span>

<span data-ttu-id="847a8-127">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="847a8-127">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="847a8-128">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="847a8-128">Shader Model</span></span>                                              | <span data-ttu-id="847a8-129">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="847a8-129">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="847a8-130">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="847a8-130">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="847a8-131">ja</span><span class="sxs-lookup"><span data-stu-id="847a8-131">yes</span></span>       |
| [<span data-ttu-id="847a8-132">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="847a8-132">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="847a8-133">ja</span><span class="sxs-lookup"><span data-stu-id="847a8-133">yes</span></span>       |
| [<span data-ttu-id="847a8-134">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="847a8-134">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="847a8-135">ja</span><span class="sxs-lookup"><span data-stu-id="847a8-135">yes</span></span>       |
| [<span data-ttu-id="847a8-136">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="847a8-136">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="847a8-137">nein</span><span class="sxs-lookup"><span data-stu-id="847a8-137">no</span></span>        |
| [<span data-ttu-id="847a8-138">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="847a8-138">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="847a8-139">nein</span><span class="sxs-lookup"><span data-stu-id="847a8-139">no</span></span>        |
| [<span data-ttu-id="847a8-140">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="847a8-140">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="847a8-141">nein</span><span class="sxs-lookup"><span data-stu-id="847a8-141">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="847a8-142">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="847a8-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="847a8-143">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="847a8-143">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





