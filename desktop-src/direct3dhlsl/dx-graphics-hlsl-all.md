---
title: alle
description: Bestimmt, ob alle Komponenten des angegebenen-Werts ungleich 0 (null) sind.
ms.assetid: 9ee079ff-cd2c-41f5-98cd-ea1f4215e7d5
keywords:
- Alle HLSL
topic_type:
- apiref
api_name:
- all
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 59d59e18655aab10d13af998f4e2aa94da3fa08b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104976849"
---
# <a name="all"></a><span data-ttu-id="2455e-104">alle</span><span class="sxs-lookup"><span data-stu-id="2455e-104">all</span></span>

<span data-ttu-id="2455e-105">Bestimmt, ob alle Komponenten des angegebenen-Werts ungleich 0 (null) sind.</span><span class="sxs-lookup"><span data-stu-id="2455e-105">Determines if all components of the specified value are non-zero.</span></span>



| <span data-ttu-id="2455e-106">*ret* all (*x*)</span><span class="sxs-lookup"><span data-stu-id="2455e-106">*ret* all(*x*)</span></span> |
|----------------|



 

## <a name="parameters"></a><span data-ttu-id="2455e-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="2455e-107">Parameters</span></span>



| <span data-ttu-id="2455e-108">Element</span><span class="sxs-lookup"><span data-stu-id="2455e-108">Item</span></span>                                                   | <span data-ttu-id="2455e-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2455e-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="2455e-110"><span id="x"></span><span id="X"></span>*Stuben*</span><span class="sxs-lookup"><span data-stu-id="2455e-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="2455e-111">\[im \] angegebenen Wert.</span><span class="sxs-lookup"><span data-stu-id="2455e-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="2455e-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2455e-112">Return Value</span></span>

<span data-ttu-id="2455e-113">**True** , wenn alle Komponenten des *x* -Parameters ungleich NULL sind. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="2455e-113">**True** if all components of the *x* parameter are non-zero; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="2455e-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2455e-114">Remarks</span></span>

<span data-ttu-id="2455e-115">Diese Funktion [**ähnelt der**](dx-graphics-hlsl-any.md) intrinsischen HLSL-Funktion.</span><span class="sxs-lookup"><span data-stu-id="2455e-115">This function is similar to the [**any**](dx-graphics-hlsl-any.md) HLSL intrinsic function.</span></span> <span data-ttu-id="2455e-116">Die **any** -Funktion bestimmt, ob Komponenten des angegebenen-Werts ungleich 0 (null) sind, während die **all** -Funktion bestimmt, ob alle Komponenten des angegebenen Werts ungleich 0 (null) sind.</span><span class="sxs-lookup"><span data-stu-id="2455e-116">The **any** function determines if any components of the specified value are non-zero, while the **all** function determines if all components of the specified value are non-zero.</span></span>

## <a name="type-description"></a><span data-ttu-id="2455e-117">Typbeschreibung</span><span class="sxs-lookup"><span data-stu-id="2455e-117">Type Description</span></span>



| <span data-ttu-id="2455e-118">Name</span><span class="sxs-lookup"><span data-stu-id="2455e-118">Name</span></span>  | [<span data-ttu-id="2455e-119">**Vorlagentyp**</span><span class="sxs-lookup"><span data-stu-id="2455e-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="2455e-120">**Komponententyp**</span><span class="sxs-lookup"><span data-stu-id="2455e-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                         | <span data-ttu-id="2455e-121">Size</span><span class="sxs-lookup"><span data-stu-id="2455e-121">Size</span></span> |
|-------|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|------|
| <span data-ttu-id="2455e-122">*x*</span><span class="sxs-lookup"><span data-stu-id="2455e-122">*x*</span></span>   | <span data-ttu-id="2455e-123">[**Skalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vektor** oder **Matrix**</span><span class="sxs-lookup"><span data-stu-id="2455e-123">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | <span data-ttu-id="2455e-124">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types), [**bool**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="2455e-124">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types), [**bool**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="2455e-125">any</span><span class="sxs-lookup"><span data-stu-id="2455e-125">any</span></span>  |
| <span data-ttu-id="2455e-126">*TZI*</span><span class="sxs-lookup"><span data-stu-id="2455e-126">*ret*</span></span> | [<span data-ttu-id="2455e-127">**Skalar**</span><span class="sxs-lookup"><span data-stu-id="2455e-127">**scalar**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                            | [<span data-ttu-id="2455e-128">**bool**</span><span class="sxs-lookup"><span data-stu-id="2455e-128">**bool**</span></span>](/windows/desktop/WinProg/windows-data-types)                                                                                 | <span data-ttu-id="2455e-129">1</span><span class="sxs-lookup"><span data-stu-id="2455e-129">1</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="2455e-130">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="2455e-130">Minimum Shader Model</span></span>

<span data-ttu-id="2455e-131">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2455e-131">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="2455e-132">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="2455e-132">Shader Model</span></span>                                                                       | <span data-ttu-id="2455e-133">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="2455e-133">Supported</span></span>             |
|------------------------------------------------------------------------------------|-----------------------|
| <span data-ttu-id="2455e-134">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) und höhere Shader-Modelle</span><span class="sxs-lookup"><span data-stu-id="2455e-134">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="2455e-135">ja</span><span class="sxs-lookup"><span data-stu-id="2455e-135">yes</span></span>                   |
| [<span data-ttu-id="2455e-136">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2455e-136">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="2455e-137">vs \_ 1 \_ 1 und PS \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="2455e-137">vs\_1\_1 and ps\_1\_4</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="2455e-138">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="2455e-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2455e-139">**Intrinsische Funktionen (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="2455e-139">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

