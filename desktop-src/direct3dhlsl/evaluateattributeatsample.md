---
title: Evaluateattributeatsample-Funktion
description: Wertet an der indizierten Stichproben Position aus.
ms.assetid: b5886004-5960-461d-a0d2-f4c3b0d09d94
keywords:
- Evaluateattributeatsample-Funktion HLSL
topic_type:
- apiref
api_name:
- EvaluateAttributeAtSample
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b183f86599d08a6892e33c169b938dc09a2b55de
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718143"
---
# <a name="evaluateattributeatsample-function"></a><span data-ttu-id="6c0fb-104">Evaluateattributeatsample-Funktion</span><span class="sxs-lookup"><span data-stu-id="6c0fb-104">EvaluateAttributeAtSample function</span></span>

<span data-ttu-id="6c0fb-105">Wertet an der indizierten Stichproben Position aus.</span><span class="sxs-lookup"><span data-stu-id="6c0fb-105">Evaluates at the indexed sample location.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c0fb-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="6c0fb-106">Syntax</span></span>

``` syntax
numeric EvaluateAttributeAtSample(
  in attrib numeric value,
  in uint sampleindex
);
```

## <a name="parameters"></a><span data-ttu-id="6c0fb-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="6c0fb-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c0fb-108">*Wert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6c0fb-108">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c0fb-109">Type: **atzb numeric**</span><span class="sxs-lookup"><span data-stu-id="6c0fb-109">Type: **attrib numeric**</span></span>

<span data-ttu-id="6c0fb-110">Der Eingabewert.</span><span class="sxs-lookup"><span data-stu-id="6c0fb-110">The input value.</span></span>

</dd> <dt>

<span data-ttu-id="6c0fb-111">*sampleingedex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6c0fb-111">*sampleindex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c0fb-112">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="6c0fb-112">Type: **uint**</span></span>

<span data-ttu-id="6c0fb-113">Der Beispiel Speicherort.</span><span class="sxs-lookup"><span data-stu-id="6c0fb-113">The sample location.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6c0fb-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6c0fb-114">Remarks</span></span>

<span data-ttu-id="6c0fb-115">Der Interpolations Modus kann **linear** oder **linear ( \_ keine \_ Perspektive** ) für die Variable sein.</span><span class="sxs-lookup"><span data-stu-id="6c0fb-115">Interpolation mode can be **linear** or **linear\_no\_perspective** on the variable.</span></span> <span data-ttu-id="6c0fb-116">Die Verwendung von " **Schwerpunkt** " oder " **Sample** " wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="6c0fb-116">Use of **centroid** or **sample** is ignored.</span></span> <span data-ttu-id="6c0fb-117">Attribute mit konstanter Interpolation sind ebenfalls zulässig. in diesem Fall wird der Beispiel Index ignoriert.</span><span class="sxs-lookup"><span data-stu-id="6c0fb-117">Attributes with constant interpolation are also allowed, in which case the sample index is ignored.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="6c0fb-118">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="6c0fb-118">Minimum Shader Model</span></span>

<span data-ttu-id="6c0fb-119">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6c0fb-119">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="6c0fb-120">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="6c0fb-120">Shader Model</span></span>                                                                | <span data-ttu-id="6c0fb-121">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="6c0fb-121">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="6c0fb-122">[Shader Model 5](d3d11-graphics-reference-sm5.md) und höhere shadermodelle</span><span class="sxs-lookup"><span data-stu-id="6c0fb-122">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="6c0fb-123">ja</span><span class="sxs-lookup"><span data-stu-id="6c0fb-123">yes</span></span>       |



 

<span data-ttu-id="6c0fb-124">Diese Funktion wird in den folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="6c0fb-124">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="6c0fb-125">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="6c0fb-125">Vertex</span></span> | <span data-ttu-id="6c0fb-126">Hülle</span><span class="sxs-lookup"><span data-stu-id="6c0fb-126">Hull</span></span> | <span data-ttu-id="6c0fb-127">Domain</span><span class="sxs-lookup"><span data-stu-id="6c0fb-127">Domain</span></span> | <span data-ttu-id="6c0fb-128">Geometrie</span><span class="sxs-lookup"><span data-stu-id="6c0fb-128">Geometry</span></span> | <span data-ttu-id="6c0fb-129">Pixel</span><span class="sxs-lookup"><span data-stu-id="6c0fb-129">Pixel</span></span> | <span data-ttu-id="6c0fb-130">Compute</span><span class="sxs-lookup"><span data-stu-id="6c0fb-130">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="6c0fb-131">x</span><span class="sxs-lookup"><span data-stu-id="6c0fb-131">x</span></span>     |         |



 

## <a name="see-also"></a><span data-ttu-id="6c0fb-132">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="6c0fb-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c0fb-133">Intrinsische Funktionen</span><span class="sxs-lookup"><span data-stu-id="6c0fb-133">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="6c0fb-134">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="6c0fb-134">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




