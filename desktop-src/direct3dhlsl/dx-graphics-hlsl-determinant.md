---
title: Determinante
description: Gibt den Determinanten der angegebenen Gleit Komma-und quadratischen Matrix zurück.
ms.assetid: 9062b6f1-8518-4ee4-8d57-5aa9e2176d05
keywords:
- Determinante HLSL
topic_type:
- apiref
api_name:
- determinant
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: eb010a0c0d0868afcb3dff488daf7926ec6c5e03
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104976713"
---
# <a name="determinant"></a><span data-ttu-id="751f9-104">Determinante</span><span class="sxs-lookup"><span data-stu-id="751f9-104">determinant</span></span>

<span data-ttu-id="751f9-105">Gibt den Determinanten der angegebenen Gleit Komma-und quadratischen Matrix zurück.</span><span class="sxs-lookup"><span data-stu-id="751f9-105">Returns the determinant of the specified floating-point, square matrix.</span></span>



| <span data-ttu-id="751f9-106">*ret* Determinant (*m*)</span><span class="sxs-lookup"><span data-stu-id="751f9-106">*ret* determinant(*m*)</span></span> |
|------------------------|



 

## <a name="parameters"></a><span data-ttu-id="751f9-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="751f9-107">Parameters</span></span>



| <span data-ttu-id="751f9-108">Element</span><span class="sxs-lookup"><span data-stu-id="751f9-108">Item</span></span>                                                   | <span data-ttu-id="751f9-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="751f9-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="751f9-110"><span id="m"></span><span id="M"></span>*800*</span><span class="sxs-lookup"><span data-stu-id="751f9-110"><span id="m"></span><span id="M"></span>*m*</span></span><br/> | <span data-ttu-id="751f9-111">\[im \] angegebenen Wert.</span><span class="sxs-lookup"><span data-stu-id="751f9-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="751f9-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="751f9-112">Return Value</span></span>

<span data-ttu-id="751f9-113">Der Gleit Komma Wert, Skalarwert, der den Determinanten des *m* -Parameters darstellt.</span><span class="sxs-lookup"><span data-stu-id="751f9-113">The floating-point, scalar value that represents the determinant of the *m* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="751f9-114">Typbeschreibung</span><span class="sxs-lookup"><span data-stu-id="751f9-114">Type Description</span></span>



| <span data-ttu-id="751f9-115">Name</span><span class="sxs-lookup"><span data-stu-id="751f9-115">Name</span></span>  | [<span data-ttu-id="751f9-116">**Vorlagentyp**</span><span class="sxs-lookup"><span data-stu-id="751f9-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="751f9-117">**Komponententyp**</span><span class="sxs-lookup"><span data-stu-id="751f9-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="751f9-118">Size</span><span class="sxs-lookup"><span data-stu-id="751f9-118">Size</span></span>                                     |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------------------------------------------|
| <span data-ttu-id="751f9-119">*m*</span><span class="sxs-lookup"><span data-stu-id="751f9-119">*m*</span></span>   | [<span data-ttu-id="751f9-120">**Matrix**</span><span class="sxs-lookup"><span data-stu-id="751f9-120">**matrix**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="751f9-121">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="751f9-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="751f9-122">beliebig (Anzahl der Zeilen = Anzahl der Spalten)</span><span class="sxs-lookup"><span data-stu-id="751f9-122">any (number of rows = number of columns)</span></span> |
| <span data-ttu-id="751f9-123">*TZI*</span><span class="sxs-lookup"><span data-stu-id="751f9-123">*ret*</span></span> | [<span data-ttu-id="751f9-124">**Skalar**</span><span class="sxs-lookup"><span data-stu-id="751f9-124">**scalar**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="751f9-125">**float**</span><span class="sxs-lookup"><span data-stu-id="751f9-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="751f9-126">1</span><span class="sxs-lookup"><span data-stu-id="751f9-126">1</span></span>                                        |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="751f9-127">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="751f9-127">Minimum Shader Model</span></span>

<span data-ttu-id="751f9-128">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="751f9-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="751f9-129">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="751f9-129">Shader Model</span></span>                                                                       | <span data-ttu-id="751f9-130">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="751f9-130">Supported</span></span>             |
|------------------------------------------------------------------------------------|-----------------------|
| <span data-ttu-id="751f9-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) und höhere Shader-Modelle</span><span class="sxs-lookup"><span data-stu-id="751f9-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="751f9-132">ja</span><span class="sxs-lookup"><span data-stu-id="751f9-132">yes</span></span>                   |
| [<span data-ttu-id="751f9-133">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="751f9-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="751f9-134">vs \_ 1 \_ 1 und PS \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="751f9-134">vs\_1\_1 and ps\_1\_4</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="751f9-135">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="751f9-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="751f9-136">**Intrinsische Funktionen (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="751f9-136">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

