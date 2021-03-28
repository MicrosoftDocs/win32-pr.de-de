---
title: Interlockedcomparestore-Funktion (HLSL-Referenz)
description: Vergleicht atomisch das Ziel mit dem Vergleichswert. Wenn Sie identisch sind, wird das Ziel mit dem Eingabe Wert überschrieben.
ms.assetid: eaf7e669-5240-40c9-9840-f4e7916e51b4
keywords:
- Interlockedcomparestore-Funktion HLSL
topic_type:
- apiref
api_name:
- InterlockedCompareStore
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: df3ffb51bbe8fe8150d19a390e62640e64ded5c9
ms.sourcegitcommit: 12e9b14501d51641b690ee0cf764e2b91eb9a140
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/06/2020
ms.locfileid: "104389765"
---
# <a name="interlockedcomparestore-function-hlsl-reference"></a><span data-ttu-id="cdde3-105">Interlockedcomparestore-Funktion (HLSL-Referenz)</span><span class="sxs-lookup"><span data-stu-id="cdde3-105">InterlockedCompareStore function (HLSL reference)</span></span>

<span data-ttu-id="cdde3-106">Vergleicht atomisch das Ziel mit dem Vergleichswert.</span><span class="sxs-lookup"><span data-stu-id="cdde3-106">Atomically compares the destination to the comparison value.</span></span> <span data-ttu-id="cdde3-107">Wenn Sie identisch sind, wird das Ziel mit dem Eingabe Wert überschrieben.</span><span class="sxs-lookup"><span data-stu-id="cdde3-107">If they are identical, the destination is overwritten with the input value.</span></span>

## <a name="syntax"></a><span data-ttu-id="cdde3-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="cdde3-108">Syntax</span></span>

``` syntax
void InterlockedCompareStore(
  in R dest,
  in T compare_value,
  in T value
);
```

## <a name="parameters"></a><span data-ttu-id="cdde3-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="cdde3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cdde3-110">*dest* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cdde3-110">*dest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cdde3-111">Typ: **R**</span><span class="sxs-lookup"><span data-stu-id="cdde3-111">Type: **R**</span></span>

<span data-ttu-id="cdde3-112">Die Zieladresse.</span><span class="sxs-lookup"><span data-stu-id="cdde3-112">The destination address.</span></span>

</dd> <dt>

<span data-ttu-id="cdde3-113">*\_ Wert vergleichen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cdde3-113">*compare\_value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cdde3-114">Typ: **T**</span><span class="sxs-lookup"><span data-stu-id="cdde3-114">Type: **T**</span></span>

<span data-ttu-id="cdde3-115">Der Vergleichswert.</span><span class="sxs-lookup"><span data-stu-id="cdde3-115">The comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="cdde3-116">*Wert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cdde3-116">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cdde3-117">Typ: **T**</span><span class="sxs-lookup"><span data-stu-id="cdde3-117">Type: **T**</span></span>

<span data-ttu-id="cdde3-118">Der Eingabewert.</span><span class="sxs-lookup"><span data-stu-id="cdde3-118">The input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cdde3-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cdde3-119">Return value</span></span>

<span data-ttu-id="cdde3-120">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="cdde3-120">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cdde3-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cdde3-121">Remarks</span></span>

