---
description: Ein Shader, der verwendet wird, um benutzerdefinierte Schnittmengen primitive für Strahlen zu implementieren, die ein zugeordnetes Begrenzungs Volume (Begrenzungsfeld) überschneiden.
ms.assetid: ''
title: Intersection-Shader
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
ms.openlocfilehash: f20d9ceb90b716ca5e5c04fb796a8b20f535825d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346036"
---
# <a name="intersection-shader"></a>Intersection-Shader

Ein Shader, der verwendet wird, um benutzerdefinierte Schnittmengen primitive für Strahlen zu implementieren, die ein zugeordnetes Begrenzungs Volume (Begrenzungsfeld) überschneiden. 

Der Schnittstellen-Shader hat keinen Zugriff auf die Ray-Nutzlast, sondern definiert die Schnittmengen Attribute für jede Treffer durch einen Report of [**Report.**](reporthit-function.md)  Durch die Behandlung von **reporthit** kann der schnittsshader frühzeitig beendet werden, wenn das Ray **-Flag \_ \_ \_ erste \_ HIT_ \und \_ \end \_ Search** festgelegt ist, oder wenn [**Accept thitandendsearch**](accepthitandendsearch-function.md) von einem beliebigen Treffer-Shader aufgerufen wird.  Andernfalls wird true zurückgegeben, wenn der Treffer akzeptiert wurde, oder false, wenn der Treffer abgelehnt wurde.  Dies bedeutet, dass ein beliebiger Treffer-Shader, falls vorhanden, ausgeführt werden muss, bevor die Steuerung bedingt an den schnittsshader zurückgegeben wird.

## <a name="shader-type-attribute"></a>Shader Type-Attribut


```
[shader("intersection")]
```



## <a name="example"></a>Beispiel

```
struct CustomPrimitiveDef { ... };
struct MyAttributes { ... };
struct CustomIntersectionIterator {...};
void InitCustomIntersectionIterator(CustomIntersectionIterator it) {...}
bool IntersectCustomPrimitiveFrontToBack(
    CustomPrimitiveDef prim,
    inout CustomIntersectionIterator it,
    float3 origin, float3 dir,
    float rayTMin, inout float curT,
    out MyAttributes attr);

[shader("intersection")]
void intersection_main()
{
    float THit = RayTCurrent();
    MyAttributes attr;
    CustomIntersectionIterator it;
    InitCustomIntersectionIterator(it); 
    while(IntersectCustomPrimitiveFrontToBack(
            CustomPrimitiveDefinitions[LocalConstants.PrimitiveIndex],
            it, ObjectRayOrigin(), ObjectRayDirection(), 
            RayTMin(), THit, attr))
    {
        // Exit on the first hit.  Note that if the ray has
        // RAY_FLAG_ACCEPT_FIRST_HIT_AND_END_SEARCH or an
        // anyhit shader is used and calls AcceptHitAndEndSearch(),
        // that would also fully exit this intersection shader (making
        // the “break” below moot in that case).        
        if (ReportHit(THit, /*hitKind*/ 0, attr) && (RayFlags() &  RAY_FLAG_FORCE_OPAQUE))
            break;
    }
}
```

 

 




