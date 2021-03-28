---
title: 'Texture1D:: MIPS. Operator-Funktion'
description: Gibt eine schreibgeschützte Ressourcen Variable oder ein Texture1D-Wert zurück.
ms.assetid: 0b64f0d3-f9a1-474b-b229-d91d18922d5c
keywords:
- MIPS. Operator Function HLSL
topic_type:
- apiref
api_name:
- mips.Operator
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4713fe20fa52e948113a220969229c413c5dc4d1
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104340228"
---
# <a name="texture1dmipsoperator----function"></a><span data-ttu-id="581c8-104">Texture1D:: MIPS. Operator-Funktion</span><span class="sxs-lookup"><span data-stu-id="581c8-104">Texture1D::mips.Operator    function</span></span>

<span data-ttu-id="581c8-105">Gibt eine schreibgeschützte Ressourcen Variable oder ein [**Texture1D**](sm5-object-texture1d.md)-Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="581c8-105">Returns a read-only resource variable or a [**Texture1D**](sm5-object-texture1d.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="581c8-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="581c8-106">Syntax</span></span>

``` syntax
R mips.Operator[][](
  in uint mipSlice,
  in uint pos
);
```

## <a name="parameters"></a><span data-ttu-id="581c8-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="581c8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="581c8-108">*mipslice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="581c8-108">*mipSlice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="581c8-109">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="581c8-109">Type: **uint**</span></span>

<span data-ttu-id="581c8-110">Der MIP-Slice-Index.</span><span class="sxs-lookup"><span data-stu-id="581c8-110">The mip slice index.</span></span>

</dd> <dt>

<span data-ttu-id="581c8-111">*POS* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="581c8-111">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="581c8-112">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="581c8-112">Type: **uint**</span></span>

<span data-ttu-id="581c8-113">Die Indexposition.</span><span class="sxs-lookup"><span data-stu-id="581c8-113">The index position.</span></span> <span data-ttu-id="581c8-114">Enthält die x-Koordinate.</span><span class="sxs-lookup"><span data-stu-id="581c8-114">Contains the x-coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="581c8-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="581c8-115">Return value</span></span>

<span data-ttu-id="581c8-116">Typ: **R**</span><span class="sxs-lookup"><span data-stu-id="581c8-116">Type: **R**</span></span>

<span data-ttu-id="581c8-117">Eine schreibgeschützte Ressourcen Variable.</span><span class="sxs-lookup"><span data-stu-id="581c8-117">A read-only resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="581c8-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="581c8-118">Remarks</span></span>

### <a name="usage-example"></a><span data-ttu-id="581c8-119">Verwendungsbeispiel</span><span class="sxs-lookup"><span data-stu-id="581c8-119">Usage Example</span></span>


```
Texture1D<float4> tex;
uint mip = 2;
uint pos = 1234;
float4 f = tex.mips[mip][pos];
      
```



<span data-ttu-id="581c8-120">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="581c8-120">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="581c8-121">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="581c8-121">Vertex</span></span> | <span data-ttu-id="581c8-122">Hülle</span><span class="sxs-lookup"><span data-stu-id="581c8-122">Hull</span></span> | <span data-ttu-id="581c8-123">Domain</span><span class="sxs-lookup"><span data-stu-id="581c8-123">Domain</span></span> | <span data-ttu-id="581c8-124">Geometrie</span><span class="sxs-lookup"><span data-stu-id="581c8-124">Geometry</span></span> | <span data-ttu-id="581c8-125">Pixel</span><span class="sxs-lookup"><span data-stu-id="581c8-125">Pixel</span></span> | <span data-ttu-id="581c8-126">Compute</span><span class="sxs-lookup"><span data-stu-id="581c8-126">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="581c8-127">x</span><span class="sxs-lookup"><span data-stu-id="581c8-127">x</span></span>      | <span data-ttu-id="581c8-128">x</span><span class="sxs-lookup"><span data-stu-id="581c8-128">x</span></span>    | <span data-ttu-id="581c8-129">x</span><span class="sxs-lookup"><span data-stu-id="581c8-129">x</span></span>      | <span data-ttu-id="581c8-130">x</span><span class="sxs-lookup"><span data-stu-id="581c8-130">x</span></span>        | <span data-ttu-id="581c8-131">x</span><span class="sxs-lookup"><span data-stu-id="581c8-131">x</span></span>     | <span data-ttu-id="581c8-132">x</span><span class="sxs-lookup"><span data-stu-id="581c8-132">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="581c8-133">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="581c8-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="581c8-134">Texture1D</span><span class="sxs-lookup"><span data-stu-id="581c8-134">Texture1D</span></span>](sm5-object-texture1d.md)
</dt> <dt>

[<span data-ttu-id="581c8-135">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="581c8-135">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




