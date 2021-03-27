---
title: ddx_fine-Funktion
description: Berechnet eine partielle Ableitung mit hoher Genauigkeit in Bezug auf die x-Koordinate des Bildschirm Raums. | ddx_fine-Funktion
ms.assetid: 41062d6f-2b7f-4594-a6de-da37ded5d444
keywords:
- ddx_fine-Funktion HLSL
topic_type:
- apiref
api_name:
- ddx_fine
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c1a579ba5899cf4d3ac3f25ef5a40337f6291977
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104982083"
---
# <a name="ddx_fine-function"></a><span data-ttu-id="14d4a-105">DDX- \_ Funktion (fein)</span><span class="sxs-lookup"><span data-stu-id="14d4a-105">ddx\_fine function</span></span>

<span data-ttu-id="14d4a-106">Berechnet eine partielle Ableitung mit hoher Genauigkeit in Bezug auf die x-Koordinate des Bildschirm Raums.</span><span class="sxs-lookup"><span data-stu-id="14d4a-106">Computes a high precision partial derivative with respect to the screen-space x-coordinate.</span></span>

## <a name="syntax"></a><span data-ttu-id="14d4a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="14d4a-107">Syntax</span></span>

``` syntax
float ddx_fine(
  in float value
);
```

## <a name="parameters"></a><span data-ttu-id="14d4a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="14d4a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14d4a-109">*Wert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="14d4a-109">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14d4a-110">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="14d4a-110">Type: **float**</span></span>

<span data-ttu-id="14d4a-111">Der Eingabewert.</span><span class="sxs-lookup"><span data-stu-id="14d4a-111">The input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14d4a-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="14d4a-112">Return value</span></span>

<span data-ttu-id="14d4a-113">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="14d4a-113">Type: **float**</span></span>

<span data-ttu-id="14d4a-114">Die partielle Ableitung mit hoher Genauigkeit des- *Werts*.</span><span class="sxs-lookup"><span data-stu-id="14d4a-114">The high precision partial derivative of *value*.</span></span>

## <a name="remarks"></a><span data-ttu-id="14d4a-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="14d4a-115">Remarks</span></span>

<span data-ttu-id="14d4a-116">Außerdem sind die folgenden überladenen Versionen verfügbar:</span><span class="sxs-lookup"><span data-stu-id="14d4a-116">The following overloaded versions are also available:</span></span>

``` syntax
float2 ddx_fine(float2 value);
float3 ddx_fine(float3 value);
float4 ddx_fine(float4 value);
```

### <a name="minimum-shader-model"></a><span data-ttu-id="14d4a-117">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="14d4a-117">Minimum Shader Model</span></span>

<span data-ttu-id="14d4a-118">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="14d4a-118">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="14d4a-119">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="14d4a-119">Shader Model</span></span>                                                                | <span data-ttu-id="14d4a-120">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="14d4a-120">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="14d4a-121">[Shader Model 5](d3d11-graphics-reference-sm5.md) und höhere shadermodelle</span><span class="sxs-lookup"><span data-stu-id="14d4a-121">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="14d4a-122">ja</span><span class="sxs-lookup"><span data-stu-id="14d4a-122">yes</span></span>       |



 

<span data-ttu-id="14d4a-123">Diese Funktion wird in den folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="14d4a-123">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="14d4a-124">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="14d4a-124">Vertex</span></span> | <span data-ttu-id="14d4a-125">Hülle</span><span class="sxs-lookup"><span data-stu-id="14d4a-125">Hull</span></span> | <span data-ttu-id="14d4a-126">Domain</span><span class="sxs-lookup"><span data-stu-id="14d4a-126">Domain</span></span> | <span data-ttu-id="14d4a-127">Geometrie</span><span class="sxs-lookup"><span data-stu-id="14d4a-127">Geometry</span></span> | <span data-ttu-id="14d4a-128">Pixel</span><span class="sxs-lookup"><span data-stu-id="14d4a-128">Pixel</span></span> | <span data-ttu-id="14d4a-129">Compute</span><span class="sxs-lookup"><span data-stu-id="14d4a-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="14d4a-130">x</span><span class="sxs-lookup"><span data-stu-id="14d4a-130">x</span></span>     |         |



 

## <a name="see-also"></a><span data-ttu-id="14d4a-131">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="14d4a-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14d4a-132">Intrinsische Funktionen</span><span class="sxs-lookup"><span data-stu-id="14d4a-132">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="14d4a-133">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="14d4a-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




