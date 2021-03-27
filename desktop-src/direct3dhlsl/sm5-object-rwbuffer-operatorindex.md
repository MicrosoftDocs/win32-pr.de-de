---
title: 'Rwbuffer:: Operator-Funktion'
description: 'Gibt eine Ressourcen Variable zurück. | Rwbuffer:: Operator-Funktion'
ms.assetid: 59e5e4ec-ff0d-43aa-805a-04b79f5ab57f
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
ms.openlocfilehash: 40336c8ad6ee9e8008b82c172f1a5b863e967c0d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995310"
---
# <a name="rwbufferoperator--function"></a><span data-ttu-id="05d1b-105">Rwbuffer:: Operator-Funktion</span><span class="sxs-lookup"><span data-stu-id="05d1b-105">RWBuffer::Operator  function</span></span>

<span data-ttu-id="05d1b-106">Gibt eine Ressourcen Variable zurück.</span><span class="sxs-lookup"><span data-stu-id="05d1b-106">Returns a resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="05d1b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="05d1b-107">Syntax</span></span>

``` syntax
R Operator[](
  in uint pos
);
```

## <a name="parameters"></a><span data-ttu-id="05d1b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="05d1b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05d1b-109">*POS* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="05d1b-109">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="05d1b-110">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="05d1b-110">Type: **uint**</span></span>

<span data-ttu-id="05d1b-111">Die Indexposition.</span><span class="sxs-lookup"><span data-stu-id="05d1b-111">The index position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05d1b-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="05d1b-112">Return value</span></span>

<span data-ttu-id="05d1b-113">Typ: **R**</span><span class="sxs-lookup"><span data-stu-id="05d1b-113">Type: **R**</span></span>

<span data-ttu-id="05d1b-114">Eine Ressourcen Variable.</span><span class="sxs-lookup"><span data-stu-id="05d1b-114">A resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="05d1b-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="05d1b-115">Remarks</span></span>

<span data-ttu-id="05d1b-116">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="05d1b-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="05d1b-117">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="05d1b-117">Vertex</span></span> | <span data-ttu-id="05d1b-118">Hülle</span><span class="sxs-lookup"><span data-stu-id="05d1b-118">Hull</span></span> | <span data-ttu-id="05d1b-119">Domain</span><span class="sxs-lookup"><span data-stu-id="05d1b-119">Domain</span></span> | <span data-ttu-id="05d1b-120">Geometrie</span><span class="sxs-lookup"><span data-stu-id="05d1b-120">Geometry</span></span> | <span data-ttu-id="05d1b-121">Pixel</span><span class="sxs-lookup"><span data-stu-id="05d1b-121">Pixel</span></span> | <span data-ttu-id="05d1b-122">Compute</span><span class="sxs-lookup"><span data-stu-id="05d1b-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="05d1b-123">x</span><span class="sxs-lookup"><span data-stu-id="05d1b-123">x</span></span>      | <span data-ttu-id="05d1b-124">x</span><span class="sxs-lookup"><span data-stu-id="05d1b-124">x</span></span>    | <span data-ttu-id="05d1b-125">x</span><span class="sxs-lookup"><span data-stu-id="05d1b-125">x</span></span>      | <span data-ttu-id="05d1b-126">x</span><span class="sxs-lookup"><span data-stu-id="05d1b-126">x</span></span>        | <span data-ttu-id="05d1b-127">x</span><span class="sxs-lookup"><span data-stu-id="05d1b-127">x</span></span>     | <span data-ttu-id="05d1b-128">x</span><span class="sxs-lookup"><span data-stu-id="05d1b-128">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="05d1b-129">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="05d1b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05d1b-130">Rwbuffer</span><span class="sxs-lookup"><span data-stu-id="05d1b-130">RWBuffer</span></span>](sm5-object-rwbuffer.md)
</dt> <dt>

[<span data-ttu-id="05d1b-131">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="05d1b-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




