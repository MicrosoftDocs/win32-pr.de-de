---
title: 'Inputpatch:: Operator-Funktion'
description: 'Gibt den n-ten Steuerungspunkt im Patch zurück. | Inputpatch:: Operator-Funktion'
ms.assetid: 2c1eda6b-a9c1-40d3-be91-7a2e8f1da9fc
keywords:
- Operator Function HLSL
topic_type:
- apiref
api_name:
- Operator
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5d95cb8adae6e7a91629614e0ae10b4161dbac3f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104219218"
---
# <a name="inputpatchoperator--function"></a><span data-ttu-id="69edb-105">Inputpatch:: Operator-Funktion</span><span class="sxs-lookup"><span data-stu-id="69edb-105">InputPatch::Operator  function</span></span>

<span data-ttu-id="69edb-106">Gibt den *n*-<sup>ten Steuerungspunkt</sup> im Patch zurück.</span><span class="sxs-lookup"><span data-stu-id="69edb-106">Returns the *n*<sup>th</sup> control point in the patch.</span></span>

## <a name="syntax"></a><span data-ttu-id="69edb-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="69edb-107">Syntax</span></span>

``` syntax
T Operator[](
  in uint n
);
```

## <a name="parameters"></a><span data-ttu-id="69edb-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="69edb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69edb-109">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="69edb-109">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69edb-110">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="69edb-110">Type: **uint**</span></span>

<span data-ttu-id="69edb-111">Der Eingabe Index.</span><span class="sxs-lookup"><span data-stu-id="69edb-111">The input index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69edb-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="69edb-112">Return value</span></span>

<span data-ttu-id="69edb-113">Typ: **T**</span><span class="sxs-lookup"><span data-stu-id="69edb-113">Type: **T**</span></span>

<span data-ttu-id="69edb-114">Der *n*-<sup>te Steuerungspunkt</sup> .</span><span class="sxs-lookup"><span data-stu-id="69edb-114">The *n*<sup>th</sup> control point.</span></span>

## <a name="remarks"></a><span data-ttu-id="69edb-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="69edb-115">Remarks</span></span>

<span data-ttu-id="69edb-116">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="69edb-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="69edb-117">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="69edb-117">Vertex</span></span> | <span data-ttu-id="69edb-118">Hülle</span><span class="sxs-lookup"><span data-stu-id="69edb-118">Hull</span></span> | <span data-ttu-id="69edb-119">Domain</span><span class="sxs-lookup"><span data-stu-id="69edb-119">Domain</span></span> | <span data-ttu-id="69edb-120">Geometrie</span><span class="sxs-lookup"><span data-stu-id="69edb-120">Geometry</span></span> | <span data-ttu-id="69edb-121">Pixel</span><span class="sxs-lookup"><span data-stu-id="69edb-121">Pixel</span></span> | <span data-ttu-id="69edb-122">Compute</span><span class="sxs-lookup"><span data-stu-id="69edb-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="69edb-123">x</span><span class="sxs-lookup"><span data-stu-id="69edb-123">x</span></span>    |        |          |       |         |



 

## <a name="see-also"></a><span data-ttu-id="69edb-124">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="69edb-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69edb-125">Input Patch</span><span class="sxs-lookup"><span data-stu-id="69edb-125">InputPatch</span></span>](sm5-object-inputpatch.md)
</dt> <dt>

[<span data-ttu-id="69edb-126">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="69edb-126">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




