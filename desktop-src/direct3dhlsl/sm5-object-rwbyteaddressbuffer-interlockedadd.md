---
title: 'Rwbyteaddressbuffer:: interlockedadd-Funktion'
description: Fügt den Wert atomisch hinzu.
ms.assetid: 27274aae-1e75-4626-9997-57c4e9393000
keywords:
- Interlockedadd-Funktion HLSL
topic_type:
- apiref
api_name:
- InterlockedAdd
api_location:
- winnt.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d352ed97df15ce076c10950c6da94aaeaff0f2d0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104993414"
---
# <a name="interlockedadd-function"></a><span data-ttu-id="ebcf4-104">Interlockedadd-Funktion</span><span class="sxs-lookup"><span data-stu-id="ebcf4-104">InterlockedAdd function</span></span>

<span data-ttu-id="ebcf4-105">Fügt den Wert atomisch hinzu.</span><span class="sxs-lookup"><span data-stu-id="ebcf4-105">Adds the value, atomically.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebcf4-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="ebcf4-106">Syntax</span></span>

``` syntax
void InterlockedAdd(
  in  UINT dest,
  in  UINT value,
  out UINT original_value
);
```

## <a name="parameters"></a><span data-ttu-id="ebcf4-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="ebcf4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ebcf4-108">*dest* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ebcf4-108">*dest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ebcf4-109">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ebcf4-109">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="ebcf4-110">Die Zieladresse.</span><span class="sxs-lookup"><span data-stu-id="ebcf4-110">The destination address.</span></span>

</dd> <dt>

<span data-ttu-id="ebcf4-111">*Wert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ebcf4-111">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ebcf4-112">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ebcf4-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="ebcf4-113">Der Eingabewert.</span><span class="sxs-lookup"><span data-stu-id="ebcf4-113">The input value.</span></span>

</dd> <dt>

<span data-ttu-id="ebcf4-114">*ursprünglicher \_ Wert* ausgehend \[\]</span><span class="sxs-lookup"><span data-stu-id="ebcf4-114">*original\_value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ebcf4-115">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ebcf4-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="ebcf4-116">Der ursprüngliche Wert.</span><span class="sxs-lookup"><span data-stu-id="ebcf4-116">The original value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ebcf4-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ebcf4-117">Return value</span></span>

<span data-ttu-id="ebcf4-118">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="ebcf4-118">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ebcf4-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ebcf4-119">Remarks</span></span>

<span data-ttu-id="ebcf4-120">Dieser Vorgang kann nur für typisierte int-oder uint-Ressourcen und Shared Memory-Variablen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="ebcf4-120">This operation can be performed only on int or uint typed resources and shared memory variables.</span></span> <span data-ttu-id="ebcf4-121">Es gibt drei Verwendungsmöglichkeiten für diese Funktion.</span><span class="sxs-lookup"><span data-stu-id="ebcf4-121">There are three possible uses for this function.</span></span> <span data-ttu-id="ebcf4-122">Der erste ist, wenn R ein Variablentyp für den gemeinsamen Speicher ist.</span><span class="sxs-lookup"><span data-stu-id="ebcf4-122">The first is when R is a shared memory variable type.</span></span> <span data-ttu-id="ebcf4-123">In diesem Fall führt die Funktion einen atomaren Add of-Wert für das Shared Memory-Register aus, auf das von dest verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="ebcf4-123">In this case, the function performs an atomic add of value to the shared memory register referenced by dest.</span></span> <span data-ttu-id="ebcf4-124">Das zweite Szenario ist, wenn R ein Ressourcen Variablentyp ist.</span><span class="sxs-lookup"><span data-stu-id="ebcf4-124">The second scenario is when R is a resource variable type.</span></span> <span data-ttu-id="ebcf4-125">In diesem Szenario führt die Funktion eine atomarische Ergänzung des Werts für den Ressourcen Speicherort aus, auf den von dest verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="ebcf4-125">In this scenario, the function performs an atomic add of the value to the resource location referenced by dest.</span></span> <span data-ttu-id="ebcf4-126">Das dritte Szenario ist, dass R ein lokaler Variablentyp ist.</span><span class="sxs-lookup"><span data-stu-id="ebcf4-126">Finally, the third scenario is when R is a local variable type.</span></span> <span data-ttu-id="ebcf4-127">In diesem Szenario wird die-Funktion auf eine Summe des Werts "dest" und "Value" reduziert, die in dest gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="ebcf4-127">In this scenario, the function reduces to a sum of the value of dest and value, stored in dest.</span></span> <span data-ttu-id="ebcf4-128">Die überladene Funktion verfügt über eine zusätzliche Ausgabevariable, die auf den ursprünglichen Wert von dest festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="ebcf4-128">The overloaded function has an additional output variable which will be set to the original value of dest.</span></span> <span data-ttu-id="ebcf4-129">Dieser überladene Vorgang ist nur verfügbar, wenn R lesbar und beschreibbar ist.</span><span class="sxs-lookup"><span data-stu-id="ebcf4-129">This overloaded operation is only available when R is readable and writable.</span></span>

<span data-ttu-id="ebcf4-130">Diese Funktion wird in den folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="ebcf4-130">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="ebcf4-131">VS</span><span class="sxs-lookup"><span data-stu-id="ebcf4-131">VS</span></span>  | <span data-ttu-id="ebcf4-132">Jh</span><span class="sxs-lookup"><span data-stu-id="ebcf4-132">HS</span></span>  | <span data-ttu-id="ebcf4-133">DS</span><span class="sxs-lookup"><span data-stu-id="ebcf4-133">DS</span></span>  | <span data-ttu-id="ebcf4-134">GS</span><span class="sxs-lookup"><span data-stu-id="ebcf4-134">GS</span></span>  | <span data-ttu-id="ebcf4-135">PS</span><span class="sxs-lookup"><span data-stu-id="ebcf4-135">PS</span></span>  | <span data-ttu-id="ebcf4-136">CS</span><span class="sxs-lookup"><span data-stu-id="ebcf4-136">CS</span></span>  |
|-----|-----|-----|-----|-----|-----|
| <span data-ttu-id="ebcf4-137">x</span><span class="sxs-lookup"><span data-stu-id="ebcf4-137">x</span></span>   | <span data-ttu-id="ebcf4-138">x</span><span class="sxs-lookup"><span data-stu-id="ebcf4-138">x</span></span>   | <span data-ttu-id="ebcf4-139">x</span><span class="sxs-lookup"><span data-stu-id="ebcf4-139">x</span></span>   | <span data-ttu-id="ebcf4-140">x</span><span class="sxs-lookup"><span data-stu-id="ebcf4-140">x</span></span>   | <span data-ttu-id="ebcf4-141">x</span><span class="sxs-lookup"><span data-stu-id="ebcf4-141">x</span></span>   | <span data-ttu-id="ebcf4-142">x</span><span class="sxs-lookup"><span data-stu-id="ebcf4-142">x</span></span>   |



 

## <a name="requirements"></a><span data-ttu-id="ebcf4-143">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="ebcf4-143">Requirements</span></span>




## <a name="see-also"></a><span data-ttu-id="ebcf4-144">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ebcf4-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebcf4-145">Rwbyteaddressbuffer</span><span class="sxs-lookup"><span data-stu-id="ebcf4-145">RWByteAddressBuffer</span></span>](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[<span data-ttu-id="ebcf4-146">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="ebcf4-146">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

