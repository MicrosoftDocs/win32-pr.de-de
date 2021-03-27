---
title: length
description: Gibt die Länge des angegebenen Gleit Komma Vektors zurück.
ms.assetid: eb06c87c-d536-448e-becb-762783cc2a77
keywords:
- Längen-HLSL
topic_type:
- apiref
api_name:
- length
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a7a93b0a7d225a25273a2ab4f8bf1d24656b6ee1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727856"
---
# <a name="length"></a><span data-ttu-id="d0488-104">length</span><span class="sxs-lookup"><span data-stu-id="d0488-104">length</span></span>

<span data-ttu-id="d0488-105">Gibt die Länge des angegebenen Gleit Komma Vektors zurück.</span><span class="sxs-lookup"><span data-stu-id="d0488-105">Returns the length of the specified floating-point vector.</span></span>



| <span data-ttu-id="d0488-106">*ret* -Länge (*x*)</span><span class="sxs-lookup"><span data-stu-id="d0488-106">*ret* length(*x*)</span></span> |
|-------------------|



 

## <a name="parameters"></a><span data-ttu-id="d0488-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="d0488-107">Parameters</span></span>



| <span data-ttu-id="d0488-108">Element</span><span class="sxs-lookup"><span data-stu-id="d0488-108">Item</span></span>                                                   | <span data-ttu-id="d0488-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d0488-109">Description</span></span>                                     |
|--------------------------------------------------------|-------------------------------------------------|
| <span data-ttu-id="d0488-110"><span id="x"></span><span id="X"></span>*Stuben*</span><span class="sxs-lookup"><span data-stu-id="d0488-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="d0488-111">Der angegebene Gleit Komma Vektor.</span><span class="sxs-lookup"><span data-stu-id="d0488-111">The specified floating-point vector.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="d0488-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d0488-112">Return Value</span></span>

<span data-ttu-id="d0488-113">Ein Gleit Komma-Skalarwert, der die Länge des *x* -Parameters darstellt.</span><span class="sxs-lookup"><span data-stu-id="d0488-113">A floating-point scalar that represents the length of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="d0488-114">Typbeschreibung</span><span class="sxs-lookup"><span data-stu-id="d0488-114">Type Description</span></span>



| <span data-ttu-id="d0488-115">Name</span><span class="sxs-lookup"><span data-stu-id="d0488-115">Name</span></span>  | [<span data-ttu-id="d0488-116">**Vorlagentyp**</span><span class="sxs-lookup"><span data-stu-id="d0488-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="d0488-117">**Komponententyp**</span><span class="sxs-lookup"><span data-stu-id="d0488-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="d0488-118">Size</span><span class="sxs-lookup"><span data-stu-id="d0488-118">Size</span></span> |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="d0488-119">*x*</span><span class="sxs-lookup"><span data-stu-id="d0488-119">*x*</span></span>   | [<span data-ttu-id="d0488-120">**ve**</span><span class="sxs-lookup"><span data-stu-id="d0488-120">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="d0488-121">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="d0488-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="d0488-122">any</span><span class="sxs-lookup"><span data-stu-id="d0488-122">any</span></span>  |
| <span data-ttu-id="d0488-123">*TZI*</span><span class="sxs-lookup"><span data-stu-id="d0488-123">*ret*</span></span> | [<span data-ttu-id="d0488-124">**Skalar**</span><span class="sxs-lookup"><span data-stu-id="d0488-124">**scalar**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="d0488-125">**float**</span><span class="sxs-lookup"><span data-stu-id="d0488-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="d0488-126">1</span><span class="sxs-lookup"><span data-stu-id="d0488-126">1</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="d0488-127">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="d0488-127">Minimum Shader Model</span></span>

<span data-ttu-id="d0488-128">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d0488-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="d0488-129">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="d0488-129">Shader Model</span></span>                                                                       | <span data-ttu-id="d0488-130">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="d0488-130">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="d0488-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) und höhere Shader-Modelle</span><span class="sxs-lookup"><span data-stu-id="d0488-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="d0488-132">ja</span><span class="sxs-lookup"><span data-stu-id="d0488-132">yes</span></span>                 |
| [<span data-ttu-id="d0488-133">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d0488-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="d0488-134">Ja ( \_ nur vs 1 \_ 1)</span><span class="sxs-lookup"><span data-stu-id="d0488-134">yes (vs\_1\_1 only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="d0488-135">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d0488-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0488-136">**Intrinsische Funktionen (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="d0488-136">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

