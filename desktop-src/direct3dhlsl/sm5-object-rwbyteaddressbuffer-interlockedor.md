---
title: 'Rwbyteaddressbuffer:: interlockedor-Funktion'
description: Führt eine atomarische oder für den Wert aus.
ms.assetid: 3a05619b-db97-4cf1-af3c-12c376e605a6
keywords:
- Interlockedor-Funktion HLSL
topic_type:
- apiref
api_name:
- InterlockedOr
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 14b902f70919c79ed3e313671ede709f284a1490
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948763"
---
# <a name="interlockedor-function"></a><span data-ttu-id="018ef-104">Interlockedor-Funktion</span><span class="sxs-lookup"><span data-stu-id="018ef-104">InterlockedOr function</span></span>

<span data-ttu-id="018ef-105">Führt eine atomarische **oder** für den Wert aus.</span><span class="sxs-lookup"><span data-stu-id="018ef-105">Performs an atomic **OR** on the value.</span></span>

## <a name="syntax"></a><span data-ttu-id="018ef-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="018ef-106">Syntax</span></span>

``` syntax
void InterlockedOr(
  in  UINT dest,
  in  UINT value,
  out UINT original_value
);
```

## <a name="parameters"></a><span data-ttu-id="018ef-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="018ef-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="018ef-108">*dest* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="018ef-108">*dest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="018ef-109">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="018ef-109">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="018ef-110">Die Zieladresse.</span><span class="sxs-lookup"><span data-stu-id="018ef-110">The destination address.</span></span>

</dd> <dt>

<span data-ttu-id="018ef-111">*Wert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="018ef-111">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="018ef-112">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="018ef-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="018ef-113">Der Eingabewert.</span><span class="sxs-lookup"><span data-stu-id="018ef-113">The input value.</span></span>

</dd> <dt>

<span data-ttu-id="018ef-114">*ursprünglicher \_ Wert* ausgehend \[\]</span><span class="sxs-lookup"><span data-stu-id="018ef-114">*original\_value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="018ef-115">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="018ef-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="018ef-116">Der ursprüngliche Wert.</span><span class="sxs-lookup"><span data-stu-id="018ef-116">The original value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="018ef-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="018ef-117">Return value</span></span>

<span data-ttu-id="018ef-118">Nichts</span><span class="sxs-lookup"><span data-stu-id="018ef-118">Nothing</span></span>

## <a name="remarks"></a><span data-ttu-id="018ef-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="018ef-119">Remarks</span></span>

<span data-ttu-id="018ef-120">Dieser Vorgang kann nur für typisierte **int** -oder **uint** -Ressourcen und Shared Memory-Variablen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="018ef-120">This operation can be performed only on **INT** or **UINT** typed resources and shared memory variables.</span></span> <span data-ttu-id="018ef-121">Es gibt drei Verwendungsmöglichkeiten für diese Funktion.</span><span class="sxs-lookup"><span data-stu-id="018ef-121">There are three possible uses for this function.</span></span> <span data-ttu-id="018ef-122">Der erste ist, wenn R ein Variablentyp für den gemeinsamen Speicher ist.</span><span class="sxs-lookup"><span data-stu-id="018ef-122">The first is when R is a shared memory variable type.</span></span> <span data-ttu-id="018ef-123">In diesem Fall führt die Funktion eine atomarische **or** -Funktion mit dem Wert des Shared Memory-Registers aus, auf das von *dest* verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="018ef-123">In this case, the function performs an atomic **OR** with the value of the shared memory register referenced by *dest*.</span></span> <span data-ttu-id="018ef-124">Das zweite Szenario ist, wenn R ein Ressourcen Variablentyp ist.</span><span class="sxs-lookup"><span data-stu-id="018ef-124">The second scenario is when R is a resource variable type.</span></span> <span data-ttu-id="018ef-125">In diesem Szenario führt die Funktion eine atomarische **or** -Funktion mit dem Wert des Ressourcen Speicher Orts aus, auf den von *dest* verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="018ef-125">In this scenario, the function performs an atomic **OR** with the value of the resource location referenced by *dest*.</span></span> <span data-ttu-id="018ef-126">Das dritte Szenario ist, dass R ein lokaler Variablentyp ist.</span><span class="sxs-lookup"><span data-stu-id="018ef-126">Finally, the third scenario is when R is a local variable type.</span></span> <span data-ttu-id="018ef-127">In diesem Szenario wird die-Funktion auf einen **oder** mit den Werten " *dest* " und " *value*" reduziert.</span><span class="sxs-lookup"><span data-stu-id="018ef-127">In this scenario, the function reduces to an **OR** with the values of *dest* and *value*.</span></span> <span data-ttu-id="018ef-128">Das Ergebnis des Vorgangs ersetzt den Wert von *dest*.</span><span class="sxs-lookup"><span data-stu-id="018ef-128">The result of the operation replaces the value of *dest*.</span></span> <span data-ttu-id="018ef-129">Die überladene Funktion verfügt über eine zusätzliche OUTPUT-Variable, die auf den ursprünglichen Wert von *dest* festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="018ef-129">The overloaded function has an additional output variable, which will be set to the original value of *dest*.</span></span> <span data-ttu-id="018ef-130">Dieser überladene Vorgang ist nur verfügbar, wenn R lesbar und beschreibbar ist.</span><span class="sxs-lookup"><span data-stu-id="018ef-130">This overloaded operation is available only when R is readable and writable.</span></span>

<span data-ttu-id="018ef-131">Diese Funktion wird in den folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="018ef-131">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="018ef-132">VS</span><span class="sxs-lookup"><span data-stu-id="018ef-132">VS</span></span>  | <span data-ttu-id="018ef-133">Jh</span><span class="sxs-lookup"><span data-stu-id="018ef-133">HS</span></span>  | <span data-ttu-id="018ef-134">DS</span><span class="sxs-lookup"><span data-stu-id="018ef-134">DS</span></span>  | <span data-ttu-id="018ef-135">GS</span><span class="sxs-lookup"><span data-stu-id="018ef-135">GS</span></span>  | <span data-ttu-id="018ef-136">PS</span><span class="sxs-lookup"><span data-stu-id="018ef-136">PS</span></span>  | <span data-ttu-id="018ef-137">CS</span><span class="sxs-lookup"><span data-stu-id="018ef-137">CS</span></span>  |
|-----|-----|-----|-----|-----|-----|
| <span data-ttu-id="018ef-138">x</span><span class="sxs-lookup"><span data-stu-id="018ef-138">x</span></span>   |  <span data-ttu-id="018ef-139">x</span><span class="sxs-lookup"><span data-stu-id="018ef-139">x</span></span>  | <span data-ttu-id="018ef-140">x</span><span class="sxs-lookup"><span data-stu-id="018ef-140">x</span></span>   | <span data-ttu-id="018ef-141">x</span><span class="sxs-lookup"><span data-stu-id="018ef-141">x</span></span>   | <span data-ttu-id="018ef-142">x</span><span class="sxs-lookup"><span data-stu-id="018ef-142">x</span></span>   | <span data-ttu-id="018ef-143">x</span><span class="sxs-lookup"><span data-stu-id="018ef-143">x</span></span>   |



 

## <a name="see-also"></a><span data-ttu-id="018ef-144">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="018ef-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="018ef-145">Rwbyteaddressbuffer</span><span class="sxs-lookup"><span data-stu-id="018ef-145">RWByteAddressBuffer</span></span>](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[<span data-ttu-id="018ef-146">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="018ef-146">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 