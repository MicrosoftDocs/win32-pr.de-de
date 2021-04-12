---
title: Waveactivezähltbits-Funktion
description: Zählt die Anzahl von booleschen Variablen, die für alle aktiven Bereiche in der aktuellen Wave als true ausgewertet werden, und repliziert das Ergebnis in alle Bereiche in der Wave.
ms.assetid: 053E100C-7E09-4F9D-9F38-9D5E208A38CE
keywords:
- Waveactivezähltbits-Funktion HLSL
topic_type:
- apiref
api_name:
- WaveActiveCountBits
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4c4d2db55e9e3a0ad8f0a66be183d6e39d2a8b9c
ms.sourcegitcommit: a232805e6c618673f2df904111cc4f5a33e15504
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/07/2020
ms.locfileid: "104316868"
---
# <a name="waveactivecountbits-function"></a><span data-ttu-id="74648-104">Waveactivezähltbits-Funktion</span><span class="sxs-lookup"><span data-stu-id="74648-104">WaveActiveCountBits function</span></span>

<span data-ttu-id="74648-105">Zählt die Anzahl von booleschen Variablen, die für alle aktiven Bereiche in der aktuellen Wave als true ausgewertet werden, und repliziert das Ergebnis in alle Bereiche in der Wave.</span><span class="sxs-lookup"><span data-stu-id="74648-105">Counts the number of boolean variables which evaluate to true across all active lanes in the current wave, and replicates the result to all lanes in the wave.</span></span>

## <a name="syntax"></a><span data-ttu-id="74648-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="74648-106">Syntax</span></span>


``` syntax
uint WaveActiveCountBits(
   bool bBit
);
```



## <a name="parameters"></a><span data-ttu-id="74648-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="74648-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74648-108">*Bbit*</span><span class="sxs-lookup"><span data-stu-id="74648-108">*bBit*</span></span> 
</dt> <dd>

<span data-ttu-id="74648-109">Die auszuwertenden booleschen Variablen.</span><span class="sxs-lookup"><span data-stu-id="74648-109">The boolean variables to evaluate.</span></span> <span data-ttu-id="74648-110">Durch die Angabe eines expliziten echten booleschen Werts wird die Anzahl der aktiven Bereiche zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="74648-110">Providing an explicit true Boolean value returns the number of active lanes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74648-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="74648-111">Return value</span></span>

<span data-ttu-id="74648-112">Die Anzahl, die in allen aktiven Bereichen in der aktuellen Wave als true ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="74648-112">The number of which evaluate to true across all active lanes in the current wave.</span></span>

## <a name="remarks"></a><span data-ttu-id="74648-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="74648-113">Remarks</span></span>

<span data-ttu-id="74648-114">Diese Funktion wird vom Shader-Modell 6,0 in allen shaderphasen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="74648-114">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="examples"></a><span data-ttu-id="74648-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="74648-115">Examples</span></span>

<span data-ttu-id="74648-116">Dies kann effizienter als ein vollständiger waveactivesum implementiert werden, wie im folgenden Beispiel beschrieben:</span><span class="sxs-lookup"><span data-stu-id="74648-116">This can be implemented more efficiently than a full WaveActiveSum, as described in the following example:</span></span>

``` syntax
result = WaveActiveCountBits( WaveActiveBallot( bBit ) );
```

## <a name="see-also"></a><span data-ttu-id="74648-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="74648-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74648-118">Übersicht über Shader-Modell 6</span><span class="sxs-lookup"><span data-stu-id="74648-118">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="74648-119">Shader-Modell 6</span><span class="sxs-lookup"><span data-stu-id="74648-119">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




