---
title: Quadleserlaneat-Funktion
description: Gibt den angegebenen Quellwert aus der durch die Lane-ID im aktuellen Quad identifizierten Spur zurück.
ms.assetid: 5CD7EE4C-E64E-46A3-ABDC-1BF65D0F96BE
keywords:
- Quada-Funktion (HLSL)
topic_type:
- apiref
api_name:
- QuadReadLaneAt
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ddc772c2dca66873891483431eab14ad504da77e
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104474644"
---
# <a name="quadreadlaneat-function"></a><span data-ttu-id="7d175-104">Quadleserlaneat-Funktion</span><span class="sxs-lookup"><span data-stu-id="7d175-104">QuadReadLaneAt function</span></span>

<span data-ttu-id="7d175-105">Gibt den angegebenen Quellwert aus der durch die Lane-ID im aktuellen Quad identifizierten Spur zurück.</span><span class="sxs-lookup"><span data-stu-id="7d175-105">Returns the specified source value from the lane identified by the lane ID within the current quad.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d175-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="7d175-106">Syntax</span></span>


``` syntax
<type> QuadReadLaneAt(
   <type> sourceValue,
   uint   quadLaneID  
);
```



## <a name="parameters"></a><span data-ttu-id="7d175-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="7d175-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d175-108">*Quellwert*</span><span class="sxs-lookup"><span data-stu-id="7d175-108">*sourceValue*</span></span> 
</dt> <dd>

<span data-ttu-id="7d175-109">Der angeforderte Typ.</span><span class="sxs-lookup"><span data-stu-id="7d175-109">The requested type.</span></span>

</dd> <dt>

<span data-ttu-id="7d175-110">*quadlaneid*</span><span class="sxs-lookup"><span data-stu-id="7d175-110">*quadLaneID*</span></span> 
</dt> <dd>

<span data-ttu-id="7d175-111">Die Lane-ID; Dabei handelt es sich um einen Wert zwischen 0 und 3.</span><span class="sxs-lookup"><span data-stu-id="7d175-111">The lane ID; this will be a value from 0 to 3.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d175-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7d175-112">Return value</span></span>

<span data-ttu-id="7d175-113">Der angegebene Quellwert.</span><span class="sxs-lookup"><span data-stu-id="7d175-113">The specified source value.</span></span> <span data-ttu-id="7d175-114">Das Ergebnis dieser Funktion ist für das Vierfache einheitlich.</span><span class="sxs-lookup"><span data-stu-id="7d175-114">The result of this function is uniform across the quad.</span></span> <span data-ttu-id="7d175-115">Wenn der Quellpfad inaktiv ist, sind die Ergebnisse nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="7d175-115">If the source lane is inactive, the results are undefined.</span></span>

## <a name="remarks"></a><span data-ttu-id="7d175-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7d175-116">Remarks</span></span>

<span data-ttu-id="7d175-117">Weitere Informationen zu den Quads finden Sie unter [Übersicht über Shader Model 6](hlsl-shader-model-6-0-features-for-direct3d-12.md).</span><span class="sxs-lookup"><span data-stu-id="7d175-117">For more information on quads, refer to [Overview of Shader Model 6](hlsl-shader-model-6-0-features-for-direct3d-12.md).</span></span>

<span data-ttu-id="7d175-118">Diese Funktion wird vom Shader-Modell 6,0 nur in Pixel-und Compute-Shadern unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7d175-118">This function is supported from shader model 6.0 only in pixel and compute shaders.</span></span>



 

## <a name="see-also"></a><span data-ttu-id="7d175-119">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="7d175-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d175-120">Shader-Modell 6</span><span class="sxs-lookup"><span data-stu-id="7d175-120">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




