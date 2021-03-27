---
title: Wavegetlanecount-Funktion
description: Gibt die Anzahl der Bereiche in einer Welle für diese Architektur zurück.
ms.assetid: 04059B5E-0F62-4623-84AD-E41FF7166B34
keywords:
- Wavegetlanecount-Funktion HLSL
topic_type:
- apiref
api_name:
- WaveGetLaneCount
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0bfdb3ce2dfde84b070fee57e7fc587a71d5f948
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104391227"
---
# <a name="wavegetlanecount-function"></a><span data-ttu-id="038a8-104">Wavegetlanecount-Funktion</span><span class="sxs-lookup"><span data-stu-id="038a8-104">WaveGetLaneCount function</span></span>

<span data-ttu-id="038a8-105">Gibt die Anzahl der Bereiche in einer Welle für diese Architektur zurück.</span><span class="sxs-lookup"><span data-stu-id="038a8-105">Returns the number of lanes in a wave on this architecture.</span></span>

## <a name="syntax"></a><span data-ttu-id="038a8-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="038a8-106">Syntax</span></span>

``` syntax
uint WaveGetLaneCount(void);
```

## <a name="parameters"></a><span data-ttu-id="038a8-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="038a8-107">Parameters</span></span>

<span data-ttu-id="038a8-108">Diese Funktion besitzt keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="038a8-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="038a8-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="038a8-109">Return value</span></span>

<span data-ttu-id="038a8-110">Das Ergebnis ist zwischen 4 und 128 und umfasst alle Wellen: aktive, inaktive und/oder hilfsbereiche.</span><span class="sxs-lookup"><span data-stu-id="038a8-110">The result will be between 4 and 128, and includes all waves: active, inactive, and/or helper lanes.</span></span> <span data-ttu-id="038a8-111">Das Ergebnis, das von dieser Funktion zurückgegeben wird, kann sich abhängig von der Treiber Implementierung erheblich unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="038a8-111">The result returned from this function may vary significantly depending on the driver implementation.</span></span>

## <a name="remarks"></a><span data-ttu-id="038a8-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="038a8-112">Remarks</span></span>

<span data-ttu-id="038a8-113">Diese Funktion wird vom Shader-Modell 6,0 in allen shaderphasen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="038a8-113">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="examples"></a><span data-ttu-id="038a8-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="038a8-114">Examples</span></span>

``` syntax
 uint laneCount = WaveGetLaneCount();    // number of lanes in wave
```

## <a name="see-also"></a><span data-ttu-id="038a8-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="038a8-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="038a8-116">Übersicht über Shader-Modell 6</span><span class="sxs-lookup"><span data-stu-id="038a8-116">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="038a8-117">Shader-Modell 6</span><span class="sxs-lookup"><span data-stu-id="038a8-117">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




