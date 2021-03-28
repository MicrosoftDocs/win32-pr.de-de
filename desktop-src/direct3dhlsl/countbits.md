---
title: countbits-Funktion
description: Zählt die Anzahl der Bits (pro Komponente) in der Eingabe Ganzzahl.
ms.assetid: c4fafbc8-e21c-48cb-b433-8241a989ec85
keywords:
- count-Bits-Funktion HLSL
topic_type:
- apiref
api_name:
- countbits
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 60d3cd63502c6217e6fb0b0ff17685b2d2b5bf25
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104038124"
---
# <a name="countbits-function"></a><span data-ttu-id="44822-104">countbits-Funktion</span><span class="sxs-lookup"><span data-stu-id="44822-104">countbits function</span></span>

<span data-ttu-id="44822-105">Zählt die Anzahl der Bits (pro Komponente) in der Eingabe Ganzzahl.</span><span class="sxs-lookup"><span data-stu-id="44822-105">Counts the number of bits (per component) in the input integer.</span></span>

## <a name="syntax"></a><span data-ttu-id="44822-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="44822-106">Syntax</span></span>

``` syntax
uint countbits(
  in uint value
);
```

## <a name="parameters"></a><span data-ttu-id="44822-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="44822-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44822-108">*Wert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="44822-108">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44822-109">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="44822-109">Type: **uint**</span></span>

<span data-ttu-id="44822-110">Der Eingabewert.</span><span class="sxs-lookup"><span data-stu-id="44822-110">The input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44822-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="44822-111">Return value</span></span>

<span data-ttu-id="44822-112">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="44822-112">Type: **uint**</span></span>

<span data-ttu-id="44822-113">Die Anzahl der Bits.</span><span class="sxs-lookup"><span data-stu-id="44822-113">The number of bits.</span></span>

## <a name="remarks"></a><span data-ttu-id="44822-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="44822-114">Remarks</span></span>

<span data-ttu-id="44822-115">Außerdem sind die folgenden überladenen Versionen verfügbar:</span><span class="sxs-lookup"><span data-stu-id="44822-115">The following overloaded versions are also available:</span></span>

``` syntax
uint count_bits(uint value);
uint2 count_bits(uint2 value);
uint3 count_bits(uint3 value);
uint4 count_bits(uint4 value);
```

### <a name="minimum-shader-model"></a><span data-ttu-id="44822-116">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="44822-116">Minimum Shader Model</span></span>

<span data-ttu-id="44822-117">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="44822-117">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="44822-118">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="44822-118">Shader Model</span></span>                                                                | <span data-ttu-id="44822-119">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="44822-119">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="44822-120">[Shader Model 5](d3d11-graphics-reference-sm5.md) und höhere shadermodelle</span><span class="sxs-lookup"><span data-stu-id="44822-120">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="44822-121">ja</span><span class="sxs-lookup"><span data-stu-id="44822-121">yes</span></span>       |



 

<span data-ttu-id="44822-122">Diese Funktion wird in den folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="44822-122">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="44822-123">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="44822-123">Vertex</span></span> | <span data-ttu-id="44822-124">Hülle</span><span class="sxs-lookup"><span data-stu-id="44822-124">Hull</span></span> | <span data-ttu-id="44822-125">Domain</span><span class="sxs-lookup"><span data-stu-id="44822-125">Domain</span></span> | <span data-ttu-id="44822-126">Geometrie</span><span class="sxs-lookup"><span data-stu-id="44822-126">Geometry</span></span> | <span data-ttu-id="44822-127">Pixel</span><span class="sxs-lookup"><span data-stu-id="44822-127">Pixel</span></span> | <span data-ttu-id="44822-128">Compute</span><span class="sxs-lookup"><span data-stu-id="44822-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="44822-129">x</span><span class="sxs-lookup"><span data-stu-id="44822-129">x</span></span>      | <span data-ttu-id="44822-130">x</span><span class="sxs-lookup"><span data-stu-id="44822-130">x</span></span>    | <span data-ttu-id="44822-131">x</span><span class="sxs-lookup"><span data-stu-id="44822-131">x</span></span>      | <span data-ttu-id="44822-132">x</span><span class="sxs-lookup"><span data-stu-id="44822-132">x</span></span>        | <span data-ttu-id="44822-133">x</span><span class="sxs-lookup"><span data-stu-id="44822-133">x</span></span>     | <span data-ttu-id="44822-134">x</span><span class="sxs-lookup"><span data-stu-id="44822-134">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="44822-135">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="44822-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44822-136">Intrinsische Funktionen</span><span class="sxs-lookup"><span data-stu-id="44822-136">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="44822-137">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="44822-137">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




