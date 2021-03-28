---
title: 'Rwstructuredbuffer:: Operator-Funktion'
description: 'Gibt eine Ressourcen Variable zurück. | Rwstructuredbuffer:: Operator-Funktion'
ms.assetid: e821b60e-38db-463f-b0c6-47f2a4c9ccee
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
ms.openlocfilehash: e915d7862f7994d3b438bf3255ee836ede4b3d7d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104530632"
---
# <a name="rwstructuredbufferoperator--function"></a><span data-ttu-id="1c79f-105">Rwstructuredbuffer:: Operator-Funktion</span><span class="sxs-lookup"><span data-stu-id="1c79f-105">RWStructuredBuffer::Operator  function</span></span>

<span data-ttu-id="1c79f-106">Gibt eine Ressourcen Variable zurück.</span><span class="sxs-lookup"><span data-stu-id="1c79f-106">Returns a resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c79f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="1c79f-107">Syntax</span></span>

``` syntax
R Operator[](
  in uint pos
);
```

## <a name="parameters"></a><span data-ttu-id="1c79f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="1c79f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c79f-109">*POS* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1c79f-109">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c79f-110">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="1c79f-110">Type: **uint**</span></span>

<span data-ttu-id="1c79f-111">Die Indexposition.</span><span class="sxs-lookup"><span data-stu-id="1c79f-111">The index position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c79f-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1c79f-112">Return value</span></span>

<span data-ttu-id="1c79f-113">Typ: **R**</span><span class="sxs-lookup"><span data-stu-id="1c79f-113">Type: **R**</span></span>

<span data-ttu-id="1c79f-114">Eine Ressourcen Variable.</span><span class="sxs-lookup"><span data-stu-id="1c79f-114">A resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="1c79f-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1c79f-115">Remarks</span></span>

<span data-ttu-id="1c79f-116">Eine strukturierte Ressource kann basierend auf den Komponentennamen der Strukturen weiter indiziert werden.</span><span class="sxs-lookup"><span data-stu-id="1c79f-116">A structured resource can be further indexed based on the component names of the structures.</span></span>

<span data-ttu-id="1c79f-117">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="1c79f-117">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="1c79f-118">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="1c79f-118">Vertex</span></span> | <span data-ttu-id="1c79f-119">Hülle</span><span class="sxs-lookup"><span data-stu-id="1c79f-119">Hull</span></span> | <span data-ttu-id="1c79f-120">Domain</span><span class="sxs-lookup"><span data-stu-id="1c79f-120">Domain</span></span> | <span data-ttu-id="1c79f-121">Geometrie</span><span class="sxs-lookup"><span data-stu-id="1c79f-121">Geometry</span></span> | <span data-ttu-id="1c79f-122">Pixel</span><span class="sxs-lookup"><span data-stu-id="1c79f-122">Pixel</span></span> | <span data-ttu-id="1c79f-123">Compute</span><span class="sxs-lookup"><span data-stu-id="1c79f-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="1c79f-124">x</span><span class="sxs-lookup"><span data-stu-id="1c79f-124">x</span></span>     | <span data-ttu-id="1c79f-125">x</span><span class="sxs-lookup"><span data-stu-id="1c79f-125">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="1c79f-126">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="1c79f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c79f-127">Rwstructuredbuffer</span><span class="sxs-lookup"><span data-stu-id="1c79f-127">RWStructuredBuffer</span></span>](sm5-object-rwstructuredbuffer.md)
</dt> <dt>

[<span data-ttu-id="1c79f-128">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="1c79f-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




