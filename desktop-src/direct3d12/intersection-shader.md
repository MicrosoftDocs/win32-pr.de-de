---
description: Ein Shader, der verwendet wird, um benutzerdefinierte Schnittmengenprimitiven für Lichtstrahl zu implementieren, die ein zugeordnetes Begrenzungsvolumen (Begrenzungsfeld) überschneiden.
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
ms.openlocfilehash: d7f9f81fdedae0fc6f6aa0448e6771c331af9c0d8924ab0f091d281565e4cfa3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119850880"
---
# <a name="intersection-shader"></a>Intersection-Shader

Ein Shader, der verwendet wird, um benutzerdefinierte Schnittmengenprimitiven für Lichtstrahl zu implementieren, die ein zugeordnetes Begrenzungsvolumen (Begrenzungsfeld) überschneiden. 

Der Schnittpunkt-Shader hat keinen Zugriff auf die Raynutzlast, definiert aber die Schnittmengenattribute für jeden Treffer durch einen Aufruf von [**ReportHit.**](reporthit-function.md)  Die Behandlung von **ReportHit** kann den Schnittpunkt-Shader früh beenden, wenn das Rayflag **RAY FLAG ACCEPT FIRST \_ \_ \_ \_ HIT_\AND \_ \END \_ SEARCH** festgelegt ist oder [**AcceptHitAndEndSearch**](accepthitandendsearch-function.md) von einem beliebigen Treffer-Shader aufgerufen wird.  Andernfalls wird TRUE zurückgegeben, wenn der Treffer akzeptiert wurde, oder FALSE, wenn der Treffer abgelehnt wurde.  Dies bedeutet, dass ein beliebiger Treffer-Shader, sofern vorhanden, ausgeführt werden muss, bevor das Steuerelement bedingt zum Schnittpunkt-Shader zurückkehrt.

## <a name="shader-type-attribute"></a>Shadertypattribut


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

 

 




