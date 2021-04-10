---
title: 'Rwbyteaddressbuffer:: interlockedmin-Funktion'
description: Sucht atomisch nach dem Minimalwert.
ms.assetid: bf650b2e-9c6c-4458-9565-1e9ec76a1472
keywords:
- Interlockedmin-Funktion HLSL
topic_type:
- apiref
api_name:
- InterlockedMin
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b818a1fa0897d103e7d609a676212c6db428935f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039012"
---
# <a name="interlockedmin-function"></a><span data-ttu-id="3c5cc-104">Interlockedmin-Funktion</span><span class="sxs-lookup"><span data-stu-id="3c5cc-104">InterlockedMin function</span></span>

<span data-ttu-id="3c5cc-105">Sucht atomisch nach dem Minimalwert.</span><span class="sxs-lookup"><span data-stu-id="3c5cc-105">Finds the minimum value, atomically.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c5cc-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="3c5cc-106">Syntax</span></span>

``` syntax
void InterlockedMin(
  in  UINT dest,
  in  UINT value,
  out UINT original_value
);
```

## <a name="parameters"></a><span data-ttu-id="3c5cc-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="3c5cc-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c5cc-108">*dest* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3c5cc-108">*dest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c5cc-109">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="3c5cc-109">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="3c5cc-110">Die Zieladresse.</span><span class="sxs-lookup"><span data-stu-id="3c5cc-110">The destination address.</span></span>

</dd> <dt>

<span data-ttu-id="3c5cc-111">*Wert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3c5cc-111">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c5cc-112">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="3c5cc-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="3c5cc-113">Der Eingabewert.</span><span class="sxs-lookup"><span data-stu-id="3c5cc-113">The input value.</span></span>

</dd> <dt>

<span data-ttu-id="3c5cc-114">*ursprünglicher \_ Wert* ausgehend \[\]</span><span class="sxs-lookup"><span data-stu-id="3c5cc-114">*original\_value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3c5cc-115">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="3c5cc-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="3c5cc-116">Der ursprüngliche Wert.</span><span class="sxs-lookup"><span data-stu-id="3c5cc-116">The original value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c5cc-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3c5cc-117">Return value</span></span>

<span data-ttu-id="3c5cc-118">Nichts</span><span class="sxs-lookup"><span data-stu-id="3c5cc-118">Nothing</span></span>

## <a name="remarks"></a><span data-ttu-id="3c5cc-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3c5cc-119">Remarks</span></span>

<span data-ttu-id="3c5cc-120">Dieser Vorgang kann nur für typisierte int-und uint-Ressourcen und Shared Memory-Variablen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="3c5cc-120">This operation can only be performed on int and uint typed resources and shared memory variables.</span></span> <span data-ttu-id="3c5cc-121">Es gibt drei Verwendungsmöglichkeiten für diese Funktion.</span><span class="sxs-lookup"><span data-stu-id="3c5cc-121">There are three possible uses for this function.</span></span> <span data-ttu-id="3c5cc-122">Der erste ist, wenn R ein Variablentyp für den gemeinsamen Speicher ist.</span><span class="sxs-lookup"><span data-stu-id="3c5cc-122">The first is when R is a shared memory variable type.</span></span> <span data-ttu-id="3c5cc-123">In diesem Fall führt die Funktion einen atomaren Mindestwert des Werts für das Shared Memory-Register aus, auf das von dest verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="3c5cc-123">In this case, the function performs an atomic minimum of the value to the shared memory register referenced by dest.</span></span> <span data-ttu-id="3c5cc-124">Das zweite Szenario ist, wenn R ein Ressourcen Variablentyp ist.</span><span class="sxs-lookup"><span data-stu-id="3c5cc-124">The second scenario is when R is a resource variable type.</span></span> <span data-ttu-id="3c5cc-125">In diesem Szenario führt die Funktion einen atomaren Mindestwert des Werts für den Ressourcen Speicherort aus, auf den "dest" verweist.</span><span class="sxs-lookup"><span data-stu-id="3c5cc-125">In this scenario, the function performs an atomic minimum of the value to the resource location referenced by dest.</span></span> <span data-ttu-id="3c5cc-126">Das dritte Szenario ist, dass R ein lokaler Variablentyp ist.</span><span class="sxs-lookup"><span data-stu-id="3c5cc-126">Finally, the third scenario is when R is a local variable type.</span></span> <span data-ttu-id="3c5cc-127">In diesem Szenario wird die Funktion auf einen minimalen Wert von "dest" und "Value" reduziert, der in dest gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="3c5cc-127">In this scenario, the function reduces to a minimum of the value of dest and value, stored in dest.</span></span> <span data-ttu-id="3c5cc-128">Die überladene Funktion verfügt über eine zusätzliche Ausgabevariable, die auf den ursprünglichen Wert von dest festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="3c5cc-128">The overloaded function has an additional output variable which will be set to the original value of dest.</span></span> <span data-ttu-id="3c5cc-129">Dieser überladene Vorgang ist nur verfügbar, wenn R lesbar und beschreibbar ist.</span><span class="sxs-lookup"><span data-stu-id="3c5cc-129">This overloaded operation is only available when R is readable and writable.</span></span>

<span data-ttu-id="3c5cc-130">Diese Funktion wird in den folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="3c5cc-130">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="3c5cc-131">VS</span><span class="sxs-lookup"><span data-stu-id="3c5cc-131">VS</span></span>  | <span data-ttu-id="3c5cc-132">Jh</span><span class="sxs-lookup"><span data-stu-id="3c5cc-132">HS</span></span>  | <span data-ttu-id="3c5cc-133">DS</span><span class="sxs-lookup"><span data-stu-id="3c5cc-133">DS</span></span>  | <span data-ttu-id="3c5cc-134">GS</span><span class="sxs-lookup"><span data-stu-id="3c5cc-134">GS</span></span>  | <span data-ttu-id="3c5cc-135">PS</span><span class="sxs-lookup"><span data-stu-id="3c5cc-135">PS</span></span>  | <span data-ttu-id="3c5cc-136">CS</span><span class="sxs-lookup"><span data-stu-id="3c5cc-136">CS</span></span>  |
|-----|-----|-----|-----|-----|-----|
| <span data-ttu-id="3c5cc-137">x</span><span class="sxs-lookup"><span data-stu-id="3c5cc-137">x</span></span>   |  <span data-ttu-id="3c5cc-138">x</span><span class="sxs-lookup"><span data-stu-id="3c5cc-138">x</span></span>  | <span data-ttu-id="3c5cc-139">x</span><span class="sxs-lookup"><span data-stu-id="3c5cc-139">x</span></span>   | <span data-ttu-id="3c5cc-140">x</span><span class="sxs-lookup"><span data-stu-id="3c5cc-140">x</span></span>   | <span data-ttu-id="3c5cc-141">x</span><span class="sxs-lookup"><span data-stu-id="3c5cc-141">x</span></span>   | <span data-ttu-id="3c5cc-142">x</span><span class="sxs-lookup"><span data-stu-id="3c5cc-142">x</span></span>   |



 

## <a name="see-also"></a><span data-ttu-id="3c5cc-143">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="3c5cc-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c5cc-144">Rwbyteaddressbuffer</span><span class="sxs-lookup"><span data-stu-id="3c5cc-144">RWByteAddressBuffer</span></span>](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[<span data-ttu-id="3c5cc-145">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="3c5cc-145">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 