---
title: mad-Funktion
description: Führt eine arithmetische Multiplikation/Add-Operation für drei Werte aus.
ms.assetid: 2e58229d-2387-4319-adc6-2d66eda88bd1
keywords:
- Mad-Funktion HLSL
topic_type:
- apiref
api_name:
- mad
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 208b1bbc87c430ca5a58a70fb3c86f9edae762bf
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104472005"
---
# <a name="mad-function"></a><span data-ttu-id="c8282-104">mad-Funktion</span><span class="sxs-lookup"><span data-stu-id="c8282-104">mad function</span></span>

<span data-ttu-id="c8282-105">Führt eine arithmetische Multiplikation/Add-Operation für drei Werte aus.</span><span class="sxs-lookup"><span data-stu-id="c8282-105">Performs an arithmetic multiply/add operation on three values.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8282-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="c8282-106">Syntax</span></span>

``` syntax
numeric mad(
  in numeric mvalue,
  in numeric avalue,
  in numeric bvalue
);
```

## <a name="parameters"></a><span data-ttu-id="c8282-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="c8282-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8282-108">*mValue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c8282-108">*mvalue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8282-109">Typ: **numerisch**</span><span class="sxs-lookup"><span data-stu-id="c8282-109">Type: **numeric**</span></span>

<span data-ttu-id="c8282-110">Der Multiplikations Wert.</span><span class="sxs-lookup"><span data-stu-id="c8282-110">The multiplication value.</span></span>

</dd> <dt>

<span data-ttu-id="c8282-111">*verfügbar* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c8282-111">*avalue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8282-112">Typ: **numerisch**</span><span class="sxs-lookup"><span data-stu-id="c8282-112">Type: **numeric**</span></span>

<span data-ttu-id="c8282-113">Der erste Additions Wert.</span><span class="sxs-lookup"><span data-stu-id="c8282-113">The first addition value.</span></span>

</dd> <dt>

<span data-ttu-id="c8282-114">*bvalue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c8282-114">*bvalue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8282-115">Typ: **numerisch**</span><span class="sxs-lookup"><span data-stu-id="c8282-115">Type: **numeric**</span></span>

<span data-ttu-id="c8282-116">Der zweite Additions Wert.</span><span class="sxs-lookup"><span data-stu-id="c8282-116">The second addition value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8282-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c8282-117">Return value</span></span>

<span data-ttu-id="c8282-118">Typ: **numerisch**</span><span class="sxs-lookup"><span data-stu-id="c8282-118">Type: **numeric**</span></span>

<span data-ttu-id="c8282-119">Das Ergebnis des *mValue* -Werts für den \*   +  *bvalue*.</span><span class="sxs-lookup"><span data-stu-id="c8282-119">The result of *mvalue* \* *avalue* + *bvalue*.</span></span>

## <a name="remarks"></a><span data-ttu-id="c8282-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c8282-120">Remarks</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="c8282-121">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="c8282-121">Minimum Shader Model</span></span>

<span data-ttu-id="c8282-122">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c8282-122">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="c8282-123">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="c8282-123">Shader Model</span></span>                                                                | <span data-ttu-id="c8282-124">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="c8282-124">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="c8282-125">[Shader Model 5](d3d11-graphics-reference-sm5.md) und höhere shadermodelle</span><span class="sxs-lookup"><span data-stu-id="c8282-125">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="c8282-126">ja</span><span class="sxs-lookup"><span data-stu-id="c8282-126">yes</span></span>       |



 

<span data-ttu-id="c8282-127">Diese Funktion wird in den folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="c8282-127">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="c8282-128">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="c8282-128">Vertex</span></span> | <span data-ttu-id="c8282-129">Hülle</span><span class="sxs-lookup"><span data-stu-id="c8282-129">Hull</span></span> | <span data-ttu-id="c8282-130">Domain</span><span class="sxs-lookup"><span data-stu-id="c8282-130">Domain</span></span> | <span data-ttu-id="c8282-131">Geometrie</span><span class="sxs-lookup"><span data-stu-id="c8282-131">Geometry</span></span> | <span data-ttu-id="c8282-132">Pixel</span><span class="sxs-lookup"><span data-stu-id="c8282-132">Pixel</span></span> | <span data-ttu-id="c8282-133">Compute</span><span class="sxs-lookup"><span data-stu-id="c8282-133">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="c8282-134">x</span><span class="sxs-lookup"><span data-stu-id="c8282-134">x</span></span>      | <span data-ttu-id="c8282-135">x</span><span class="sxs-lookup"><span data-stu-id="c8282-135">x</span></span>    | <span data-ttu-id="c8282-136">x</span><span class="sxs-lookup"><span data-stu-id="c8282-136">x</span></span>      | <span data-ttu-id="c8282-137">x</span><span class="sxs-lookup"><span data-stu-id="c8282-137">x</span></span>        | <span data-ttu-id="c8282-138">x</span><span class="sxs-lookup"><span data-stu-id="c8282-138">x</span></span>     | <span data-ttu-id="c8282-139">x</span><span class="sxs-lookup"><span data-stu-id="c8282-139">x</span></span>       |



 

