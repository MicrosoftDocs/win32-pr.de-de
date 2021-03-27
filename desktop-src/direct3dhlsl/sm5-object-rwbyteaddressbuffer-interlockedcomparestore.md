---
title: 'Rwbyteaddressbuffer:: interlockedcomparestore-Funktion'
description: Vergleicht die Eingabe atomarisch mit dem Vergleichswert.
ms.assetid: d82a73b6-24a5-4eb3-9f20-15ba263c93d0
keywords:
- Interlockedcomparestore-Funktion HLSL
topic_type:
- apiref
api_name:
- InterlockedCompareStore
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: abaa390ba74657e42b54a5147a7bc4006564a5fb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103858387"
---
# <a name="interlockedcomparestore-function"></a><span data-ttu-id="62236-104">Interlockedcomparestore-Funktion</span><span class="sxs-lookup"><span data-stu-id="62236-104">InterlockedCompareStore function</span></span>

<span data-ttu-id="62236-105">Vergleicht die Eingabe atomarisch mit dem Vergleichswert.</span><span class="sxs-lookup"><span data-stu-id="62236-105">Ccompares the input to the comparison value, atomically.</span></span>

## <a name="syntax"></a><span data-ttu-id="62236-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="62236-106">Syntax</span></span>

``` syntax
void InterlockedCompareStore(
  in UINT dest,
  in UINT compare_value,
  in UINT value
);
```

## <a name="parameters"></a><span data-ttu-id="62236-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="62236-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62236-108">*dest* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="62236-108">*dest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62236-109">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="62236-109">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="62236-110">Die Zieladresse.</span><span class="sxs-lookup"><span data-stu-id="62236-110">The destination address.</span></span>

</dd> <dt>

<span data-ttu-id="62236-111">*\_ Wert vergleichen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="62236-111">*compare\_value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62236-112">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="62236-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="62236-113">Der Vergleichswert.</span><span class="sxs-lookup"><span data-stu-id="62236-113">The comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="62236-114">*Wert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="62236-114">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62236-115">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="62236-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="62236-116">Der Eingabewert.</span><span class="sxs-lookup"><span data-stu-id="62236-116">The input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62236-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="62236-117">Return value</span></span>

<span data-ttu-id="62236-118">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="62236-118">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="62236-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="62236-119">Remarks</span></span>

<span data-ttu-id="62236-120">Dieser Vorgang kann nur für typisierte int-oder uint-Ressourcen und Shared Memory-Variablen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="62236-120">This operation can only be performed on int or uint typed resources and shared memory variables.</span></span> <span data-ttu-id="62236-121">Es gibt drei Verwendungsmöglichkeiten für diese Funktion.</span><span class="sxs-lookup"><span data-stu-id="62236-121">There are three possible uses for this function.</span></span> <span data-ttu-id="62236-122">Der erste ist, wenn R ein Variablentyp für den gemeinsamen Speicher ist.</span><span class="sxs-lookup"><span data-stu-id="62236-122">The first is when R is a shared memory variable type.</span></span> <span data-ttu-id="62236-123">In diesem Fall führt die Funktion den Vorgang für das Shared Memory-Register aus, auf das von dest verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="62236-123">In this case, the function performs the operation on the shared memory register referenced by dest.</span></span> <span data-ttu-id="62236-124">Das zweite Szenario ist, wenn R ein Ressourcen Variablentyp ist.</span><span class="sxs-lookup"><span data-stu-id="62236-124">The second scenario is when R is a resource variable type.</span></span> <span data-ttu-id="62236-125">In diesem Szenario führt die Funktion den Vorgang an dem Ressourcen Speicherort aus, auf den "dest" verweist.</span><span class="sxs-lookup"><span data-stu-id="62236-125">In this scenario, the function performs the operation on the resource location referenced by dest.</span></span> <span data-ttu-id="62236-126">Das dritte Szenario ist, dass R ein lokaler Variablentyp ist.</span><span class="sxs-lookup"><span data-stu-id="62236-126">Finally, the third scenario is when R is a local variable type.</span></span> <span data-ttu-id="62236-127">In diesem Szenario wird die Funktion auf den Vorgang reduziert, der mit lokalen Vorgängen ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="62236-127">In this scenario, the function reduces to the operation performed using local operations.</span></span>

<span data-ttu-id="62236-128">Diese Funktion wird in den folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="62236-128">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="62236-129">VS</span><span class="sxs-lookup"><span data-stu-id="62236-129">VS</span></span>  | <span data-ttu-id="62236-130">Jh</span><span class="sxs-lookup"><span data-stu-id="62236-130">HS</span></span>  | <span data-ttu-id="62236-131">DS</span><span class="sxs-lookup"><span data-stu-id="62236-131">DS</span></span>  | <span data-ttu-id="62236-132">GS</span><span class="sxs-lookup"><span data-stu-id="62236-132">GS</span></span>  | <span data-ttu-id="62236-133">PS</span><span class="sxs-lookup"><span data-stu-id="62236-133">PS</span></span>  | <span data-ttu-id="62236-134">CS</span><span class="sxs-lookup"><span data-stu-id="62236-134">CS</span></span>  |
|-----|-----|-----|-----|-----|-----|
| <span data-ttu-id="62236-135">x</span><span class="sxs-lookup"><span data-stu-id="62236-135">x</span></span>   | <span data-ttu-id="62236-136">x</span><span class="sxs-lookup"><span data-stu-id="62236-136">x</span></span>   | <span data-ttu-id="62236-137">x</span><span class="sxs-lookup"><span data-stu-id="62236-137">x</span></span>   | <span data-ttu-id="62236-138">x</span><span class="sxs-lookup"><span data-stu-id="62236-138">x</span></span>   | <span data-ttu-id="62236-139">x</span><span class="sxs-lookup"><span data-stu-id="62236-139">x</span></span>   | <span data-ttu-id="62236-140">x</span><span class="sxs-lookup"><span data-stu-id="62236-140">x</span></span>   |



 

## <a name="see-also"></a><span data-ttu-id="62236-141">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="62236-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62236-142">Rwbyteaddressbuffer</span><span class="sxs-lookup"><span data-stu-id="62236-142">RWByteAddressBuffer</span></span>](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[<span data-ttu-id="62236-143">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="62236-143">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 