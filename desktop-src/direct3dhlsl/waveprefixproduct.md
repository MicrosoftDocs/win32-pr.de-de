---
title: WavePrefixProduct-Funktion
description: Gibt das Produkt aller Werte in den aktiven Bereichen in dieser Welle mit Indizes zurück, die kleiner sind als diese Strecke.
ms.assetid: 3A5B271D-EF45-4511-9086-A9AD0D215D9A
keywords:
- Waveprefixproduct-Funktion HLSL
topic_type:
- apiref
api_name:
- WavePrefixProduct
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d073d72590951ddbbbb74274d4cd237e0a138c4f
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104391226"
---
# <a name="waveprefixproduct-function"></a><span data-ttu-id="47bcd-104">WavePrefixProduct-Funktion</span><span class="sxs-lookup"><span data-stu-id="47bcd-104">WavePrefixProduct function</span></span>

<span data-ttu-id="47bcd-105">Gibt das Produkt aller Werte in den aktiven Bereichen in dieser Welle mit Indizes zurück, die kleiner sind als diese Strecke.</span><span class="sxs-lookup"><span data-stu-id="47bcd-105">Returns the product of all of the values in the active lanes in this wave with indices less than this lane.</span></span>

## <a name="syntax"></a><span data-ttu-id="47bcd-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="47bcd-106">Syntax</span></span>

``` syntax
<type> WavePrefixProduct(
   <type> value
);
```

## <a name="parameters"></a><span data-ttu-id="47bcd-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="47bcd-107">Parameters</span></span>

<span data-ttu-id="47bcd-108">*value*</span><span class="sxs-lookup"><span data-stu-id="47bcd-108">*value*</span></span> 

<span data-ttu-id="47bcd-109">Der zu multiplizierende Wert.</span><span class="sxs-lookup"><span data-stu-id="47bcd-109">The value to multiply.</span></span>

## <a name="return-value"></a><span data-ttu-id="47bcd-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="47bcd-110">Return value</span></span>

<span data-ttu-id="47bcd-111">Das Produkt aller Werte.</span><span class="sxs-lookup"><span data-stu-id="47bcd-111">The product of all the values.</span></span>

## <a name="remarks"></a><span data-ttu-id="47bcd-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="47bcd-112">Remarks</span></span>

<span data-ttu-id="47bcd-113">Die Reihenfolge der Vorgänge in dieser Routine kann nicht garantiert werden.</span><span class="sxs-lookup"><span data-stu-id="47bcd-113">The order of operations on this routine cannot be guaranteed.</span></span> <span data-ttu-id="47bcd-114">Daher \[ wird das genaue Flag darin \] ignoriert.</span><span class="sxs-lookup"><span data-stu-id="47bcd-114">So, effectively, the \[precise\] flag is ignored within it.</span></span>

<span data-ttu-id="47bcd-115">Ein postfix-Produkt kann berechnet werden, indem das Präfix Product mit dem Wert der aktuellen Lane multipliziert wird.</span><span class="sxs-lookup"><span data-stu-id="47bcd-115">A postfix product can be computed by multiplying the prefix product by the current lane's value.</span></span>

<span data-ttu-id="47bcd-116">Beachten Sie, dass die aktive Spur mit dem niedrigsten Index immer 1 für das Präfix Produkt empfängt.</span><span class="sxs-lookup"><span data-stu-id="47bcd-116">Note that the active lane with the lowest index will always receive a 1 for its prefix product.</span></span>

<span data-ttu-id="47bcd-117">Diese Funktion wird vom Shader-Modell 6,0 in allen shaderphasen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="47bcd-117">This function is supported from shader model 6.0 in all shader stages.</span></span> 

## <a name="examples"></a><span data-ttu-id="47bcd-118">Beispiele</span><span class="sxs-lookup"><span data-stu-id="47bcd-118">Examples</span></span>

```hlsl
uint numToMultiply = 2;
uint prefixProduct = WavePrefixProduct( numToMultiply );
```

<span data-ttu-id="47bcd-119">Auf einem Computer mit einer Wellengröße von 8 und allen aktiven Bereichen außer den Bereichen 0 und 4 werden die folgenden Werte von waveprefixproduct zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="47bcd-119">On a machine with a wave size of 8, and all lanes active except lanes 0 and 4, the following values would be returned from WavePrefixProduct.</span></span>

