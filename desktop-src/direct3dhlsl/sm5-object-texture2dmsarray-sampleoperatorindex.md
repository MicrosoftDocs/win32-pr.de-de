---
title: 'Texture2DMSArray:: Sample. Operator-Funktion'
description: 'Gibt eine schreibgeschützte Ressourcen Variable zurück. | Texture2DMSArray:: Sample. Operator-Funktion'
ms.assetid: 5334c1d5-dfbd-4987-875c-0b92967b0f13
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
ms.openlocfilehash: e78746e0afe03e65a313982ca35c27a75ea14f1b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104982005"
---
# <a name="texture2dmsarraysampleoperator----function"></a><span data-ttu-id="23013-105">Texture2DMSArray:: Sample. Operator-Funktion</span><span class="sxs-lookup"><span data-stu-id="23013-105">Texture2DMSArray::sample.Operator    function</span></span>

<span data-ttu-id="23013-106">Gibt eine schreibgeschützte Ressourcen Variable zurück.</span><span class="sxs-lookup"><span data-stu-id="23013-106">Returns a read-only resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="23013-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="23013-107">Syntax</span></span>

``` syntax
R sample.Operator[][](
  in uint sampleSlice,
  in uint3 pos
);
```

## <a name="parameters"></a><span data-ttu-id="23013-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="23013-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23013-109">*sampleslice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="23013-109">*sampleSlice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23013-110">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="23013-110">Type: **uint**</span></span>

<span data-ttu-id="23013-111">Der Beispiel-Slice-Index.</span><span class="sxs-lookup"><span data-stu-id="23013-111">The sample slice index.</span></span>

</dd> <dt>

<span data-ttu-id="23013-112">*POS* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="23013-112">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23013-113">Typ: **uint3**</span><span class="sxs-lookup"><span data-stu-id="23013-113">Type: **uint3**</span></span>

<span data-ttu-id="23013-114">Die Indexposition.</span><span class="sxs-lookup"><span data-stu-id="23013-114">The index position.</span></span> <span data-ttu-id="23013-115">Die erste und die zweite Komponente enthalten die (x, y)-Koordinaten.</span><span class="sxs-lookup"><span data-stu-id="23013-115">The first and second components contain the (x, y) coordinates.</span></span> <span data-ttu-id="23013-116">Die dritte Komponente gibt den gewünschten Array Slice an.</span><span class="sxs-lookup"><span data-stu-id="23013-116">The third component indicates the desired array slice.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23013-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="23013-117">Return value</span></span>

<span data-ttu-id="23013-118">Typ: **R**</span><span class="sxs-lookup"><span data-stu-id="23013-118">Type: **R**</span></span>

<span data-ttu-id="23013-119">Eine schreibgeschützte Ressourcen Variable.</span><span class="sxs-lookup"><span data-stu-id="23013-119">A read-only resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="23013-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="23013-120">Remarks</span></span>

### <a name="usage-example"></a><span data-ttu-id="23013-121">Verwendungsbeispiel</span><span class="sxs-lookup"><span data-stu-id="23013-121">Usage Example</span></span>


```
Texture2DMSArray<float4, 4> alpha;

float4 main( float3 tcoord : texturecoord0 ) : SV_Target
{
     return s_msTexture.sample[2][tcoord];
}
```



<span data-ttu-id="23013-122">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="23013-122">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="23013-123">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="23013-123">Vertex</span></span> | <span data-ttu-id="23013-124">Hülle</span><span class="sxs-lookup"><span data-stu-id="23013-124">Hull</span></span> | <span data-ttu-id="23013-125">Domain</span><span class="sxs-lookup"><span data-stu-id="23013-125">Domain</span></span> | <span data-ttu-id="23013-126">Geometrie</span><span class="sxs-lookup"><span data-stu-id="23013-126">Geometry</span></span> | <span data-ttu-id="23013-127">Pixel</span><span class="sxs-lookup"><span data-stu-id="23013-127">Pixel</span></span> | <span data-ttu-id="23013-128">Compute</span><span class="sxs-lookup"><span data-stu-id="23013-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="23013-129">x</span><span class="sxs-lookup"><span data-stu-id="23013-129">x</span></span>      | <span data-ttu-id="23013-130">x</span><span class="sxs-lookup"><span data-stu-id="23013-130">x</span></span>    | <span data-ttu-id="23013-131">x</span><span class="sxs-lookup"><span data-stu-id="23013-131">x</span></span>      | <span data-ttu-id="23013-132">x</span><span class="sxs-lookup"><span data-stu-id="23013-132">x</span></span>        | <span data-ttu-id="23013-133">x</span><span class="sxs-lookup"><span data-stu-id="23013-133">x</span></span>     | <span data-ttu-id="23013-134">x</span><span class="sxs-lookup"><span data-stu-id="23013-134">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="23013-135">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="23013-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23013-136">Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="23013-136">Texture2DMSArray</span></span>](sm5-object-texture2dmsarray.md)
</dt> <dt>

[<span data-ttu-id="23013-137">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="23013-137">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




