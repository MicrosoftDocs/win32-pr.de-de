---
title: 'Appendstructuredbuffer:: Append-Funktion'
description: Fügt einen Wert an das Ende des Puffers an.
ms.assetid: 667bc6dc-c0d0-419a-9227-99ce30b9cc73
keywords:
- Funktion HLSL anfügen
topic_type:
- apiref
api_name:
- Append
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 79db73558cb243437560cc77ed66b64f2807fe13
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2019
ms.locfileid: "103948279"
---
# <a name="append-function"></a><span data-ttu-id="a8bfb-104">Append-Funktion</span><span class="sxs-lookup"><span data-stu-id="a8bfb-104">Append function</span></span>

<span data-ttu-id="a8bfb-105">Fügt einen Wert an das Ende des Puffers an.</span><span class="sxs-lookup"><span data-stu-id="a8bfb-105">Appends a value to the end of the buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8bfb-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="a8bfb-106">Syntax</span></span>

``` syntax
void Append(
  in T value
);
```

## <a name="parameters"></a><span data-ttu-id="a8bfb-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="a8bfb-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8bfb-108">*Wert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a8bfb-108">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8bfb-109">Typ: **T**</span><span class="sxs-lookup"><span data-stu-id="a8bfb-109">Type: **T**</span></span>

<span data-ttu-id="a8bfb-110">Der Eingabewert.</span><span class="sxs-lookup"><span data-stu-id="a8bfb-110">The input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8bfb-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a8bfb-111">Return value</span></span>

<span data-ttu-id="a8bfb-112">Keine</span><span class="sxs-lookup"><span data-stu-id="a8bfb-112">None</span></span>

## <a name="remarks"></a><span data-ttu-id="a8bfb-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a8bfb-113">Remarks</span></span>

<span data-ttu-id="a8bfb-114">"T" kann ein beliebiger Datentyp sein, einschließlich Strukturen.</span><span class="sxs-lookup"><span data-stu-id="a8bfb-114">T can be any data type including structures.</span></span>

<span data-ttu-id="a8bfb-115">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="a8bfb-115">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="a8bfb-116">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="a8bfb-116">Vertex</span></span> | <span data-ttu-id="a8bfb-117">Hülle</span><span class="sxs-lookup"><span data-stu-id="a8bfb-117">Hull</span></span> | <span data-ttu-id="a8bfb-118">Domain</span><span class="sxs-lookup"><span data-stu-id="a8bfb-118">Domain</span></span> | <span data-ttu-id="a8bfb-119">Geometrie</span><span class="sxs-lookup"><span data-stu-id="a8bfb-119">Geometry</span></span> | <span data-ttu-id="a8bfb-120">Pixel</span><span class="sxs-lookup"><span data-stu-id="a8bfb-120">Pixel</span></span> | <span data-ttu-id="a8bfb-121">Compute</span><span class="sxs-lookup"><span data-stu-id="a8bfb-121">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="a8bfb-122">x</span><span class="sxs-lookup"><span data-stu-id="a8bfb-122">x</span></span>      | <span data-ttu-id="a8bfb-123">x</span><span class="sxs-lookup"><span data-stu-id="a8bfb-123">x</span></span>    | <span data-ttu-id="a8bfb-124">x</span><span class="sxs-lookup"><span data-stu-id="a8bfb-124">x</span></span>      | <span data-ttu-id="a8bfb-125">x</span><span class="sxs-lookup"><span data-stu-id="a8bfb-125">x</span></span>        | <span data-ttu-id="a8bfb-126">x</span><span class="sxs-lookup"><span data-stu-id="a8bfb-126">x</span></span>     | <span data-ttu-id="a8bfb-127">x</span><span class="sxs-lookup"><span data-stu-id="a8bfb-127">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="a8bfb-128">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="a8bfb-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8bfb-129">Appendstructuredbuffer</span><span class="sxs-lookup"><span data-stu-id="a8bfb-129">AppendStructuredBuffer</span></span>](sm5-object-appendstructuredbuffer.md)
</dt> <dt>

[<span data-ttu-id="a8bfb-130">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="a8bfb-130">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




