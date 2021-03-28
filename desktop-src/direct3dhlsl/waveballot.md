---
title: Waveactiveballot-Funktion
description: Gibt einen uint4-Wert zurück, der eine Bitmaske der Auswertung des booleschen Ausdrucks für alle aktiven Bereiche in der aktuellen Wave enthält.
ms.assetid: 67FE28E0-F397-431A-8CF8-64E4AD88CDBC
keywords:
- Waveactiveballot-Funktion HLSL
topic_type:
- apiref
api_name:
- WaveActiveBallot
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e3cdd89fad7da1e4ba7f3d5e032370834166a114
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104517210"
---
# <a name="waveactiveballot-function"></a><span data-ttu-id="0f6f7-104">Waveactiveballot-Funktion</span><span class="sxs-lookup"><span data-stu-id="0f6f7-104">WaveActiveBallot function</span></span>

<span data-ttu-id="0f6f7-105">Gibt einen uint4-Wert zurück, der eine Bitmaske der Auswertung des booleschen Ausdrucks für alle aktiven Bereiche in der aktuellen Wave enthält.</span><span class="sxs-lookup"><span data-stu-id="0f6f7-105">Returns a uint4 containing a bitmask of the evaluation of the Boolean expression for all active lanes in the current wave.</span></span> 

## <a name="syntax"></a><span data-ttu-id="0f6f7-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="0f6f7-106">Syntax</span></span>

``` syntax
uint4 WaveBallot(
   bool expr
);
```

## <a name="parameters"></a><span data-ttu-id="0f6f7-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="0f6f7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f6f7-108">*expr*</span><span class="sxs-lookup"><span data-stu-id="0f6f7-108">*expr*</span></span> 
</dt> <dd>

<span data-ttu-id="0f6f7-109">Der auszuwertende boolesche Ausdruck.</span><span class="sxs-lookup"><span data-stu-id="0f6f7-109">The boolean expression to evaluate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f6f7-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0f6f7-110">Return value</span></span>

<span data-ttu-id="0f6f7-111">Ein uint4-Wert, der eine Bitmaske der Auswertung des booleschen Ausdrucks für alle aktiven Bereiche in der aktuellen Wave enthält.</span><span class="sxs-lookup"><span data-stu-id="0f6f7-111">A uint4 containing a bitmask of the evaluation of the Boolean expression for all active lanes in the current wave.</span></span> <span data-ttu-id="0f6f7-112">Das unwichtigste Bit entspricht dem Bereich mit dem Index 0 (null).</span><span class="sxs-lookup"><span data-stu-id="0f6f7-112">The least-significant bit corresponds to the lane with index zero.</span></span> <span data-ttu-id="0f6f7-113">Die Bits, die inaktiven Bereichen entsprechen, sind 0 (null).</span><span class="sxs-lookup"><span data-stu-id="0f6f7-113">The bits corresponding to inactive lanes will be zero.</span></span> <span data-ttu-id="0f6f7-114">Die Bits, die größer oder gleich [**wavegetlanecount**](wavegetlanecount.md) sind, sind 0 (null).</span><span class="sxs-lookup"><span data-stu-id="0f6f7-114">The bits that are greater than or equal to [**WaveGetLaneCount**](wavegetlanecount.md) will be zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f6f7-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0f6f7-115">Remarks</span></span>

<span data-ttu-id="0f6f7-116">Unterschiedliche GPUs verfügen über unterschiedliche SIMD-Prozessor breiten (Lane Counts).</span><span class="sxs-lookup"><span data-stu-id="0f6f7-116">Different GPUs have different SIMD processor widths (lane counts).</span></span> <span data-ttu-id="0f6f7-117">Die meisten dieser **wavexxx** -Funktionen können auf Abstraktions Ebene betrieben werden, wenn die Breite des SIMD-Computers verborgen ist.</span><span class="sxs-lookup"><span data-stu-id="0f6f7-117">Most of these **WaveXXX** functions are able to operate at level of abstraction where SIMD machine width is concealed.</span></span> <span data-ttu-id="0f6f7-118">Verwenden Sie die systeminternen Funktionen, die nicht auf der Computer Breite basieren, um die Portabilität von Code über GPUs zu maximieren.</span><span class="sxs-lookup"><span data-stu-id="0f6f7-118">To maximize portability of code across GPUs, use the intrinsics that don’t rely on machine width.</span></span> <span data-ttu-id="0f6f7-119">Verwenden Sie z.B. Folgendes:</span><span class="sxs-lookup"><span data-stu-id="0f6f7-119">For example, use:</span></span>

``` syntax
uint result = WaveActiveCountBits( bBit );
```

<span data-ttu-id="0f6f7-120">anstelle von:</span><span class="sxs-lookup"><span data-stu-id="0f6f7-120">Instead of:</span></span>

``` syntax
uint result = countbits( WaveActiveBallot( bBit ) );
```

<span data-ttu-id="0f6f7-121">Diese Funktion wird vom Shader-Modell 6,0 in allen shaderphasen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0f6f7-121">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="examples"></a><span data-ttu-id="0f6f7-122">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0f6f7-122">Examples</span></span>

``` syntax
// get a bitwise representation of the number of currently active lanes:
uint4 waveBits = WaveActiveBallot( true ); // convert to bits 
```

## <a name="see-also"></a><span data-ttu-id="0f6f7-123">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="0f6f7-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f6f7-124">Übersicht über Shader-Modell 6</span><span class="sxs-lookup"><span data-stu-id="0f6f7-124">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="0f6f7-125">Shader-Modell 6</span><span class="sxs-lookup"><span data-stu-id="0f6f7-125">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




