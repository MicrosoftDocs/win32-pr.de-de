---
title: Waveactiveproduct-Funktion
description: Multipliziert die Werte des Ausdrucks über alle aktiven Bereiche in der aktuellen Welle und repliziert Sie zurück in alle aktiven Bereiche.
ms.assetid: B259244D-C993-4F4A-AF09-F077D99AD025
keywords:
- Waveactiveproduct-Funktion HLSL
topic_type:
- apiref
api_name:
- WaveActiveProduct
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b8e1d400541a2654657c1a462c38494d20af13e6
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "103858550"
---
# <a name="waveactiveproduct-function"></a><span data-ttu-id="281cb-104">Waveactiveproduct-Funktion</span><span class="sxs-lookup"><span data-stu-id="281cb-104">WaveActiveProduct function</span></span>

<span data-ttu-id="281cb-105">Multipliziert die Werte des Ausdrucks über alle aktiven Bereiche in der aktuellen Welle und repliziert Sie zurück in alle aktiven Bereiche.</span><span class="sxs-lookup"><span data-stu-id="281cb-105">Multiplies the values of the expression together across all active lanes in the current wave and replicates it back to all active lanes.</span></span>

## <a name="syntax"></a><span data-ttu-id="281cb-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="281cb-106">Syntax</span></span>

``` syntax
<type> WaveActiveProduct(
   <type> expr
);
```

## <a name="parameters"></a><span data-ttu-id="281cb-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="281cb-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="281cb-108">*expr*</span><span class="sxs-lookup"><span data-stu-id="281cb-108">*expr*</span></span> 
</dt> <dd>

<span data-ttu-id="281cb-109">Der auszuwertende Ausdruck.</span><span class="sxs-lookup"><span data-stu-id="281cb-109">The expression to evaluate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="281cb-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="281cb-110">Return value</span></span>

<span data-ttu-id="281cb-111">Der Produktwert.</span><span class="sxs-lookup"><span data-stu-id="281cb-111">The product value.</span></span>

## <a name="remarks"></a><span data-ttu-id="281cb-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="281cb-112">Remarks</span></span>

<span data-ttu-id="281cb-113">Die Reihenfolge der Vorgänge ist nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="281cb-113">The order of operations is undefined.</span></span>

<span data-ttu-id="281cb-114">Diese Funktion wird vom Shader-Modell 6,0 in allen shaderphasen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="281cb-114">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="see-also"></a><span data-ttu-id="281cb-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="281cb-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="281cb-116">Übersicht über Shader-Modell 6</span><span class="sxs-lookup"><span data-stu-id="281cb-116">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="281cb-117">Shader-Modell 6</span><span class="sxs-lookup"><span data-stu-id="281cb-117">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




