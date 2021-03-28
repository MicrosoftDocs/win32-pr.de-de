---
title: 'Structuredbuffer:: Operator-Funktion'
description: Gibt eine schreibgeschützte Ressourcen Variable eines structuredbuffer zurück.
ms.assetid: e2a1b0f7-f374-44a3-b567-8a2318e8b2b8
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
ms.openlocfilehash: 1f0d75bdfbcd3bfc560e896416f241f1291120d6
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104102718"
---
# <a name="structuredbufferoperator--function"></a><span data-ttu-id="70f6c-104">Structuredbuffer:: Operator-Funktion</span><span class="sxs-lookup"><span data-stu-id="70f6c-104">StructuredBuffer::Operator  function</span></span>

<span data-ttu-id="70f6c-105">Gibt eine schreibgeschützte Ressourcen Variable eines [**structuredbuffer**](sm5-object-structuredbuffer.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="70f6c-105">Returns a read-only resource variable of a [**StructuredBuffer**](sm5-object-structuredbuffer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="70f6c-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="70f6c-106">Syntax</span></span>

``` syntax
R Operator[](
  in uint pos
);
```

## <a name="parameters"></a><span data-ttu-id="70f6c-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="70f6c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70f6c-108">*POS* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="70f6c-108">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70f6c-109">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="70f6c-109">Type: **uint**</span></span>

<span data-ttu-id="70f6c-110">Die Indexposition.</span><span class="sxs-lookup"><span data-stu-id="70f6c-110">The index position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70f6c-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="70f6c-111">Return value</span></span>

<span data-ttu-id="70f6c-112">Typ: **R**</span><span class="sxs-lookup"><span data-stu-id="70f6c-112">Type: **R**</span></span>

<span data-ttu-id="70f6c-113">Eine schreibgeschützte Ressourcen Variable.</span><span class="sxs-lookup"><span data-stu-id="70f6c-113">A read-only resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="70f6c-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="70f6c-114">Remarks</span></span>

<span data-ttu-id="70f6c-115">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="70f6c-115">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="70f6c-116">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="70f6c-116">Vertex</span></span> | <span data-ttu-id="70f6c-117">Hülle</span><span class="sxs-lookup"><span data-stu-id="70f6c-117">Hull</span></span> | <span data-ttu-id="70f6c-118">Domain</span><span class="sxs-lookup"><span data-stu-id="70f6c-118">Domain</span></span> | <span data-ttu-id="70f6c-119">Geometrie</span><span class="sxs-lookup"><span data-stu-id="70f6c-119">Geometry</span></span> | <span data-ttu-id="70f6c-120">Pixel</span><span class="sxs-lookup"><span data-stu-id="70f6c-120">Pixel</span></span> | <span data-ttu-id="70f6c-121">Compute</span><span class="sxs-lookup"><span data-stu-id="70f6c-121">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="70f6c-122">x</span><span class="sxs-lookup"><span data-stu-id="70f6c-122">x</span></span>      | <span data-ttu-id="70f6c-123">x</span><span class="sxs-lookup"><span data-stu-id="70f6c-123">x</span></span>    | <span data-ttu-id="70f6c-124">x</span><span class="sxs-lookup"><span data-stu-id="70f6c-124">x</span></span>      | <span data-ttu-id="70f6c-125">x</span><span class="sxs-lookup"><span data-stu-id="70f6c-125">x</span></span>        | <span data-ttu-id="70f6c-126">x</span><span class="sxs-lookup"><span data-stu-id="70f6c-126">x</span></span>     | <span data-ttu-id="70f6c-127">x</span><span class="sxs-lookup"><span data-stu-id="70f6c-127">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="70f6c-128">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="70f6c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70f6c-129">Structuredbuffer</span><span class="sxs-lookup"><span data-stu-id="70f6c-129">StructuredBuffer</span></span>](sm5-object-structuredbuffer.md)
</dt> <dt>

[<span data-ttu-id="70f6c-130">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="70f6c-130">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




