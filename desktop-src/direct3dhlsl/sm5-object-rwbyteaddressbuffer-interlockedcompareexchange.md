---
title: 'Rwbyteaddressbuffer:: interlockedcompareexchange-Funktion'
description: Vergleicht die Eingabe mit dem Vergleichswert und tauscht das Ergebnis atomarisch aus.
ms.assetid: 9d6e8d95-5157-49a7-8a79-f3ca6ba87ebb
keywords:
- Interlockedcompareexchange-Funktion HLSL
topic_type:
- apiref
api_name:
- InterlockedCompareExchange
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 18c7e5d58fe926d09e7ec48ee12a2336627d5db2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729144"
---
# <a name="interlockedcompareexchange-function"></a><span data-ttu-id="b2acb-104">Interlockedcompareexchange-Funktion</span><span class="sxs-lookup"><span data-stu-id="b2acb-104">InterlockedCompareExchange function</span></span>

<span data-ttu-id="b2acb-105">Vergleicht die Eingabe mit dem Vergleichswert und tauscht das Ergebnis atomarisch aus.</span><span class="sxs-lookup"><span data-stu-id="b2acb-105">Compares the input to the comparison value and exchanges the result, atomically.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2acb-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="b2acb-106">Syntax</span></span>

``` syntax
void InterlockedCompareExchange(
  in  UINT dest,
  in  UINT compare_value,
  in  UINT value,
  out UINT original_value
);
```

## <a name="parameters"></a><span data-ttu-id="b2acb-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="b2acb-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2acb-108">*dest* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b2acb-108">*dest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2acb-109">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b2acb-109">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="b2acb-110">Die Zieladresse.</span><span class="sxs-lookup"><span data-stu-id="b2acb-110">The destination address.</span></span>

</dd> <dt>

<span data-ttu-id="b2acb-111">*\_ Wert vergleichen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b2acb-111">*compare\_value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2acb-112">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b2acb-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="b2acb-113">Der Vergleichswert.</span><span class="sxs-lookup"><span data-stu-id="b2acb-113">The comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="b2acb-114">*Wert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b2acb-114">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2acb-115">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b2acb-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="b2acb-116">Der Eingabewert.</span><span class="sxs-lookup"><span data-stu-id="b2acb-116">The input value.</span></span>

</dd> <dt>

<span data-ttu-id="b2acb-117">*ursprünglicher \_ Wert* ausgehend \[\]</span><span class="sxs-lookup"><span data-stu-id="b2acb-117">*original\_value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b2acb-118">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b2acb-118">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="b2acb-119">Der ursprüngliche Wert.</span><span class="sxs-lookup"><span data-stu-id="b2acb-119">The original value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2acb-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b2acb-120">Return value</span></span>

<span data-ttu-id="b2acb-121">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="b2acb-121">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b2acb-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b2acb-122">Remarks</span></span>

<span data-ttu-id="b2acb-123">Vergleicht atomisch den Wert von " *dest* " mit dem *Vergleichs \_ Wert*, speichert den Wert in " *dest* ", wenn die Werte entsprechen, und gibt den ursprünglichen Wert von " *dest* " im *ursprünglichen \_ Wert* zurück</span><span class="sxs-lookup"><span data-stu-id="b2acb-123">Atomically compares the value in *dest* to *compare\_value*, stores value in *dest* if the values match, returns the original value of *dest* in *original\_value*.</span></span> <span data-ttu-id="b2acb-124">Dieser Vorgang kann nur für typisierte **int** -oder *uint* -Ressourcen und Shared Memory-Variablen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="b2acb-124">This operation can only be performed on **int** or *uint* typed resources and shared memory variables.</span></span> <span data-ttu-id="b2acb-125">Es gibt drei Verwendungsmöglichkeiten für diese Funktion.</span><span class="sxs-lookup"><span data-stu-id="b2acb-125">There are three possible uses for this function.</span></span> <span data-ttu-id="b2acb-126">Der erste ist, wenn R ein Variablentyp für den gemeinsamen Speicher ist.</span><span class="sxs-lookup"><span data-stu-id="b2acb-126">The first is when R is a shared memory variable type.</span></span> <span data-ttu-id="b2acb-127">In diesem Fall führt die Funktion den Vorgang für das Shared Memory-Register aus, auf das von *dest* verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="b2acb-127">In this case, the function performs the operation on the shared memory register referenced by *dest*.</span></span> <span data-ttu-id="b2acb-128">Das zweite Szenario ist, wenn R ein Ressourcen Variablentyp ist.</span><span class="sxs-lookup"><span data-stu-id="b2acb-128">The second scenario is when R is a resource variable type.</span></span> <span data-ttu-id="b2acb-129">In diesem Szenario führt die Funktion den Vorgang an dem Ressourcen Speicherort aus, auf den " *dest*" verweist.</span><span class="sxs-lookup"><span data-stu-id="b2acb-129">In this scenario, the function performs the operation on the resource location referenced by *dest*.</span></span> <span data-ttu-id="b2acb-130">Das dritte Szenario ist, dass R ein lokaler Variablentyp ist.</span><span class="sxs-lookup"><span data-stu-id="b2acb-130">Finally, the third scenario is when R is a local variable type.</span></span> <span data-ttu-id="b2acb-131">In diesem Szenario wird die Funktion auf den Vorgang reduziert, der mit lokalen Vorgängen ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b2acb-131">In this scenario, the function reduces to the operation performed using local operations.</span></span> <span data-ttu-id="b2acb-132">Dieser Vorgang ist nur verfügbar, wenn R lesbar und beschreibbar ist.</span><span class="sxs-lookup"><span data-stu-id="b2acb-132">This operation is only available when R is readable and writable.</span></span>

