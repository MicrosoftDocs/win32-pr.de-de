---
description: Die Werte für Breite, Höhe und Tiefe aus der D3D12_DISPATCH_RAYS_DESC Struktur, die in den ursprünglichen dispatchrays-aufrufen angegeben sind.
ms.assetid: ''
title: DispatchRaysDimensions
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DispatchRaysDimensions
api_type:
- NA
ms.openlocfilehash: e35c967ad831c82912d2962da72d9ad17eab1c15
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106339712"
---
# <a name="dispatchraysdimensions"></a><span data-ttu-id="14148-103">DispatchRaysDimensions</span><span class="sxs-lookup"><span data-stu-id="14148-103">DispatchRaysDimensions</span></span>

<span data-ttu-id="14148-104">Die Werte für Breite, Höhe und Tiefe der **D3D12 \_ Dispatch \_ Rays \_** -Struktur, die in den ursprünglichen [**dispatchrays**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-dispatchrays) -aufrufen angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="14148-104">The width, height and depth values from the **D3D12\_DISPATCH\_RAYS\_DESC** structure specified in the originating [**DispatchRays**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-dispatchrays) call.</span></span>

## <a name="syntax"></a><span data-ttu-id="14148-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="14148-105">Syntax</span></span>

```
uint3 DispatchRaysDimensions();
```

## <a name="remarks"></a><span data-ttu-id="14148-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="14148-106">Remarks</span></span>

<span data-ttu-id="14148-107">Diese Funktion kann von den folgenden Raytracing-shadertypen aufgerufen werden:</span><span class="sxs-lookup"><span data-stu-id="14148-107">This function can be called from the following raytracing shader types:</span></span>

* [<span data-ttu-id="14148-108">**Any Hit-Shader**</span><span class="sxs-lookup"><span data-stu-id="14148-108">**Any Hit Shader**</span></span>](any-hit-shader.md)
* [<span data-ttu-id="14148-109">**Callable-Shader**</span><span class="sxs-lookup"><span data-stu-id="14148-109">**Callable Shader**</span></span>](callable-shader.md)
* [<span data-ttu-id="14148-110">**Closest Hit-Shader**</span><span class="sxs-lookup"><span data-stu-id="14148-110">**Closest Hit Shader**</span></span>](closest-hit-shader.md)
* [<span data-ttu-id="14148-111">**Intersection-Shader**</span><span class="sxs-lookup"><span data-stu-id="14148-111">**Intersection Shader**</span></span>](intersection-shader.md)
* [<span data-ttu-id="14148-112">**Miss-Shader**</span><span class="sxs-lookup"><span data-stu-id="14148-112">**Miss Shader**</span></span>](miss-shader.md)
* [<span data-ttu-id="14148-113">**Ray Generation-Shader**</span><span class="sxs-lookup"><span data-stu-id="14148-113">**Ray Generation Shader**</span></span>](ray-generation-shader.md)

## <a name="see-also"></a><span data-ttu-id="14148-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="14148-114">See also</span></span>

* [<span data-ttu-id="14148-115">Direct3D 12-Raytracing, HLSL-Referenz</span><span class="sxs-lookup"><span data-stu-id="14148-115">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
