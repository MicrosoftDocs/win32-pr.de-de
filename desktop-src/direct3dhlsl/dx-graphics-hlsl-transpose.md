---
title: austauschen
description: Vertauscht die angegebene Eingabe Matrix.
ms.assetid: 2a2ff2fb-73f0-4bb8-af83-38fe0567d122
keywords:
- HLSL austauschen
topic_type:
- apiref
api_name:
- transpose
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 44f129a87edaff260de87136954be7598ee3acb6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390427"
---
# <a name="transpose"></a><span data-ttu-id="39cd2-104">austauschen</span><span class="sxs-lookup"><span data-stu-id="39cd2-104">transpose</span></span>

<span data-ttu-id="39cd2-105">Vertauscht die angegebene Eingabe Matrix.</span><span class="sxs-lookup"><span data-stu-id="39cd2-105">Transposes the specified input matrix.</span></span>



| <span data-ttu-id="39cd2-106">Ret-austauschen (*x*)</span><span class="sxs-lookup"><span data-stu-id="39cd2-106">ret transpose(*x*)</span></span> |
|--------------------|



 

## <a name="parameters"></a><span data-ttu-id="39cd2-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="39cd2-107">Parameters</span></span>



| <span data-ttu-id="39cd2-108">Element</span><span class="sxs-lookup"><span data-stu-id="39cd2-108">Item</span></span>                                                   | <span data-ttu-id="39cd2-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="39cd2-109">Description</span></span>                             |
|--------------------------------------------------------|-----------------------------------------|
| <span data-ttu-id="39cd2-110"><span id="x"></span><span id="X"></span>*Stuben*</span><span class="sxs-lookup"><span data-stu-id="39cd2-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="39cd2-111">\[in \] der angegebenen Matrix.</span><span class="sxs-lookup"><span data-stu-id="39cd2-111">\[in\] The specified matrix.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="39cd2-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="39cd2-112">Return Value</span></span>

<span data-ttu-id="39cd2-113">Der übersetzte Wert des *x* -Parameters.</span><span class="sxs-lookup"><span data-stu-id="39cd2-113">The transposed value of the *x* parameter.</span></span>

## <a name="remarks"></a><span data-ttu-id="39cd2-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="39cd2-114">Remarks</span></span>

<span data-ttu-id="39cd2-115">Wenn die Dimensionen der Quell Matrix *Zeilen* *Spalten* sind, handelt es sich bei der resultierenden Matrix um *Spalten* *Zeilen*.</span><span class="sxs-lookup"><span data-stu-id="39cd2-115">If the dimensions of the source matrix are *rows* *columns*, the resulting matrix is *columns* *rows*.</span></span>

## <a name="type-description"></a><span data-ttu-id="39cd2-116">Typbeschreibung</span><span class="sxs-lookup"><span data-stu-id="39cd2-116">Type Description</span></span>



| <span data-ttu-id="39cd2-117">Name</span><span class="sxs-lookup"><span data-stu-id="39cd2-117">Name</span></span> | [<span data-ttu-id="39cd2-118">**Vorlagentyp**</span><span class="sxs-lookup"><span data-stu-id="39cd2-118">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="39cd2-119">**Komponententyp**</span><span class="sxs-lookup"><span data-stu-id="39cd2-119">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                         | <span data-ttu-id="39cd2-120">Size</span><span class="sxs-lookup"><span data-stu-id="39cd2-120">Size</span></span>                                                                                   |
|------|-------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="39cd2-121">*x*</span><span class="sxs-lookup"><span data-stu-id="39cd2-121">*x*</span></span>  | [<span data-ttu-id="39cd2-122">**Matrix**</span><span class="sxs-lookup"><span data-stu-id="39cd2-122">**matrix**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="39cd2-123">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types), [**bool**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="39cd2-123">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types), [**bool**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="39cd2-124">any</span><span class="sxs-lookup"><span data-stu-id="39cd2-124">any</span></span>                                                                                    |
| <span data-ttu-id="39cd2-125">TZI</span><span class="sxs-lookup"><span data-stu-id="39cd2-125">ret</span></span>  | [<span data-ttu-id="39cd2-126">**Matrix**</span><span class="sxs-lookup"><span data-stu-id="39cd2-126">**matrix**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="39cd2-127">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types), [**bool**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="39cd2-127">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types), [**bool**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="39cd2-128">Rows = gleiche Anzahl von Spalten wie Eingabe *x*, Spalten = gleiche Anzahl von Zeilen als Eingabe *x*</span><span class="sxs-lookup"><span data-stu-id="39cd2-128">rows = same number of columns as input *x*, columns = same number of rows as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="39cd2-129">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="39cd2-129">Minimum Shader Model</span></span>

<span data-ttu-id="39cd2-130">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="39cd2-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="39cd2-131">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="39cd2-131">Shader Model</span></span>                                                                       | <span data-ttu-id="39cd2-132">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="39cd2-132">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="39cd2-133">[Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) und höhere Shader-Modelle</span><span class="sxs-lookup"><span data-stu-id="39cd2-133">[Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) and higher shader models</span></span> | <span data-ttu-id="39cd2-134">ja</span><span class="sxs-lookup"><span data-stu-id="39cd2-134">yes</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="39cd2-135">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="39cd2-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39cd2-136">**Intrinsische Funktionen (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="39cd2-136">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

