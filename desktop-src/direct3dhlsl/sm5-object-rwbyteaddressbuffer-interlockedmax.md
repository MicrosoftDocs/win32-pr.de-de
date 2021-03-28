---
title: 'Rwbyteaddressbuffer:: interlockedmax-Funktion'
description: Findet atomisch den maximalen Wert.
ms.assetid: 2e78065f-c1ee-47ac-a826-c8a46c730c4a
keywords:
- Interlockedmax-Funktion HLSL
topic_type:
- apiref
api_name:
- InterlockedMax
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e77f925a0950d3731af58c2c6835867640760371
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104993463"
---
# <a name="interlockedmax-function"></a><span data-ttu-id="c98b8-104">Interlockedmax-Funktion</span><span class="sxs-lookup"><span data-stu-id="c98b8-104">InterlockedMax function</span></span>

<span data-ttu-id="c98b8-105">Findet atomisch den maximalen Wert.</span><span class="sxs-lookup"><span data-stu-id="c98b8-105">Finds the maximum value, atomically.</span></span>

## <a name="syntax"></a><span data-ttu-id="c98b8-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="c98b8-106">Syntax</span></span>

``` syntax
void InterlockedMax(
  in  UINT dest,
  in  UINT value,
  out UINT original_value
);
```

## <a name="parameters"></a><span data-ttu-id="c98b8-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="c98b8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c98b8-108">*dest* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c98b8-108">*dest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c98b8-109">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c98b8-109">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c98b8-110">Die Zieladresse.</span><span class="sxs-lookup"><span data-stu-id="c98b8-110">The destination address.</span></span>

</dd> <dt>

<span data-ttu-id="c98b8-111">*Wert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c98b8-111">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c98b8-112">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c98b8-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c98b8-113">Der Eingabewert.</span><span class="sxs-lookup"><span data-stu-id="c98b8-113">The input value.</span></span>

</dd> <dt>

<span data-ttu-id="c98b8-114">*ursprünglicher \_ Wert* ausgehend \[\]</span><span class="sxs-lookup"><span data-stu-id="c98b8-114">*original\_value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c98b8-115">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c98b8-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c98b8-116">Der ursprüngliche Wert.</span><span class="sxs-lookup"><span data-stu-id="c98b8-116">The original value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c98b8-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c98b8-117">Return value</span></span>

<span data-ttu-id="c98b8-118">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="c98b8-118">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c98b8-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c98b8-119">Remarks</span></span>

<span data-ttu-id="c98b8-120">Dieser Vorgang kann nur für typisierte int-und uint-Ressourcen und Shared Memory-Variablen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="c98b8-120">This operation can only be performed on int and uint typed resources and shared memory variables.</span></span> <span data-ttu-id="c98b8-121">Es gibt drei Verwendungsmöglichkeiten für diese Funktion.</span><span class="sxs-lookup"><span data-stu-id="c98b8-121">There are three possible uses for this function.</span></span> <span data-ttu-id="c98b8-122">Der erste ist, wenn R ein Variablentyp für den gemeinsamen Speicher ist.</span><span class="sxs-lookup"><span data-stu-id="c98b8-122">The first is when R is a shared memory variable type.</span></span> <span data-ttu-id="c98b8-123">In diesem Fall führt die Funktion einen atomaren Maximalwert des Werts für das Shared Memory-Register aus, auf das von dest verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="c98b8-123">In this case, the function performs an atomic maximum of the value to the shared memory register referenced by dest.</span></span> <span data-ttu-id="c98b8-124">Das zweite Szenario ist, wenn R ein Ressourcen Variablentyp ist.</span><span class="sxs-lookup"><span data-stu-id="c98b8-124">The second scenario is when R is a resource variable type.</span></span> <span data-ttu-id="c98b8-125">In diesem Szenario führt die Funktion einen atomaren Maximalwert des Werts für den Ressourcen Speicherort aus, auf den "dest" verweist.</span><span class="sxs-lookup"><span data-stu-id="c98b8-125">In this scenario, the function performs an atomic maximum of the value to the resource location referenced by dest.</span></span> <span data-ttu-id="c98b8-126">Das dritte Szenario ist, dass R ein lokaler Variablentyp ist.</span><span class="sxs-lookup"><span data-stu-id="c98b8-126">Finally, the third scenario is when R is a local variable type.</span></span> <span data-ttu-id="c98b8-127">In diesem Szenario verringert die-Funktion den Höchstwert von "dest" und "Value", der in dest gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="c98b8-127">In this scenario, the function reduces to a maximum of the value of dest and value, stored in dest.</span></span> <span data-ttu-id="c98b8-128">Die überladene Funktion verfügt über eine zusätzliche Ausgabevariable, die auf den ursprünglichen Wert von dest festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="c98b8-128">The overloaded function has an additional output variable which will be set to the original value of dest.</span></span> <span data-ttu-id="c98b8-129">Dieser überladene Vorgang ist nur verfügbar, wenn R lesbar und beschreibbar ist.</span><span class="sxs-lookup"><span data-stu-id="c98b8-129">This overloaded operation is only available when R is readable and writable.</span></span>

<span data-ttu-id="c98b8-130">Diese Funktion wird in den folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="c98b8-130">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="c98b8-131">VS</span><span class="sxs-lookup"><span data-stu-id="c98b8-131">VS</span></span>  | <span data-ttu-id="c98b8-132">Jh</span><span class="sxs-lookup"><span data-stu-id="c98b8-132">HS</span></span>  | <span data-ttu-id="c98b8-133">DS</span><span class="sxs-lookup"><span data-stu-id="c98b8-133">DS</span></span>  | <span data-ttu-id="c98b8-134">GS</span><span class="sxs-lookup"><span data-stu-id="c98b8-134">GS</span></span>  | <span data-ttu-id="c98b8-135">PS</span><span class="sxs-lookup"><span data-stu-id="c98b8-135">PS</span></span>  | <span data-ttu-id="c98b8-136">CS</span><span class="sxs-lookup"><span data-stu-id="c98b8-136">CS</span></span>  |
|-----|-----|-----|-----|-----|-----|
| <span data-ttu-id="c98b8-137">x</span><span class="sxs-lookup"><span data-stu-id="c98b8-137">x</span></span>   | <span data-ttu-id="c98b8-138">x</span><span class="sxs-lookup"><span data-stu-id="c98b8-138">x</span></span>   | <span data-ttu-id="c98b8-139">x</span><span class="sxs-lookup"><span data-stu-id="c98b8-139">x</span></span>   | <span data-ttu-id="c98b8-140">x</span><span class="sxs-lookup"><span data-stu-id="c98b8-140">x</span></span>   | <span data-ttu-id="c98b8-141">x</span><span class="sxs-lookup"><span data-stu-id="c98b8-141">x</span></span>   | <span data-ttu-id="c98b8-142">x</span><span class="sxs-lookup"><span data-stu-id="c98b8-142">x</span></span>   |



 

## <a name="see-also"></a><span data-ttu-id="c98b8-143">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c98b8-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c98b8-144">Rwbyteaddressbuffer</span><span class="sxs-lookup"><span data-stu-id="c98b8-144">RWByteAddressBuffer</span></span>](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[<span data-ttu-id="c98b8-145">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="c98b8-145">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 