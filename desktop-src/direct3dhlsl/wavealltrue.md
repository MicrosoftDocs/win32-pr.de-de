---
title: Waveactivealltrue-Funktion
description: Gibt "true" zurück, wenn der Ausdruck in allen aktiven Bereichen in der aktuellen Wave "true" ist.
ms.assetid: C4EC5A02-6070-4FF4-B855-F597FFFE66F0
keywords:
- Waveactivealltrue-Funktion HLSL
topic_type:
- apiref
api_name:
- WaveActiveAllTrue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a26e0ce757257d6fdd8296239dcf086bff5f1666
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104474638"
---
# <a name="waveactivealltrue-function"></a><span data-ttu-id="75a72-104">Waveactivealltrue-Funktion</span><span class="sxs-lookup"><span data-stu-id="75a72-104">WaveActiveAllTrue function</span></span>

<span data-ttu-id="75a72-105">Gibt "true" zurück, wenn der Ausdruck in allen aktiven Bereichen in der aktuellen Wave "true" ist.</span><span class="sxs-lookup"><span data-stu-id="75a72-105">Returns true if the expression is true in all active lanes in the current wave.</span></span>

## <a name="syntax"></a><span data-ttu-id="75a72-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="75a72-106">Syntax</span></span>

``` syntax
bool WaveActiveAllTrue(
   bool expr
);
```

## <a name="parameters"></a><span data-ttu-id="75a72-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="75a72-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75a72-108">*expr*</span><span class="sxs-lookup"><span data-stu-id="75a72-108">*expr*</span></span> 
</dt> <dd>

<span data-ttu-id="75a72-109">Der auszuwertende boolesche Ausdruck.</span><span class="sxs-lookup"><span data-stu-id="75a72-109">The boolean expression to evaluate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75a72-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="75a72-110">Return value</span></span>

<span data-ttu-id="75a72-111">True, wenn der Ausdruck in allen Bereichen den Wert true hat.</span><span class="sxs-lookup"><span data-stu-id="75a72-111">True if the expression is true in all lanes.</span></span>

## <a name="remarks"></a><span data-ttu-id="75a72-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="75a72-112">Remarks</span></span>

<span data-ttu-id="75a72-113">Diese Funktion wird vom Shader-Modell 6,0 in allen shaderphasen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="75a72-113">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="see-also"></a><span data-ttu-id="75a72-114">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="75a72-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75a72-115">Übersicht über Shader-Modell 6</span><span class="sxs-lookup"><span data-stu-id="75a72-115">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="75a72-116">Shader-Modell 6</span><span class="sxs-lookup"><span data-stu-id="75a72-116">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




