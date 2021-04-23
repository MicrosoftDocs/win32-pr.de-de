---
title: countbits-Funktion
description: Zählt die Anzahl der Bits (pro Komponente), die in der Eingabe-Ganzzahl festgelegt sind.
ms.assetid: c4fafbc8-e21c-48cb-b433-8241a989ec85
keywords:
- countbits-Funktion HLSL
topic_type:
- apiref
api_name:
- countbits
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 357aceca6e2aea261a9e94212b58ff6308c99560
ms.sourcegitcommit: 435ea8f5bf06808ffa7dce39afb0ee6de842ba2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2021
ms.locfileid: "107925623"
---
# <a name="countbits-function"></a><span data-ttu-id="f9396-104">countbits-Funktion</span><span class="sxs-lookup"><span data-stu-id="f9396-104">countbits function</span></span>

<span data-ttu-id="f9396-105">Zählt die Anzahl der Bits (pro Komponente), die in der Eingabe-Ganzzahl festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="f9396-105">Counts the number of bits (per component) set in the input integer.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9396-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="f9396-106">Syntax</span></span>

``` syntax
uint countbits(
  in uint value
);
```

## <a name="parameters"></a><span data-ttu-id="f9396-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="f9396-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9396-108">*value* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="f9396-108">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9396-109">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="f9396-109">Type: **uint**</span></span>

<span data-ttu-id="f9396-110">Der Eingabewert.</span><span class="sxs-lookup"><span data-stu-id="f9396-110">The input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9396-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f9396-111">Return value</span></span>

<span data-ttu-id="f9396-112">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="f9396-112">Type: **uint**</span></span>

<span data-ttu-id="f9396-113">Die Anzahl der Bits.</span><span class="sxs-lookup"><span data-stu-id="f9396-113">The number of bits.</span></span>

## <a name="remarks"></a><span data-ttu-id="f9396-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f9396-114">Remarks</span></span>

<span data-ttu-id="f9396-115">Die folgenden überladenen Versionen sind ebenfalls verfügbar:</span><span class="sxs-lookup"><span data-stu-id="f9396-115">The following overloaded versions are also available:</span></span>

``` syntax
uint count_bits(uint value);
uint2 count_bits(uint2 value);
uint3 count_bits(uint3 value);
uint4 count_bits(uint4 value);
```

### <a name="minimum-shader-model"></a><span data-ttu-id="f9396-116">Minimales Shadermodell</span><span class="sxs-lookup"><span data-stu-id="f9396-116">Minimum Shader Model</span></span>

<span data-ttu-id="f9396-117">Diese Funktion wird in den folgenden Shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f9396-117">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="f9396-118">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="f9396-118">Shader Model</span></span>                                                                | <span data-ttu-id="f9396-119">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="f9396-119">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="f9396-120">[Shadermodell 5](d3d11-graphics-reference-sm5.md) und höher– Shadermodelle</span><span class="sxs-lookup"><span data-stu-id="f9396-120">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="f9396-121">ja</span><span class="sxs-lookup"><span data-stu-id="f9396-121">yes</span></span>       |



 

<span data-ttu-id="f9396-122">Diese Funktion wird in den folgenden Shadertypen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="f9396-122">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="f9396-123">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="f9396-123">Vertex</span></span> | <span data-ttu-id="f9396-124">Rumpf</span><span class="sxs-lookup"><span data-stu-id="f9396-124">Hull</span></span> | <span data-ttu-id="f9396-125">Domain</span><span class="sxs-lookup"><span data-stu-id="f9396-125">Domain</span></span> | <span data-ttu-id="f9396-126">Geometrie</span><span class="sxs-lookup"><span data-stu-id="f9396-126">Geometry</span></span> | <span data-ttu-id="f9396-127">Pixel</span><span class="sxs-lookup"><span data-stu-id="f9396-127">Pixel</span></span> | <span data-ttu-id="f9396-128">Compute</span><span class="sxs-lookup"><span data-stu-id="f9396-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="f9396-129">x</span><span class="sxs-lookup"><span data-stu-id="f9396-129">x</span></span>      | <span data-ttu-id="f9396-130">x</span><span class="sxs-lookup"><span data-stu-id="f9396-130">x</span></span>    | <span data-ttu-id="f9396-131">x</span><span class="sxs-lookup"><span data-stu-id="f9396-131">x</span></span>      | <span data-ttu-id="f9396-132">x</span><span class="sxs-lookup"><span data-stu-id="f9396-132">x</span></span>        | <span data-ttu-id="f9396-133">x</span><span class="sxs-lookup"><span data-stu-id="f9396-133">x</span></span>     | <span data-ttu-id="f9396-134">x</span><span class="sxs-lookup"><span data-stu-id="f9396-134">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="f9396-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f9396-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9396-136">Systeminterne Funktionen</span><span class="sxs-lookup"><span data-stu-id="f9396-136">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="f9396-137">Shadermodell 5</span><span class="sxs-lookup"><span data-stu-id="f9396-137">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




