---
description: An die traceray-Funktion übergeben, um den Ursprung, die Richtung und die Blöcke des Strahls zu definieren.
ms.assetid: ''
title: Rayde-Struktur
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RAY_FLAG
api_type:
- NA
ms.openlocfilehash: a5fd6e041fc476c24ff926c9c8f99f05699f5e41
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345454"
---
# <a name="raydesc-structure"></a><span data-ttu-id="8ade6-103">Rayde-Struktur</span><span class="sxs-lookup"><span data-stu-id="8ade6-103">RayDesc structure</span></span>

<span data-ttu-id="8ade6-104">An die [**traceray**](traceray-function.md) -Funktion übergeben, um den Ursprung, die Richtung und die Blöcke des Strahls zu definieren.</span><span class="sxs-lookup"><span data-stu-id="8ade6-104">Passed to the [**TraceRay**](traceray-function.md) function to define the origin, direction, and extents of the ray.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ade6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8ade6-105">Syntax</span></span>


```
struct RayDesc
{
    float3 Origin;
    float  TMin;
    float3 Direction;
    float  TMax;
};

```



## <a name="fields"></a><span data-ttu-id="8ade6-106">Felder</span><span class="sxs-lookup"><span data-stu-id="8ade6-106">Fields</span></span>

<dl> <dt>

<span data-ttu-id="8ade6-107"><span id="Origin"></span><span id="origin"></span>**Entstehungs**</span><span class="sxs-lookup"><span data-stu-id="8ade6-107"><span id="Origin"></span><span id="origin"></span>**Origin**</span></span>
</dt> <dd>

<span data-ttu-id="8ade6-108">Der Ursprung des Strahls.</span><span class="sxs-lookup"><span data-stu-id="8ade6-108">The origin of the ray.</span></span>

</dd> <dt>

<span data-ttu-id="8ade6-109"><span id="TMin"></span><span id="tmin"></span>**Tmin**</span><span class="sxs-lookup"><span data-stu-id="8ade6-109"><span id="TMin"></span><span id="tmin"></span>**TMin**</span></span>
</dt> <dd>

<span data-ttu-id="8ade6-110">Der minimale Umfang des Strahls.</span><span class="sxs-lookup"><span data-stu-id="8ade6-110">The minimum extent of the ray.</span></span>


</dd> <dt>

<span data-ttu-id="8ade6-111"><span id="Direction"></span><span id="direction"></span>**Orientierung**</span><span class="sxs-lookup"><span data-stu-id="8ade6-111"><span id="Direction"></span><span id="direction"></span>**Direction**</span></span>
</dt> <dd>

<span data-ttu-id="8ade6-112">Die Richtung des Strahls.</span><span class="sxs-lookup"><span data-stu-id="8ade6-112">The direction of the ray.</span></span>


</dd> <dt>

<span data-ttu-id="8ade6-113"><span id="TMax"></span><span id="tmax"></span>**TMAX**</span><span class="sxs-lookup"><span data-stu-id="8ade6-113"><span id="TMax"></span><span id="tmax"></span>**TMax**</span></span>
</dt> <dd>

<span data-ttu-id="8ade6-114">Der maximale Umfang des Strahls.</span><span class="sxs-lookup"><span data-stu-id="8ade6-114">The maximum extent of the ray.</span></span>


</dd>

## <a name="requirements"></a><span data-ttu-id="8ade6-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8ade6-115">Requirements</span></span>



## <a name="see-also"></a><span data-ttu-id="8ade6-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="8ade6-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ade6-117">Direct3D 12-Raytracing, HLSL-Referenz</span><span class="sxs-lookup"><span data-stu-id="8ade6-117">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




