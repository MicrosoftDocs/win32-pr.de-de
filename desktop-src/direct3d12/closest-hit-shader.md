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
# <a name="closest-hit-shader"></a>Closest Hit-Shader

Ein Shader, der aufgerufen wird, wenn er aktiviert ist, und der nächstgelegene Treffer wurde ermittelt oder die Überprüfung der Ray-Schnittmenge wurde beendet. In diesem Shader kommt es in der Regel zu Oberflächen Schattierung und zusätzlicher Ray-Generierung.  Die nächsten Treffer-Shader müssen einen Nutz Last Parameter, gefolgt von einem Attribute-Parameter, deklarieren.  Jede muss ein benutzerdefinierter Strukturtyp sein, der mit den Typen übereinstimmt, die für [**traceray**](traceray-function.md) bzw. [**reporthit**](reporthit-function.md) verwendet werden, oder die [**Struktur der Schnittstellen Attribute**](intersection-attributes.md) bei Verwendung von Dreiecks Schnittstellen mit fester Funktionsweise.

## <a name="shader-type-attribute"></a>Shader Type-Attribut


```
[shader("closesthit")]
```



## <a name="example"></a>Beispiel

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

 

 




