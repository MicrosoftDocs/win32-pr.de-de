---
title: Quadread acrossy-Funktion
description: Gibt den angegebenen Quellwert zurück, der von der anderen Strecke in diesem Quad in der Y-Richtung gelesen wird.
ms.assetid: 6C03D1E6-433F-4CCA-A5EA-C3F34BB2B93B
keywords:
- Quada-Funktion (HLSL)
topic_type:
- apiref
api_name:
- QuadReadAcrossY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 72b5ede0df733e60ba4b1bcc01a04f1daaedc708
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104976880"
---
# <a name="quadreadacrossy-function"></a><span data-ttu-id="c4d5b-104">Quadread acrossy-Funktion</span><span class="sxs-lookup"><span data-stu-id="c4d5b-104">QuadReadAcrossY function</span></span>

<span data-ttu-id="c4d5b-105">Gibt den angegebenen Quellwert zurück, der von der anderen Strecke in diesem Quad in der Y-Richtung gelesen wird.</span><span class="sxs-lookup"><span data-stu-id="c4d5b-105">Returns the specified source value read from the other lane in this quad in the Y direction.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4d5b-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="c4d5b-106">Syntax</span></span>

``` syntax
<type> QuadReadAcrossY(
   <type> localValue
);
```

## <a name="parameters"></a><span data-ttu-id="c4d5b-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="c4d5b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4d5b-108">*localvalue*</span><span class="sxs-lookup"><span data-stu-id="c4d5b-108">*localValue*</span></span> 
</dt> <dd>

<span data-ttu-id="c4d5b-109">Der angeforderte Typ.</span><span class="sxs-lookup"><span data-stu-id="c4d5b-109">The requested type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4d5b-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c4d5b-110">Return value</span></span>

<span data-ttu-id="c4d5b-111">Der angegebene Quellwert.</span><span class="sxs-lookup"><span data-stu-id="c4d5b-111">The specified source value.</span></span> <span data-ttu-id="c4d5b-112">Wenn der Quellpfad inaktiv ist, sind die Ergebnisse nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="c4d5b-112">If the source lane is inactive, the results are undefined.</span></span>

## <a name="remarks"></a><span data-ttu-id="c4d5b-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c4d5b-113">Remarks</span></span>

<span data-ttu-id="c4d5b-114">Weitere Informationen zu den Quads finden Sie unter [Übersicht über Shader Model 6](hlsl-shader-model-6-0-features-for-direct3d-12.md).</span><span class="sxs-lookup"><span data-stu-id="c4d5b-114">For more information on quads, refer to [Overview of Shader Model 6](hlsl-shader-model-6-0-features-for-direct3d-12.md).</span></span>

<span data-ttu-id="c4d5b-115">Diese Funktion wird vom Shader-Modell 6,0 nur in Pixel-und Compute-Shadern unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c4d5b-115">This function is supported from shader model 6.0 only in pixel and compute shaders.</span></span>



 

## <a name="see-also"></a><span data-ttu-id="c4d5b-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c4d5b-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4d5b-117">Shader-Modell 6</span><span class="sxs-lookup"><span data-stu-id="c4d5b-117">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




