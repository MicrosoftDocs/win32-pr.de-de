---
title: Wavereadlanefirst-Funktion
description: Gibt den Wert des Ausdrucks für die aktive Spur der aktuellen Welle mit dem kleinsten Index zurück.
ms.assetid: 89CA4FD5-4573-42ED-88D3-01C79C69FF6F
keywords:
- Wavereadlanefirst-Funktion HLSL
topic_type:
- apiref
api_name:
- WaveReadLaneFirst
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 04d10e5439b8cd653f7c0a37d3a951167561f964
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104976888"
---
# <a name="wavereadlanefirst-function"></a><span data-ttu-id="4d822-104">Wavereadlanefirst-Funktion</span><span class="sxs-lookup"><span data-stu-id="4d822-104">WaveReadLaneFirst function</span></span>

<span data-ttu-id="4d822-105">Gibt den Wert des Ausdrucks für die aktive Spur der aktuellen Welle mit dem kleinsten Index zurück.</span><span class="sxs-lookup"><span data-stu-id="4d822-105">Returns the value of the expression for the active lane of the current wave with the smallest index.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d822-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="4d822-106">Syntax</span></span>

``` syntax
<type> WaveReadLaneFirst(
   <type> expr
);
```

## <a name="parameters"></a><span data-ttu-id="4d822-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="4d822-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d822-108">*expr*</span><span class="sxs-lookup"><span data-stu-id="4d822-108">*expr*</span></span> 
</dt> <dd>

<span data-ttu-id="4d822-109">Der auszuwertende Ausdruck.</span><span class="sxs-lookup"><span data-stu-id="4d822-109">The expression to evaluate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d822-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4d822-110">Return value</span></span>

<span data-ttu-id="4d822-111">Der resultierende Wert ist in der gesamten Wave einheitlich.</span><span class="sxs-lookup"><span data-stu-id="4d822-111">The resulting value is uniform across the wave.</span></span>

## <a name="remarks"></a><span data-ttu-id="4d822-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4d822-112">Remarks</span></span>

<span data-ttu-id="4d822-113">Diese Funktion wird vom Shader-Modell 6,0 in allen shaderphasen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4d822-113">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="see-also"></a><span data-ttu-id="4d822-114">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="4d822-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d822-115">Übersicht über Shader-Modell 6</span><span class="sxs-lookup"><span data-stu-id="4d822-115">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="4d822-116">Shader-Modell 6</span><span class="sxs-lookup"><span data-stu-id="4d822-116">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




