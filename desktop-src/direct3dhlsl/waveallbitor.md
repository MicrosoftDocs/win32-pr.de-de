---
title: Waveactivebitor-Funktion
description: Gibt das bitweise OR aller Werte des Ausdrucks für alle aktiven Bereiche in der aktuellen Wave zurück und repliziert Sie zurück in alle aktiven Bereiche.
ms.assetid: FC8E5987-DAA7-41E6-A1AB-AA0E6A82CFC7
keywords:
- Waveactivebitor-Funktion HLSL
topic_type:
- apiref
api_name:
- WaveActiveBitOr
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6870ac8406a581e358b00ef728562dc59118a933
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104039841"
---
# <a name="waveactivebitor-function"></a><span data-ttu-id="799de-104">Waveactivebitor-Funktion</span><span class="sxs-lookup"><span data-stu-id="799de-104">WaveActiveBitOr function</span></span>

<span data-ttu-id="799de-105">Gibt das bitweise OR aller Werte des Ausdrucks für alle aktiven Bereiche in der aktuellen Wave zurück und repliziert Sie zurück in alle aktiven Bereiche.</span><span class="sxs-lookup"><span data-stu-id="799de-105">Returns the bitwise OR of all the values of the expression across all active lanes in the current wave and replicates it back to all active lanes.</span></span>

## <a name="syntax"></a><span data-ttu-id="799de-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="799de-106">Syntax</span></span>

``` syntax
<int_type> WaveActiveBitOr(
   <int_type> expr
);
```

## <a name="parameters"></a><span data-ttu-id="799de-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="799de-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="799de-108">*expr*</span><span class="sxs-lookup"><span data-stu-id="799de-108">*expr*</span></span> 
</dt> <dd>

<span data-ttu-id="799de-109">Der auszuwertende Ausdruck.</span><span class="sxs-lookup"><span data-stu-id="799de-109">The expression to evaluate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="799de-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="799de-110">Return value</span></span>

<span data-ttu-id="799de-111">Der bitweise OR-Wert.</span><span class="sxs-lookup"><span data-stu-id="799de-111">The bitwise OR value.</span></span>

## <a name="remarks"></a><span data-ttu-id="799de-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="799de-112">Remarks</span></span>

<span data-ttu-id="799de-113">Diese Funktion wird vom Shader-Modell 6,0 in allen shaderphasen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="799de-113">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="see-also"></a><span data-ttu-id="799de-114">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="799de-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="799de-115">Übersicht über Shader-Modell 6</span><span class="sxs-lookup"><span data-stu-id="799de-115">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="799de-116">Shader-Modell 6</span><span class="sxs-lookup"><span data-stu-id="799de-116">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




