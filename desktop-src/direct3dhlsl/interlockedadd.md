---
title: Interlockedadd-Funktion (HLSL-Referenz)
description: Führt einen garantierten atomaren Wert für das Hinzufügen von Werten zur dest-Ressourcenvariablen aus.
ms.assetid: b3b9cf5c-0da0-4c72-a83f-a0d96f1cac32
keywords:
- Interlockedadd-Funktion HLSL
topic_type:
- apiref
api_name:
- InterlockedAdd
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1d58965ea47fcad8452979a8c8ffe5b289392850
ms.sourcegitcommit: 12e9b14501d51641b690ee0cf764e2b91eb9a140
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/06/2020
ms.locfileid: "104389761"
---
# <a name="interlockedadd-function-hlsl-reference"></a><span data-ttu-id="c416f-104">Interlockedadd-Funktion (HLSL-Referenz)</span><span class="sxs-lookup"><span data-stu-id="c416f-104">InterlockedAdd function (HLSL reference)</span></span>

<span data-ttu-id="c416f-105">Führt einen garantierten atomaren Wert für das Hinzufügen von Werten zur dest-Ressourcenvariablen aus.</span><span class="sxs-lookup"><span data-stu-id="c416f-105">Performs a guaranteed atomic add of value to the dest resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="c416f-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="c416f-106">Syntax</span></span>

``` syntax
void InterlockedAdd(
  in  R dest,
  in  T value,
  out T original_value
);
```

## <a name="parameters"></a><span data-ttu-id="c416f-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="c416f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c416f-108">*dest* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c416f-108">*dest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c416f-109">Typ: **R**</span><span class="sxs-lookup"><span data-stu-id="c416f-109">Type: **R**</span></span>

<span data-ttu-id="c416f-110">Die Zieladresse.</span><span class="sxs-lookup"><span data-stu-id="c416f-110">The destination address.</span></span>

</dd> <dt>

<span data-ttu-id="c416f-111">*Wert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c416f-111">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c416f-112">Typ: **T**</span><span class="sxs-lookup"><span data-stu-id="c416f-112">Type: **T**</span></span>

<span data-ttu-id="c416f-113">Der Eingabewert.</span><span class="sxs-lookup"><span data-stu-id="c416f-113">The input value.</span></span>

</dd> <dt>

<span data-ttu-id="c416f-114">*ursprünglicher \_ Wert* ausgehend \[\]</span><span class="sxs-lookup"><span data-stu-id="c416f-114">*original\_value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c416f-115">Typ: **T**</span><span class="sxs-lookup"><span data-stu-id="c416f-115">Type: **T**</span></span>

<span data-ttu-id="c416f-116">Optional.</span><span class="sxs-lookup"><span data-stu-id="c416f-116">Optional.</span></span> <span data-ttu-id="c416f-117">Der ursprüngliche Eingabe Wert.</span><span class="sxs-lookup"><span data-stu-id="c416f-117">The original input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c416f-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c416f-118">Return value</span></span>

<span data-ttu-id="c416f-119">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="c416f-119">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c416f-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c416f-120">Remarks</span></span>

<span data-ttu-id="c416f-121">Dieser Vorgang kann nur für typisierte int-oder uint-Ressourcen und Shared Memory-Variablen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="c416f-121">This operation can only be performed on int or uint typed resources and shared memory variables.</span></span> <span data-ttu-id="c416f-122">Es gibt zwei Verwendungsmöglichkeiten für diese Funktion.</span><span class="sxs-lookup"><span data-stu-id="c416f-122">There are two possible uses for this function.</span></span> <span data-ttu-id="c416f-123">Der erste ist, wenn R ein Variablentyp für den gemeinsamen Speicher ist.</span><span class="sxs-lookup"><span data-stu-id="c416f-123">The first is when R is a shared memory variable type.</span></span> <span data-ttu-id="c416f-124">In diesem Fall führt die Funktion einen atomaren Add of-Wert für das Shared Memory-Register aus, auf das von dest verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="c416f-124">In this case, the function performs an atomic add of value to the shared memory register referenced by dest.</span></span> <span data-ttu-id="c416f-125">Das zweite Szenario ist, wenn R ein Ressourcen Variablentyp ist.</span><span class="sxs-lookup"><span data-stu-id="c416f-125">The second scenario is when R is a resource variable type.</span></span> <span data-ttu-id="c416f-126">In diesem Szenario führt die Funktion einen atomaren Wert hinzu, der dem Ressourcen Speicherort entspricht, auf den von dest verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="c416f-126">In this scenario, the function performs an atomic add of value to the resource location referenced by dest.</span></span> <span data-ttu-id="c416f-127">Die überladene Funktion verfügt über eine zusätzliche Ausgabevariable, die auf den ursprünglichen Wert von dest festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="c416f-127">The overloaded function has an additional output variable which will be set to the original value of dest.</span></span> <span data-ttu-id="c416f-128">Dieser überladene Vorgang ist nur verfügbar, wenn R lesbar und beschreibbar ist.</span><span class="sxs-lookup"><span data-stu-id="c416f-128">This overloaded operation is only available when R is readable and writable.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="c416f-129">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="c416f-129">Minimum Shader Model</span></span>

<span data-ttu-id="c416f-130">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c416f-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="c416f-131">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="c416f-131">Shader Model</span></span>                                                                | <span data-ttu-id="c416f-132">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="c416f-132">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="c416f-133">[Shader Model 5](d3d11-graphics-reference-sm5.md) und höhere shadermodelle</span><span class="sxs-lookup"><span data-stu-id="c416f-133">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="c416f-134">ja</span><span class="sxs-lookup"><span data-stu-id="c416f-134">yes</span></span>       |



 

<span data-ttu-id="c416f-135">Diese Funktion wird in den folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="c416f-135">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="c416f-136">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="c416f-136">Vertex</span></span> | <span data-ttu-id="c416f-137">Hülle</span><span class="sxs-lookup"><span data-stu-id="c416f-137">Hull</span></span> | <span data-ttu-id="c416f-138">Domain</span><span class="sxs-lookup"><span data-stu-id="c416f-138">Domain</span></span> | <span data-ttu-id="c416f-139">Geometrie</span><span class="sxs-lookup"><span data-stu-id="c416f-139">Geometry</span></span> | <span data-ttu-id="c416f-140">Pixel</span><span class="sxs-lookup"><span data-stu-id="c416f-140">Pixel</span></span> | <span data-ttu-id="c416f-141">Compute</span><span class="sxs-lookup"><span data-stu-id="c416f-141">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="c416f-142">x</span><span class="sxs-lookup"><span data-stu-id="c416f-142">x</span></span>      | <span data-ttu-id="c416f-143">x</span><span class="sxs-lookup"><span data-stu-id="c416f-143">x</span></span>    | <span data-ttu-id="c416f-144">x</span><span class="sxs-lookup"><span data-stu-id="c416f-144">x</span></span>      | <span data-ttu-id="c416f-145">x</span><span class="sxs-lookup"><span data-stu-id="c416f-145">x</span></span>        | <span data-ttu-id="c416f-146">x</span><span class="sxs-lookup"><span data-stu-id="c416f-146">x</span></span>     | <span data-ttu-id="c416f-147">x</span><span class="sxs-lookup"><span data-stu-id="c416f-147">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="c416f-148">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c416f-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c416f-149">Intrinsische Funktionen</span><span class="sxs-lookup"><span data-stu-id="c416f-149">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="c416f-150">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="c416f-150">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




