---
title: any
description: Bestimmt, ob Komponenten des angegebenen-Werts ungleich 0 (null) sind.
ms.assetid: 69a30478-662a-47de-babc-3cc67f89809c
keywords:
- beliebiger HLSL
topic_type:
- apiref
api_name:
- any
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6bc5a908336f011973690bd3ca3d598583b0d32d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104976848"
---
# <a name="any"></a><span data-ttu-id="5d082-104">any</span><span class="sxs-lookup"><span data-stu-id="5d082-104">any</span></span>

<span data-ttu-id="5d082-105">Bestimmt, ob Komponenten des angegebenen-Werts ungleich 0 (null) sind.</span><span class="sxs-lookup"><span data-stu-id="5d082-105">Determines if any components of the specified value are non-zero.</span></span>



| <span data-ttu-id="5d082-106">*ret* any (*x*)</span><span class="sxs-lookup"><span data-stu-id="5d082-106">*ret* any(*x*)</span></span> |
|----------------|



 

## <a name="parameters"></a><span data-ttu-id="5d082-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="5d082-107">Parameters</span></span>



| <span data-ttu-id="5d082-108">Element</span><span class="sxs-lookup"><span data-stu-id="5d082-108">Item</span></span>                                                   | <span data-ttu-id="5d082-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5d082-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="5d082-110"><span id="x"></span><span id="X"></span>*Stuben*</span><span class="sxs-lookup"><span data-stu-id="5d082-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="5d082-111">\[im \] angegebenen Wert.</span><span class="sxs-lookup"><span data-stu-id="5d082-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="5d082-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5d082-112">Return Value</span></span>

<span data-ttu-id="5d082-113">**True** , wenn Komponenten des *x* -Parameters ungleich NULL sind. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="5d082-113">**True** if any components of the *x* parameter are non-zero; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="5d082-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5d082-114">Remarks</span></span>

<span data-ttu-id="5d082-115">Diese Funktion ähnelt der intrinsischen Funktion [**alle**](dx-graphics-hlsl-all.md) HLSL.</span><span class="sxs-lookup"><span data-stu-id="5d082-115">This function is similar to the [**all**](dx-graphics-hlsl-all.md) HLSL intrinsic function.</span></span> <span data-ttu-id="5d082-116">Die **any** -Funktion bestimmt, ob Komponenten des angegebenen-Werts ungleich 0 (null) sind, während die **all** -Funktion bestimmt, ob alle Komponenten des angegebenen Werts ungleich 0 (null) sind.</span><span class="sxs-lookup"><span data-stu-id="5d082-116">The **any** function determines if any components of the specified value are non-zero, while the **all** function determines if all components of the specified value are non-zero.</span></span>

## <a name="type-description"></a><span data-ttu-id="5d082-117">Typbeschreibung</span><span class="sxs-lookup"><span data-stu-id="5d082-117">Type Description</span></span>



| <span data-ttu-id="5d082-118">Name</span><span class="sxs-lookup"><span data-stu-id="5d082-118">Name</span></span>  | [<span data-ttu-id="5d082-119">**Vorlagentyp**</span><span class="sxs-lookup"><span data-stu-id="5d082-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="5d082-120">**Komponententyp**</span><span class="sxs-lookup"><span data-stu-id="5d082-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                         | <span data-ttu-id="5d082-121">Size</span><span class="sxs-lookup"><span data-stu-id="5d082-121">Size</span></span> |
|-------|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|------|
| <span data-ttu-id="5d082-122">*x*</span><span class="sxs-lookup"><span data-stu-id="5d082-122">*x*</span></span>   | <span data-ttu-id="5d082-123">[**Skalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vektor** oder **Matrix**</span><span class="sxs-lookup"><span data-stu-id="5d082-123">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | <span data-ttu-id="5d082-124">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types), [**bool**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="5d082-124">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types), [**bool**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="5d082-125">any</span><span class="sxs-lookup"><span data-stu-id="5d082-125">any</span></span>  |
| <span data-ttu-id="5d082-126">*TZI*</span><span class="sxs-lookup"><span data-stu-id="5d082-126">*ret*</span></span> | [<span data-ttu-id="5d082-127">**Skalar**</span><span class="sxs-lookup"><span data-stu-id="5d082-127">**scalar**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                            | [<span data-ttu-id="5d082-128">**bool**</span><span class="sxs-lookup"><span data-stu-id="5d082-128">**bool**</span></span>](/windows/desktop/WinProg/windows-data-types)                                                                                 | <span data-ttu-id="5d082-129">1</span><span class="sxs-lookup"><span data-stu-id="5d082-129">1</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="5d082-130">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="5d082-130">Minimum Shader Model</span></span>

<span data-ttu-id="5d082-131">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5d082-131">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="5d082-132">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="5d082-132">Shader Model</span></span>                                                                       | <span data-ttu-id="5d082-133">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="5d082-133">Supported</span></span>             |
|------------------------------------------------------------------------------------|-----------------------|
| <span data-ttu-id="5d082-134">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) und höhere Shader-Modelle</span><span class="sxs-lookup"><span data-stu-id="5d082-134">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="5d082-135">ja</span><span class="sxs-lookup"><span data-stu-id="5d082-135">yes</span></span>                   |
| [<span data-ttu-id="5d082-136">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5d082-136">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="5d082-137">vs \_ 1 \_ 1 und PS \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="5d082-137">vs\_1\_1 and ps\_1\_4</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="5d082-138">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="5d082-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d082-139">**Intrinsische Funktionen (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="5d082-139">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

