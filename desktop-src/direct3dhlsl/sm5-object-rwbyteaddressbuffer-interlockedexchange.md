---
title: 'Rwbyteaddressbuffer:: interlockedexchange-Funktion'
description: Tauscht einen Wert atomarisch aus.
ms.assetid: a50f4cba-a7a2-44b0-9de7-003b4c7a947f
keywords:
- Interlockedexchange-Funktion HLSL
topic_type:
- apiref
api_name:
- InterlockedExchange
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 47c51374b7dcd62ac208e0aa8811a8d693ce0ac6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104993351"
---
# <a name="interlockedexchange-function"></a><span data-ttu-id="8ad9e-104">Interlockedexchange-Funktion</span><span class="sxs-lookup"><span data-stu-id="8ad9e-104">InterlockedExchange function</span></span>

<span data-ttu-id="8ad9e-105">Tauscht einen Wert atomarisch aus.</span><span class="sxs-lookup"><span data-stu-id="8ad9e-105">Exchanges a value, atomically.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ad9e-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="8ad9e-106">Syntax</span></span>

``` syntax
void InterlockedExchange(
  in  UINT dest,
  in  UINT value,
  out UINT original_value
);
```

## <a name="parameters"></a><span data-ttu-id="8ad9e-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="8ad9e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ad9e-108">*dest* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8ad9e-108">*dest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ad9e-109">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="8ad9e-109">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="8ad9e-110">Die Zieladresse.</span><span class="sxs-lookup"><span data-stu-id="8ad9e-110">The destination address.</span></span>

</dd> <dt>

<span data-ttu-id="8ad9e-111">*Wert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8ad9e-111">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ad9e-112">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="8ad9e-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="8ad9e-113">Der Eingabewert.</span><span class="sxs-lookup"><span data-stu-id="8ad9e-113">The input value.</span></span>

</dd> <dt>

<span data-ttu-id="8ad9e-114">*ursprünglicher \_ Wert* ausgehend \[\]</span><span class="sxs-lookup"><span data-stu-id="8ad9e-114">*original\_value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8ad9e-115">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="8ad9e-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="8ad9e-116">Der ursprüngliche Wert.</span><span class="sxs-lookup"><span data-stu-id="8ad9e-116">The original value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ad9e-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8ad9e-117">Return value</span></span>

<span data-ttu-id="8ad9e-118">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="8ad9e-118">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ad9e-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8ad9e-119">Remarks</span></span>

<span data-ttu-id="8ad9e-120">Dieser Vorgang kann nur für skalartypisierte Ressourcen und Shared Memory-Variablen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="8ad9e-120">This operation can only be performed on scalar-typed resources and shared memory variables.</span></span> <span data-ttu-id="8ad9e-121">Es gibt drei Verwendungsmöglichkeiten für diese Funktion.</span><span class="sxs-lookup"><span data-stu-id="8ad9e-121">There are three possible uses for this function.</span></span> <span data-ttu-id="8ad9e-122">Der erste ist, wenn R ein Variablentyp für den gemeinsamen Speicher ist.</span><span class="sxs-lookup"><span data-stu-id="8ad9e-122">The first is when R is a shared memory variable type.</span></span> <span data-ttu-id="8ad9e-123">In diesem Fall führt die Funktion den Vorgang für das Shared Memory-Register aus, auf das von dest verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="8ad9e-123">In this case, the function performs the operation on the shared memory register referenced by dest.</span></span> <span data-ttu-id="8ad9e-124">Das zweite Szenario ist, wenn R ein Ressourcen Variablentyp ist.</span><span class="sxs-lookup"><span data-stu-id="8ad9e-124">The second scenario is when R is a resource variable type.</span></span> <span data-ttu-id="8ad9e-125">In diesem Szenario führt die Funktion den Vorgang an dem Ressourcen Speicherort aus, auf den "dest" verweist.</span><span class="sxs-lookup"><span data-stu-id="8ad9e-125">In this scenario, the function performs the operation on the resource location referenced by dest.</span></span> <span data-ttu-id="8ad9e-126">Das dritte Szenario ist, dass R ein lokaler Variablentyp ist.</span><span class="sxs-lookup"><span data-stu-id="8ad9e-126">Finally, the third scenario is when R is a local variable type.</span></span> <span data-ttu-id="8ad9e-127">In diesem Szenario wird die Funktion auf den Vorgang reduziert, der mit lokalen Vorgängen ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8ad9e-127">In this scenario, the function reduces to the operation performed using local operations.</span></span> <span data-ttu-id="8ad9e-128">Dieser Vorgang ist nur verfügbar, wenn R lesbar und beschreibbar ist.</span><span class="sxs-lookup"><span data-stu-id="8ad9e-128">This operation is only available when R is readable and writable.</span></span>

<span data-ttu-id="8ad9e-129">Diese Funktion wird in den folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="8ad9e-129">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="8ad9e-130">VS</span><span class="sxs-lookup"><span data-stu-id="8ad9e-130">VS</span></span>  | <span data-ttu-id="8ad9e-131">Jh</span><span class="sxs-lookup"><span data-stu-id="8ad9e-131">HS</span></span>  | <span data-ttu-id="8ad9e-132">DS</span><span class="sxs-lookup"><span data-stu-id="8ad9e-132">DS</span></span>  | <span data-ttu-id="8ad9e-133">GS</span><span class="sxs-lookup"><span data-stu-id="8ad9e-133">GS</span></span>  | <span data-ttu-id="8ad9e-134">PS</span><span class="sxs-lookup"><span data-stu-id="8ad9e-134">PS</span></span>  | <span data-ttu-id="8ad9e-135">CS</span><span class="sxs-lookup"><span data-stu-id="8ad9e-135">CS</span></span>  |
|-----|-----|-----|-----|-----|-----|
|  <span data-ttu-id="8ad9e-136">x</span><span class="sxs-lookup"><span data-stu-id="8ad9e-136">x</span></span>  |  <span data-ttu-id="8ad9e-137">x</span><span class="sxs-lookup"><span data-stu-id="8ad9e-137">x</span></span>  |  <span data-ttu-id="8ad9e-138">x</span><span class="sxs-lookup"><span data-stu-id="8ad9e-138">x</span></span>  |  <span data-ttu-id="8ad9e-139">x</span><span class="sxs-lookup"><span data-stu-id="8ad9e-139">x</span></span>  | <span data-ttu-id="8ad9e-140">x</span><span class="sxs-lookup"><span data-stu-id="8ad9e-140">x</span></span>   | <span data-ttu-id="8ad9e-141">x</span><span class="sxs-lookup"><span data-stu-id="8ad9e-141">x</span></span>   |



 

## <a name="see-also"></a><span data-ttu-id="8ad9e-142">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="8ad9e-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ad9e-143">Rwbyteaddressbuffer</span><span class="sxs-lookup"><span data-stu-id="8ad9e-143">RWByteAddressBuffer</span></span>](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[<span data-ttu-id="8ad9e-144">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="8ad9e-144">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 