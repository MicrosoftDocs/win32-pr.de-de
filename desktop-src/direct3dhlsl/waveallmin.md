---
title: Waveactivemin-Funktion
description: Gibt den minimalen Wert des Ausdrucks über alle aktiven Bereiche in der aktuellen Wave zurück, die auf alle aktiven Bereiche repliziert werden.
ms.assetid: BA762C02-894C-4AF9-A226-C1E3AAC286FF
keywords:
- Waveactivemin-Funktion HLSL
topic_type:
- apiref
api_name:
- WaveActiveMin
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 91555df354ab2b7ffc447a9422c4811ae23e6e0c
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104039840"
---
# <a name="waveactivemin-function"></a><span data-ttu-id="5f8b3-104">Waveactivemin-Funktion</span><span class="sxs-lookup"><span data-stu-id="5f8b3-104">WaveActiveMin function</span></span>

<span data-ttu-id="5f8b3-105">Gibt den minimalen Wert des Ausdrucks über alle aktiven Bereiche in der aktuellen Wave zurück, die auf alle aktiven Bereiche repliziert werden.</span><span class="sxs-lookup"><span data-stu-id="5f8b3-105">Returns the minimum value of the expression across all active lanes in the current wave replicates it back to all active lanes.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f8b3-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="5f8b3-106">Syntax</span></span>

``` syntax
<type> WaveActiveMin(
   <type> expr
);
```

## <a name="parameters"></a><span data-ttu-id="5f8b3-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="5f8b3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f8b3-108">*expr*</span><span class="sxs-lookup"><span data-stu-id="5f8b3-108">*expr*</span></span> 
</dt> <dd>

<span data-ttu-id="5f8b3-109">Der auszuwertende Ausdruck.</span><span class="sxs-lookup"><span data-stu-id="5f8b3-109">The expression to evaluate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f8b3-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5f8b3-110">Return value</span></span>

<span data-ttu-id="5f8b3-111">Der Minimalwert.</span><span class="sxs-lookup"><span data-stu-id="5f8b3-111">The minimum value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f8b3-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5f8b3-112">Remarks</span></span>

<span data-ttu-id="5f8b3-113">Die Reihenfolge der Vorgänge ist nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="5f8b3-113">The order of operations is undefined.</span></span>

<span data-ttu-id="5f8b3-114">Diese Funktion wird vom Shader-Modell 6,0 in allen shaderphasen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5f8b3-114">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="examples"></a><span data-ttu-id="5f8b3-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5f8b3-115">Examples</span></span>

``` syntax
 float3 minPos = WaveActiveMin( myPoint.position );
    BoundingBox.min = min( minPos, BoundingBox.min );
```

## <a name="see-also"></a><span data-ttu-id="5f8b3-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="5f8b3-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f8b3-117">Übersicht über Shader-Modell 6</span><span class="sxs-lookup"><span data-stu-id="5f8b3-117">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="5f8b3-118">Shader-Modell 6</span><span class="sxs-lookup"><span data-stu-id="5f8b3-118">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