<span data-ttu-id="cdde3-122">Vergleicht atomarisch den Wert, auf den mit dem " *dest* " *verwiesen wird,* mit dem Wert "Wert vergleichen" und speichert den *Wert* in dem Speicherort, auf den *\_*</span><span class="sxs-lookup"><span data-stu-id="cdde3-122">Atomically compares the value referenced by *dest* with *compare\_value* and stores *value* in the location referenced by *dest* if the values match.</span></span> <span data-ttu-id="cdde3-123">Dieser Vorgang kann nur für typisierte **int** -oder **uint** -Ressourcen und Shared Memory-Variablen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="cdde3-123">This operation can only be performed on **int** or **uint** typed resources and shared memory variables.</span></span> <span data-ttu-id="cdde3-124">Es gibt zwei Verwendungsmöglichkeiten für diese Funktion.</span><span class="sxs-lookup"><span data-stu-id="cdde3-124">There are two possible uses for this function.</span></span> <span data-ttu-id="cdde3-125">Der erste ist, wenn R ein Variablentyp für den gemeinsamen Speicher ist.</span><span class="sxs-lookup"><span data-stu-id="cdde3-125">The first is when R is a shared memory variable type.</span></span> <span data-ttu-id="cdde3-126">In diesem Fall führt die Funktion den Vorgang für das Shared Memory-Register aus, auf das von *dest* verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="cdde3-126">In this case, the function performs the operation on the shared memory register referenced by *dest*.</span></span> <span data-ttu-id="cdde3-127">Das zweite Szenario ist, wenn R ein Ressourcen Variablentyp ist.</span><span class="sxs-lookup"><span data-stu-id="cdde3-127">The second scenario is when R is a resource variable type.</span></span> <span data-ttu-id="cdde3-128">In diesem Szenario führt die Funktion den Vorgang an dem Ressourcen Speicherort aus, auf den " *dest*" verweist.</span><span class="sxs-lookup"><span data-stu-id="cdde3-128">In this scenario, the function performs the operation on the resource location referenced by *dest*.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="cdde3-129">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="cdde3-129">Minimum Shader Model</span></span>

<span data-ttu-id="cdde3-130">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="cdde3-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="cdde3-131">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="cdde3-131">Shader Model</span></span>                                                                | <span data-ttu-id="cdde3-132">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="cdde3-132">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="cdde3-133">[Shader Model 5](d3d11-graphics-reference-sm5.md) und höhere shadermodelle</span><span class="sxs-lookup"><span data-stu-id="cdde3-133">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="cdde3-134">ja</span><span class="sxs-lookup"><span data-stu-id="cdde3-134">yes</span></span>       |



 

<span data-ttu-id="cdde3-135">Diese Funktion wird in den folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="cdde3-135">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="cdde3-136">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="cdde3-136">Vertex</span></span> | <span data-ttu-id="cdde3-137">Hülle</span><span class="sxs-lookup"><span data-stu-id="cdde3-137">Hull</span></span> | <span data-ttu-id="cdde3-138">Domain</span><span class="sxs-lookup"><span data-stu-id="cdde3-138">Domain</span></span> | <span data-ttu-id="cdde3-139">Geometrie</span><span class="sxs-lookup"><span data-stu-id="cdde3-139">Geometry</span></span> | <span data-ttu-id="cdde3-140">Pixel</span><span class="sxs-lookup"><span data-stu-id="cdde3-140">Pixel</span></span> | <span data-ttu-id="cdde3-141">Compute</span><span class="sxs-lookup"><span data-stu-id="cdde3-141">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|  <span data-ttu-id="cdde3-142">x</span><span class="sxs-lookup"><span data-stu-id="cdde3-142">x</span></span>     | <span data-ttu-id="cdde3-143">x</span><span class="sxs-lookup"><span data-stu-id="cdde3-143">x</span></span>    |  <span data-ttu-id="cdde3-144">x</span><span class="sxs-lookup"><span data-stu-id="cdde3-144">x</span></span>     |  <span data-ttu-id="cdde3-145">x</span><span class="sxs-lookup"><span data-stu-id="cdde3-145">x</span></span>       | <span data-ttu-id="cdde3-146">x</span><span class="sxs-lookup"><span data-stu-id="cdde3-146">x</span></span>     | <span data-ttu-id="cdde3-147">x</span><span class="sxs-lookup"><span data-stu-id="cdde3-147">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="cdde3-148">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="cdde3-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cdde3-149">Intrinsische Funktionen</span><span class="sxs-lookup"><span data-stu-id="cdde3-149">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="cdde3-150">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="cdde3-150">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




