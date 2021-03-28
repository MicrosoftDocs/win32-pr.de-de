---
title: isFinite (corecrt \_ Math. h)
description: Bestimmt, ob der angegebene Gleit Komma Wert begrenzt ist.
ms.assetid: 8be10499-2d06-4520-9697-dab2f461bd0d
keywords:
- isFinite HLSL
topic_type:
- apiref
api_name:
- isfinite
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f63c943dadccad9f485668948f366698f3bce5e6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104995877"
---
# <a name="isfinite"></a><span data-ttu-id="a7462-104">isFinite</span><span class="sxs-lookup"><span data-stu-id="a7462-104">isfinite</span></span>

<span data-ttu-id="a7462-105">Bestimmt, ob der angegebene Gleit Komma Wert begrenzt ist.</span><span class="sxs-lookup"><span data-stu-id="a7462-105">Determines if the specified floating-point value is finite.</span></span>



| <span data-ttu-id="a7462-106">*ret* isFinite (*x*)</span><span class="sxs-lookup"><span data-stu-id="a7462-106">*ret* isfinite(*x*)</span></span> |
|---------------------|



 

## <a name="parameters"></a><span data-ttu-id="a7462-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="a7462-107">Parameters</span></span>



| <span data-ttu-id="a7462-108">Element</span><span class="sxs-lookup"><span data-stu-id="a7462-108">Item</span></span>                                                   | <span data-ttu-id="a7462-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a7462-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="a7462-110"><span id="x"></span><span id="X"></span>*Stuben*</span><span class="sxs-lookup"><span data-stu-id="a7462-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="a7462-111">\[im \] angegebenen Wert.</span><span class="sxs-lookup"><span data-stu-id="a7462-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="a7462-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a7462-112">Return Value</span></span>

<span data-ttu-id="a7462-113">Gibt einen Wert mit der gleichen Größe wie die Eingabe zurück, wobei ein Wert auf **true** festgelegt ist, wenn der *x* -Parameter begrenzt ist. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="a7462-113">Returns a value of the same size as the input, with a value set to **True** if the *x* parameter is finite; otherwise **False**.</span></span>

## <a name="type-description"></a><span data-ttu-id="a7462-114">Typbeschreibung</span><span class="sxs-lookup"><span data-stu-id="a7462-114">Type Description</span></span>



| <span data-ttu-id="a7462-115">Name</span><span class="sxs-lookup"><span data-stu-id="a7462-115">Name</span></span>  | [<span data-ttu-id="a7462-116">**Vorlagentyp**</span><span class="sxs-lookup"><span data-stu-id="a7462-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="a7462-117">**Komponententyp**</span><span class="sxs-lookup"><span data-stu-id="a7462-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="a7462-118">Size</span><span class="sxs-lookup"><span data-stu-id="a7462-118">Size</span></span>     |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|----------|
| <span data-ttu-id="a7462-119">*x*</span><span class="sxs-lookup"><span data-stu-id="a7462-119">*x*</span></span>   | <span data-ttu-id="a7462-120">[**Skalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vektor** oder **Matrix**</span><span class="sxs-lookup"><span data-stu-id="a7462-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="a7462-121">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="a7462-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="a7462-122">any</span><span class="sxs-lookup"><span data-stu-id="a7462-122">any</span></span>      |
| <span data-ttu-id="a7462-123">*TZI*</span><span class="sxs-lookup"><span data-stu-id="a7462-123">*ret*</span></span> | <span data-ttu-id="a7462-124">[**Skalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vektor** oder **Matrix**</span><span class="sxs-lookup"><span data-stu-id="a7462-124">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="a7462-125">**bool**</span><span class="sxs-lookup"><span data-stu-id="a7462-125">**bool**</span></span>](/windows/desktop/WinProg/windows-data-types)                         | <span data-ttu-id="a7462-126">als Eingabe</span><span class="sxs-lookup"><span data-stu-id="a7462-126">as input</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="a7462-127">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="a7462-127">Minimum Shader Model</span></span>

<span data-ttu-id="a7462-128">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a7462-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="a7462-129">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="a7462-129">Shader Model</span></span>                                                                       | <span data-ttu-id="a7462-130">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="a7462-130">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="a7462-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) und höhere Shader-Modelle</span><span class="sxs-lookup"><span data-stu-id="a7462-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="a7462-132">ja</span><span class="sxs-lookup"><span data-stu-id="a7462-132">yes</span></span>                 |
| [<span data-ttu-id="a7462-133">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a7462-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="a7462-134">Ja ( \_ nur vs 1 \_ 1)</span><span class="sxs-lookup"><span data-stu-id="a7462-134">yes (vs\_1\_1 only)</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="a7462-135">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="a7462-135">Requirements</span></span>



| <span data-ttu-id="a7462-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a7462-136">Requirement</span></span> | <span data-ttu-id="a7462-137">Wert</span><span class="sxs-lookup"><span data-stu-id="a7462-137">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7462-138">Header</span><span class="sxs-lookup"><span data-stu-id="a7462-138">Header</span></span><br/> | <dl> <span data-ttu-id="a7462-139"><dt>Corecrt \_ Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="a7462-139"><dt>Corecrt\_math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7462-140">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="a7462-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7462-141">**Intrinsische Funktionen (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="a7462-141">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

