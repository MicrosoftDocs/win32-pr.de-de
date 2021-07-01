---
title: GetRenderTargetSamplePosition
description: Ruft die Samplingposition (x,y) für einen angegebenen Beispielindex ab.
ms.assetid: 07f14d1c-4fe5-4838-acce-d664cdc641e6
keywords:
- GetRenderTargetSamplePosition HLSL
topic_type:
- apiref
api_name:
- GetRenderTargetSamplePosition
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c31bc829f8990517ddbea8be7c25eead413ab666
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120575"
---
# <a name="getrendertargetsampleposition"></a><span data-ttu-id="bfd75-104">GetRenderTargetSamplePosition</span><span class="sxs-lookup"><span data-stu-id="bfd75-104">GetRenderTargetSamplePosition</span></span>

<span data-ttu-id="bfd75-105">Ruft die Samplingposition (x,y) für einen angegebenen Beispielindex ab.</span><span class="sxs-lookup"><span data-stu-id="bfd75-105">Gets the sampling position (x,y) for a given sample index.</span></span>

<span data-ttu-id="bfd75-106">float<2> GetRenderTargetSamplePosition( in int<1> Index</span><span class="sxs-lookup"><span data-stu-id="bfd75-106">float<2> GetRenderTargetSamplePosition( in int<1> Index</span></span><br/><span data-ttu-id="bfd75-107">);</span><span class="sxs-lookup"><span data-stu-id="bfd75-107">);</span></span>



 

## <a name="parameters"></a><span data-ttu-id="bfd75-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="bfd75-108">Parameters</span></span>



| <span data-ttu-id="bfd75-109">Element</span><span class="sxs-lookup"><span data-stu-id="bfd75-109">Item</span></span>                                                                                       | <span data-ttu-id="bfd75-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bfd75-110">Description</span></span>                                  |
|--------------------------------------------------------------------------------------------|----------------------------------------------|
| <span data-ttu-id="bfd75-111"><span id="Index"></span><span id="index"></span><span id="INDEX"></span>*Index*</span><span class="sxs-lookup"><span data-stu-id="bfd75-111"><span id="Index"></span><span id="index"></span><span id="INDEX"></span>*Index*</span></span><br/> | <span data-ttu-id="bfd75-112">\[in \] einem nullbasierten Beispielindex.</span><span class="sxs-lookup"><span data-stu-id="bfd75-112">\[in\] A zero-based sample index.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="bfd75-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bfd75-113">Return Value</span></span>

<span data-ttu-id="bfd75-114">Die Position (x,y) des angegebenen Beispiels.</span><span class="sxs-lookup"><span data-stu-id="bfd75-114">The (x,y) position of the given sample.</span></span>

## <a name="remarks"></a><span data-ttu-id="bfd75-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bfd75-115">Remarks</span></span>

<span data-ttu-id="bfd75-116">Verwenden Sie diese Funktion und [**GetRenderTargetSampleCount,**](dx-graphics-hlsl-getrendertargetsamplecount.md) um die Anzahl und Position der Samplingspeicherorte für ein Renderziel zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="bfd75-116">Use this function and [**GetRenderTargetSampleCount**](dx-graphics-hlsl-getrendertargetsamplecount.md) to find out the number and position of the sampling locations for a render target.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="bfd75-117">Shader-Mindestmodell</span><span class="sxs-lookup"><span data-stu-id="bfd75-117">Minimum Shader Model</span></span>

<span data-ttu-id="bfd75-118">Diese Funktion wird in den folgenden Shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bfd75-118">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="bfd75-119">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="bfd75-119">Shader Model</span></span>                                                        | <span data-ttu-id="bfd75-120">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="bfd75-120">Supported</span></span> |
|---------------------------------------------------------------------|-----------|
| <span data-ttu-id="bfd75-121">[Shadermodell 4](dx-graphics-hlsl-sm4.md) und höhere Shadermodelle</span><span class="sxs-lookup"><span data-stu-id="bfd75-121">[Shader Model 4](dx-graphics-hlsl-sm4.md) and higher shader models</span></span> | <span data-ttu-id="bfd75-122">Ja</span><span class="sxs-lookup"><span data-stu-id="bfd75-122">yes</span></span>       |
| [<span data-ttu-id="bfd75-123">Shadermodell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bfd75-123">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md)           | <span data-ttu-id="bfd75-124">Nein</span><span class="sxs-lookup"><span data-stu-id="bfd75-124">no</span></span>        |
| [<span data-ttu-id="bfd75-125">Shadermodell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bfd75-125">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md)           | <span data-ttu-id="bfd75-126">Nein</span><span class="sxs-lookup"><span data-stu-id="bfd75-126">no</span></span>        |
| [<span data-ttu-id="bfd75-127">Shadermodell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bfd75-127">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)           | <span data-ttu-id="bfd75-128">Nein</span><span class="sxs-lookup"><span data-stu-id="bfd75-128">no</span></span>        |



 

## <a name="see-also"></a><span data-ttu-id="bfd75-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bfd75-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bfd75-130">**Systeminterne Funktionen (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="bfd75-130">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 





