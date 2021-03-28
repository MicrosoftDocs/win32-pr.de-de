---
title: ddx_coarse-Funktion
description: Berechnet eine partielle Ableitung mit niedriger Genauigkeit in Bezug auf die x-Koordinate des Bildschirm Raums.
ms.assetid: 5719f45d-b2ae-4916-8f31-c2797b661814
keywords:
- ddx_coarse-Funktion HLSL
topic_type:
- apiref
api_name:
- ddx_coarse
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4f9d4805a1d516a5d8980fcd8209fd6733fe86c4
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104038123"
---
# <a name="ddx_coarse-function"></a><span data-ttu-id="c9a5c-104">grobe DDX- \_ Funktion</span><span class="sxs-lookup"><span data-stu-id="c9a5c-104">ddx\_coarse function</span></span>

<span data-ttu-id="c9a5c-105">Berechnet eine partielle Ableitung mit niedriger Genauigkeit in Bezug auf die x-Koordinate des Bildschirm Raums.</span><span class="sxs-lookup"><span data-stu-id="c9a5c-105">Computes a low precision partial derivative with respect to the screen-space x-coordinate.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9a5c-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="c9a5c-106">Syntax</span></span>

``` syntax
float ddx_coarse(
  in float value
);
```

## <a name="parameters"></a><span data-ttu-id="c9a5c-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="c9a5c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9a5c-108">*Wert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c9a5c-108">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9a5c-109">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="c9a5c-109">Type: **float**</span></span>

<span data-ttu-id="c9a5c-110">Der Eingabewert.</span><span class="sxs-lookup"><span data-stu-id="c9a5c-110">The input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9a5c-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c9a5c-111">Return value</span></span>

<span data-ttu-id="c9a5c-112">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="c9a5c-112">Type: **float**</span></span>

<span data-ttu-id="c9a5c-113">Die partielle Ableitung mit niedriger Genauigkeit des *Werts*.</span><span class="sxs-lookup"><span data-stu-id="c9a5c-113">The low precision partial derivative of *value*.</span></span>

## <a name="remarks"></a><span data-ttu-id="c9a5c-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c9a5c-114">Remarks</span></span>

<span data-ttu-id="c9a5c-115">Außerdem sind die folgenden überladenen Versionen verfügbar:</span><span class="sxs-lookup"><span data-stu-id="c9a5c-115">The following overloaded versions are also available:</span></span>

``` syntax
float2 ddx_coarse(float2 value);
float3 ddx_coarse(float3 value);
float4 ddx_coarse(float4 value);
```

### <a name="minimum-shader-model"></a><span data-ttu-id="c9a5c-116">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="c9a5c-116">Minimum Shader Model</span></span>

<span data-ttu-id="c9a5c-117">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c9a5c-117">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="c9a5c-118">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="c9a5c-118">Shader Model</span></span>                                                                | <span data-ttu-id="c9a5c-119">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="c9a5c-119">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="c9a5c-120">[Shader Model 5](d3d11-graphics-reference-sm5.md) und höhere shadermodelle</span><span class="sxs-lookup"><span data-stu-id="c9a5c-120">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="c9a5c-121">ja</span><span class="sxs-lookup"><span data-stu-id="c9a5c-121">yes</span></span>       |



 

<span data-ttu-id="c9a5c-122">Diese Funktion wird in den folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="c9a5c-122">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="c9a5c-123">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="c9a5c-123">Vertex</span></span> | <span data-ttu-id="c9a5c-124">Hülle</span><span class="sxs-lookup"><span data-stu-id="c9a5c-124">Hull</span></span> | <span data-ttu-id="c9a5c-125">Domain</span><span class="sxs-lookup"><span data-stu-id="c9a5c-125">Domain</span></span> | <span data-ttu-id="c9a5c-126">Geometrie</span><span class="sxs-lookup"><span data-stu-id="c9a5c-126">Geometry</span></span> | <span data-ttu-id="c9a5c-127">Pixel</span><span class="sxs-lookup"><span data-stu-id="c9a5c-127">Pixel</span></span> | <span data-ttu-id="c9a5c-128">Compute</span><span class="sxs-lookup"><span data-stu-id="c9a5c-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="c9a5c-129">x</span><span class="sxs-lookup"><span data-stu-id="c9a5c-129">x</span></span>     |         |



 

## <a name="see-also"></a><span data-ttu-id="c9a5c-130">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c9a5c-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9a5c-131">Intrinsische Funktionen</span><span class="sxs-lookup"><span data-stu-id="c9a5c-131">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="c9a5c-132">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="c9a5c-132">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




