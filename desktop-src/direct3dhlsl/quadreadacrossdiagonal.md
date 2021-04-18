---
title: Quad-acrossdiagonal-Funktion
description: Gibt den angegebenen lokalen Wert zurück, der aus der Diagonal umgekehrten Spur in diesem Quad gelesen wird.
ms.assetid: 2914F1F9-5CE2-437A-ADDB-4955D2C1490B
keywords:
- HLSL-Funktion der quadread acrossdiagonal
topic_type:
- apiref
api_name:
- QuadReadAcrossDiagonal
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0e208a022f339e69ea63120db1f67070fa4dfed7
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104993630"
---
# <a name="quadreadacrossdiagonal-function"></a><span data-ttu-id="5f52b-104">Quad-acrossdiagonal-Funktion</span><span class="sxs-lookup"><span data-stu-id="5f52b-104">QuadReadAcrossDiagonal function</span></span>

<span data-ttu-id="5f52b-105">Gibt den angegebenen lokalen Wert zurück, der aus der Diagonal umgekehrten Spur in diesem Quad gelesen wird.</span><span class="sxs-lookup"><span data-stu-id="5f52b-105">Returns the specified local value which is read from the diagonally opposite lane in this quad.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f52b-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="5f52b-106">Syntax</span></span>


``` syntax
<type> QuadReadAcrossDiagonal(
   <type> localValue
);
```



## <a name="parameters"></a><span data-ttu-id="5f52b-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="5f52b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f52b-108">*localvalue*</span><span class="sxs-lookup"><span data-stu-id="5f52b-108">*localValue*</span></span> 
</dt> <dd>

<span data-ttu-id="5f52b-109">Der angeforderte Typ.</span><span class="sxs-lookup"><span data-stu-id="5f52b-109">The requested type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f52b-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5f52b-110">Return value</span></span>

<span data-ttu-id="5f52b-111">Der angegebene lokale Wert, der aus der Diagonal umgekehrten Strecke in diesem Quad gelesen wird.</span><span class="sxs-lookup"><span data-stu-id="5f52b-111">The specified local value which is read from the diagonally opposite lane in this quad.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f52b-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5f52b-112">Remarks</span></span>

<span data-ttu-id="5f52b-113">Weitere Informationen zu den Quads finden Sie unter [Übersicht über Shader Model 6](hlsl-shader-model-6-0-features-for-direct3d-12.md).</span><span class="sxs-lookup"><span data-stu-id="5f52b-113">For more information on quads, refer to [Overview of Shader Model 6](hlsl-shader-model-6-0-features-for-direct3d-12.md).</span></span>

<span data-ttu-id="5f52b-114">Diese Funktion wird vom Shader-Modell 6,0 nur in Pixel-und Compute-Shadern unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5f52b-114">This function is supported from shader model 6.0 only in pixel and compute shaders.</span></span>



 

## <a name="see-also"></a><span data-ttu-id="5f52b-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="5f52b-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f52b-116">Shader-Modell 6</span><span class="sxs-lookup"><span data-stu-id="5f52b-116">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