| <span data-ttu-id="47bcd-120">Lane-Index</span><span class="sxs-lookup"><span data-stu-id="47bcd-120">lane index</span></span> | <span data-ttu-id="47bcd-121">status</span><span class="sxs-lookup"><span data-stu-id="47bcd-121">status</span></span>   | <span data-ttu-id="47bcd-122">prefixproduct</span><span class="sxs-lookup"><span data-stu-id="47bcd-122">prefixProduct</span></span> | 
|------------|----------|---------------|
| <span data-ttu-id="47bcd-123">0</span><span class="sxs-lookup"><span data-stu-id="47bcd-123">0</span></span>          | <span data-ttu-id="47bcd-124">inactive</span><span class="sxs-lookup"><span data-stu-id="47bcd-124">inactive</span></span> | <span data-ttu-id="47bcd-125">–</span><span class="sxs-lookup"><span data-stu-id="47bcd-125">n/a</span></span>           |
| <span data-ttu-id="47bcd-126">1</span><span class="sxs-lookup"><span data-stu-id="47bcd-126">1</span></span>          | <span data-ttu-id="47bcd-127">aktiv</span><span class="sxs-lookup"><span data-stu-id="47bcd-127">active</span></span>   | <span data-ttu-id="47bcd-128">= 1</span><span class="sxs-lookup"><span data-stu-id="47bcd-128">= 1</span></span>           |
| <span data-ttu-id="47bcd-129">2</span><span class="sxs-lookup"><span data-stu-id="47bcd-129">2</span></span>          | <span data-ttu-id="47bcd-130">aktiv</span><span class="sxs-lookup"><span data-stu-id="47bcd-130">active</span></span>   | <span data-ttu-id="47bcd-131">= 1 \* 2</span><span class="sxs-lookup"><span data-stu-id="47bcd-131">= 1\*2</span></span>        |
| <span data-ttu-id="47bcd-132">3</span><span class="sxs-lookup"><span data-stu-id="47bcd-132">3</span></span>          | <span data-ttu-id="47bcd-133">aktiv</span><span class="sxs-lookup"><span data-stu-id="47bcd-133">active</span></span>   | <span data-ttu-id="47bcd-134">= 1 \* 2 \* 2</span><span class="sxs-lookup"><span data-stu-id="47bcd-134">= 1\*2\*2</span></span>     |
| <span data-ttu-id="47bcd-135">4</span><span class="sxs-lookup"><span data-stu-id="47bcd-135">4</span></span>          | <span data-ttu-id="47bcd-136">inactive</span><span class="sxs-lookup"><span data-stu-id="47bcd-136">inactive</span></span> | <span data-ttu-id="47bcd-137">–</span><span class="sxs-lookup"><span data-stu-id="47bcd-137">n/a</span></span>           |
| <span data-ttu-id="47bcd-138">5</span><span class="sxs-lookup"><span data-stu-id="47bcd-138">5</span></span>          | <span data-ttu-id="47bcd-139">aktiv</span><span class="sxs-lookup"><span data-stu-id="47bcd-139">active</span></span>   | <span data-ttu-id="47bcd-140">= 1 \* 2 \* 2 2 \*</span><span class="sxs-lookup"><span data-stu-id="47bcd-140">= 1\*2\*2\*2</span></span>       |
| <span data-ttu-id="47bcd-141">6</span><span class="sxs-lookup"><span data-stu-id="47bcd-141">6</span></span>          | <span data-ttu-id="47bcd-142">aktiv</span><span class="sxs-lookup"><span data-stu-id="47bcd-142">active</span></span>   | <span data-ttu-id="47bcd-143">= 1 \* 2 \* 2 2 \* 2 2 \*</span><span class="sxs-lookup"><span data-stu-id="47bcd-143">= 1\*2\*2\*2\*2</span></span>    |
| <span data-ttu-id="47bcd-144">7</span><span class="sxs-lookup"><span data-stu-id="47bcd-144">7</span></span>          | <span data-ttu-id="47bcd-145">aktiv</span><span class="sxs-lookup"><span data-stu-id="47bcd-145">active</span></span>   | <span data-ttu-id="47bcd-146">= 1 2 2 2 2 2 2 \* \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="47bcd-146">= 1\*2\*2\*2\*2\*2</span></span> |

## <a name="see-also"></a><span data-ttu-id="47bcd-147">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="47bcd-147">See also</span></span>

[<span data-ttu-id="47bcd-148">Übersicht über Shader-Modell 6</span><span class="sxs-lookup"><span data-stu-id="47bcd-148">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)

[<span data-ttu-id="47bcd-149">Shader-Modell 6</span><span class="sxs-lookup"><span data-stu-id="47bcd-149">Shader Model 6</span></span>](shader-model-6-0.md)
