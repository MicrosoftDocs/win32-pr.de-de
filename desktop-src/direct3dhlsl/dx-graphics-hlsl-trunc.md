---
title: trunc (corecrt \_ Math. h)
description: Kürzen eines Gleit Komma Werts in die ganzzahlige Komponente.
ms.assetid: a0978fa2-71f8-4257-8c90-96224c2ec953
keywords:
- trunc HLSL
topic_type:
- apiref
api_name:
- trunc
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34493f60e60bc0dce35f5f9db50360265191c742
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104995944"
---
# <a name="trunc"></a><span data-ttu-id="a1f28-104">trunc</span><span class="sxs-lookup"><span data-stu-id="a1f28-104">trunc</span></span>

<span data-ttu-id="a1f28-105">Kürzen eines Gleit Komma Werts in die ganzzahlige Komponente.</span><span class="sxs-lookup"><span data-stu-id="a1f28-105">Truncates a floating-point value to the integer component.</span></span>



| <span data-ttu-id="a1f28-106">Ret trunc (*x*)</span><span class="sxs-lookup"><span data-stu-id="a1f28-106">ret trunc(*x*)</span></span> |
|----------------|



 

## <a name="parameters"></a><span data-ttu-id="a1f28-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="a1f28-107">Parameters</span></span>



| <span data-ttu-id="a1f28-108">Element</span><span class="sxs-lookup"><span data-stu-id="a1f28-108">Item</span></span>                                                   | <span data-ttu-id="a1f28-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a1f28-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="a1f28-110"><span id="x"></span><span id="X"></span>*Stuben*</span><span class="sxs-lookup"><span data-stu-id="a1f28-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="a1f28-111">\[in \] der angegebenen Eingabe.</span><span class="sxs-lookup"><span data-stu-id="a1f28-111">\[in\] The specified input.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="a1f28-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a1f28-112">Return Value</span></span>

<span data-ttu-id="a1f28-113">Der Eingabe Wert, der auf eine ganzzahlige Komponente gekürzt wird.</span><span class="sxs-lookup"><span data-stu-id="a1f28-113">The input value truncated to an integer component.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1f28-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a1f28-114">Remarks</span></span>

<span data-ttu-id="a1f28-115">Diese Funktion verkürzt einen Gleit Komma Wert auf die ganzzahlige Komponente.</span><span class="sxs-lookup"><span data-stu-id="a1f28-115">This function truncates a floating-point value to the integer component.</span></span> <span data-ttu-id="a1f28-116">Wenn ein Gleit Komma Wert von 1,6 ist, würde die trunc-Funktion 1,0 zurückgeben, wobei der Wert der Round-Funktion [**(DirectX HLSL)**](dx-graphics-hlsl-round.md) 2,0 zurückgeben würde.</span><span class="sxs-lookup"><span data-stu-id="a1f28-116">Given a floating-point value of 1.6, the trunc function would return 1.0, where as the [**round (DirectX HLSL)**](dx-graphics-hlsl-round.md) function would return 2.0.</span></span>

## <a name="type-description"></a><span data-ttu-id="a1f28-117">Typbeschreibung</span><span class="sxs-lookup"><span data-stu-id="a1f28-117">Type Description</span></span>



| <span data-ttu-id="a1f28-118">Name</span><span class="sxs-lookup"><span data-stu-id="a1f28-118">Name</span></span> | [<span data-ttu-id="a1f28-119">**Vorlagentyp**</span><span class="sxs-lookup"><span data-stu-id="a1f28-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="a1f28-120">**Komponententyp**</span><span class="sxs-lookup"><span data-stu-id="a1f28-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="a1f28-121">Size</span><span class="sxs-lookup"><span data-stu-id="a1f28-121">Size</span></span>                         |
|------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|------------------------------|
| <span data-ttu-id="a1f28-122">*x*</span><span class="sxs-lookup"><span data-stu-id="a1f28-122">*x*</span></span>  | <span data-ttu-id="a1f28-123">[**Skalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vektor** oder **Matrix**</span><span class="sxs-lookup"><span data-stu-id="a1f28-123">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="a1f28-124">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="a1f28-124">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="a1f28-125">any</span><span class="sxs-lookup"><span data-stu-id="a1f28-125">any</span></span>                          |
| <span data-ttu-id="a1f28-126">TZI</span><span class="sxs-lookup"><span data-stu-id="a1f28-126">ret</span></span>  | <span data-ttu-id="a1f28-127">Gleicher Typ wie Eingabe x</span><span class="sxs-lookup"><span data-stu-id="a1f28-127">Same type as input x</span></span>                                                                                           | [<span data-ttu-id="a1f28-128">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="a1f28-128">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="a1f28-129">Gleiche Dimension (n) wie Eingabe x</span><span class="sxs-lookup"><span data-stu-id="a1f28-129">Same dimension(s) as input x</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="a1f28-130">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="a1f28-130">Minimum Shader Model</span></span>

<span data-ttu-id="a1f28-131">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a1f28-131">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="a1f28-132">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="a1f28-132">Shader Model</span></span>                                                                       | <span data-ttu-id="a1f28-133">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="a1f28-133">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="a1f28-134">[Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) und höhere Shader-Modelle</span><span class="sxs-lookup"><span data-stu-id="a1f28-134">[Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) and higher shader models</span></span> | <span data-ttu-id="a1f28-135">ja</span><span class="sxs-lookup"><span data-stu-id="a1f28-135">yes</span></span>       |



 

## <a name="requirements"></a><span data-ttu-id="a1f28-136">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="a1f28-136">Requirements</span></span>



| <span data-ttu-id="a1f28-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a1f28-137">Requirement</span></span> | <span data-ttu-id="a1f28-138">Wert</span><span class="sxs-lookup"><span data-stu-id="a1f28-138">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1f28-139">Header</span><span class="sxs-lookup"><span data-stu-id="a1f28-139">Header</span></span><br/> | <dl> <span data-ttu-id="a1f28-140"><dt>Corecrt \_ Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="a1f28-140"><dt>Corecrt\_math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1f28-141">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="a1f28-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1f28-142">**Intrinsische Funktionen (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="a1f28-142">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

