---
title: Waveprefixzähltbits-Funktion
description: Gibt die Summe aller angegebenen booleschen Variablen für alle aktiven Bereiche mit Indizes zurück, die kleiner als die aktuelle Seite sind.
ms.assetid: AEC9AFD7-6478-4397-B531-73990D30AA48
keywords:
- Waveprefixzähltbits-Funktion HLSL
topic_type:
- apiref
api_name:
- WavePrefixCountBits
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 72f35df1e463ff89441938e4cae19a890821baf9
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104039845"
---
# <a name="waveprefixcountbits-function"></a><span data-ttu-id="a3ec1-104">Waveprefixzähltbits-Funktion</span><span class="sxs-lookup"><span data-stu-id="a3ec1-104">WavePrefixCountBits function</span></span>

<span data-ttu-id="a3ec1-105">Gibt die Summe aller angegebenen booleschen Variablen für alle aktiven Bereiche mit Indizes zurück, die kleiner als die aktuelle Seite sind.</span><span class="sxs-lookup"><span data-stu-id="a3ec1-105">Returns the sum of all the specified boolean variables set to true across all active lanes with indices smaller than the current lane.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3ec1-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="a3ec1-106">Syntax</span></span>


``` syntax
uint WavePrefixCountBits(
   bool bBit
);
```



## <a name="parameters"></a><span data-ttu-id="a3ec1-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="a3ec1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3ec1-108">*Bbit*</span><span class="sxs-lookup"><span data-stu-id="a3ec1-108">*bBit*</span></span> 
</dt> <dd>

<span data-ttu-id="a3ec1-109">Die angegebenen booleschen Variablen.</span><span class="sxs-lookup"><span data-stu-id="a3ec1-109">The specified boolean variables.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3ec1-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a3ec1-110">Return value</span></span>

<span data-ttu-id="a3ec1-111">Die Summe aller angegebenen booleschen Variablen ist für alle aktiven Bereiche mit Indizes, die kleiner als die aktuelle Strecke sind, auf true festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a3ec1-111">The sum of all the specified Boolean variables set to true across all active lanes with indices smaller than the current lane.</span></span>

## <a name="remarks"></a><span data-ttu-id="a3ec1-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a3ec1-112">Remarks</span></span>

<span data-ttu-id="a3ec1-113">Diese Funktion wird vom Shader-Modell 6,0 in allen shaderphasen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a3ec1-113">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="examples"></a><span data-ttu-id="a3ec1-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a3ec1-114">Examples</span></span>

<span data-ttu-id="a3ec1-115">Im folgenden Code wird beschrieben, wie ein komprimierter Schreibvorgang in einen geordneten Stream implementiert wird, wobei die Anzahl der pro Lane geschriebenen Elemente entweder 1 oder 0 ist.</span><span class="sxs-lookup"><span data-stu-id="a3ec1-115">The following code describes how to implement a compacted write to an ordered stream where the number of elements written per lane is either 1 or 0.</span></span>

``` syntax
bool bDoesThisLaneHaveAnAppendItem = <expr>;
// compute number of items to append for the whole wave
uint laneAppendOffset = WavePrefixCountBits( bDoesThisLaneHaveAnAppendItem );
uint appendCount = WaveActiveCountBits( bDoesThisLaneHaveAnAppendItem);
// update the output location for this whole wave
uint appendOffset;
if ( WaveIsFirstLane () )
{
    // this way, we only issue one atomic for the entire wave, which reduces contention
    // and keeps the output data for each lane in this wave together in the output buffer
    InterlockedAdd(bufferSize, appendCount, appendOffset);
}
appendOffset = WaveReadLaneFirst( appendOffset ); // broadcast value
appendOffset += laneAppendOffset; // and add in the offset for this lane
buffer[appendOffset] = myData; // write to the offset location for this lane
```

## <a name="see-also"></a><span data-ttu-id="a3ec1-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="a3ec1-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3ec1-117">Übersicht über Shader-Modell 6</span><span class="sxs-lookup"><span data-stu-id="a3ec1-117">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="a3ec1-118">Shader-Modell 6</span><span class="sxs-lookup"><span data-stu-id="a3ec1-118">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