<span data-ttu-id="c8282-140">Shaderautoren können **die Mad-Hardware Anweisung** in der kompilierten Shader-Ausgabe mit dem **Mad** instrauc explizit als Ziel verwenden. Dies ist besonders nützlich für Shader, die Ergebnisse mit dem Schlüsselwort " [präzise](dx-graphics-hlsl-appendix-keywords.md) " markieren.</span><span class="sxs-lookup"><span data-stu-id="c8282-140">Shader authors can use the **mad** instrinsic to explicitly target the **mad** hardware instruction in the compiled shader output, which is particularly useful with shaders that mark results with the [precise](dx-graphics-hlsl-appendix-keywords.md) keyword.</span></span> <span data-ttu-id="c8282-141">Die **Mad** -Anweisung kann in Hardware als "Fused" implementiert werden, was eine höhere Genauigkeit als die Implementierung einer **mul** -Anweisung, gefolgt von einer **Add** -Anweisung oder als **mul**-  +  **Add**, bietet.</span><span class="sxs-lookup"><span data-stu-id="c8282-141">The **mad** instruction can be implemented in hardware as either "fused," which offers higher precision than implementing a **mul** instruction followed by an **add** instruction, or as a **mul** + **add**.</span></span>

<span data-ttu-id="c8282-142">Wenn shaderautoren den **Mad** instrauc verwenden, um ein Ergebnis zu berechnen, das der Shader als genau gekennzeichnet hat, geben Sie der Hardware an, dass eine beliebige gültige Implementierung der **Mad** -Anweisung verwendet werden soll ("Fused" oder "Not"), solange die Implementierung für alle Verwendungen dieses **verrückten** in jedem Shader auf dieser Hardware konsistent ist.</span><span class="sxs-lookup"><span data-stu-id="c8282-142">If shader authors use the **mad** instrinsic to calculate a result that the shader marked as precise, they indicate to the hardware to use any valid implementation of the **mad** instruction (fused or not) as long as the implementation is consistent for all uses of that **mad** intrinsic in any shader on that hardware.</span></span> <span data-ttu-id="c8282-143">Shader können dann potenzielle Leistungsverbesserungen nutzen, indem Sie eine native **Mad** -Anweisung (im Gegensatz zu **mul**  +  **Add**) auf Hardware anwenden.</span><span class="sxs-lookup"><span data-stu-id="c8282-143">Shaders can then take advantage of potential performance improvements by using a native **mad** instruction (versus **mul** + **add**) on some hardware.</span></span> <span data-ttu-id="c8282-144">Das Ergebnis der Ausführung einer systemeigenen **Mad** -Hardware Anweisung unterscheidet sich möglicherweise von der Durchführung einer **mul** , gefolgt von einem **Add**-in.</span><span class="sxs-lookup"><span data-stu-id="c8282-144">The result of performing a native **mad** hardware instruction might or might not be different than performing a **mul** followed by an **add**.</span></span> <span data-ttu-id="c8282-145">Allerdings muss das Ergebnis, was das Ergebnis ist, konsistent sein, damit derselbe Vorgang in mehreren Shader oder unterschiedlichen Teilen eines Shader erfolgt.</span><span class="sxs-lookup"><span data-stu-id="c8282-145">However, whatever the result is, the result must be consistent for the same operation to occur in multiple shaders or different parts of a shader.</span></span>

## <a name="see-also"></a><span data-ttu-id="c8282-146">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c8282-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8282-147">Intrinsische Funktionen</span><span class="sxs-lookup"><span data-stu-id="c8282-147">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="c8282-148">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="c8282-148">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




