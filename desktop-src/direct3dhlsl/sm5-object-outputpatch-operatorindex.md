---
title: 'Outputpatch:: Operator-Funktion'
description: 'Gibt den n-ten Steuerungspunkt im Patch zurück. | Outputpatch:: Operator-Funktion'
ms.assetid: 3ac15fe8-8bab-46a2-8826-61ade927c99e
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
ms.openlocfilehash: 8194713dc4967151991fab95000fa70c40122f26
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104352709"
---
# <a name="outputpatchoperator--function"></a><span data-ttu-id="e7773-105">Outputpatch:: Operator-Funktion</span><span class="sxs-lookup"><span data-stu-id="e7773-105">OutputPatch::Operator  function</span></span>

<span data-ttu-id="e7773-106">Gibt den *n*-<sup>ten Steuerungspunkt</sup> im Patch zurück.</span><span class="sxs-lookup"><span data-stu-id="e7773-106">Returns the *n*<sup>th</sup> control point in the patch.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7773-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e7773-107">Syntax</span></span>

``` syntax
T Operator[](
  in uint n
);
```

## <a name="parameters"></a><span data-ttu-id="e7773-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e7773-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7773-109">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e7773-109">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7773-110">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="e7773-110">Type: **uint**</span></span>

<span data-ttu-id="e7773-111">Der Eingabe Index.</span><span class="sxs-lookup"><span data-stu-id="e7773-111">The input index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7773-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e7773-112">Return value</span></span>

<span data-ttu-id="e7773-113">Typ: **T**</span><span class="sxs-lookup"><span data-stu-id="e7773-113">Type: **T**</span></span>

<span data-ttu-id="e7773-114">Der *n*-<sup>te Steuerungspunkt</sup> .</span><span class="sxs-lookup"><span data-stu-id="e7773-114">The *n*<sup>th</sup> control point.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7773-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e7773-115">Remarks</span></span>

<span data-ttu-id="e7773-116">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="e7773-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="e7773-117">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="e7773-117">Vertex</span></span> | <span data-ttu-id="e7773-118">Hülle</span><span class="sxs-lookup"><span data-stu-id="e7773-118">Hull</span></span> | <span data-ttu-id="e7773-119">Domain</span><span class="sxs-lookup"><span data-stu-id="e7773-119">Domain</span></span> | <span data-ttu-id="e7773-120">Geometrie</span><span class="sxs-lookup"><span data-stu-id="e7773-120">Geometry</span></span> | <span data-ttu-id="e7773-121">Pixel</span><span class="sxs-lookup"><span data-stu-id="e7773-121">Pixel</span></span> | <span data-ttu-id="e7773-122">Compute</span><span class="sxs-lookup"><span data-stu-id="e7773-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="e7773-123">x</span><span class="sxs-lookup"><span data-stu-id="e7773-123">x</span></span>    | <span data-ttu-id="e7773-124">x</span><span class="sxs-lookup"><span data-stu-id="e7773-124">x</span></span>      |          |       |         |



 

## <a name="see-also"></a><span data-ttu-id="e7773-125">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e7773-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7773-126">Outputpatch</span><span class="sxs-lookup"><span data-stu-id="e7773-126">OutputPatch</span></span>](sm5-object-outputpatch.md)
</dt> <dt>

[<span data-ttu-id="e7773-127">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="e7773-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




