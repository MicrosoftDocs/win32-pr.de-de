---
title: isinf (corecrt \_ Math. h)
description: Bestimmt, ob der angegebene Wert unendlich ist.
ms.assetid: 2028dc5a-e48b-4081-a0ec-35901113aab6
keywords:
- isinf HLSL
topic_type:
- apiref
api_name:
- isinf
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4df738438d62d5a66dd3b08ad769d475df562d5f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219582"
---
# <a name="isinf"></a><span data-ttu-id="75ed9-104">isinf</span><span class="sxs-lookup"><span data-stu-id="75ed9-104">isinf</span></span>

<span data-ttu-id="75ed9-105">Bestimmt, ob der angegebene Wert unendlich ist.</span><span class="sxs-lookup"><span data-stu-id="75ed9-105">Determines if the specified value is infinite.</span></span>



| <span data-ttu-id="75ed9-106">*ret* isinf (*x*)</span><span class="sxs-lookup"><span data-stu-id="75ed9-106">*ret* isinf(*x*)</span></span> |
|------------------|



 

## <a name="parameters"></a><span data-ttu-id="75ed9-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="75ed9-107">Parameters</span></span>



| <span data-ttu-id="75ed9-108">Element</span><span class="sxs-lookup"><span data-stu-id="75ed9-108">Item</span></span>                                                   | <span data-ttu-id="75ed9-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="75ed9-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="75ed9-110"><span id="x"></span><span id="X"></span>*Stuben*</span><span class="sxs-lookup"><span data-stu-id="75ed9-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="75ed9-111">\[im \] angegebenen Wert.</span><span class="sxs-lookup"><span data-stu-id="75ed9-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="75ed9-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="75ed9-112">Return Value</span></span>

<span data-ttu-id="75ed9-113">Gibt einen Wert mit der gleichen Größe wie die Eingabe zurück, wobei ein Wert auf **true** festgelegt ist, wenn der *x* -Parameter + INF oder-INF ist.</span><span class="sxs-lookup"><span data-stu-id="75ed9-113">Returns a value of the same size as the input, with a value set to **True** if the *x* parameter is +INF or -INF.</span></span> <span data-ttu-id="75ed9-114">Andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="75ed9-114">Otherwise, **False**.</span></span>

## <a name="type-description"></a><span data-ttu-id="75ed9-115">Typbeschreibung</span><span class="sxs-lookup"><span data-stu-id="75ed9-115">Type Description</span></span>



| <span data-ttu-id="75ed9-116">Name</span><span class="sxs-lookup"><span data-stu-id="75ed9-116">Name</span></span>  | [<span data-ttu-id="75ed9-117">**Vorlagentyp**</span><span class="sxs-lookup"><span data-stu-id="75ed9-117">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="75ed9-118">**Komponententyp**</span><span class="sxs-lookup"><span data-stu-id="75ed9-118">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="75ed9-119">Size</span><span class="sxs-lookup"><span data-stu-id="75ed9-119">Size</span></span>     |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|----------|
| <span data-ttu-id="75ed9-120">*x*</span><span class="sxs-lookup"><span data-stu-id="75ed9-120">*x*</span></span>   | <span data-ttu-id="75ed9-121">[**Skalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vektor** oder **Matrix**</span><span class="sxs-lookup"><span data-stu-id="75ed9-121">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="75ed9-122">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="75ed9-122">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="75ed9-123">any</span><span class="sxs-lookup"><span data-stu-id="75ed9-123">any</span></span>      |
| <span data-ttu-id="75ed9-124">*TZI*</span><span class="sxs-lookup"><span data-stu-id="75ed9-124">*ret*</span></span> | <span data-ttu-id="75ed9-125">[**Skalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vektor** oder **Matrix**</span><span class="sxs-lookup"><span data-stu-id="75ed9-125">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="75ed9-126">**bool**</span><span class="sxs-lookup"><span data-stu-id="75ed9-126">**bool**</span></span>](/windows/desktop/WinProg/windows-data-types)                         | <span data-ttu-id="75ed9-127">als Eingabe</span><span class="sxs-lookup"><span data-stu-id="75ed9-127">as input</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="75ed9-128">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="75ed9-128">Minimum Shader Model</span></span>

<span data-ttu-id="75ed9-129">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="75ed9-129">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="75ed9-130">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="75ed9-130">Shader Model</span></span>                                                                       | <span data-ttu-id="75ed9-131">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="75ed9-131">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="75ed9-132">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) und höhere Shader-Modelle</span><span class="sxs-lookup"><span data-stu-id="75ed9-132">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="75ed9-133">ja</span><span class="sxs-lookup"><span data-stu-id="75ed9-133">yes</span></span>                 |
| [<span data-ttu-id="75ed9-134">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="75ed9-134">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="75ed9-135">Ja ( \_ nur vs 1 \_ 1)</span><span class="sxs-lookup"><span data-stu-id="75ed9-135">yes (vs\_1\_1 only)</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="75ed9-136">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="75ed9-136">Requirements</span></span>



| <span data-ttu-id="75ed9-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="75ed9-137">Requirement</span></span> | <span data-ttu-id="75ed9-138">Wert</span><span class="sxs-lookup"><span data-stu-id="75ed9-138">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="75ed9-139">Header</span><span class="sxs-lookup"><span data-stu-id="75ed9-139">Header</span></span><br/> | <dl> <span data-ttu-id="75ed9-140"><dt>Corecrt \_ Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="75ed9-140"><dt>Corecrt\_math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75ed9-141">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="75ed9-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75ed9-142">**Intrinsische Funktionen (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="75ed9-142">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

