---
title: WavePrefixSum-Funktion
description: Gibt die Summe aller Werte in den aktiven Bereichen mit kleineren Indizes als dieser zurück.
ms.assetid: F51B90AB-3E85-4521-8A2C-7C16A4ECB1F9
keywords:
- Waveprefixsum-Funktion HLSL
topic_type:
- apiref
api_name:
- WavePrefixSum
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b133aa37b522156df73914eef66c4d3695a70ed7
ms.sourcegitcommit: 41c742c88f7d9ce05e107008f186b6e872ff9288
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/31/2021
ms.locfileid: "104980984"
---
# <a name="waveprefixsum-function"></a><span data-ttu-id="dcfdd-104">WavePrefixSum-Funktion</span><span class="sxs-lookup"><span data-stu-id="dcfdd-104">WavePrefixSum function</span></span>

<span data-ttu-id="dcfdd-105">Gibt die Summe aller Werte in den aktiven Bereichen mit kleineren Indizes als dieser zurück.</span><span class="sxs-lookup"><span data-stu-id="dcfdd-105">Returns the sum of all of the values in the active lanes with smaller indices than this one.</span></span>

## <a name="syntax"></a><span data-ttu-id="dcfdd-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="dcfdd-106">Syntax</span></span>

``` syntax
<type> WavePrefixSum(
   <type> value
);
```

## <a name="parameters"></a><span data-ttu-id="dcfdd-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="dcfdd-107">Parameters</span></span>

<span data-ttu-id="dcfdd-108">*value*</span><span class="sxs-lookup"><span data-stu-id="dcfdd-108">*value*</span></span> 

<span data-ttu-id="dcfdd-109">Der Wert, der addiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="dcfdd-109">The value to sum up.</span></span>

## <a name="return-value"></a><span data-ttu-id="dcfdd-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dcfdd-110">Return value</span></span>

<span data-ttu-id="dcfdd-111">Die Summe der Werte.</span><span class="sxs-lookup"><span data-stu-id="dcfdd-111">The sum of the values.</span></span>

## <a name="remarks"></a><span data-ttu-id="dcfdd-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dcfdd-112">Remarks</span></span>

<span data-ttu-id="dcfdd-113">Die Reihenfolge der Vorgänge in dieser Routine kann nicht garantiert werden.</span><span class="sxs-lookup"><span data-stu-id="dcfdd-113">The order of operations on this routine cannot be guaranteed.</span></span> <span data-ttu-id="dcfdd-114">Daher \[ wird das genaue Flag darin \] ignoriert.</span><span class="sxs-lookup"><span data-stu-id="dcfdd-114">So, effectively, the \[precise\] flag is ignored within it.</span></span>

<span data-ttu-id="dcfdd-115">Sie können eine postfix Summe berechnen, indem Sie das Präfix Sum dem Wert der aktuellen Lane hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="dcfdd-115">A postfix sum can be computed by adding the prefix sum to the current lane's value.</span></span>

<span data-ttu-id="dcfdd-116">Beachten Sie, dass die aktive Spur mit dem niedrigsten Index immer 0 für die Präfix Summe erhält.</span><span class="sxs-lookup"><span data-stu-id="dcfdd-116">Note that the active lane with the lowest index will always receive a 0 for its prefix sum.</span></span>

<span data-ttu-id="dcfdd-117">Diese Funktion wird vom Shader-Modell 6,0 in allen shaderphasen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="dcfdd-117">This function is supported from shader model 6.0 in all shader stages.</span></span> 

## <a name="examples"></a><span data-ttu-id="dcfdd-118">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dcfdd-118">Examples</span></span>

```hlsl
uint numToSum = 2;
uint prefixSum = WavePrefixSum( numToSum );
```

<span data-ttu-id="dcfdd-119">Auf einem Computer mit einer Wellengröße von 8 und allen aktiven Bereichen außer den Bereichen 0 und 4 werden die folgenden Werte von waveprefixsum zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="dcfdd-119">On a machine with a wave size of 8, and all lanes active except lanes 0 and 4, the following values would be returned from WavePrefixSum.</span></span>

