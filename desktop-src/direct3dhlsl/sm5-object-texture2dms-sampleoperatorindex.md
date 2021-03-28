---
title: 'Texture2DMS:: Sample. Operator-Funktion'
description: 'Ruft einen Wert aus der Ressource an dem Speicherort und dem angegebenen Beispiel Index ab. | Texture2DMS:: Sample. Operator-Funktion'
ms.assetid: 5bc24129-b690-44dd-ae85-8533b10befaa
keywords:
- Blutprobe. Operator Function HLSL
topic_type:
- apiref
api_name:
- sample.Operator
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1a73577fa67992b212b4769059f1523e584acbaf
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104219381"
---
# <a name="texture2dmssampleoperator----function"></a><span data-ttu-id="e94b1-105">Texture2DMS:: Sample. Operator-Funktion</span><span class="sxs-lookup"><span data-stu-id="e94b1-105">Texture2DMS::sample.Operator    function</span></span>

<span data-ttu-id="e94b1-106">Ruft einen Wert aus der Ressource an dem Speicherort und dem angegebenen Beispiel Index ab.</span><span class="sxs-lookup"><span data-stu-id="e94b1-106">Retrieves a value from the resource at the location and sample index provided.</span></span>

## <a name="syntax"></a><span data-ttu-id="e94b1-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e94b1-107">Syntax</span></span>

``` syntax
R sample.Operator[][](
  in uint sampleSlice,
  in uint2 pos
);
```

## <a name="parameters"></a><span data-ttu-id="e94b1-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e94b1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e94b1-109">*sampleslice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e94b1-109">*sampleSlice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e94b1-110">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="e94b1-110">Type: **uint**</span></span>

<span data-ttu-id="e94b1-111">Der Beispiel-Slice-Index.</span><span class="sxs-lookup"><span data-stu-id="e94b1-111">The sample slice index.</span></span>

</dd> <dt>

<span data-ttu-id="e94b1-112">*POS* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e94b1-112">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e94b1-113">Typ: **uint2**</span><span class="sxs-lookup"><span data-stu-id="e94b1-113">Type: **uint2**</span></span>

<span data-ttu-id="e94b1-114">Die Indexposition.</span><span class="sxs-lookup"><span data-stu-id="e94b1-114">The index position.</span></span> <span data-ttu-id="e94b1-115">Die-Komponenten enthalten die (x, y)-Koordinaten.</span><span class="sxs-lookup"><span data-stu-id="e94b1-115">The components contain the (x, y) coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e94b1-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e94b1-116">Return value</span></span>

<span data-ttu-id="e94b1-117">Typ: **R**</span><span class="sxs-lookup"><span data-stu-id="e94b1-117">Type: **R**</span></span>

<span data-ttu-id="e94b1-118">Eine schreibgeschützte Ressourcen Variable.</span><span class="sxs-lookup"><span data-stu-id="e94b1-118">A read-only resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="e94b1-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e94b1-119">Remarks</span></span>

### <a name="usage-example"></a><span data-ttu-id="e94b1-120">Verwendungsbeispiel</span><span class="sxs-lookup"><span data-stu-id="e94b1-120">Usage Example</span></span>


```
Texture2DMS<float4, 8> tex;

float4 main( float3 tcoord : texturecoord0 ) : SV_Target
{
     return s_msTexture.sample[2][tcoord];
}
```



<span data-ttu-id="e94b1-121">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="e94b1-121">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="e94b1-122">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="e94b1-122">Vertex</span></span> | <span data-ttu-id="e94b1-123">Hülle</span><span class="sxs-lookup"><span data-stu-id="e94b1-123">Hull</span></span> | <span data-ttu-id="e94b1-124">Domain</span><span class="sxs-lookup"><span data-stu-id="e94b1-124">Domain</span></span> | <span data-ttu-id="e94b1-125">Geometrie</span><span class="sxs-lookup"><span data-stu-id="e94b1-125">Geometry</span></span> | <span data-ttu-id="e94b1-126">Pixel</span><span class="sxs-lookup"><span data-stu-id="e94b1-126">Pixel</span></span> | <span data-ttu-id="e94b1-127">Compute</span><span class="sxs-lookup"><span data-stu-id="e94b1-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="e94b1-128">x</span><span class="sxs-lookup"><span data-stu-id="e94b1-128">x</span></span>      | <span data-ttu-id="e94b1-129">x</span><span class="sxs-lookup"><span data-stu-id="e94b1-129">x</span></span>    | <span data-ttu-id="e94b1-130">x</span><span class="sxs-lookup"><span data-stu-id="e94b1-130">x</span></span>      | <span data-ttu-id="e94b1-131">x</span><span class="sxs-lookup"><span data-stu-id="e94b1-131">x</span></span>        | <span data-ttu-id="e94b1-132">x</span><span class="sxs-lookup"><span data-stu-id="e94b1-132">x</span></span>     | <span data-ttu-id="e94b1-133">x</span><span class="sxs-lookup"><span data-stu-id="e94b1-133">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="e94b1-134">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e94b1-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e94b1-135">Texture2DMS</span><span class="sxs-lookup"><span data-stu-id="e94b1-135">Texture2DMS</span></span>](sm5-object-texture2dms.md)
</dt> <dt>

[<span data-ttu-id="e94b1-136">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="e94b1-136">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




