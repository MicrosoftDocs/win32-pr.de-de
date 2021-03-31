---
title: GetRenderTargetSampleCount
description: Ruft die Anzahl der Stichproben für ein Renderziel ab.
ms.assetid: e813134e-c58c-4845-b519-c1074993801e
keywords:
- GetRenderTargetSampleCount HLSL
topic_type:
- apiref
api_name:
- GetRenderTargetSampleCount
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 96c159a2ed63684b4bad2cbc6fa789c2dbd76edf
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104471997"
---
# <a name="getrendertargetsamplecount"></a><span data-ttu-id="7b118-104">GetRenderTargetSampleCount</span><span class="sxs-lookup"><span data-stu-id="7b118-104">GetRenderTargetSampleCount</span></span>

<span data-ttu-id="7b118-105">Ruft die Anzahl der Stichproben für ein Renderziel ab.</span><span class="sxs-lookup"><span data-stu-id="7b118-105">Gets the number of samples for a render target.</span></span>



| <span data-ttu-id="7b118-106">*Uint* GetRenderTargetSampleCount()</span><span class="sxs-lookup"><span data-stu-id="7b118-106">*UINT* GetRenderTargetSampleCount()</span></span> |
|-------------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="7b118-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="7b118-107">Parameters</span></span>



| <span data-ttu-id="7b118-108">Element</span><span class="sxs-lookup"><span data-stu-id="7b118-108">Item</span></span>                                                                                 | <span data-ttu-id="7b118-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7b118-109">Description</span></span> |
|--------------------------------------------------------------------------------------|-------------|
| <span data-ttu-id="7b118-110"><span id="None"></span><span id="none"></span><span id="NONE"></span>Gar</span><span class="sxs-lookup"><span data-stu-id="7b118-110"><span id="None"></span><span id="none"></span><span id="NONE"></span>None</span></span><br/> |             |



 

## <a name="return-value"></a><span data-ttu-id="7b118-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7b118-111">Return Value</span></span>

<span data-ttu-id="7b118-112">Die Anzahl der Stichproben.</span><span class="sxs-lookup"><span data-stu-id="7b118-112">The number of samples.</span></span>

## <a name="remarks"></a><span data-ttu-id="7b118-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7b118-113">Remarks</span></span>

<span data-ttu-id="7b118-114">Verwenden Sie diese Funktion und [**GetRenderTargetSamplePosition**](dx-graphics-hlsl-getrendertargetsampleposition.md) , um die Anzahl und Position der Stichproben Speicherorte für ein Renderziel zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="7b118-114">Use this function and [**GetRenderTargetSamplePosition**](dx-graphics-hlsl-getrendertargetsampleposition.md) to find out the number and position of the sampling locations for a render target.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="7b118-115">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="7b118-115">Minimum Shader Model</span></span>

<span data-ttu-id="7b118-116">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7b118-116">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="7b118-117">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="7b118-117">Shader Model</span></span>                                                        | <span data-ttu-id="7b118-118">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="7b118-118">Supported</span></span> |
|---------------------------------------------------------------------|-----------|
| <span data-ttu-id="7b118-119">[Shader Model 4](dx-graphics-hlsl-sm4.md) und höhere shadermodelle</span><span class="sxs-lookup"><span data-stu-id="7b118-119">[Shader Model 4](dx-graphics-hlsl-sm4.md) and higher shader models</span></span> | <span data-ttu-id="7b118-120">ja</span><span class="sxs-lookup"><span data-stu-id="7b118-120">yes</span></span>       |
| [<span data-ttu-id="7b118-121">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7b118-121">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md)           | <span data-ttu-id="7b118-122">nein</span><span class="sxs-lookup"><span data-stu-id="7b118-122">no</span></span>        |
| [<span data-ttu-id="7b118-123">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7b118-123">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md)           | <span data-ttu-id="7b118-124">nein</span><span class="sxs-lookup"><span data-stu-id="7b118-124">no</span></span>        |
| [<span data-ttu-id="7b118-125">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7b118-125">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)           | <span data-ttu-id="7b118-126">Nein</span><span class="sxs-lookup"><span data-stu-id="7b118-126">no</span></span>        |



 

## <a name="see-also"></a><span data-ttu-id="7b118-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7b118-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b118-128">**Intrinsische Funktionen (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="7b118-128">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 





