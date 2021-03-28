---
title: Interlockedcompareexchange-Funktion (HLSL-Referenz)
description: Vergleicht atomisch das Ziel mit dem Vergleichswert. Wenn Sie identisch sind, wird das Ziel mit dem Eingabe Wert überschrieben. Der ursprüngliche Wert wird auf den ursprünglichen Wert des Ziels festgelegt.
ms.assetid: 85d1ba58-8e79-41cd-abd6-7ffff59839c7
keywords:
- Interlockedcompareexchange-Funktion HLSL
topic_type:
- apiref
api_name:
- InterlockedCompareExchange
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 74bc189996752d754599bf4547e8baa4d9fb74cc
ms.sourcegitcommit: 12e9b14501d51641b690ee0cf764e2b91eb9a140
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/06/2020
ms.locfileid: "104993318"
---
# <a name="interlockedcompareexchange-function-hlsl-reference"></a><span data-ttu-id="343d2-106">Interlockedcompareexchange-Funktion (HLSL-Referenz)</span><span class="sxs-lookup"><span data-stu-id="343d2-106">InterlockedCompareExchange function (HLSL reference)</span></span>

<span data-ttu-id="343d2-107">Vergleicht atomisch das Ziel mit dem Vergleichswert.</span><span class="sxs-lookup"><span data-stu-id="343d2-107">Atomically compares the destination with the comparison value.</span></span> <span data-ttu-id="343d2-108">Wenn Sie identisch sind, wird das Ziel mit dem Eingabe Wert überschrieben.</span><span class="sxs-lookup"><span data-stu-id="343d2-108">If they are identical, the destination is overwritten with the input value.</span></span> <span data-ttu-id="343d2-109">Der ursprüngliche Wert wird auf den ursprünglichen Wert des Ziels festgelegt.</span><span class="sxs-lookup"><span data-stu-id="343d2-109">The original value is set to the destination's original value.</span></span>

## <a name="syntax"></a><span data-ttu-id="343d2-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="343d2-110">Syntax</span></span>

``` syntax
void InterlockedCompareExchange(
  in  R dest,
  in  T compare_value,
  in  T value,
  out T original_value
);
```

## <a name="parameters"></a><span data-ttu-id="343d2-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="343d2-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="343d2-112">*dest* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="343d2-112">*dest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="343d2-113">Typ: **R**</span><span class="sxs-lookup"><span data-stu-id="343d2-113">Type: **R**</span></span>

<span data-ttu-id="343d2-114">Die Zieladresse.</span><span class="sxs-lookup"><span data-stu-id="343d2-114">The destination address.</span></span>

</dd> <dt>

<span data-ttu-id="343d2-115">*\_ Wert vergleichen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="343d2-115">*compare\_value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="343d2-116">Typ: **T**</span><span class="sxs-lookup"><span data-stu-id="343d2-116">Type: **T**</span></span>

<span data-ttu-id="343d2-117">Der Vergleichswert.</span><span class="sxs-lookup"><span data-stu-id="343d2-117">The comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="343d2-118">*Wert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="343d2-118">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="343d2-119">Typ: **T**</span><span class="sxs-lookup"><span data-stu-id="343d2-119">Type: **T**</span></span>

<span data-ttu-id="343d2-120">Der Eingabewert.</span><span class="sxs-lookup"><span data-stu-id="343d2-120">The input value.</span></span>

</dd> <dt>

<span data-ttu-id="343d2-121">*ursprünglicher \_ Wert* ausgehend \[\]</span><span class="sxs-lookup"><span data-stu-id="343d2-121">*original\_value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="343d2-122">Typ: **T**</span><span class="sxs-lookup"><span data-stu-id="343d2-122">Type: **T**</span></span>

<span data-ttu-id="343d2-123">Der ursprüngliche Wert.</span><span class="sxs-lookup"><span data-stu-id="343d2-123">The original value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="343d2-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="343d2-124">Return value</span></span>

<span data-ttu-id="343d2-125">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="343d2-125">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="343d2-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="343d2-126">Remarks</span></span>

