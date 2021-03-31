---
title: reversebits-Funktion
description: Kehrt die Reihenfolge der Bits pro Komponente um.
ms.assetid: dad46e25-9980-4645-98eb-d834db704fc8
keywords:
- reversebits-Funktion HLSL
topic_type:
- apiref
api_name:
- reversebits
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d98b824883ddc4f06e6c11d30c2759bb0fc2be26
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104471957"
---
# <a name="reversebits-function"></a><span data-ttu-id="f50fc-104">reversebits-Funktion</span><span class="sxs-lookup"><span data-stu-id="f50fc-104">reversebits function</span></span>

<span data-ttu-id="f50fc-105">Kehrt die Reihenfolge der Bits pro Komponente um.</span><span class="sxs-lookup"><span data-stu-id="f50fc-105">Reverses the order of the bits, per component.</span></span>

## <a name="syntax"></a><span data-ttu-id="f50fc-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="f50fc-106">Syntax</span></span>

``` syntax
uint reversebits(
  in uint value
);
```

## <a name="parameters"></a><span data-ttu-id="f50fc-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="f50fc-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f50fc-108">*Wert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f50fc-108">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f50fc-109">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="f50fc-109">Type: **uint**</span></span>

<span data-ttu-id="f50fc-110">Der Eingabewert.</span><span class="sxs-lookup"><span data-stu-id="f50fc-110">The input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f50fc-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f50fc-111">Return value</span></span>

<span data-ttu-id="f50fc-112">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="f50fc-112">Type: **uint**</span></span>

<span data-ttu-id="f50fc-113">Der Eingabe Wert, bei dem die bitreihenfolge umgekehrt ist.</span><span class="sxs-lookup"><span data-stu-id="f50fc-113">The input value, with the bit order reversed.</span></span>

## <a name="remarks"></a><span data-ttu-id="f50fc-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f50fc-114">Remarks</span></span>

<span data-ttu-id="f50fc-115">Außerdem sind die folgenden überladenen Versionen verfügbar:</span><span class="sxs-lookup"><span data-stu-id="f50fc-115">The following overloaded versions are also available:</span></span>

``` syntax
uint2 reversebits(uint2 value);
uint3 reversebits(uint3 value);
uint4 reversebits(uint4 value);
```

### <a name="minimum-shader-model"></a><span data-ttu-id="f50fc-116">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="f50fc-116">Minimum Shader Model</span></span>

<span data-ttu-id="f50fc-117">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f50fc-117">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="f50fc-118">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="f50fc-118">Shader Model</span></span>                                                                | <span data-ttu-id="f50fc-119">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="f50fc-119">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="f50fc-120">[Shader Model 5](d3d11-graphics-reference-sm5.md) und höhere shadermodelle</span><span class="sxs-lookup"><span data-stu-id="f50fc-120">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="f50fc-121">ja</span><span class="sxs-lookup"><span data-stu-id="f50fc-121">yes</span></span>       |



 

<span data-ttu-id="f50fc-122">Diese Funktion wird in den folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="f50fc-122">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="f50fc-123">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="f50fc-123">Vertex</span></span> | <span data-ttu-id="f50fc-124">Hülle</span><span class="sxs-lookup"><span data-stu-id="f50fc-124">Hull</span></span> | <span data-ttu-id="f50fc-125">Domain</span><span class="sxs-lookup"><span data-stu-id="f50fc-125">Domain</span></span> | <span data-ttu-id="f50fc-126">Geometrie</span><span class="sxs-lookup"><span data-stu-id="f50fc-126">Geometry</span></span> | <span data-ttu-id="f50fc-127">Pixel</span><span class="sxs-lookup"><span data-stu-id="f50fc-127">Pixel</span></span> | <span data-ttu-id="f50fc-128">Compute</span><span class="sxs-lookup"><span data-stu-id="f50fc-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="f50fc-129">x</span><span class="sxs-lookup"><span data-stu-id="f50fc-129">x</span></span>      | <span data-ttu-id="f50fc-130">x</span><span class="sxs-lookup"><span data-stu-id="f50fc-130">x</span></span>    | <span data-ttu-id="f50fc-131">x</span><span class="sxs-lookup"><span data-stu-id="f50fc-131">x</span></span>      | <span data-ttu-id="f50fc-132">x</span><span class="sxs-lookup"><span data-stu-id="f50fc-132">x</span></span>        | <span data-ttu-id="f50fc-133">x</span><span class="sxs-lookup"><span data-stu-id="f50fc-133">x</span></span>     | <span data-ttu-id="f50fc-134">x</span><span class="sxs-lookup"><span data-stu-id="f50fc-134">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="f50fc-135">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f50fc-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f50fc-136">Intrinsische Funktionen</span><span class="sxs-lookup"><span data-stu-id="f50fc-136">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="f50fc-137">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="f50fc-137">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




