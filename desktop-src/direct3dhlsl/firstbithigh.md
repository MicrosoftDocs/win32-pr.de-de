---
title: firstbithigh-Funktion
description: Ruft den Speicherort des ersten festgelegten Bits ab dem höchsten bestellbit ab und arbeitet nach unten pro Komponente.
ms.assetid: 0fa89a9e-1706-44f7-8dd3-c37af5c11ddc
keywords:
- firstbithigh-Funktion HLSL
topic_type:
- apiref
api_name:
- firstbithigh
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4da4956aa3a12d064566a3767423f42039b01355
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390503"
---
# <a name="firstbithigh-function"></a><span data-ttu-id="5f4b4-104">firstbithigh-Funktion</span><span class="sxs-lookup"><span data-stu-id="5f4b4-104">firstbithigh function</span></span>

<span data-ttu-id="5f4b4-105">Ruft den Speicherort des ersten festgelegten Bits ab dem höchsten bestellbit ab und arbeitet nach unten pro Komponente.</span><span class="sxs-lookup"><span data-stu-id="5f4b4-105">Gets the location of the first set bit starting from the highest order bit and working downward, per component.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f4b4-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="5f4b4-106">Syntax</span></span>

``` syntax
int firstbithigh(
  in int value
);
```

## <a name="parameters"></a><span data-ttu-id="5f4b4-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="5f4b4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f4b4-108">*Wert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5f4b4-108">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f4b4-109">Typ: **[ **int**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="5f4b4-109">Type: **[**int**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="5f4b4-110">Der Eingabewert.</span><span class="sxs-lookup"><span data-stu-id="5f4b4-110">The input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f4b4-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5f4b4-111">Return value</span></span>

<span data-ttu-id="5f4b4-112">Typ: **[ **int**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="5f4b4-112">Type: **[**int**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="5f4b4-113">Der Speicherort des ersten festgelegten Bits.</span><span class="sxs-lookup"><span data-stu-id="5f4b4-113">The location of the first set bit.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f4b4-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5f4b4-114">Remarks</span></span>

<span data-ttu-id="5f4b4-115">Bei einer Ganzzahl mit Vorzeichen ist das erste bedeutende Bit für eine negative Zahl 0 (null).</span><span class="sxs-lookup"><span data-stu-id="5f4b4-115">For a signed integer, the first significant bit is zero for a negative number.</span></span>

<span data-ttu-id="5f4b4-116">Außerdem sind die folgenden überladenen Versionen verfügbar:</span><span class="sxs-lookup"><span data-stu-id="5f4b4-116">The following overloaded versions are also available:</span></span>

``` syntax
int2 firstbithigh(int2 value);
int3 firstbithigh(int3 value);
int4 firstbithigh(int4 value);
uint firstbithigh(uint value);
uint2 firstbithigh(uint2 value);
uint3 firstbithigh(uint3 value);
uint4 firstbithigh(uint4 value);
```

### <a name="minimum-shader-model"></a><span data-ttu-id="5f4b4-117">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="5f4b4-117">Minimum Shader Model</span></span>

<span data-ttu-id="5f4b4-118">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5f4b4-118">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="5f4b4-119">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="5f4b4-119">Shader Model</span></span>                                                                | <span data-ttu-id="5f4b4-120">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="5f4b4-120">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="5f4b4-121">[Shader Model 5](d3d11-graphics-reference-sm5.md) und höhere shadermodelle</span><span class="sxs-lookup"><span data-stu-id="5f4b4-121">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="5f4b4-122">ja</span><span class="sxs-lookup"><span data-stu-id="5f4b4-122">yes</span></span>       |



 

<span data-ttu-id="5f4b4-123">Diese Funktion wird in den folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="5f4b4-123">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="5f4b4-124">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="5f4b4-124">Vertex</span></span> | <span data-ttu-id="5f4b4-125">Hülle</span><span class="sxs-lookup"><span data-stu-id="5f4b4-125">Hull</span></span> | <span data-ttu-id="5f4b4-126">Domain</span><span class="sxs-lookup"><span data-stu-id="5f4b4-126">Domain</span></span> | <span data-ttu-id="5f4b4-127">Geometrie</span><span class="sxs-lookup"><span data-stu-id="5f4b4-127">Geometry</span></span> | <span data-ttu-id="5f4b4-128">Pixel</span><span class="sxs-lookup"><span data-stu-id="5f4b4-128">Pixel</span></span> | <span data-ttu-id="5f4b4-129">Compute</span><span class="sxs-lookup"><span data-stu-id="5f4b4-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="5f4b4-130">x</span><span class="sxs-lookup"><span data-stu-id="5f4b4-130">x</span></span>      | <span data-ttu-id="5f4b4-131">x</span><span class="sxs-lookup"><span data-stu-id="5f4b4-131">x</span></span>    | <span data-ttu-id="5f4b4-132">x</span><span class="sxs-lookup"><span data-stu-id="5f4b4-132">x</span></span>      | <span data-ttu-id="5f4b4-133">x</span><span class="sxs-lookup"><span data-stu-id="5f4b4-133">x</span></span>        | <span data-ttu-id="5f4b4-134">x</span><span class="sxs-lookup"><span data-stu-id="5f4b4-134">x</span></span>     | <span data-ttu-id="5f4b4-135">x</span><span class="sxs-lookup"><span data-stu-id="5f4b4-135">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="5f4b4-136">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="5f4b4-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f4b4-137">Intrinsische Funktionen</span><span class="sxs-lookup"><span data-stu-id="5f4b4-137">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="5f4b4-138">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="5f4b4-138">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 