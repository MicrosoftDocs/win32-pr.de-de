---
title: 'Rwbyteaddressbuffer:: interlockedxor-Funktion'
description: Führt einen atomaren XOR-Wert für den Wert aus.
ms.assetid: 692f8b5e-a81e-4700-8a8d-3594aba85671
keywords:
- Interlockedxor-Funktion HLSL
topic_type:
- apiref
api_name:
- InterlockedXor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 920ae912c599b66a03a25d7bc8ecc9b199036b26
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948762"
---
# <a name="interlockedxor-function"></a><span data-ttu-id="25c2e-104">Interlockedxor-Funktion</span><span class="sxs-lookup"><span data-stu-id="25c2e-104">InterlockedXor function</span></span>

<span data-ttu-id="25c2e-105">Führt einen atomaren **Xor** -Wert für den Wert aus.</span><span class="sxs-lookup"><span data-stu-id="25c2e-105">Performs an atomic **XOR** on the value.</span></span>

## <a name="syntax"></a><span data-ttu-id="25c2e-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="25c2e-106">Syntax</span></span>

``` syntax
void InterlockedXor(
  in  UINT dest,
  in  UINT value,
  out UINT original_value
);
```

## <a name="parameters"></a><span data-ttu-id="25c2e-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="25c2e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25c2e-108">*dest* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="25c2e-108">*dest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25c2e-109">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="25c2e-109">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="25c2e-110">Die Zieladresse.</span><span class="sxs-lookup"><span data-stu-id="25c2e-110">The destination address.</span></span>

</dd> <dt>

<span data-ttu-id="25c2e-111">*Wert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="25c2e-111">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25c2e-112">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="25c2e-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="25c2e-113">Der Eingabewert.</span><span class="sxs-lookup"><span data-stu-id="25c2e-113">The input value.</span></span>

</dd> <dt>

<span data-ttu-id="25c2e-114">*ursprünglicher \_ Wert* ausgehend \[\]</span><span class="sxs-lookup"><span data-stu-id="25c2e-114">*original\_value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="25c2e-115">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="25c2e-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="25c2e-116">Der ursprüngliche Wert.</span><span class="sxs-lookup"><span data-stu-id="25c2e-116">The original value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25c2e-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="25c2e-117">Return value</span></span>

<span data-ttu-id="25c2e-118">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="25c2e-118">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="25c2e-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="25c2e-119">Remarks</span></span>

<span data-ttu-id="25c2e-120">Dieser Vorgang kann nur für typisierte **int** -oder **uint** -Ressourcen und Shared Memory-Variablen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="25c2e-120">This operation can be performed only on **INT** or **UINT** typed resources and shared memory variables.</span></span> <span data-ttu-id="25c2e-121">Es gibt drei Verwendungsmöglichkeiten für diese Funktion.</span><span class="sxs-lookup"><span data-stu-id="25c2e-121">There are three possible uses for this function.</span></span> <span data-ttu-id="25c2e-122">Der erste ist, wenn R ein Variablentyp für den gemeinsamen Speicher ist.</span><span class="sxs-lookup"><span data-stu-id="25c2e-122">The first is when R is a shared memory variable type.</span></span> <span data-ttu-id="25c2e-123">In diesem Fall führt die Funktion einen atomaren **Xor** -Wert mit dem Wert des freigegebenen Speicher Registers aus, auf das von *dest* verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="25c2e-123">In this case, the function performs an atomic **XOR** with the value of the shared memory register referenced by *dest*.</span></span> <span data-ttu-id="25c2e-124">Das zweite Szenario ist, wenn R ein Ressourcen Variablentyp ist.</span><span class="sxs-lookup"><span data-stu-id="25c2e-124">The second scenario is when R is a resource variable type.</span></span> <span data-ttu-id="25c2e-125">In diesem Szenario führt die-Funktion einen atomaren **Xor** -Wert mit dem Wert des Ressourcen Speicher Orts aus, auf den " *dest*" verweist.</span><span class="sxs-lookup"><span data-stu-id="25c2e-125">In this scenario, the function performs an atomic **XOR** with the value of the resource location referenced by *dest*.</span></span> <span data-ttu-id="25c2e-126">Das dritte Szenario ist, dass R ein lokaler Variablentyp ist.</span><span class="sxs-lookup"><span data-stu-id="25c2e-126">Finally, the third scenario is when R is a local variable type.</span></span> <span data-ttu-id="25c2e-127">In diesem Szenario wird die Funktion auf einen **Xor** -Wert der Werte " *dest* " und " *value*" reduziert.</span><span class="sxs-lookup"><span data-stu-id="25c2e-127">In this scenario, the function reduces to an **XOR** of the values of *dest* and *value*.</span></span> <span data-ttu-id="25c2e-128">Das Ergebnis des Vorgangs ersetzt den Wert in *dest*.</span><span class="sxs-lookup"><span data-stu-id="25c2e-128">The result of the operation replaces the value in *dest*.</span></span> <span data-ttu-id="25c2e-129">Die überladene Funktion verfügt über eine zusätzliche Ausgabevariable, die auf den ursprünglichen Wert von *dest* festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="25c2e-129">The overloaded function has an additional output variable which will be set to the original value of *dest*.</span></span> <span data-ttu-id="25c2e-130">Dieser überladene Vorgang ist nur verfügbar, wenn R lesbar und beschreibbar ist.</span><span class="sxs-lookup"><span data-stu-id="25c2e-130">This overloaded operation is available only when R is readable and writable.</span></span>

<span data-ttu-id="25c2e-131">Diese Funktion wird in den folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="25c2e-131">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="25c2e-132">VS</span><span class="sxs-lookup"><span data-stu-id="25c2e-132">VS</span></span>  | <span data-ttu-id="25c2e-133">Jh</span><span class="sxs-lookup"><span data-stu-id="25c2e-133">HS</span></span>  | <span data-ttu-id="25c2e-134">DS</span><span class="sxs-lookup"><span data-stu-id="25c2e-134">DS</span></span>  | <span data-ttu-id="25c2e-135">GS</span><span class="sxs-lookup"><span data-stu-id="25c2e-135">GS</span></span>  | <span data-ttu-id="25c2e-136">PS</span><span class="sxs-lookup"><span data-stu-id="25c2e-136">PS</span></span>  | <span data-ttu-id="25c2e-137">CS</span><span class="sxs-lookup"><span data-stu-id="25c2e-137">CS</span></span>  |
|-----|-----|-----|-----|-----|-----|
| <span data-ttu-id="25c2e-138">x</span><span class="sxs-lookup"><span data-stu-id="25c2e-138">x</span></span>   |  <span data-ttu-id="25c2e-139">x</span><span class="sxs-lookup"><span data-stu-id="25c2e-139">x</span></span>  | <span data-ttu-id="25c2e-140">x</span><span class="sxs-lookup"><span data-stu-id="25c2e-140">x</span></span>   | <span data-ttu-id="25c2e-141">x</span><span class="sxs-lookup"><span data-stu-id="25c2e-141">x</span></span>   | <span data-ttu-id="25c2e-142">x</span><span class="sxs-lookup"><span data-stu-id="25c2e-142">x</span></span>   | <span data-ttu-id="25c2e-143">x</span><span class="sxs-lookup"><span data-stu-id="25c2e-143">x</span></span>   |



 

## <a name="see-also"></a><span data-ttu-id="25c2e-144">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="25c2e-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25c2e-145">Rwbyteaddressbuffer</span><span class="sxs-lookup"><span data-stu-id="25c2e-145">RWByteAddressBuffer</span></span>](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[<span data-ttu-id="25c2e-146">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="25c2e-146">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 