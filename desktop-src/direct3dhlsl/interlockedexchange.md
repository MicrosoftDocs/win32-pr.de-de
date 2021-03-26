---
title: Interlockedexchange-Funktion (HLSL-Referenz)
description: Weist dem dest einen Wert zu und gibt den ursprünglichen Wert zurück.
ms.assetid: 1e7ce7ff-9e23-47fa-8e76-713f6bf57abf
keywords:
- Interlockedexchange-Funktion HLSL
topic_type:
- apiref
api_name:
- InterlockedExchange
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7c39dc4f68429fa3f070d446f998fd528a99af01
ms.sourcegitcommit: 12e9b14501d51641b690ee0cf764e2b91eb9a140
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/06/2020
ms.locfileid: "104976584"
---
# <a name="interlockedexchange-function-hlsl-reference"></a><span data-ttu-id="dfaed-104">Interlockedexchange-Funktion (HLSL-Referenz)</span><span class="sxs-lookup"><span data-stu-id="dfaed-104">InterlockedExchange function (HLSL reference)</span></span>

<span data-ttu-id="dfaed-105">Weist dem dest einen Wert zu und gibt den ursprünglichen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="dfaed-105">Assigns value to dest and returns the original value.</span></span>

## <a name="syntax"></a><span data-ttu-id="dfaed-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="dfaed-106">Syntax</span></span>

``` syntax
void InterlockedExchange(
  in  R dest,
  in  T value,
  out T original_value
);
```

## <a name="parameters"></a><span data-ttu-id="dfaed-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="dfaed-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dfaed-108">*dest* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dfaed-108">*dest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dfaed-109">Typ: **R**</span><span class="sxs-lookup"><span data-stu-id="dfaed-109">Type: **R**</span></span>

<span data-ttu-id="dfaed-110">Die Zieladresse.</span><span class="sxs-lookup"><span data-stu-id="dfaed-110">The destination address.</span></span>

</dd> <dt>

<span data-ttu-id="dfaed-111">*Wert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dfaed-111">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dfaed-112">Typ: **T**</span><span class="sxs-lookup"><span data-stu-id="dfaed-112">Type: **T**</span></span>

<span data-ttu-id="dfaed-113">Der Eingabewert.</span><span class="sxs-lookup"><span data-stu-id="dfaed-113">The input value.</span></span>

</dd> <dt>

<span data-ttu-id="dfaed-114">*ursprünglicher \_ Wert* ausgehend \[\]</span><span class="sxs-lookup"><span data-stu-id="dfaed-114">*original\_value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dfaed-115">Typ: **T**</span><span class="sxs-lookup"><span data-stu-id="dfaed-115">Type: **T**</span></span>

<span data-ttu-id="dfaed-116">Der ursprüngliche Wert.</span><span class="sxs-lookup"><span data-stu-id="dfaed-116">The original value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dfaed-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dfaed-117">Return value</span></span>

<span data-ttu-id="dfaed-118">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="dfaed-118">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="dfaed-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dfaed-119">Remarks</span></span>

<span data-ttu-id="dfaed-120">Dieser Vorgang kann nur für skalartypisierte Ressourcen und Shared Memory-Variablen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="dfaed-120">This operation can only be performed on scalar-typed resources and shared memory variables.</span></span> <span data-ttu-id="dfaed-121">Es gibt zwei Verwendungsmöglichkeiten für diese Funktion.</span><span class="sxs-lookup"><span data-stu-id="dfaed-121">There are two possible uses for this function.</span></span> <span data-ttu-id="dfaed-122">Der erste ist, wenn R ein Variablentyp für den gemeinsamen Speicher ist.</span><span class="sxs-lookup"><span data-stu-id="dfaed-122">The first is when R is a shared memory variable type.</span></span> <span data-ttu-id="dfaed-123">In diesem Fall führt die Funktion den Vorgang für das Shared Memory-Register aus, auf das von dest verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="dfaed-123">In this case, the function performs the operation on the shared memory register referenced by dest.</span></span> <span data-ttu-id="dfaed-124">Das zweite Szenario ist, wenn R ein Ressourcen Variablentyp ist.</span><span class="sxs-lookup"><span data-stu-id="dfaed-124">The second scenario is when R is a resource variable type.</span></span> <span data-ttu-id="dfaed-125">In diesem Szenario führt die Funktion den Vorgang an dem Ressourcen Speicherort aus, auf den "dest" verweist.</span><span class="sxs-lookup"><span data-stu-id="dfaed-125">In this scenario, the function performs the operation on the resource location referenced by dest.</span></span> <span data-ttu-id="dfaed-126">Dieser Vorgang ist nur verfügbar, wenn R lesbar und beschreibbar ist.</span><span class="sxs-lookup"><span data-stu-id="dfaed-126">This operation is only available when R is readable and writable.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="dfaed-127">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="dfaed-127">Minimum Shader Model</span></span>

<span data-ttu-id="dfaed-128">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="dfaed-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="dfaed-129">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="dfaed-129">Shader Model</span></span>                                                                | <span data-ttu-id="dfaed-130">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="dfaed-130">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="dfaed-131">[Shader Model 5](d3d11-graphics-reference-sm5.md) und höhere shadermodelle</span><span class="sxs-lookup"><span data-stu-id="dfaed-131">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="dfaed-132">ja</span><span class="sxs-lookup"><span data-stu-id="dfaed-132">yes</span></span>       |



 

<span data-ttu-id="dfaed-133">Diese Funktion wird in den folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="dfaed-133">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="dfaed-134">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="dfaed-134">Vertex</span></span> | <span data-ttu-id="dfaed-135">Hülle</span><span class="sxs-lookup"><span data-stu-id="dfaed-135">Hull</span></span> | <span data-ttu-id="dfaed-136">Domain</span><span class="sxs-lookup"><span data-stu-id="dfaed-136">Domain</span></span> | <span data-ttu-id="dfaed-137">Geometrie</span><span class="sxs-lookup"><span data-stu-id="dfaed-137">Geometry</span></span> | <span data-ttu-id="dfaed-138">Pixel</span><span class="sxs-lookup"><span data-stu-id="dfaed-138">Pixel</span></span> | <span data-ttu-id="dfaed-139">Compute</span><span class="sxs-lookup"><span data-stu-id="dfaed-139">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="dfaed-140">x</span><span class="sxs-lookup"><span data-stu-id="dfaed-140">x</span></span>      |  <span data-ttu-id="dfaed-141">x</span><span class="sxs-lookup"><span data-stu-id="dfaed-141">x</span></span>   | <span data-ttu-id="dfaed-142">x</span><span class="sxs-lookup"><span data-stu-id="dfaed-142">x</span></span>      |  <span data-ttu-id="dfaed-143">x</span><span class="sxs-lookup"><span data-stu-id="dfaed-143">x</span></span>       | <span data-ttu-id="dfaed-144">x</span><span class="sxs-lookup"><span data-stu-id="dfaed-144">x</span></span>     | <span data-ttu-id="dfaed-145">x</span><span class="sxs-lookup"><span data-stu-id="dfaed-145">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="dfaed-146">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="dfaed-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfaed-147">Intrinsische Funktionen</span><span class="sxs-lookup"><span data-stu-id="dfaed-147">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="dfaed-148">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="dfaed-148">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




