---
title: firstbitlow-Funktion
description: Gibt den Speicherort des ersten festgelegten Bits ab dem niedrigsten bestellbit zurück und arbeitet nach oben pro Komponente.
ms.assetid: 204250f3-1a9b-445d-bd16-4cc9a5d9d60a
keywords:
- firstbitlow-Funktion HLSL
topic_type:
- apiref
api_name:
- firstbitlow
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a647314383bc022b7c3b3e1b5a255a42a099c620
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039183"
---
# <a name="firstbitlow-function"></a><span data-ttu-id="795fd-104">firstbitlow-Funktion</span><span class="sxs-lookup"><span data-stu-id="795fd-104">firstbitlow function</span></span>

<span data-ttu-id="795fd-105">Gibt den Speicherort des ersten festgelegten Bits ab dem niedrigsten bestellbit zurück und arbeitet nach oben pro Komponente.</span><span class="sxs-lookup"><span data-stu-id="795fd-105">Returns the location of the first set bit starting from the lowest order bit and working upward, per component.</span></span>

## <a name="syntax"></a><span data-ttu-id="795fd-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="795fd-106">Syntax</span></span>

``` syntax
int firstbitlow(
  in int value
);
```

## <a name="parameters"></a><span data-ttu-id="795fd-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="795fd-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="795fd-108">*Wert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="795fd-108">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="795fd-109">Typ: **[ **int**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="795fd-109">Type: **[**int**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="795fd-110">Der Eingabewert.</span><span class="sxs-lookup"><span data-stu-id="795fd-110">The input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="795fd-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="795fd-111">Return value</span></span>

<span data-ttu-id="795fd-112">Typ: **[ **int**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="795fd-112">Type: **[**int**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="795fd-113">Der Speicherort des ersten festgelegten Bits.</span><span class="sxs-lookup"><span data-stu-id="795fd-113">The location of the first set bit.</span></span>

## <a name="remarks"></a><span data-ttu-id="795fd-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="795fd-114">Remarks</span></span>

<span data-ttu-id="795fd-115">Außerdem sind die folgenden überladenen Versionen verfügbar:</span><span class="sxs-lookup"><span data-stu-id="795fd-115">The following overloaded versions are also available:</span></span>

``` syntax
uint2 firstbitlow(uint2 value);
uint3 firstbitlow(uint3 value);
uint4 firstbitlow(uint4 value);
```

### <a name="minimum-shader-model"></a><span data-ttu-id="795fd-116">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="795fd-116">Minimum Shader Model</span></span>

<span data-ttu-id="795fd-117">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="795fd-117">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="795fd-118">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="795fd-118">Shader Model</span></span>                                                                | <span data-ttu-id="795fd-119">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="795fd-119">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="795fd-120">[Shader Model 5](d3d11-graphics-reference-sm5.md) und höhere shadermodelle</span><span class="sxs-lookup"><span data-stu-id="795fd-120">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="795fd-121">ja</span><span class="sxs-lookup"><span data-stu-id="795fd-121">yes</span></span>       |



 

<span data-ttu-id="795fd-122">Diese Funktion wird in den folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="795fd-122">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="795fd-123">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="795fd-123">Vertex</span></span> | <span data-ttu-id="795fd-124">Hülle</span><span class="sxs-lookup"><span data-stu-id="795fd-124">Hull</span></span> | <span data-ttu-id="795fd-125">Domain</span><span class="sxs-lookup"><span data-stu-id="795fd-125">Domain</span></span> | <span data-ttu-id="795fd-126">Geometrie</span><span class="sxs-lookup"><span data-stu-id="795fd-126">Geometry</span></span> | <span data-ttu-id="795fd-127">Pixel</span><span class="sxs-lookup"><span data-stu-id="795fd-127">Pixel</span></span> | <span data-ttu-id="795fd-128">Compute</span><span class="sxs-lookup"><span data-stu-id="795fd-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="795fd-129">x</span><span class="sxs-lookup"><span data-stu-id="795fd-129">x</span></span>      | <span data-ttu-id="795fd-130">x</span><span class="sxs-lookup"><span data-stu-id="795fd-130">x</span></span>    | <span data-ttu-id="795fd-131">x</span><span class="sxs-lookup"><span data-stu-id="795fd-131">x</span></span>      | <span data-ttu-id="795fd-132">x</span><span class="sxs-lookup"><span data-stu-id="795fd-132">x</span></span>        | <span data-ttu-id="795fd-133">x</span><span class="sxs-lookup"><span data-stu-id="795fd-133">x</span></span>     | <span data-ttu-id="795fd-134">x</span><span class="sxs-lookup"><span data-stu-id="795fd-134">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="795fd-135">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="795fd-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="795fd-136">Intrinsische Funktionen</span><span class="sxs-lookup"><span data-stu-id="795fd-136">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="795fd-137">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="795fd-137">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 