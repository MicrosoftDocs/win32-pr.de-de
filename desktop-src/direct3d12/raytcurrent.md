---
description: Ein float-Wert, der den aktuellen parametrischen Endpunkt für den Strahl darstellt.
ms.assetid: ''
title: Raycurrent
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RayTCurrent
api_type:
- NA
ms.openlocfilehash: 4f090bab88c6be671ca0614255fd7bdebb0d1549
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106342773"
---
# <a name="raytcurrent"></a><span data-ttu-id="66fdb-103">Raycurrent</span><span class="sxs-lookup"><span data-stu-id="66fdb-103">RayTCurrent</span></span>

<span data-ttu-id="66fdb-104">Ein float-Wert, der den aktuellen parametrischen Endpunkt für den Strahl darstellt.</span><span class="sxs-lookup"><span data-stu-id="66fdb-104">A float representing the current parametric ending point for the ray.</span></span>  

## <a name="syntax"></a><span data-ttu-id="66fdb-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="66fdb-105">Syntax</span></span>

```
float RayTCurrent();

```


## <a name="remarks"></a><span data-ttu-id="66fdb-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="66fdb-106">Remarks</span></span>

<span data-ttu-id="66fdb-107">**Raytcurrent** definiert den aktuellen Endpunkt des Strahls gemäß der folgenden Formel: Origin + (Direction \* raytcurrent).</span><span class="sxs-lookup"><span data-stu-id="66fdb-107">**RayTCurrent** defines the current ending point of the ray according to the following formula: Origin + (Direction \* RayTCurrent).</span></span>  <span data-ttu-id="66fdb-108">Der *Ursprung* und die *Richtung* können sich entweder in der Welt oder im Objektbereich befinden, was zu einer Welt-oder einem Objekt Raum Endpunkt führt.</span><span class="sxs-lookup"><span data-stu-id="66fdb-108">*Origin* and *Direction* may be in either world or object space, which results in either a world or an object space ending point.</span></span>

<span data-ttu-id="66fdb-109">" **Raytcurrent** " wird im Aufrufe " [**traceray**](traceray-function.md) " mit dem Wert " [**raydebug:: TMAX**](raydesc.md) " initialisiert und anschließend während der Ablauf Verfolgungs Abfrage aktualisiert, wenn interabschnitte gemeldet werden (in jedem beliebigen Treffer) und akzeptiert werden.</span><span class="sxs-lookup"><span data-stu-id="66fdb-109">**RayTCurrent** is initialized in the call [**TraceRay**](traceray-function.md) call with the [**RayDesc::TMax**](raydesc.md) value and then is updated during the trace query as intersections are reported (in the any hit), and accepted.</span></span>

<span data-ttu-id="66fdb-110">Im [Schnittpunkt-Shader](intersection-shader.md)stellt Sie den Abstand zum nächstgelegenen Schnittpunkt dar, der bisher gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="66fdb-110">In the [intersection shader](intersection-shader.md), it represents the distance to the closest intersection found so far.</span></span>  <span data-ttu-id="66fdb-111">Der Wert wird nach () auf den Thit-Wert aktualisiert, sofern der Treffer akzeptiert wurde.</span><span class="sxs-lookup"><span data-stu-id="66fdb-111">It will be updated after () to the THit value provided if the hit was accepted.</span></span>

<span data-ttu-id="66fdb-112">Im [beliebigen Treffer-Shader](any-hit-shader.md)stellt Sie den Abstand zur aktuellen Schnittmenge dar, die gemeldet wird.</span><span class="sxs-lookup"><span data-stu-id="66fdb-112">In the [any hit shader](any-hit-shader.md), it represents the distance to the current intersection being reported.</span></span>

<span data-ttu-id="66fdb-113">Im [nächsten Treffer-Shader](closest-hit-shader.md)stellt Sie den Abstand zur nächstgelegenen Schnittmenge dar, die akzeptiert wird.</span><span class="sxs-lookup"><span data-stu-id="66fdb-113">In the [closest hit shader](closest-hit-shader.md), it represents the distance to the closest intersection accepted.</span></span>

<span data-ttu-id="66fdb-114">Im [fehl-Shader](miss-shader.md)ist es gleich *TMAX* , das an den **traceray** -Befehl übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="66fdb-114">In the [miss shader](miss-shader.md), it is equal to *TMax* passed to the **TraceRay** call.</span></span>


<span data-ttu-id="66fdb-115">Diese Funktion kann von den folgenden Raytracing-shadertypen aufgerufen werden:</span><span class="sxs-lookup"><span data-stu-id="66fdb-115">This function can be called from the following raytracing shader types:</span></span>

* [<span data-ttu-id="66fdb-116">**Any Hit-Shader**</span><span class="sxs-lookup"><span data-stu-id="66fdb-116">**Any Hit Shader**</span></span>](any-hit-shader.md)
* [<span data-ttu-id="66fdb-117">**Closest Hit-Shader**</span><span class="sxs-lookup"><span data-stu-id="66fdb-117">**Closest Hit Shader**</span></span>](closest-hit-shader.md)
* [<span data-ttu-id="66fdb-118">**Intersection-Shader**</span><span class="sxs-lookup"><span data-stu-id="66fdb-118">**Intersection Shader**</span></span>](intersection-shader.md)
* [<span data-ttu-id="66fdb-119">**Miss-Shader**</span><span class="sxs-lookup"><span data-stu-id="66fdb-119">**Miss Shader**</span></span>](miss-shader.md)





## <a name="see-also"></a><span data-ttu-id="66fdb-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="66fdb-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66fdb-121">Direct3D 12-Raytracing, HLSL-Referenz</span><span class="sxs-lookup"><span data-stu-id="66fdb-121">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




