---
title: Wavereadlaneat-Funktion
description: Gibt den Wert des Ausdrucks für den angegebenen Lane-Index innerhalb der angegebenen Wave zurück.
ms.assetid: CA9467D9-8885-4A5D-87F3-5BA40AE78993
keywords:
- Wavereadlaneat-Funktion HLSL
topic_type:
- apiref
api_name:
- WaveReadLaneAt
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e40940f2df6685a3096da6886ad3bcb6d9ca99af
ms.sourcegitcommit: 4423a9d48f1c90d2ec2eca68e9cae30df1787f25
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2020
ms.locfileid: "104390103"
---
# <a name="wavereadlaneat-function"></a><span data-ttu-id="ba926-104">Wavereadlaneat-Funktion</span><span class="sxs-lookup"><span data-stu-id="ba926-104">WaveReadLaneAt function</span></span>

<span data-ttu-id="ba926-105">Gibt den Wert des Ausdrucks für den angegebenen Lane-Index innerhalb der angegebenen Wave zurück.</span><span class="sxs-lookup"><span data-stu-id="ba926-105">Returns the value of the expression for the given lane index within the specified wave.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba926-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="ba926-106">Syntax</span></span>

``` syntax
<type> WaveReadLaneAt(
   <type> expr,
   uint laneIndex
);
```

## <a name="parameters"></a><span data-ttu-id="ba926-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="ba926-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba926-108">*expr*</span><span class="sxs-lookup"><span data-stu-id="ba926-108">*expr*</span></span> 
</dt> <dd>

<span data-ttu-id="ba926-109">Der auszuwertende Ausdruck.</span><span class="sxs-lookup"><span data-stu-id="ba926-109">The expression to evaluate.</span></span>

</dd> <dt>

<span data-ttu-id="ba926-110">*laneingedex*</span><span class="sxs-lookup"><span data-stu-id="ba926-110">*laneIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="ba926-111">Der Index der Spur, für die das *expr* -Ergebnis zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ba926-111">The index of the lane for which the *expr* result will be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba926-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ba926-112">Return value</span></span>

<span data-ttu-id="ba926-113">Der resultierende Wert ist das Ergebnis von *expr*.</span><span class="sxs-lookup"><span data-stu-id="ba926-113">The resulting value is the result of *expr*.</span></span> <span data-ttu-id="ba926-114">Er ist einheitlich, wenn *laneingedex* einheitlich ist.</span><span class="sxs-lookup"><span data-stu-id="ba926-114">It will be uniform if *laneIndex* is uniform.</span></span>

## <a name="remarks"></a><span data-ttu-id="ba926-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ba926-115">Remarks</span></span>

<span data-ttu-id="ba926-116">Bei dieser Funktion handelt es sich tatsächlich um eine Übertragung des Werts in der laneindexth-Spur.</span><span class="sxs-lookup"><span data-stu-id="ba926-116">This function is effectively a broadcast of the value in the laneIndex’th lane.</span></span>

<span data-ttu-id="ba926-117">Diese Funktion wird vom Shader-Modell 6,0 in den folgenden shadertypen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="ba926-117">This function is supported from shader model 6.0, in the following types of shaders:</span></span>



| <span data-ttu-id="ba926-118">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="ba926-118">Vertex</span></span> | <span data-ttu-id="ba926-119">Hülle</span><span class="sxs-lookup"><span data-stu-id="ba926-119">Hull</span></span> | <span data-ttu-id="ba926-120">Domain</span><span class="sxs-lookup"><span data-stu-id="ba926-120">Domain</span></span> | <span data-ttu-id="ba926-121">Geometrie</span><span class="sxs-lookup"><span data-stu-id="ba926-121">Geometry</span></span> | <span data-ttu-id="ba926-122">Pixel</span><span class="sxs-lookup"><span data-stu-id="ba926-122">Pixel</span></span> | <span data-ttu-id="ba926-123">Compute</span><span class="sxs-lookup"><span data-stu-id="ba926-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="ba926-124">x</span><span class="sxs-lookup"><span data-stu-id="ba926-124">x</span></span>     | <span data-ttu-id="ba926-125">x</span><span class="sxs-lookup"><span data-stu-id="ba926-125">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="ba926-126">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ba926-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba926-127">Übersicht über Shader-Modell 6</span><span class="sxs-lookup"><span data-stu-id="ba926-127">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="ba926-128">Shader-Modell 6</span><span class="sxs-lookup"><span data-stu-id="ba926-128">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




