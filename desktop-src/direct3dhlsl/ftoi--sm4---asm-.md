---
title: 'ftoi (sm4 – asm) '
description: Gleit Komma Zahl Konvertierungen mit Vorzeichen.
ms.assetid: 580AB4A6-0C1C-409B-B2B9-BA1D37772F46
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c02ce1b506d112a59d3087f59d219557575b8def
ms.sourcegitcommit: 8c658e9872a2173e3dcec94195f9067fbcd85d3d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/17/2020
ms.locfileid: "104316670"
---
# <a name="ftoi-sm4---asm"></a><span data-ttu-id="48f5e-103">ftoi (sm4 – asm) </span><span class="sxs-lookup"><span data-stu-id="48f5e-103">ftoi (sm4 - asm)</span></span>

<span data-ttu-id="48f5e-104">Gleit Komma Zahl Konvertierungen mit Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="48f5e-104">Floating point to signed integer conversion.</span></span>

| <span data-ttu-id="48f5e-105">f: dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="48f5e-105">ftoi dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|-|

| <span data-ttu-id="48f5e-106">Element</span><span class="sxs-lookup"><span data-stu-id="48f5e-106">Item</span></span> | <span data-ttu-id="48f5e-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="48f5e-107">Description</span></span> |
|-|-|
| <span data-ttu-id="48f5e-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="48f5e-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="48f5e-109">\[in \] der Adresse des Vorgangs Ergebnisses.</span><span class="sxs-lookup"><span data-stu-id="48f5e-109">\[in\] The address of the result of the operation.</span></span><br/> <span data-ttu-id="48f5e-110">*dest*  =  [Round \_ z](round-z--sm4---asm-.md)(*src0*)</span><span class="sxs-lookup"><span data-stu-id="48f5e-110">*dest* = [round\_z](round-z--sm4---asm-.md)(*src0*)</span></span><br/> |
| <span data-ttu-id="48f5e-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="48f5e-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="48f5e-112">\[in \] der zu konvertierenden Komponente.</span><span class="sxs-lookup"><span data-stu-id="48f5e-112">\[in\] The component to convert.</span></span><br/> |

## <a name="remarks"></a><span data-ttu-id="48f5e-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="48f5e-113">Remarks</span></span>

<span data-ttu-id="48f5e-114">Die Konvertierung erfolgt pro Komponente.</span><span class="sxs-lookup"><span data-stu-id="48f5e-114">The conversion is performed per component.</span></span> <span data-ttu-id="48f5e-115">Die Rundung erfolgt immer in Richtung 0 (null) und folgt der C-Konvention für Umwandlungen von float in int. Anwendungen, die eine andere Rundungs Semantik erfordern, können die **runden** Anweisungen vor dem umwandeln in eine ganze Zahl aufrufen.</span><span class="sxs-lookup"><span data-stu-id="48f5e-115">Rounding is always performed towards zero, following the C convention for casts from float to int. Applications that require different rounding semantics can invoke the **round** instructions before casting to integer.</span></span>

<span data-ttu-id="48f5e-116">Eingaben werden an den Bereich \[ 2147483648.999 f... 2147483647.999 f \] vor der Konvertierung, und Eingabe-NaN-Werte führen zu einem Ergebnis von NULL.</span><span class="sxs-lookup"><span data-stu-id="48f5e-116">Inputs are clamped to the range \[-2147483648.999f ... 2147483647.999f\] prior to conversion, and input NaN values produce a zero result.</span></span>

<span data-ttu-id="48f5e-117">Optionale Modifizierer Negation und absolute Werte werden vor der Konvertierung auf die Quell Werte angewendet.</span><span class="sxs-lookup"><span data-stu-id="48f5e-117">Optional negate and absolute value modifiers are applied to the source values before conversion.</span></span>

<span data-ttu-id="48f5e-118">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="48f5e-118">This instruction applies to the following shader stages:</span></span>

| <span data-ttu-id="48f5e-119">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="48f5e-119">Vertex Shader</span></span> | <span data-ttu-id="48f5e-120">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="48f5e-120">Geometry Shader</span></span> | <span data-ttu-id="48f5e-121">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="48f5e-121">Pixel Shader</span></span> |
|-|-|-|
| <span data-ttu-id="48f5e-122">x</span><span class="sxs-lookup"><span data-stu-id="48f5e-122">x</span></span> | <span data-ttu-id="48f5e-123">x</span><span class="sxs-lookup"><span data-stu-id="48f5e-123">x</span></span> | <span data-ttu-id="48f5e-124">x</span><span class="sxs-lookup"><span data-stu-id="48f5e-124">x</span></span> |

## <a name="minimum-shader-model"></a><span data-ttu-id="48f5e-125">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="48f5e-125">Minimum Shader Model</span></span>

<span data-ttu-id="48f5e-126">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="48f5e-126">This function is supported in the following shader models.</span></span>

| <span data-ttu-id="48f5e-127">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="48f5e-127">Shader Model</span></span> | <span data-ttu-id="48f5e-128">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="48f5e-128">Supported</span></span> |
|-|-|
| [<span data-ttu-id="48f5e-129">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="48f5e-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md) | <span data-ttu-id="48f5e-130">ja</span><span class="sxs-lookup"><span data-stu-id="48f5e-130">yes</span></span> |
| [<span data-ttu-id="48f5e-131">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="48f5e-131">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md) | <span data-ttu-id="48f5e-132">ja</span><span class="sxs-lookup"><span data-stu-id="48f5e-132">yes</span></span> |
| [<span data-ttu-id="48f5e-133">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="48f5e-133">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md) | <span data-ttu-id="48f5e-134">ja</span><span class="sxs-lookup"><span data-stu-id="48f5e-134">yes</span></span> |
| [<span data-ttu-id="48f5e-135">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="48f5e-135">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="48f5e-136">nein</span><span class="sxs-lookup"><span data-stu-id="48f5e-136">no</span></span> |
| [<span data-ttu-id="48f5e-137">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="48f5e-137">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="48f5e-138">nein</span><span class="sxs-lookup"><span data-stu-id="48f5e-138">no</span></span> |
| [<span data-ttu-id="48f5e-139">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="48f5e-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="48f5e-140">nein</span><span class="sxs-lookup"><span data-stu-id="48f5e-140">no</span></span> |

## <a name="related-topics"></a><span data-ttu-id="48f5e-141">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="48f5e-141">Related topics</span></span>

[<span data-ttu-id="48f5e-142">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="48f5e-142">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
