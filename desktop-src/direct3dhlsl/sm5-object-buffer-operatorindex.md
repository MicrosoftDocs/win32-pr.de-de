---
title: 'Buffer:: Operator-Funktion'
description: 'Gibt eine schreibgeschützte Ressourcen Variable zurück. | Buffer:: Operator-Funktion'
ms.assetid: 6a9e1176-439b-4565-9c7e-957d7c4045f0
keywords:
- Operator Funktion Direct Write
topic_type:
- apiref
api_name:
- Operator
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0b811dd2409a00bb07f0b2441f6d57d4bd122f50
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104393906"
---
# <a name="bufferoperator--function"></a><span data-ttu-id="113a5-105">Buffer:: Operator-Funktion</span><span class="sxs-lookup"><span data-stu-id="113a5-105">Buffer::Operator  function</span></span>

<span data-ttu-id="113a5-106">Gibt eine schreibgeschützte Ressourcen Variable zurück.</span><span class="sxs-lookup"><span data-stu-id="113a5-106">Returns a read-only resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="113a5-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="113a5-107">Syntax</span></span>

``` syntax
R Operator[](
  in uint pos
);
```

## <a name="parameters"></a><span data-ttu-id="113a5-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="113a5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="113a5-109">*POS* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="113a5-109">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="113a5-110">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="113a5-110">Type: **uint**</span></span>

<span data-ttu-id="113a5-111">Die Indexposition.</span><span class="sxs-lookup"><span data-stu-id="113a5-111">The index position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="113a5-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="113a5-112">Return value</span></span>

<span data-ttu-id="113a5-113">Typ: **R**</span><span class="sxs-lookup"><span data-stu-id="113a5-113">Type: **R**</span></span>

<span data-ttu-id="113a5-114">Eine schreibgeschützte Ressourcen Variable.</span><span class="sxs-lookup"><span data-stu-id="113a5-114">A read-only resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="113a5-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="113a5-115">Remarks</span></span>

<span data-ttu-id="113a5-116">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="113a5-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="113a5-117">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="113a5-117">Vertex</span></span> | <span data-ttu-id="113a5-118">Hülle</span><span class="sxs-lookup"><span data-stu-id="113a5-118">Hull</span></span> | <span data-ttu-id="113a5-119">Domain</span><span class="sxs-lookup"><span data-stu-id="113a5-119">Domain</span></span> | <span data-ttu-id="113a5-120">Geometrie</span><span class="sxs-lookup"><span data-stu-id="113a5-120">Geometry</span></span> | <span data-ttu-id="113a5-121">Pixel</span><span class="sxs-lookup"><span data-stu-id="113a5-121">Pixel</span></span> | <span data-ttu-id="113a5-122">Compute</span><span class="sxs-lookup"><span data-stu-id="113a5-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="113a5-123">x</span><span class="sxs-lookup"><span data-stu-id="113a5-123">x</span></span>     | <span data-ttu-id="113a5-124">x</span><span class="sxs-lookup"><span data-stu-id="113a5-124">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="113a5-125">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="113a5-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="113a5-126">Buffer</span><span class="sxs-lookup"><span data-stu-id="113a5-126">Buffer</span></span>](sm5-object-buffer.md)
</dt> <dt>

[<span data-ttu-id="113a5-127">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="113a5-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




