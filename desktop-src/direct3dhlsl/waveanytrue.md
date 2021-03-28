---
title: Waveactiveanytrue-Funktion
description: Gibt "true" zurück, wenn der Ausdruck in einer der aktiven Bereiche in der aktuellen Wave "true" ist.
ms.assetid: 203E2E1D-0AA2-4E4A-80F7-D1FE7579A742
keywords:
- Waveactiveanytrue-Funktion HLSL
topic_type:
- apiref
api_name:
- WaveActiveAnyTrue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 16801c4329f5bc0bf325d8bb67e8c0bb94887678
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104993614"
---
# <a name="waveactiveanytrue-function"></a><span data-ttu-id="9e58e-104">Waveactiveanytrue-Funktion</span><span class="sxs-lookup"><span data-stu-id="9e58e-104">WaveActiveAnyTrue function</span></span>

<span data-ttu-id="9e58e-105">Gibt "true" zurück, wenn der Ausdruck in einer der aktiven Bereiche in der aktuellen Wave "true" ist.</span><span class="sxs-lookup"><span data-stu-id="9e58e-105">Returns true if the expression is true in any of the active lanes in the current wave.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e58e-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="9e58e-106">Syntax</span></span>

``` syntax
bool WaveActiveAnyTrue(
   bool expr
);
```

## <a name="parameters"></a><span data-ttu-id="9e58e-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="9e58e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e58e-108">*expr*</span><span class="sxs-lookup"><span data-stu-id="9e58e-108">*expr*</span></span> 
</dt> <dd>

<span data-ttu-id="9e58e-109">Der auszuwertende boolesche Ausdruck.</span><span class="sxs-lookup"><span data-stu-id="9e58e-109">The boolean expression to evaluate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e58e-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9e58e-110">Return value</span></span>

<span data-ttu-id="9e58e-111">True, wenn der Ausdruck in einer beliebigen Spur true ist.</span><span class="sxs-lookup"><span data-stu-id="9e58e-111">True if the expression is true in any lane.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e58e-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9e58e-112">Remarks</span></span>

<span data-ttu-id="9e58e-113">Diese Funktion wird vom Shader-Modell 6,0 in allen shaderphasen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9e58e-113">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="see-also"></a><span data-ttu-id="9e58e-114">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="9e58e-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e58e-115">Übersicht über Shader-Modell 6</span><span class="sxs-lookup"><span data-stu-id="9e58e-115">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="9e58e-116">Shader-Modell 6</span><span class="sxs-lookup"><span data-stu-id="9e58e-116">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




