---
title: WaveReadLaneAt-Funktion
description: Gibt den Wert des Ausdrucks für den angegebenen Lane-Index innerhalb der angegebenen Welle zurück.
ms.assetid: CA9467D9-8885-4A5D-87F3-5BA40AE78993
keywords:
- WaveReadLaneAt-Funktion HLSL
topic_type:
- apiref
api_name:
- WaveReadLaneAt
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 573730053a93a110381637ef8e62dc08a4aa1535
ms.sourcegitcommit: 1897c2a39b4ac4ca4b1e4aec394cef2ce2619c03
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/06/2021
ms.locfileid: "113316482"
---
# <a name="wavereadlaneat-function"></a><span data-ttu-id="2e7d4-104">WaveReadLaneAt-Funktion</span><span class="sxs-lookup"><span data-stu-id="2e7d4-104">WaveReadLaneAt function</span></span>

<span data-ttu-id="2e7d4-105">Gibt den Wert des Ausdrucks für den angegebenen Lane-Index innerhalb der angegebenen Welle zurück.</span><span class="sxs-lookup"><span data-stu-id="2e7d4-105">Returns the value of the expression for the given lane index within the specified wave.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e7d4-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="2e7d4-106">Syntax</span></span>

``` syntax
<type> WaveReadLaneAt(
   <type> expr,
   uint laneIndex
);
```

## <a name="parameters"></a><span data-ttu-id="2e7d4-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="2e7d4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e7d4-108">*expr*</span><span class="sxs-lookup"><span data-stu-id="2e7d4-108">*expr*</span></span> 
</dt> <dd>

<span data-ttu-id="2e7d4-109">Der auszuwertende Ausdruck.</span><span class="sxs-lookup"><span data-stu-id="2e7d4-109">The expression to evaluate.</span></span>

</dd> <dt>

<span data-ttu-id="2e7d4-110">*laneIndex*</span><span class="sxs-lookup"><span data-stu-id="2e7d4-110">*laneIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="2e7d4-111">Der Index der Spur, für die *das Expr-Ergebnis* zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="2e7d4-111">The index of the lane for which the *expr* result will be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e7d4-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2e7d4-112">Return value</span></span>

<span data-ttu-id="2e7d4-113">Der resultierende Wert ist das Ergebnis von *expr*.</span><span class="sxs-lookup"><span data-stu-id="2e7d4-113">The resulting value is the result of *expr*.</span></span> <span data-ttu-id="2e7d4-114">Sie ist einheitlich, wenn *laneIndex* gleich ist.</span><span class="sxs-lookup"><span data-stu-id="2e7d4-114">It will be uniform if *laneIndex* is uniform.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e7d4-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2e7d4-115">Remarks</span></span>

<span data-ttu-id="2e7d4-116">Diese Funktion ist effektiv eine Übertragung des Werts in *der laneIndex*-th lane.</span><span class="sxs-lookup"><span data-stu-id="2e7d4-116">This function is effectively a broadcast of the value in the *laneIndex*'th lane.</span></span>

<span data-ttu-id="2e7d4-117">Diese Funktion wird von Shadermodell 6.0 in allen Shaderstufen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2e7d4-117">This function is supported from shader model 6.0 in all shader stages.</span></span>

## <a name="see-also"></a><span data-ttu-id="2e7d4-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2e7d4-118">See also</span></span>

* [<span data-ttu-id="2e7d4-119">Übersicht über Shadermodell 6</span><span class="sxs-lookup"><span data-stu-id="2e7d4-119">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
* [<span data-ttu-id="2e7d4-120">Shadermodell 6</span><span class="sxs-lookup"><span data-stu-id="2e7d4-120">Shader Model 6</span></span>](shader-model-6-0.md)