<span data-ttu-id="343d2-127">Vergleicht atomarisch den Wert *, auf den* mit dem Wert " *dest* " verwiesen wird, mit einem *Vergleichs \_ Wert*, speichert den *Wert* an dem Speicherort *, auf den " \_* *dest* " verweist, wenn die Werte entsprechen</span><span class="sxs-lookup"><span data-stu-id="343d2-127">Atomically compares the value referenced by *dest* with *compare\_value*, stores *value* in the location referenced by *dest* if the values match, returns the original value of *dest* in *original\_value*.</span></span> <span data-ttu-id="343d2-128">Dieser Vorgang kann nur für typisierte **int** -oder **uint** -Ressourcen und Shared Memory-Variablen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="343d2-128">This operation can only be performed on **int** or **uint** typed resources and shared memory variables.</span></span> <span data-ttu-id="343d2-129">Es gibt zwei Verwendungsmöglichkeiten für diese Funktion.</span><span class="sxs-lookup"><span data-stu-id="343d2-129">There are two possible uses for this function.</span></span> <span data-ttu-id="343d2-130">Der erste ist, wenn R ein Variablentyp für den gemeinsamen Speicher ist.</span><span class="sxs-lookup"><span data-stu-id="343d2-130">The first is when R is a shared memory variable type.</span></span> <span data-ttu-id="343d2-131">In diesem Fall führt die Funktion den Vorgang für das Shared Memory-Register aus, auf das von *dest* verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="343d2-131">In this case, the function performs the operation on the shared memory register referenced by *dest*.</span></span> <span data-ttu-id="343d2-132">Das zweite Szenario ist, wenn R ein Ressourcen Variablentyp ist.</span><span class="sxs-lookup"><span data-stu-id="343d2-132">The second scenario is when R is a resource variable type.</span></span> <span data-ttu-id="343d2-133">In diesem Szenario führt die Funktion den Vorgang an dem Ressourcen Speicherort aus, auf den " *dest*" verweist.</span><span class="sxs-lookup"><span data-stu-id="343d2-133">In this scenario, the function performs the operation on the resource location referenced by *dest*.</span></span> <span data-ttu-id="343d2-134">Dieser Vorgang ist nur verfügbar, wenn R lesbar und beschreibbar ist.</span><span class="sxs-lookup"><span data-stu-id="343d2-134">This operation is only available when R is readable and writable.</span></span>

> [!Note]  
> <span data-ttu-id="343d2-135">Wenn Sie in einer [**for**](dx-graphics-hlsl-for.md) -oder [**while**](dx-graphics-hlsl-while.md) -Compute-Shader-Schleife **interlockedcompareexchange** aufrufen, müssen Sie für die ordnungsgemäße Kompilierung das Attribut " **\[ \_ UAV- \_ \] Bedingung zulassen** " in dieser Schleife verwenden.</span><span class="sxs-lookup"><span data-stu-id="343d2-135">If you call **InterlockedCompareExchange** in a [**for**](dx-graphics-hlsl-for.md) or [**while**](dx-graphics-hlsl-while.md) compute shader loop, to properly compile, you must use the **\[allow\_uav\_condition\]** attribute on that loop.</span></span>

 

### <a name="minimum-shader-model"></a><span data-ttu-id="343d2-136">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="343d2-136">Minimum Shader Model</span></span>

<span data-ttu-id="343d2-137">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="343d2-137">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="343d2-138">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="343d2-138">Shader Model</span></span>                                                                | <span data-ttu-id="343d2-139">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="343d2-139">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="343d2-140">[Shader Model 5](d3d11-graphics-reference-sm5.md) und höhere shadermodelle</span><span class="sxs-lookup"><span data-stu-id="343d2-140">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="343d2-141">ja</span><span class="sxs-lookup"><span data-stu-id="343d2-141">yes</span></span>       |



 

<span data-ttu-id="343d2-142">Diese Funktion wird in den folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="343d2-142">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="343d2-143">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="343d2-143">Vertex</span></span> | <span data-ttu-id="343d2-144">Hülle</span><span class="sxs-lookup"><span data-stu-id="343d2-144">Hull</span></span> | <span data-ttu-id="343d2-145">Domain</span><span class="sxs-lookup"><span data-stu-id="343d2-145">Domain</span></span> | <span data-ttu-id="343d2-146">Geometrie</span><span class="sxs-lookup"><span data-stu-id="343d2-146">Geometry</span></span> | <span data-ttu-id="343d2-147">Pixel</span><span class="sxs-lookup"><span data-stu-id="343d2-147">Pixel</span></span> | <span data-ttu-id="343d2-148">Compute</span><span class="sxs-lookup"><span data-stu-id="343d2-148">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="343d2-149">x</span><span class="sxs-lookup"><span data-stu-id="343d2-149">x</span></span>      |  <span data-ttu-id="343d2-150">x</span><span class="sxs-lookup"><span data-stu-id="343d2-150">x</span></span>   |  <span data-ttu-id="343d2-151">x</span><span class="sxs-lookup"><span data-stu-id="343d2-151">x</span></span>     |  <span data-ttu-id="343d2-152">x</span><span class="sxs-lookup"><span data-stu-id="343d2-152">x</span></span>       | <span data-ttu-id="343d2-153">x</span><span class="sxs-lookup"><span data-stu-id="343d2-153">x</span></span>     | <span data-ttu-id="343d2-154">x</span><span class="sxs-lookup"><span data-stu-id="343d2-154">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="343d2-155">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="343d2-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="343d2-156">Intrinsische Funktionen</span><span class="sxs-lookup"><span data-stu-id="343d2-156">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="343d2-157">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="343d2-157">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




