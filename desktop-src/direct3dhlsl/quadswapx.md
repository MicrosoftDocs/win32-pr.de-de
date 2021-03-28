---
title: Quad-acrossx-Funktion
description: Gibt den angegebenen lokalen Wert zurück, der von der anderen Strecke in diesem Quad in der X-Richtung gelesen wird.
ms.assetid: 7A7E0623-30EC-4167-90A5-D79E10A394CC
keywords:
- Quads-acrossx-Funktion (HLSL)
topic_type:
- apiref
api_name:
- QuadReadAcrossX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cd41b0bd84861d23153f02ba6328d17b70287866
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104102554"
---
# <a name="quadreadacrossx-function"></a><span data-ttu-id="6be75-104">Quad-acrossx-Funktion</span><span class="sxs-lookup"><span data-stu-id="6be75-104">QuadReadAcrossX function</span></span>

<span data-ttu-id="6be75-105">Gibt den angegebenen lokalen Wert zurück, der von der anderen Strecke in diesem Quad in der X-Richtung gelesen wird.</span><span class="sxs-lookup"><span data-stu-id="6be75-105">Returns the specified local value read from the other lane in this quad in the X direction.</span></span>

## <a name="syntax"></a><span data-ttu-id="6be75-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="6be75-106">Syntax</span></span>

``` syntax
<type> QuadReadAcrossX(
   <type> localValue
);
```

## <a name="parameters"></a><span data-ttu-id="6be75-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="6be75-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6be75-108">*localvalue*</span><span class="sxs-lookup"><span data-stu-id="6be75-108">*localValue*</span></span> 
</dt> <dd>

<span data-ttu-id="6be75-109">Der angeforderte Typ.</span><span class="sxs-lookup"><span data-stu-id="6be75-109">The requested type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6be75-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6be75-110">Return value</span></span>

<span data-ttu-id="6be75-111">Der angegebene lokale Wert.</span><span class="sxs-lookup"><span data-stu-id="6be75-111">The specified local value.</span></span> <span data-ttu-id="6be75-112">Wenn der Quellpfad inaktiv ist, sind die Ergebnisse nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="6be75-112">If the source lane is inactive, the results are undefined.</span></span>

## <a name="remarks"></a><span data-ttu-id="6be75-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6be75-113">Remarks</span></span>

<span data-ttu-id="6be75-114">Weitere Informationen zu den Quads finden Sie unter [Übersicht über Shader Model 6](hlsl-shader-model-6-0-features-for-direct3d-12.md).</span><span class="sxs-lookup"><span data-stu-id="6be75-114">For more information on quads, refer to [Overview of Shader Model 6](hlsl-shader-model-6-0-features-for-direct3d-12.md).</span></span>

<span data-ttu-id="6be75-115">Diese Funktion wird vom Shader-Modell 6,0 nur in Pixel-und Compute-Shadern unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6be75-115">This function is supported from shader model 6.0 only in pixel and compute shaders.</span></span>



 

## <a name="see-also"></a><span data-ttu-id="6be75-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="6be75-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6be75-117">Shader-Modell 6</span><span class="sxs-lookup"><span data-stu-id="6be75-117">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




