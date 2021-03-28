---
title: ddy_coarse-Funktion
description: Berechnet eine partielle Ableitung mit niedriger Genauigkeit in Bezug auf die y-Koordinate für den Bildschirmbereich.
ms.assetid: f6103cd3-f7ee-41c2-b3cf-9e72ca84b25e
keywords:
- ddy_coarse-Funktion HLSL
topic_type:
- apiref
api_name:
- ddy_coarse
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b6fef330e919a31e39306742bb03280454d47626
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104038122"
---
# <a name="ddy_coarse-function"></a><span data-ttu-id="d79f8-104">rauen \_ grobe Funktion</span><span class="sxs-lookup"><span data-stu-id="d79f8-104">ddy\_coarse function</span></span>

<span data-ttu-id="d79f8-105">Berechnet eine partielle Ableitung mit niedriger Genauigkeit in Bezug auf die y-Koordinate für den Bildschirmbereich.</span><span class="sxs-lookup"><span data-stu-id="d79f8-105">Computes a low precision partial derivative with respect to the screen-space y-coordinate.</span></span>

## <a name="syntax"></a><span data-ttu-id="d79f8-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="d79f8-106">Syntax</span></span>

``` syntax
float ddy_coarse(
  in float value
);
```

## <a name="parameters"></a><span data-ttu-id="d79f8-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="d79f8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d79f8-108">*Wert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d79f8-108">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d79f8-109">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="d79f8-109">Type: **float**</span></span>

<span data-ttu-id="d79f8-110">Der Eingabewert.</span><span class="sxs-lookup"><span data-stu-id="d79f8-110">The input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d79f8-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d79f8-111">Return value</span></span>

<span data-ttu-id="d79f8-112">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="d79f8-112">Type: **float**</span></span>

<span data-ttu-id="d79f8-113">Die partielle Ableitung mit niedriger Genauigkeit des *Werts*.</span><span class="sxs-lookup"><span data-stu-id="d79f8-113">The low precision partial derivative of *value*.</span></span>

## <a name="remarks"></a><span data-ttu-id="d79f8-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d79f8-114">Remarks</span></span>

<span data-ttu-id="d79f8-115">Außerdem sind die folgenden überladenen Versionen verfügbar:</span><span class="sxs-lookup"><span data-stu-id="d79f8-115">The following overloaded versions are also available:</span></span>

``` syntax
float2 ddy_coarse(float2 value);
float3 ddy_coarse(float3 value);
float4 ddy_coarse(float4 value);
```

### <a name="minimum-shader-model"></a><span data-ttu-id="d79f8-116">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="d79f8-116">Minimum Shader Model</span></span>

<span data-ttu-id="d79f8-117">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d79f8-117">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="d79f8-118">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="d79f8-118">Shader Model</span></span>                                                                | <span data-ttu-id="d79f8-119">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="d79f8-119">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="d79f8-120">[Shader Model 5](d3d11-graphics-reference-sm5.md) und höhere shadermodelle</span><span class="sxs-lookup"><span data-stu-id="d79f8-120">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="d79f8-121">ja</span><span class="sxs-lookup"><span data-stu-id="d79f8-121">yes</span></span>       |



 

<span data-ttu-id="d79f8-122">Diese Funktion wird in den folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="d79f8-122">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="d79f8-123">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="d79f8-123">Vertex</span></span> | <span data-ttu-id="d79f8-124">Hülle</span><span class="sxs-lookup"><span data-stu-id="d79f8-124">Hull</span></span> | <span data-ttu-id="d79f8-125">Domain</span><span class="sxs-lookup"><span data-stu-id="d79f8-125">Domain</span></span> | <span data-ttu-id="d79f8-126">Geometrie</span><span class="sxs-lookup"><span data-stu-id="d79f8-126">Geometry</span></span> | <span data-ttu-id="d79f8-127">Pixel</span><span class="sxs-lookup"><span data-stu-id="d79f8-127">Pixel</span></span> | <span data-ttu-id="d79f8-128">Compute</span><span class="sxs-lookup"><span data-stu-id="d79f8-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="d79f8-129">x</span><span class="sxs-lookup"><span data-stu-id="d79f8-129">x</span></span>     |         |



 

## <a name="see-also"></a><span data-ttu-id="d79f8-130">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d79f8-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d79f8-131">Intrinsische Funktionen</span><span class="sxs-lookup"><span data-stu-id="d79f8-131">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="d79f8-132">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="d79f8-132">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




