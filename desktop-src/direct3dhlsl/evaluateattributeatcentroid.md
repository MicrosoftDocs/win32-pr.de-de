---
title: Evaluateattributeatcentroid-Funktion
description: Wertet am Pixel Schwerpunkt aus.
ms.assetid: 6735b3f4-765f-4cd9-9f38-326a52709021
keywords:
- Evaluateattributeatcentroid-Funktion HLSL
topic_type:
- apiref
api_name:
- EvaluateAttributeAtCentroid
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ee95c7f2f202dfd0065e5e9c30003cc46fd29281
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104389181"
---
# <a name="evaluateattributeatcentroid-function"></a><span data-ttu-id="268e3-104">Evaluateattributeatcentroid-Funktion</span><span class="sxs-lookup"><span data-stu-id="268e3-104">EvaluateAttributeAtCentroid function</span></span>

<span data-ttu-id="268e3-105">Wertet am Pixel Schwerpunkt aus.</span><span class="sxs-lookup"><span data-stu-id="268e3-105">Evaluates at the pixel centroid.</span></span>

## <a name="syntax"></a><span data-ttu-id="268e3-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="268e3-106">Syntax</span></span>

``` syntax
numeric EvaluateAttributeAtCentroid(
  in attrib numeric value
);
```

## <a name="parameters"></a><span data-ttu-id="268e3-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="268e3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="268e3-108">*Wert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="268e3-108">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="268e3-109">Type: **atzb numeric**</span><span class="sxs-lookup"><span data-stu-id="268e3-109">Type: **attrib numeric**</span></span>

<span data-ttu-id="268e3-110">Der Eingabewert.</span><span class="sxs-lookup"><span data-stu-id="268e3-110">The input value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="268e3-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="268e3-111">Remarks</span></span>

<span data-ttu-id="268e3-112">Der Interpolations Modus kann **linear** oder **linear ( \_ keine \_ Perspektive** ) für die Variable sein.</span><span class="sxs-lookup"><span data-stu-id="268e3-112">Interpolation mode can be **linear** or **linear\_no\_perspective** on the variable.</span></span> <span data-ttu-id="268e3-113">Die Verwendung von " **Schwerpunkt** " oder " **Sample** " wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="268e3-113">Use of **centroid** or **sample** is ignored.</span></span> <span data-ttu-id="268e3-114">Attribute mit konstanter Interpolation sind ebenfalls zulässig. in diesem Fall wird der Beispiel Index ignoriert.</span><span class="sxs-lookup"><span data-stu-id="268e3-114">Attributes with constant interpolation are also allowed, in which case the sample index is ignored.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="268e3-115">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="268e3-115">Minimum Shader Model</span></span>

<span data-ttu-id="268e3-116">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="268e3-116">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="268e3-117">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="268e3-117">Shader Model</span></span>                                                                | <span data-ttu-id="268e3-118">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="268e3-118">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="268e3-119">[Shader Model 5](d3d11-graphics-reference-sm5.md) und höhere shadermodelle</span><span class="sxs-lookup"><span data-stu-id="268e3-119">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="268e3-120">ja</span><span class="sxs-lookup"><span data-stu-id="268e3-120">yes</span></span>       |



 

<span data-ttu-id="268e3-121">Diese Funktion wird in den folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="268e3-121">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="268e3-122">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="268e3-122">Vertex</span></span> | <span data-ttu-id="268e3-123">Hülle</span><span class="sxs-lookup"><span data-stu-id="268e3-123">Hull</span></span> | <span data-ttu-id="268e3-124">Domain</span><span class="sxs-lookup"><span data-stu-id="268e3-124">Domain</span></span> | <span data-ttu-id="268e3-125">Geometrie</span><span class="sxs-lookup"><span data-stu-id="268e3-125">Geometry</span></span> | <span data-ttu-id="268e3-126">Pixel</span><span class="sxs-lookup"><span data-stu-id="268e3-126">Pixel</span></span> | <span data-ttu-id="268e3-127">Compute</span><span class="sxs-lookup"><span data-stu-id="268e3-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="268e3-128">x</span><span class="sxs-lookup"><span data-stu-id="268e3-128">x</span></span>     |         |



 

## <a name="see-also"></a><span data-ttu-id="268e3-129">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="268e3-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="268e3-130">Intrinsische Funktionen</span><span class="sxs-lookup"><span data-stu-id="268e3-130">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="268e3-131">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="268e3-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




