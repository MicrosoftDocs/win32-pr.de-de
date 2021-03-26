---
title: Waveisfirstlane-Funktion
description: Gibt nur für die aktive Spur in der aktuellen Wave mit dem kleinsten Index true zurück.
ms.assetid: 5D90F713-08C7-4BD4-867B-2E7CA3A85E87
keywords:
- Waveisfirstlane-Funktion HLSL
topic_type:
- apiref
api_name:
- WaveIsFirstLane
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 49e875463d8281ff7e7699694c02d087df1a372f
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104316778"
---
# <a name="waveisfirstlane-function"></a><span data-ttu-id="22aeb-104">Waveisfirstlane-Funktion</span><span class="sxs-lookup"><span data-stu-id="22aeb-104">WaveIsFirstLane function</span></span>

<span data-ttu-id="22aeb-105">Gibt nur für die aktive Spur in der aktuellen Wave mit dem kleinsten Index true zurück.</span><span class="sxs-lookup"><span data-stu-id="22aeb-105">Returns true only for the active lane in the current wave with the smallest index.</span></span>

## <a name="syntax"></a><span data-ttu-id="22aeb-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="22aeb-106">Syntax</span></span>


``` syntax
bool WaveIsFirstLane(void);
```



## <a name="parameters"></a><span data-ttu-id="22aeb-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="22aeb-107">Parameters</span></span>

<span data-ttu-id="22aeb-108">Diese Funktion besitzt keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="22aeb-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="22aeb-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="22aeb-109">Return value</span></span>

<span data-ttu-id="22aeb-110">True gilt nur für die aktive Spur in der aktuellen Wave mit dem kleinsten Index.</span><span class="sxs-lookup"><span data-stu-id="22aeb-110">True only for the active lane in the current wave with the smallest index.</span></span>

## <a name="remarks"></a><span data-ttu-id="22aeb-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="22aeb-111">Remarks</span></span>

<span data-ttu-id="22aeb-112">Diese Funktion kann verwendet werden, um Vorgänge zu identifizieren, die nur einmal pro Wave ausgeführt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="22aeb-112">This function can be used to identify operations that are to be executed only once per wave.</span></span>

<span data-ttu-id="22aeb-113">Diese Funktion wird vom Shader-Modell 6,0 in allen shaderphasen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="22aeb-113">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="examples"></a><span data-ttu-id="22aeb-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="22aeb-114">Examples</span></span>

``` syntax
 if ( WaveIsFirstLane() )
{
    . . . // once per-wave code
}
```

## <a name="see-also"></a><span data-ttu-id="22aeb-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="22aeb-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22aeb-116">Übersicht über Shader-Modell 6</span><span class="sxs-lookup"><span data-stu-id="22aeb-116">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="22aeb-117">Shader-Modell 6</span><span class="sxs-lookup"><span data-stu-id="22aeb-117">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




