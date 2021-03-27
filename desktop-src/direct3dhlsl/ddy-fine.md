---
title: ddy_fine-Funktion
description: Berechnet eine partielle Ableitung mit hoher Genauigkeit in Bezug auf die x-Koordinate des Bildschirm Raums. | ddy_fine-Funktion
ms.assetid: 29fcdbc9-470b-4b5b-b18c-f75dd2c87920
keywords:
- ddy_fine-Funktion HLSL
topic_type:
- apiref
api_name:
- ddy_fine
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2a4cb297180a4988cb049ccebfa4f82571c4655c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995775"
---
# <a name="ddy_fine-function"></a><span data-ttu-id="9dfb7-105">ddY \_ fein-Funktion</span><span class="sxs-lookup"><span data-stu-id="9dfb7-105">ddy\_fine function</span></span>

<span data-ttu-id="9dfb7-106">Berechnet eine partielle Ableitung mit hoher Genauigkeit in Bezug auf die x-Koordinate des Bildschirm Raums.</span><span class="sxs-lookup"><span data-stu-id="9dfb7-106">Computes a high precision partial derivative with respect to the screen-space x-coordinate.</span></span>

## <a name="syntax"></a><span data-ttu-id="9dfb7-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="9dfb7-107">Syntax</span></span>

``` syntax
float ddy_fine(
  in float value
);
```

## <a name="parameters"></a><span data-ttu-id="9dfb7-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="9dfb7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9dfb7-109">*Wert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9dfb7-109">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9dfb7-110">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="9dfb7-110">Type: **float**</span></span>

<span data-ttu-id="9dfb7-111">Der Eingabewert.</span><span class="sxs-lookup"><span data-stu-id="9dfb7-111">The input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9dfb7-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9dfb7-112">Return value</span></span>

<span data-ttu-id="9dfb7-113">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="9dfb7-113">Type: **float**</span></span>

<span data-ttu-id="9dfb7-114">Die partielle Ableitung mit hoher Genauigkeit des- *Werts*.</span><span class="sxs-lookup"><span data-stu-id="9dfb7-114">The high precision partial derivative of *value*.</span></span>

## <a name="remarks"></a><span data-ttu-id="9dfb7-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9dfb7-115">Remarks</span></span>

<span data-ttu-id="9dfb7-116">Außerdem sind die folgenden überladenen Versionen verfügbar:</span><span class="sxs-lookup"><span data-stu-id="9dfb7-116">The following overloaded versions are also available:</span></span>

``` syntax
float2 ddy_fine(float2 value);
float3 ddy_fine(float3 value);
float4 ddy_fine(float4 value);  
```

### <a name="minimum-shader-model"></a><span data-ttu-id="9dfb7-117">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="9dfb7-117">Minimum Shader Model</span></span>

<span data-ttu-id="9dfb7-118">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9dfb7-118">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="9dfb7-119">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="9dfb7-119">Shader Model</span></span>                                                                | <span data-ttu-id="9dfb7-120">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="9dfb7-120">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="9dfb7-121">[Shader Model 5](d3d11-graphics-reference-sm5.md) und höhere shadermodelle</span><span class="sxs-lookup"><span data-stu-id="9dfb7-121">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="9dfb7-122">ja</span><span class="sxs-lookup"><span data-stu-id="9dfb7-122">yes</span></span>       |



 

<span data-ttu-id="9dfb7-123">Diese Funktion wird in den folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="9dfb7-123">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="9dfb7-124">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="9dfb7-124">Vertex</span></span> | <span data-ttu-id="9dfb7-125">Hülle</span><span class="sxs-lookup"><span data-stu-id="9dfb7-125">Hull</span></span> | <span data-ttu-id="9dfb7-126">Domain</span><span class="sxs-lookup"><span data-stu-id="9dfb7-126">Domain</span></span> | <span data-ttu-id="9dfb7-127">Geometrie</span><span class="sxs-lookup"><span data-stu-id="9dfb7-127">Geometry</span></span> | <span data-ttu-id="9dfb7-128">Pixel</span><span class="sxs-lookup"><span data-stu-id="9dfb7-128">Pixel</span></span> | <span data-ttu-id="9dfb7-129">Compute</span><span class="sxs-lookup"><span data-stu-id="9dfb7-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="9dfb7-130">x</span><span class="sxs-lookup"><span data-stu-id="9dfb7-130">x</span></span>     |         |



 

## <a name="see-also"></a><span data-ttu-id="9dfb7-131">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="9dfb7-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9dfb7-132">Intrinsische Funktionen</span><span class="sxs-lookup"><span data-stu-id="9dfb7-132">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="9dfb7-133">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="9dfb7-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




