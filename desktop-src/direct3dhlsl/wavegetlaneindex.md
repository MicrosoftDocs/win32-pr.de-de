---
title: Wavegetlaneingedex-Funktion
description: Gibt den Index der aktuellen Lane innerhalb der aktuellen Wave zurück.
ms.assetid: C05BD814-23DF-432F-8669-C03842B77AC7
keywords:
- Wavegetlaneingedex-Funktion HLSL
topic_type:
- apiref
api_name:
- WaveGetLaneIndex
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8adea1091739981523ab19b69158ead9aafa600c
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104993615"
---
# <a name="wavegetlaneindex-function"></a><span data-ttu-id="8c845-104">Wavegetlaneingedex-Funktion</span><span class="sxs-lookup"><span data-stu-id="8c845-104">WaveGetLaneIndex function</span></span>

<span data-ttu-id="8c845-105">Gibt den Index der aktuellen Lane innerhalb der aktuellen Wave zurück.</span><span class="sxs-lookup"><span data-stu-id="8c845-105">Returns the index of the current lane within the current wave.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c845-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="8c845-106">Syntax</span></span>

``` syntax
uint WaveGetLaneIndex(void);
```

## <a name="parameters"></a><span data-ttu-id="8c845-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="8c845-107">Parameters</span></span>

<span data-ttu-id="8c845-108">Diese Funktion besitzt keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="8c845-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8c845-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8c845-109">Return value</span></span>

<span data-ttu-id="8c845-110">Der aktuelle Bereichs Index.</span><span class="sxs-lookup"><span data-stu-id="8c845-110">The current lane index.</span></span> <span data-ttu-id="8c845-111">Das Ergebnis liegt zwischen 0 und dem von [**wavegetlanecount**](wavegetlanecount.md)zurückgegebenen Ergebnis.</span><span class="sxs-lookup"><span data-stu-id="8c845-111">The result will be between 0 and the result returned from [**WaveGetLaneCount**](wavegetlanecount.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="8c845-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8c845-112">Remarks</span></span>

<span data-ttu-id="8c845-113">Diese Funktion wird vom Shader-Modell 6,0 in allen shaderphasen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8c845-113">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="see-also"></a><span data-ttu-id="8c845-114">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="8c845-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c845-115">Übersicht über Shader-Modell 6</span><span class="sxs-lookup"><span data-stu-id="8c845-115">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="8c845-116">Shader-Modell 6</span><span class="sxs-lookup"><span data-stu-id="8c845-116">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




