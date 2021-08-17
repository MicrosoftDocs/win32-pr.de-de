---
description: Ein Shader, der TraceRay aufruft, um Lichtstrahl zu generieren.
ms.assetid: ''
title: Ray Generation-Shader
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
ms.openlocfilehash: fdc177040cac7324545172319c318d07cded6dba42cfeed4756a7afaa88439aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119123712"
---
# <a name="ray-generation-shader"></a>Ray Generation-Shader

Ein Shader, der [**TraceRay**](traceray-function.md) aufruft, um Lichtstrahl zu generieren. Die anfängliche benutzerdefinierte Raynutzlast für jeden Strahl wird der **TraceRay-Aufrufsite** bereitgestellt.  [**CallShader**](callshader-function.md) kann auch in Raygenerierungsshadern verwendet werden, um [aufrufbare Shader](callable-shader.md)aufzurufen.

**DispatchRays** ruft ein Raster von Raygenerierungs-Shaderaufrufen auf.  Jeder Aufruf (Thread) eines Raygenerierungs-Shaders kennt seine Position im Gesamtraster, kann beliebige Lichtstrahle über [**TraceRay**](traceray-function.md)generieren und arbeitet unabhängig von anderen Aufrufen. Es gibt keine definierte Ausführungsreihenfolge von Threads in Bezug aufeinander.

## <a name="shader-type-attribute"></a>Shadertypattribut


```
[shader("raygeneration")]
```



## <a name="example"></a>Beispiel

```
struct SceneConstantStructure { ... };
ConstantBuffer<SceneConstantStructure> SceneConstants;
RaytracingAccelerationStructure MyAccelerationStructure : register(t3);
struct MyPayload { ... };

[shader("raygeneration")]
void raygen_main()
{
    RayDesc myRay = {
        SceneConstants.CameraOrigin,
        SceneConstants.TMin,
        computeRayDirection(SceneConstants.LensParams, DispatchRaysIndex(), 
                            DispatchRaysDimensions()),
        SceneConstants.TMax};
    MyPayload payload = { ... };    // init payload
    TraceRay(
        MyAccelerationStructure,
        SceneConstants.RayFlags,
        SceneConstants.InstanceInclusionMask,
        SceneConstants.RayContributionToHitGroupIndex,
        SceneConstants.MultiplierForGeometryContributionToHitGroupIndex,
        SceneConstants.MissShaderIndex,
        myRay,
        payload);
    WriteFinalPixel(DispatchRaysIndex(), payload);
}
```

 

 




