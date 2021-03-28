---
title: asuint-Funktion
description: Interpretiert das Bitmuster eines 64-Bit-Werts als zwei Ganzzahlen 32 ohne Vorzeichen zurück.
ms.assetid: 29671661-4fec-46e5-9b6f-56fba8e1d756
keywords:
- asuint-Funktion HLSL
topic_type:
- apiref
api_name:
- asuint
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c54ed89e112482df4a54f35e24a04694e88fa490
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104038140"
---
# <a name="asuint-function"></a><span data-ttu-id="42f64-104">asuint-Funktion</span><span class="sxs-lookup"><span data-stu-id="42f64-104">asuint function</span></span>

<span data-ttu-id="42f64-105">Interpretiert das Bitmuster eines 64-Bit-Werts als zwei Ganzzahlen 32 ohne Vorzeichen zurück.</span><span class="sxs-lookup"><span data-stu-id="42f64-105">Reinterprets the bit pattern of a 64-bit value as two unsigned 32-bit integers.</span></span>

## <a name="syntax"></a><span data-ttu-id="42f64-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="42f64-106">Syntax</span></span>

``` syntax
void asuint(
  in  double value,
  out uint lowbits,
  out uint highbits
);
```

## <a name="parameters"></a><span data-ttu-id="42f64-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="42f64-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42f64-108">*Wert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="42f64-108">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42f64-109">Typ: **Double**</span><span class="sxs-lookup"><span data-stu-id="42f64-109">Type: **double**</span></span>

<span data-ttu-id="42f64-110">Der Eingabewert.</span><span class="sxs-lookup"><span data-stu-id="42f64-110">The input value.</span></span>

</dd> <dt>

<span data-ttu-id="42f64-111">*lowbits* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="42f64-111">*lowbits* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="42f64-112">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="42f64-112">Type: **uint**</span></span>

<span data-ttu-id="42f64-113">Das niedrige 32-Bit-Muster des *Werts*.</span><span class="sxs-lookup"><span data-stu-id="42f64-113">The low 32-bit pattern of *value*.</span></span>

</dd> <dt>

<span data-ttu-id="42f64-114">*highbits* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="42f64-114">*highbits* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="42f64-115">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="42f64-115">Type: **uint**</span></span>

<span data-ttu-id="42f64-116">Das hohe 32-Bit-Muster des *Werts*.</span><span class="sxs-lookup"><span data-stu-id="42f64-116">The high 32-bit pattern of *value*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42f64-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="42f64-117">Return value</span></span>

<span data-ttu-id="42f64-118">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="42f64-118">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="42f64-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="42f64-119">Remarks</span></span>

<span data-ttu-id="42f64-120">Diese Funktion ist eine Alternative Version von " [**asuint**](dx-graphics-hlsl-asuint.md) ", die in früheren shadermodellen verfügbar war und für Shader Model 5 eingeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="42f64-120">This function is an alternate version of the [**asuint**](dx-graphics-hlsl-asuint.md) intrinsic that has been available in earlier shader models, and was introduced for Shader Model 5.</span></span> <span data-ttu-id="42f64-121">Die ursprüngliche Funktion (im HLSL-Compiler mit der unterschiedlichen Signatur erkannt) bleibt für Shader Model 5 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="42f64-121">The original function (recognized in the HLSL compiler by its different signature) remains available to Shader Model 5.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="42f64-122">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="42f64-122">Minimum Shader Model</span></span>

<span data-ttu-id="42f64-123">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="42f64-123">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="42f64-124">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="42f64-124">Shader Model</span></span>                                                                | <span data-ttu-id="42f64-125">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="42f64-125">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="42f64-126">[Shader Model 5](d3d11-graphics-reference-sm5.md) und höhere shadermodelle</span><span class="sxs-lookup"><span data-stu-id="42f64-126">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="42f64-127">ja</span><span class="sxs-lookup"><span data-stu-id="42f64-127">yes</span></span>       |



 

<span data-ttu-id="42f64-128">Diese Funktion wird in den folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="42f64-128">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="42f64-129">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="42f64-129">Vertex</span></span> | <span data-ttu-id="42f64-130">Hülle</span><span class="sxs-lookup"><span data-stu-id="42f64-130">Hull</span></span> | <span data-ttu-id="42f64-131">Domain</span><span class="sxs-lookup"><span data-stu-id="42f64-131">Domain</span></span> | <span data-ttu-id="42f64-132">Geometrie</span><span class="sxs-lookup"><span data-stu-id="42f64-132">Geometry</span></span> | <span data-ttu-id="42f64-133">Pixel</span><span class="sxs-lookup"><span data-stu-id="42f64-133">Pixel</span></span> | <span data-ttu-id="42f64-134">Compute</span><span class="sxs-lookup"><span data-stu-id="42f64-134">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="42f64-135">x</span><span class="sxs-lookup"><span data-stu-id="42f64-135">x</span></span>      | <span data-ttu-id="42f64-136">x</span><span class="sxs-lookup"><span data-stu-id="42f64-136">x</span></span>    | <span data-ttu-id="42f64-137">x</span><span class="sxs-lookup"><span data-stu-id="42f64-137">x</span></span>      | <span data-ttu-id="42f64-138">x</span><span class="sxs-lookup"><span data-stu-id="42f64-138">x</span></span>        | <span data-ttu-id="42f64-139">x</span><span class="sxs-lookup"><span data-stu-id="42f64-139">x</span></span>     | <span data-ttu-id="42f64-140">x</span><span class="sxs-lookup"><span data-stu-id="42f64-140">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="42f64-141">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="42f64-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42f64-142">Intrinsische Funktionen</span><span class="sxs-lookup"><span data-stu-id="42f64-142">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="42f64-143">**asuint (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="42f64-143">**asuint (DirectX HLSL)**</span></span>](dx-graphics-hlsl-asuint.md)
</dt> <dt>

[<span data-ttu-id="42f64-144">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="42f64-144">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




