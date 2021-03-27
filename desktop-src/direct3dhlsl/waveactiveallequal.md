---
title: Waveactiveallequal-Funktion
description: Gibt true zurück, wenn der Ausdruck für jede aktive Strecke in der aktuellen Wave identisch ist (und somit einheitlich ist).
ms.assetid: E0A051A8-0ADD-4EC7-8D9A-8820CED9DA9D
keywords:
- Waveactiveallequal-Funktion HLSL
topic_type:
- apiref
api_name:
- WaveActiveAllEqual
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 34745e428fcd4453ce7274fc2a5accc6185f5b10
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "103734800"
---
# <a name="waveactiveallequal-function"></a><span data-ttu-id="4da0b-104">Waveactiveallequal-Funktion</span><span class="sxs-lookup"><span data-stu-id="4da0b-104">WaveActiveAllEqual function</span></span>

<span data-ttu-id="4da0b-105">Gibt true zurück, wenn der Ausdruck für jede aktive Strecke in der aktuellen Wave identisch ist (und somit einheitlich ist).</span><span class="sxs-lookup"><span data-stu-id="4da0b-105">Returns true if the expression is the same for every active lane in the current wave (and thus uniform across it).</span></span>

## <a name="syntax"></a><span data-ttu-id="4da0b-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="4da0b-106">Syntax</span></span>


``` syntax
bool WaveActiveAllEqual(
   <type> expr
);
```



## <a name="parameters"></a><span data-ttu-id="4da0b-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="4da0b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4da0b-108">*expr*</span><span class="sxs-lookup"><span data-stu-id="4da0b-108">*expr*</span></span> 
</dt> <dd>

<span data-ttu-id="4da0b-109">Der auszuwertende Ausdruck.</span><span class="sxs-lookup"><span data-stu-id="4da0b-109">The expression to evaluate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4da0b-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4da0b-110">Return value</span></span>

<span data-ttu-id="4da0b-111">True, wenn der Ausdruck für jede aktive Strecke in der aktuellen Wave gleich ist.</span><span class="sxs-lookup"><span data-stu-id="4da0b-111">True if the expression is the same for every active lane in the current wave.</span></span>

## <a name="remarks"></a><span data-ttu-id="4da0b-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4da0b-112">Remarks</span></span>

<span data-ttu-id="4da0b-113">Diese Funktion wird vom Shader-Modell 6,0 in allen shaderphasen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4da0b-113">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="see-also"></a><span data-ttu-id="4da0b-114">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="4da0b-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4da0b-115">Übersicht über Shader-Modell 6</span><span class="sxs-lookup"><span data-stu-id="4da0b-115">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="4da0b-116">Shader-Modell 6</span><span class="sxs-lookup"><span data-stu-id="4da0b-116">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




