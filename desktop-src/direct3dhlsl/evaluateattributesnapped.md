---
title: Evaluateattributesnapped-Funktion
description: Wertet den Pixel Schwerpunkt mit einem Offset aus.
ms.assetid: f5085016-0e94-49bb-96b6-42fa15c30b9f
keywords:
- Evaluateattributesnapped-Funktion HLSL
topic_type:
- apiref
api_name:
- EvaluateAttributeSnapped
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 70a9389ed9e9f4fff16f82610cb611bc4da2c7a3
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104992895"
---
# <a name="evaluateattributesnapped-function"></a><span data-ttu-id="91cb5-104">Evaluateattributesnapped-Funktion</span><span class="sxs-lookup"><span data-stu-id="91cb5-104">EvaluateAttributeSnapped function</span></span>

<span data-ttu-id="91cb5-105">Wertet den Pixel Schwerpunkt mit einem Offset aus.</span><span class="sxs-lookup"><span data-stu-id="91cb5-105">Evaluates at the pixel centroid with an offset.</span></span>

## <a name="syntax"></a><span data-ttu-id="91cb5-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="91cb5-106">Syntax</span></span>

``` syntax
numeric EvaluateAttributeSnapped(
  in attrib numeric value,
  in 
            int2 offset
);
```

## <a name="parameters"></a><span data-ttu-id="91cb5-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="91cb5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91cb5-108">*Wert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="91cb5-108">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91cb5-109">Type: **atzb numeric**</span><span class="sxs-lookup"><span data-stu-id="91cb5-109">Type: **attrib numeric**</span></span>

<span data-ttu-id="91cb5-110">Der Eingabewert.</span><span class="sxs-lookup"><span data-stu-id="91cb5-110">The input value.</span></span>

</dd> <dt>

<span data-ttu-id="91cb5-111">*Offset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="91cb5-111">*offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91cb5-112">Typ: **int2**</span><span class="sxs-lookup"><span data-stu-id="91cb5-112">Type: **int2**</span></span>

<span data-ttu-id="91cb5-113">Ein 2D-Offset aus dem Pixel Center unter Verwendung eines 16x16-Rasters.</span><span class="sxs-lookup"><span data-stu-id="91cb5-113">A 2D offset from the pixel center using a 16x16 grid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="91cb5-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="91cb5-114">Remarks</span></span>

<span data-ttu-id="91cb5-115">Der Bereich für den *Offset* -Parameter muss durch den folgenden Bytecode definiert werden.</span><span class="sxs-lookup"><span data-stu-id="91cb5-115">The range for the *offset* parameter must be defined by the following byte code.</span></span>

<span data-ttu-id="91cb5-116">Es werden nur die am wenigsten wichtigen 4 Bits der ersten beiden Komponenten (U, V) des Pixel Offsets verwendet.</span><span class="sxs-lookup"><span data-stu-id="91cb5-116">Only the least significant 4 bits of the first two components (U, V) of the pixel offset are used.</span></span> <span data-ttu-id="91cb5-117">Die Konvertierung des 4-Bit-Fixpunkts in float ist wie folgt (MSB... LSB), wobei MSB Teil des Bruchteils ist und das Vorzeichen bestimmt:</span><span class="sxs-lookup"><span data-stu-id="91cb5-117">The conversion from the 4-bit fixed point to float is as follows (MSB...LSB), where the MSB is both a part of the fraction and determines the sign:</span></span>

-   <span data-ttu-id="91cb5-118">1000 =-0,5 f (-8/16)</span><span class="sxs-lookup"><span data-stu-id="91cb5-118">1000 = -0.5f (-8 / 16)</span></span>
-   <span data-ttu-id="91cb5-119">1001 =-0.4375 f (-7/16)</span><span class="sxs-lookup"><span data-stu-id="91cb5-119">1001 = -0.4375f (-7 / 16)</span></span>
-   <span data-ttu-id="91cb5-120">1010 =-0,375 f (-6/16)</span><span class="sxs-lookup"><span data-stu-id="91cb5-120">1010 = -0.375f (-6 / 16)</span></span>
-   <span data-ttu-id="91cb5-121">1011 =-0.3125 f (-5/16)</span><span class="sxs-lookup"><span data-stu-id="91cb5-121">1011 = -0.3125f (-5 / 16)</span></span>
-   <span data-ttu-id="91cb5-122">1100 =-0,25 f (-4/16)</span><span class="sxs-lookup"><span data-stu-id="91cb5-122">1100 = -0.25f (-4 / 16)</span></span>
-   <span data-ttu-id="91cb5-123">1101 =-0.1875 f (-3/16)</span><span class="sxs-lookup"><span data-stu-id="91cb5-123">1101 = -0.1875f (-3 / 16)</span></span>
-   <span data-ttu-id="91cb5-124">1110 =-0,125 f (-2/16)</span><span class="sxs-lookup"><span data-stu-id="91cb5-124">1110 = -0.125f (-2 / 16)</span></span>
-   <span data-ttu-id="91cb5-125">1111 =-0.0625 f (-1/16)</span><span class="sxs-lookup"><span data-stu-id="91cb5-125">1111 = -0.0625f (-1 / 16)</span></span>
-   <span data-ttu-id="91cb5-126">0000 = 0,0 f (0/16)</span><span class="sxs-lookup"><span data-stu-id="91cb5-126">0000 = 0.0f ( 0 / 16)</span></span>
-   <span data-ttu-id="91cb5-127">0001 = 0.0625 f (1/16)</span><span class="sxs-lookup"><span data-stu-id="91cb5-127">0001 = 0.0625f ( 1 / 16)</span></span>
-   <span data-ttu-id="91cb5-128">0010 = 0,125 f (2/16)</span><span class="sxs-lookup"><span data-stu-id="91cb5-128">0010 = 0.125f ( 2 / 16)</span></span>
-   <span data-ttu-id="91cb5-129">0011 = 0.1875 f (3/16)</span><span class="sxs-lookup"><span data-stu-id="91cb5-129">0011 = 0.1875f ( 3 / 16)</span></span>
-   <span data-ttu-id="91cb5-130">0100 = 0,25 f (4/16)</span><span class="sxs-lookup"><span data-stu-id="91cb5-130">0100 = 0.25f ( 4 / 16)</span></span>
-   <span data-ttu-id="91cb5-131">0101 = 0.3125 f (5/16)</span><span class="sxs-lookup"><span data-stu-id="91cb5-131">0101 = 0.3125f ( 5 / 16)</span></span>
-   <span data-ttu-id="91cb5-132">0110 = 0,375 f (6/16)</span><span class="sxs-lookup"><span data-stu-id="91cb5-132">0110 = 0.375f ( 6 / 16)</span></span>
-   <span data-ttu-id="91cb5-133">0111 = 0.4375 f (7/16)</span><span class="sxs-lookup"><span data-stu-id="91cb5-133">0111 = 0.4375f ( 7 / 16)</span></span>