| <span data-ttu-id="dcfdd-120">Lane-Index</span><span class="sxs-lookup"><span data-stu-id="dcfdd-120">lane index</span></span> | <span data-ttu-id="dcfdd-121">status</span><span class="sxs-lookup"><span data-stu-id="dcfdd-121">status</span></span>   | <span data-ttu-id="dcfdd-122">prefixsum</span><span class="sxs-lookup"><span data-stu-id="dcfdd-122">prefixSum</span></span>     | 
|------------|----------|---------------|
| <span data-ttu-id="dcfdd-123">0</span><span class="sxs-lookup"><span data-stu-id="dcfdd-123">0</span></span>          | <span data-ttu-id="dcfdd-124">inactive</span><span class="sxs-lookup"><span data-stu-id="dcfdd-124">inactive</span></span> | <span data-ttu-id="dcfdd-125">–</span><span class="sxs-lookup"><span data-stu-id="dcfdd-125">n/a</span></span>           |
| <span data-ttu-id="dcfdd-126">1</span><span class="sxs-lookup"><span data-stu-id="dcfdd-126">1</span></span>          | <span data-ttu-id="dcfdd-127">aktiv</span><span class="sxs-lookup"><span data-stu-id="dcfdd-127">active</span></span>   | <span data-ttu-id="dcfdd-128">= 0</span><span class="sxs-lookup"><span data-stu-id="dcfdd-128">= 0</span></span>           |
| <span data-ttu-id="dcfdd-129">2</span><span class="sxs-lookup"><span data-stu-id="dcfdd-129">2</span></span>          | <span data-ttu-id="dcfdd-130">aktiv</span><span class="sxs-lookup"><span data-stu-id="dcfdd-130">active</span></span>   | <span data-ttu-id="dcfdd-131">= 0 + 2</span><span class="sxs-lookup"><span data-stu-id="dcfdd-131">= 0+2</span></span>         |
| <span data-ttu-id="dcfdd-132">3</span><span class="sxs-lookup"><span data-stu-id="dcfdd-132">3</span></span>          | <span data-ttu-id="dcfdd-133">aktiv</span><span class="sxs-lookup"><span data-stu-id="dcfdd-133">active</span></span>   | <span data-ttu-id="dcfdd-134">= 0 + 2 + 2</span><span class="sxs-lookup"><span data-stu-id="dcfdd-134">= 0+2+2</span></span>       |
| <span data-ttu-id="dcfdd-135">4</span><span class="sxs-lookup"><span data-stu-id="dcfdd-135">4</span></span>          | <span data-ttu-id="dcfdd-136">inactive</span><span class="sxs-lookup"><span data-stu-id="dcfdd-136">inactive</span></span> | <span data-ttu-id="dcfdd-137">–</span><span class="sxs-lookup"><span data-stu-id="dcfdd-137">n/a</span></span>           |
| <span data-ttu-id="dcfdd-138">5</span><span class="sxs-lookup"><span data-stu-id="dcfdd-138">5</span></span>          | <span data-ttu-id="dcfdd-139">aktiv</span><span class="sxs-lookup"><span data-stu-id="dcfdd-139">active</span></span>   | <span data-ttu-id="dcfdd-140">= 0 + 2 + 2 + 2</span><span class="sxs-lookup"><span data-stu-id="dcfdd-140">= 0+2+2+2</span></span>     |
| <span data-ttu-id="dcfdd-141">6</span><span class="sxs-lookup"><span data-stu-id="dcfdd-141">6</span></span>          | <span data-ttu-id="dcfdd-142">aktiv</span><span class="sxs-lookup"><span data-stu-id="dcfdd-142">active</span></span>   | <span data-ttu-id="dcfdd-143">= 0 + 2 + 2 + 2 + 2</span><span class="sxs-lookup"><span data-stu-id="dcfdd-143">= 0+2+2+2+2</span></span>   |
| <span data-ttu-id="dcfdd-144">7</span><span class="sxs-lookup"><span data-stu-id="dcfdd-144">7</span></span>          | <span data-ttu-id="dcfdd-145">aktiv</span><span class="sxs-lookup"><span data-stu-id="dcfdd-145">active</span></span>   | <span data-ttu-id="dcfdd-146">= 0 + 2 + 2 + 2 + 2 + 2</span><span class="sxs-lookup"><span data-stu-id="dcfdd-146">= 0+2+2+2+2+2</span></span> |

## <a name="see-also"></a><span data-ttu-id="dcfdd-147">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="dcfdd-147">See also</span></span>

[<span data-ttu-id="dcfdd-148">Übersicht über Shader-Modell 6</span><span class="sxs-lookup"><span data-stu-id="dcfdd-148">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)

[<span data-ttu-id="dcfdd-149">Shader-Modell 6</span><span class="sxs-lookup"><span data-stu-id="dcfdd-149">Shader Model 6</span></span>](shader-model-6-0.md)