> [!Note]  
> <span data-ttu-id="b2acb-133">Wenn Sie in einer [**for**](dx-graphics-hlsl-for.md) -oder [**while**](dx-graphics-hlsl-while.md) -Compute-Shader-Schleife **interlockedcompareexchange** aufrufen, müssen Sie für die ordnungsgemäße Kompilierung das Attribut " **\[ \_ UAV- \_ \] Bedingung zulassen** " in dieser Schleife verwenden.</span><span class="sxs-lookup"><span data-stu-id="b2acb-133">If you call **InterlockedCompareExchange** in a [**for**](dx-graphics-hlsl-for.md) or [**while**](dx-graphics-hlsl-while.md) compute shader loop, to properly compile, you must use the **\[allow\_uav\_condition\]** attribute on that loop.</span></span>

 

<span data-ttu-id="b2acb-134">Diese Funktion wird in den folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="b2acb-134">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="b2acb-135">VS</span><span class="sxs-lookup"><span data-stu-id="b2acb-135">VS</span></span>  | <span data-ttu-id="b2acb-136">Jh</span><span class="sxs-lookup"><span data-stu-id="b2acb-136">HS</span></span>  | <span data-ttu-id="b2acb-137">DS</span><span class="sxs-lookup"><span data-stu-id="b2acb-137">DS</span></span>  | <span data-ttu-id="b2acb-138">GS</span><span class="sxs-lookup"><span data-stu-id="b2acb-138">GS</span></span>  | <span data-ttu-id="b2acb-139">PS</span><span class="sxs-lookup"><span data-stu-id="b2acb-139">PS</span></span>  | <span data-ttu-id="b2acb-140">CS</span><span class="sxs-lookup"><span data-stu-id="b2acb-140">CS</span></span>  |
|-----|-----|-----|-----|-----|-----|
| <span data-ttu-id="b2acb-141">x</span><span class="sxs-lookup"><span data-stu-id="b2acb-141">x</span></span>   | <span data-ttu-id="b2acb-142">x</span><span class="sxs-lookup"><span data-stu-id="b2acb-142">x</span></span>   | <span data-ttu-id="b2acb-143">x</span><span class="sxs-lookup"><span data-stu-id="b2acb-143">x</span></span>   | <span data-ttu-id="b2acb-144">x</span><span class="sxs-lookup"><span data-stu-id="b2acb-144">x</span></span>   | <span data-ttu-id="b2acb-145">x</span><span class="sxs-lookup"><span data-stu-id="b2acb-145">x</span></span>   | <span data-ttu-id="b2acb-146">x</span><span class="sxs-lookup"><span data-stu-id="b2acb-146">x</span></span>   |



 

## <a name="see-also"></a><span data-ttu-id="b2acb-147">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b2acb-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2acb-148">Rwbyteaddressbuffer</span><span class="sxs-lookup"><span data-stu-id="b2acb-148">RWByteAddressBuffer</span></span>](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[<span data-ttu-id="b2acb-149">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="b2acb-149">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 