> [!Note]  
> <span data-ttu-id="91cb5-134">Der linke und obere Rand eines Pixels sind im Offset enthalten. die unteren und rechten Ränder werden jedoch nicht eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="91cb5-134">The left and top edges of a pixel are included in the offset; however, the bottom and right edges are not included.</span></span> <span data-ttu-id="91cb5-135">Alle anderen Bits in der 32-Bit-Ganzzahl von Werten für Werte und V-Offset werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="91cb5-135">All other bits in the 32-bit integer U and V offset values are ignored.</span></span>

 

<span data-ttu-id="91cb5-136">Eine-Implementierung kann den vom Shader bereitgestellten Offset annehmen und einen vollständigen 32-Bit-fest Komma Wert (28,4) abrufen, der den gültigen Bereich umfasst, indem die folgende Berechnung durchgeführt wird:</span><span class="sxs-lookup"><span data-stu-id="91cb5-136">An implementation can take the offset provided by the shader and obtain a full 32-bit fixed point value (28.4), which spans the valid range, by performing the following calculation:</span></span>


```
iU = (iU<<28)>>28  // keep lowest 4 bits and sign extend, which yields [-8..7]
```



<span data-ttu-id="91cb5-137">Wenn eine Implementierung den Offset einem Gleit Komma Offset zuordnen muss, wird die folgende Berechnung durchführt:</span><span class="sxs-lookup"><span data-stu-id="91cb5-137">If an implementation must map the offset to a floating-point offset, it performs the following calculation:</span></span>


```
fU = ((float)iU)/16
```



### <a name="minimum-shader-model"></a><span data-ttu-id="91cb5-138">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="91cb5-138">Minimum Shader Model</span></span>

<span data-ttu-id="91cb5-139">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="91cb5-139">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="91cb5-140">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="91cb5-140">Shader Model</span></span>                                                                | <span data-ttu-id="91cb5-141">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="91cb5-141">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="91cb5-142">[Shader Model 5](d3d11-graphics-reference-sm5.md) und höhere shadermodelle</span><span class="sxs-lookup"><span data-stu-id="91cb5-142">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="91cb5-143">ja</span><span class="sxs-lookup"><span data-stu-id="91cb5-143">yes</span></span>       |



 

<span data-ttu-id="91cb5-144">Diese Funktion wird in den folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="91cb5-144">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="91cb5-145">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="91cb5-145">Vertex</span></span> | <span data-ttu-id="91cb5-146">Hülle</span><span class="sxs-lookup"><span data-stu-id="91cb5-146">Hull</span></span> | <span data-ttu-id="91cb5-147">Domain</span><span class="sxs-lookup"><span data-stu-id="91cb5-147">Domain</span></span> | <span data-ttu-id="91cb5-148">Geometrie</span><span class="sxs-lookup"><span data-stu-id="91cb5-148">Geometry</span></span> | <span data-ttu-id="91cb5-149">Pixel</span><span class="sxs-lookup"><span data-stu-id="91cb5-149">Pixel</span></span> | <span data-ttu-id="91cb5-150">Compute</span><span class="sxs-lookup"><span data-stu-id="91cb5-150">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="91cb5-151">x</span><span class="sxs-lookup"><span data-stu-id="91cb5-151">x</span></span>     |         |



 

## <a name="see-also"></a><span data-ttu-id="91cb5-152">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="91cb5-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91cb5-153">Intrinsische Funktionen</span><span class="sxs-lookup"><span data-stu-id="91cb5-153">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="91cb5-154">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="91cb5-154">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




