---
title: Waveactivesum-Funktion
description: Fasst den Wert des Ausdrucks für alle aktiven Bereiche in der aktuellen Wave zusammen und repliziert Sie in allen Bereichen in der aktuellen Wave.
ms.assetid: 94CEF4AA-D6DE-4B00-9743-F491F255FE3D
keywords:
- Waveactivesum-Funktion HLSL
topic_type:
- apiref
api_name:
- WaveActiveSum
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b98ecf2521841b9da73e1b917d44f1d91b7876d2
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "103949220"
---
# <a name="waveactivesum-function"></a><span data-ttu-id="288bf-104">Waveactivesum-Funktion</span><span class="sxs-lookup"><span data-stu-id="288bf-104">WaveActiveSum function</span></span>

<span data-ttu-id="288bf-105">Fasst den Wert des Ausdrucks für alle aktiven Bereiche in der aktuellen Wave zusammen und repliziert Sie in allen Bereichen in der aktuellen Wave.</span><span class="sxs-lookup"><span data-stu-id="288bf-105">Sums up the value of the expression across all active lanes in the current wave and replicates it to all lanes in the current wave.</span></span>

## <a name="syntax"></a><span data-ttu-id="288bf-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="288bf-106">Syntax</span></span>

``` syntax
<type> WaveActiveSum(
   <type> expr
);
```

## <a name="parameters"></a><span data-ttu-id="288bf-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="288bf-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="288bf-108">*expr*</span><span class="sxs-lookup"><span data-stu-id="288bf-108">*expr*</span></span> 
</dt> <dd>

<span data-ttu-id="288bf-109">Der auszuwertende Ausdruck.</span><span class="sxs-lookup"><span data-stu-id="288bf-109">The expression to evaluate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="288bf-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="288bf-110">Return value</span></span>

<span data-ttu-id="288bf-111">Der Sum-Wert.</span><span class="sxs-lookup"><span data-stu-id="288bf-111">The sum value.</span></span>

## <a name="remarks"></a><span data-ttu-id="288bf-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="288bf-112">Remarks</span></span>

<span data-ttu-id="288bf-113">Die Reihenfolge der Vorgänge ist nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="288bf-113">The order of operations is undefined.</span></span>

<span data-ttu-id="288bf-114">Diese Funktion wird vom Shader-Modell 6,0 in allen shaderphasen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="288bf-114">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="examples"></a><span data-ttu-id="288bf-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="288bf-115">Examples</span></span>

``` syntax
float3 total = WaveActiveSum( position ); // sum positions in wave
float3 center = total/count;           // compute average of these positions
```

## <a name="see-also"></a><span data-ttu-id="288bf-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="288bf-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="288bf-117">Übersicht über Shader-Modell 6</span><span class="sxs-lookup"><span data-stu-id="288bf-117">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="288bf-118">Shader-Modell 6</span><span class="sxs-lookup"><span data-stu-id="288bf-118">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




