---
description: Ein float-Wert, der den aktuellen parametrischen Anfangspunkt für den Strahl darstellt.
ms.assetid: ''
title: Raytmin
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RayTMin
api_type:
- NA
ms.openlocfilehash: 00db0eb46e8c011e5b31f773679e19ca6dd4a7a0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346450"
---
# <a name="raytmin"></a><span data-ttu-id="ed4bd-103">Raytmin</span><span class="sxs-lookup"><span data-stu-id="ed4bd-103">RayTMin</span></span>

<span data-ttu-id="ed4bd-104">Ein float-Wert, der den aktuellen parametrischen Anfangspunkt für den Strahl darstellt.</span><span class="sxs-lookup"><span data-stu-id="ed4bd-104">A float representing the current parametric starting point for the ray.</span></span> 

## <a name="syntax"></a><span data-ttu-id="ed4bd-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ed4bd-105">Syntax</span></span>

```
float RayTMin();

```

## <a name="remarks"></a><span data-ttu-id="ed4bd-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ed4bd-106">Remarks</span></span>

<span data-ttu-id="ed4bd-107">**Raytmin** definiert den Anfangspunkt des Strahls gemäß der folgenden Formel: Origin + (Direction \* raytmin).</span><span class="sxs-lookup"><span data-stu-id="ed4bd-107">**RayTMin** defines the starting point of the ray according to the following formula: Origin + (Direction \* RayTMin).</span></span>  <span data-ttu-id="ed4bd-108">Der *Ursprung* und die *Richtung* können sich entweder in der Welt oder im Objektbereich befinden, was zu einem Ausgangspunkt der Welt oder einem Objektbereich führt.</span><span class="sxs-lookup"><span data-stu-id="ed4bd-108">*Origin* and *Direction* may be in either world or object space, which results in either a world or an object space starting point.</span></span>

<span data-ttu-id="ed4bd-109">**Raytmin** wird im Aufrufe von [**traceray**](traceray-function.md)angegeben und ist für die Dauer des Aufrufes konstant.</span><span class="sxs-lookup"><span data-stu-id="ed4bd-109">**RayTMin** is specified in the call to [**TraceRay**](traceray-function.md), and is constant for the duration of that call.</span></span>




<span data-ttu-id="ed4bd-110">Diese Funktion kann von den folgenden Raytracing-shadertypen aufgerufen werden:</span><span class="sxs-lookup"><span data-stu-id="ed4bd-110">This function can be called from the following raytracing shader types:</span></span>

* [<span data-ttu-id="ed4bd-111">**Any Hit-Shader**</span><span class="sxs-lookup"><span data-stu-id="ed4bd-111">**Any Hit Shader**</span></span>](any-hit-shader.md)
* [<span data-ttu-id="ed4bd-112">**Closest Hit-Shader**</span><span class="sxs-lookup"><span data-stu-id="ed4bd-112">**Closest Hit Shader**</span></span>](closest-hit-shader.md)
* [<span data-ttu-id="ed4bd-113">**Intersection-Shader**</span><span class="sxs-lookup"><span data-stu-id="ed4bd-113">**Intersection Shader**</span></span>](intersection-shader.md)
* [<span data-ttu-id="ed4bd-114">**Miss-Shader**</span><span class="sxs-lookup"><span data-stu-id="ed4bd-114">**Miss Shader**</span></span>](miss-shader.md)





## <a name="see-also"></a><span data-ttu-id="ed4bd-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ed4bd-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed4bd-116">Direct3D 12-Raytracing, HLSL-Referenz</span><span class="sxs-lookup"><span data-stu-id="ed4bd-116">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




