---
title: Waveactivebitxor-Funktion
description: Gibt das bitweise XOR aller Werte des Ausdrucks über alle aktiven Bereiche in der aktuellen Wave zurück und repliziert Sie zurück in alle aktiven Bereiche.
ms.assetid: A6807D17-1E6E-4997-AB52-32FAB5857219
keywords:
- Waveactivebitxor-Funktion HLSL
topic_type:
- apiref
api_name:
- WaveActiveBitXor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7e55ce8a43311f4f4c428e97bff1e107ab5c7038
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104039839"
---
# <a name="waveactivebitxor-function"></a><span data-ttu-id="b5465-104">Waveactivebitxor-Funktion</span><span class="sxs-lookup"><span data-stu-id="b5465-104">WaveActiveBitXor function</span></span>

<span data-ttu-id="b5465-105">Gibt das bitweise XOR aller Werte des Ausdrucks über alle aktiven Bereiche in der aktuellen Wave zurück und repliziert Sie zurück in alle aktiven Bereiche.</span><span class="sxs-lookup"><span data-stu-id="b5465-105">Returns the bitwise XOR of all the values of the expression across all active lanes in the current wave and replicates it back to all active lanes.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5465-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="b5465-106">Syntax</span></span>

``` syntax
<int_type> WaveActiveBitXor(
   <int_type> expr
);
```

## <a name="parameters"></a><span data-ttu-id="b5465-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="b5465-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5465-108">*expr*</span><span class="sxs-lookup"><span data-stu-id="b5465-108">*expr*</span></span> 
</dt> <dd>

<span data-ttu-id="b5465-109">Der auszuwertende Ausdruck.</span><span class="sxs-lookup"><span data-stu-id="b5465-109">The expression to evaluate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5465-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b5465-110">Return value</span></span>

<span data-ttu-id="b5465-111">Der bitweise XOR-Wert.</span><span class="sxs-lookup"><span data-stu-id="b5465-111">The bitwise XOR value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5465-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b5465-112">Remarks</span></span>

<span data-ttu-id="b5465-113">Diese Funktion wird vom Shader-Modell 6,0 in allen shaderphasen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b5465-113">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="see-also"></a><span data-ttu-id="b5465-114">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b5465-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5465-115">Übersicht über Shader-Modell 6</span><span class="sxs-lookup"><span data-stu-id="b5465-115">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="b5465-116">Shader-Modell 6</span><span class="sxs-lookup"><span data-stu-id="b5465-116">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




