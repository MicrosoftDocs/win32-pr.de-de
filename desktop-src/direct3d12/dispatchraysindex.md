---
description: Ruft die aktuelle Position innerhalb der Breite, Höhe und Tiefe ab, die mit dem systeminternen [**dispatchraysdimensions**](dispatchraysdimensions.md) -System Wert abgerufen wird.
title: 'DispatchRaysIndex '
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DispatchRaysIndex
api_type:
- NA
ms.openlocfilehash: aa26400c26aba4ee9e647bcd0a79bad3f3d52f7c
ms.sourcegitcommit: 4e4f9e7c90d25af0774deec1d44bd49fa9b6daa9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2020
ms.locfileid: "106338099"
---
# <a name="dispatchraysindex"></a><span data-ttu-id="8e1a5-103">DispatchRaysIndex </span><span class="sxs-lookup"><span data-stu-id="8e1a5-103">DispatchRaysIndex</span></span>

<span data-ttu-id="8e1a5-104">Ruft die aktuelle Position innerhalb der Breite, Höhe und Tiefe ab, die mit dem systeminternen [**dispatchraysdimensions**](dispatchraysdimensions.md) -System Wert abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="8e1a5-104">Gets the current location within the width, height, and depth obtained with the [**DispatchRaysDimensions**](dispatchraysdimensions.md) system value intrinsic.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e1a5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8e1a5-105">Syntax</span></span>

```syntax
uint3 DispatchRaysIndex();
```

## <a name="remarks"></a><span data-ttu-id="8e1a5-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8e1a5-106">Remarks</span></span>

<span data-ttu-id="8e1a5-107">Diese Funktion kann von den folgenden Raytracing-shadertypen aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="8e1a5-107">This function can be called from the following raytracing shader types.</span></span>

* [<span data-ttu-id="8e1a5-108">**Any Hit-Shader**</span><span class="sxs-lookup"><span data-stu-id="8e1a5-108">**Any Hit Shader**</span></span>](any-hit-shader.md)
* [<span data-ttu-id="8e1a5-109">**Callable-Shader**</span><span class="sxs-lookup"><span data-stu-id="8e1a5-109">**Callable Shader**</span></span>](callable-shader.md)
* [<span data-ttu-id="8e1a5-110">**Closest Hit-Shader**</span><span class="sxs-lookup"><span data-stu-id="8e1a5-110">**Closest Hit Shader**</span></span>](closest-hit-shader.md)
* [<span data-ttu-id="8e1a5-111">**Intersection-Shader**</span><span class="sxs-lookup"><span data-stu-id="8e1a5-111">**Intersection Shader**</span></span>](intersection-shader.md)
* [<span data-ttu-id="8e1a5-112">**Miss-Shader**</span><span class="sxs-lookup"><span data-stu-id="8e1a5-112">**Miss Shader**</span></span>](miss-shader.md)
* [<span data-ttu-id="8e1a5-113">**Ray Generation-Shader**</span><span class="sxs-lookup"><span data-stu-id="8e1a5-113">**Ray Generation Shader**</span></span>](ray-generation-shader.md)

## <a name="see-also"></a><span data-ttu-id="8e1a5-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8e1a5-114">See also</span></span>

* [<span data-ttu-id="8e1a5-115">Direct3D 12-Raytracing, HLSL-Referenz</span><span class="sxs-lookup"><span data-stu-id="8e1a5-115">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
