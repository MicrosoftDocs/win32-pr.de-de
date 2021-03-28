---
title: IsNaN (corecrt \_ Math. h)
description: Bestimmt, ob der angegebene Wert NaN oder QNAN ist.
ms.assetid: 09085634-e610-4793-848e-abda8241f1cc
keywords:
- IsNaN HLSL
topic_type:
- apiref
api_name:
- isnan
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef9f4549b6a142f5bf6011cdfb144de92efde64c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104050928"
---
# <a name="isnan"></a><span data-ttu-id="914de-104">IsNaN</span><span class="sxs-lookup"><span data-stu-id="914de-104">isnan</span></span>

<span data-ttu-id="914de-105">Bestimmt, ob der angegebene Wert NaN oder QNAN ist.</span><span class="sxs-lookup"><span data-stu-id="914de-105">Determines if the specified value is NAN or QNAN.</span></span>



| <span data-ttu-id="914de-106">*ret* IsNaN (*x*)</span><span class="sxs-lookup"><span data-stu-id="914de-106">*ret* isnan(*x*)</span></span> |
|------------------|



 

## <a name="parameters"></a><span data-ttu-id="914de-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="914de-107">Parameters</span></span>



| <span data-ttu-id="914de-108">Element</span><span class="sxs-lookup"><span data-stu-id="914de-108">Item</span></span>                                                   | <span data-ttu-id="914de-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="914de-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="914de-110"><span id="x"></span><span id="X"></span>*Stuben*</span><span class="sxs-lookup"><span data-stu-id="914de-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="914de-111">\[im \] angegebenen Wert.</span><span class="sxs-lookup"><span data-stu-id="914de-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="914de-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="914de-112">Return Value</span></span>

<span data-ttu-id="914de-113">Gibt einen Wert mit der gleichen Größe wie die Eingabe zurück, wobei ein Wert auf **true** festgelegt ist, wenn der *x* -Parameter NaN oder QNAN ist.</span><span class="sxs-lookup"><span data-stu-id="914de-113">Returns a value of the same size as the input, with a value set to **True** if the *x* parameter is NAN or QNAN.</span></span> <span data-ttu-id="914de-114">Andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="914de-114">Otherwise, **False**.</span></span>

## <a name="type-description"></a><span data-ttu-id="914de-115">Typbeschreibung</span><span class="sxs-lookup"><span data-stu-id="914de-115">Type Description</span></span>



| <span data-ttu-id="914de-116">Name</span><span class="sxs-lookup"><span data-stu-id="914de-116">Name</span></span>  | [<span data-ttu-id="914de-117">**Vorlagentyp**</span><span class="sxs-lookup"><span data-stu-id="914de-117">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="914de-118">**Komponententyp**</span><span class="sxs-lookup"><span data-stu-id="914de-118">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="914de-119">Size</span><span class="sxs-lookup"><span data-stu-id="914de-119">Size</span></span>     |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|----------|
| <span data-ttu-id="914de-120">*x*</span><span class="sxs-lookup"><span data-stu-id="914de-120">*x*</span></span>   | <span data-ttu-id="914de-121">[**Skalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vektor** oder **Matrix**</span><span class="sxs-lookup"><span data-stu-id="914de-121">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="914de-122">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="914de-122">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="914de-123">any</span><span class="sxs-lookup"><span data-stu-id="914de-123">any</span></span>      |
| <span data-ttu-id="914de-124">*TZI*</span><span class="sxs-lookup"><span data-stu-id="914de-124">*ret*</span></span> | <span data-ttu-id="914de-125">[**Skalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vektor** oder **Matrix**</span><span class="sxs-lookup"><span data-stu-id="914de-125">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="914de-126">**bool**</span><span class="sxs-lookup"><span data-stu-id="914de-126">**bool**</span></span>](/windows/desktop/WinProg/windows-data-types)                         | <span data-ttu-id="914de-127">als Eingabe</span><span class="sxs-lookup"><span data-stu-id="914de-127">as input</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="914de-128">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="914de-128">Minimum Shader Model</span></span>

<span data-ttu-id="914de-129">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="914de-129">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="914de-130">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="914de-130">Shader Model</span></span>                                                                       | <span data-ttu-id="914de-131">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="914de-131">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="914de-132">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) und höhere Shader-Modelle</span><span class="sxs-lookup"><span data-stu-id="914de-132">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="914de-133">ja</span><span class="sxs-lookup"><span data-stu-id="914de-133">yes</span></span>                 |
| [<span data-ttu-id="914de-134">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="914de-134">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="914de-135">Ja ( \_ nur vs 1 \_ 1)</span><span class="sxs-lookup"><span data-stu-id="914de-135">yes (vs\_1\_1 only)</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="914de-136">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="914de-136">Requirements</span></span>



| <span data-ttu-id="914de-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="914de-137">Requirement</span></span> | <span data-ttu-id="914de-138">Wert</span><span class="sxs-lookup"><span data-stu-id="914de-138">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="914de-139">Header</span><span class="sxs-lookup"><span data-stu-id="914de-139">Header</span></span><br/> | <dl> <span data-ttu-id="914de-140"><dt>Corecrt \_ Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="914de-140"><dt>Corecrt\_math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="914de-141">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="914de-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="914de-142">**Intrinsische Funktionen (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="914de-142">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

