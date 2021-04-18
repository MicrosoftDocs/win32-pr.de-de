---
description: Ein Shader, der aufgerufen wird, wenn er aktiviert ist, und der nächstgelegene Treffer wurde ermittelt oder die Überprüfung der Ray-Schnittmenge wurde beendet.
ms.assetid: ''
title: Closest Hit-Shader
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
ms.openlocfilehash: 347ad66dce0a81b929d5dc3c82051bf84226e723
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343616"
---
# <a name="closest-hit-shader"></a><span data-ttu-id="3de96-103">Closest Hit-Shader</span><span class="sxs-lookup"><span data-stu-id="3de96-103">Closest Hit Shader</span></span>

<span data-ttu-id="3de96-104">Ein Shader, der aufgerufen wird, wenn er aktiviert ist, und der nächstgelegene Treffer wurde ermittelt oder die Überprüfung der Ray-Schnittmenge wurde beendet.</span><span class="sxs-lookup"><span data-stu-id="3de96-104">A shader that is invoked when it is enabled and the closest hit has been determined or ray intersection search ended.</span></span> <span data-ttu-id="3de96-105">In diesem Shader kommt es in der Regel zu Oberflächen Schattierung und zusätzlicher Ray-Generierung.</span><span class="sxs-lookup"><span data-stu-id="3de96-105">This shader is where surface shading and additional ray generation will typically occur.</span></span>  <span data-ttu-id="3de96-106">Die nächsten Treffer-Shader müssen einen Nutz Last Parameter, gefolgt von einem Attribute-Parameter, deklarieren.</span><span class="sxs-lookup"><span data-stu-id="3de96-106">Closest hit shaders must declare a payload parameter, followed by an attributes parameter.</span></span>  <span data-ttu-id="3de96-107">Jede muss ein benutzerdefinierter Strukturtyp sein, der mit den Typen übereinstimmt, die für [**traceray**](traceray-function.md) bzw. [**reporthit**](reporthit-function.md) verwendet werden, oder die [**Struktur der Schnittstellen Attribute**](intersection-attributes.md) bei Verwendung von Dreiecks Schnittstellen mit fester Funktionsweise.</span><span class="sxs-lookup"><span data-stu-id="3de96-107">Each must be a user-defined structure type matching types used for [**TraceRay**](traceray-function.md) and [**ReportHit**](reporthit-function.md) respectively, or the [**Intersection Attributes Structure**](intersection-attributes.md) when fixed-function triangle intersection is used.</span></span>

## <a name="shader-type-attribute"></a><span data-ttu-id="3de96-108">Shader Type-Attribut</span><span class="sxs-lookup"><span data-stu-id="3de96-108">Shader Type attribute</span></span>


```
[shader("closesthit")]
```



## <a name="example"></a><span data-ttu-id="3de96-109">Beispiel</span><span class="sxs-lookup"><span data-stu-id="3de96-109">Example</span></span>

```
[shader("closesthit")]
void closesthit_main(inout MyPayload payload, in MyAttributes attr)
{
    CallShader( ... );  // maybe
    // update payload for surface
    // trace reflection
    float3 worldRayOrigin = WorldRayOrigin() + WorldRayDirection() * RayTCurrent();
    float3 worldNormal = mul(attr.normal, (float3x3)ObjectToWorld3x4());
    RayDesc reflectedRay = { worldRayOrigin, SceneConstants.Epsilon,
                             ReflectRay(WorldRayDirection(), worldNormal),
                             SceneConstants.TMax };
    TraceRay(MyAccelerationStructure,
             SceneConstants.RayFlags,
             SceneConstants.InstanceInclusionMask,
             SceneConstants.RayContributionToHitGroupIndex,
             SceneConstants.MultiplierForGeometryContributionToHitGroupIndex,
             SceneConstants.MissShaderIndex,
             reflectedRay,
             payload);
    // Combine final contributions into ray payload
    // this ray query is now complete.
    // Alternately, could look at data in payload result based on that make other TraceRay
    // calls.  No constraints on the code structure.
}

```

 

 




