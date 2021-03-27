---
title: Waveactivemax-Funktion
description: Gibt den maximalen Wert des Ausdrucks für alle aktiven Bereiche in der aktuellen Wave zurück und repliziert Sie zurück in alle aktiven Bereiche.
ms.assetid: 19101C56-2618-4F34-8725-DF92198ABDA4
keywords:
- Waveactivemax-Funktion HLSL
topic_type:
- apiref
api_name:
- WaveActiveMax
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7c0fd10f578d598c326cdfb4cf943d3a35fe78a9
ms.sourcegitcommit: a232805e6c618673f2df904111cc4f5a33e15504
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/07/2020
ms.locfileid: "104391275"
---
# <a name="waveactivemax-function"></a><span data-ttu-id="7d7c3-104">Waveactivemax-Funktion</span><span class="sxs-lookup"><span data-stu-id="7d7c3-104">WaveActiveMax function</span></span>

<span data-ttu-id="7d7c3-105">Gibt den maximalen Wert des Ausdrucks für alle aktiven Bereiche in der aktuellen Wave zurück und repliziert Sie zurück in alle aktiven Bereiche.</span><span class="sxs-lookup"><span data-stu-id="7d7c3-105">Returns the maximum value of the expression across all active lanes in the current wave and replicates it back to all active lanes.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d7c3-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="7d7c3-106">Syntax</span></span>

``` syntax
<type> WaveActiveMax(
   <type> expr
);
```

## <a name="parameters"></a><span data-ttu-id="7d7c3-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="7d7c3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d7c3-108">*expr*</span><span class="sxs-lookup"><span data-stu-id="7d7c3-108">*expr*</span></span> 
</dt> <dd>

<span data-ttu-id="7d7c3-109">Der auszuwertende Ausdruck.</span><span class="sxs-lookup"><span data-stu-id="7d7c3-109">The expression to evaluate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d7c3-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7d7c3-110">Return value</span></span>

<span data-ttu-id="7d7c3-111">Der Maximalwert.</span><span class="sxs-lookup"><span data-stu-id="7d7c3-111">The maximum value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7d7c3-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7d7c3-112">Remarks</span></span>

<span data-ttu-id="7d7c3-113">Die Reihenfolge der Vorgänge ist nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="7d7c3-113">The order of operations is undefined.</span></span>

<span data-ttu-id="7d7c3-114">Diese Funktion wird vom Shader-Modell 6,0 in allen shaderphasen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7d7c3-114">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="examples"></a><span data-ttu-id="7d7c3-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7d7c3-115">Examples</span></span>

``` syntax
 float3 maxPos = WaveActiveMax( myPoint.position );
    BoundingBox.max = max( maxPos, BoundingBox.max );
```

## <a name="see-also"></a><span data-ttu-id="7d7c3-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="7d7c3-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d7c3-117">Übersicht über Shader-Modell 6</span><span class="sxs-lookup"><span data-stu-id="7d7c3-117">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="7d7c3-118">Shader-Modell 6</span><span class="sxs-lookup"><span data-stu-id="7d7c3-118">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




