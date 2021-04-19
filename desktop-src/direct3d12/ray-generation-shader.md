---
description: Ein Shader, der traceray aufruft, um Strahlen zu generieren.
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
ms.openlocfilehash: 75d67293e489eee0f1d100002965c017de7c682c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106342613"
---
# <a name="ray-generation-shader"></a>Ray Generation-Shader

Ein Shader, der [**traceray**](traceray-function.md) aufruft, um Strahlen zu generieren. Die ursprüngliche benutzerdefinierte Ray-Nutzlast für jeden Strahl wird der **traceray** -Website für Anrufe bereitgestellt.  [**Callshader**](callshader-function.md) kann auch in Ray-Generierungs-Shadern verwendet werden, um [Aufruf Bare Shader](callable-shader.md)aufzurufen.

**Dispatchrays** Ruft ein Raster von Shader-Aufrufen der Ray-Generierung auf.  Jeder Aufruf (Thread) eines Ray-Generierungs-Shaders kennt seinen Speicherort im Gesamt Raster, kann beliebige Strahlen über [**traceray**](traceray-function.md)generieren und funktioniert unabhängig von anderen aufrufen. Es gibt keine definierte Reihenfolge der Ausführung von Threads in Bezug zueinander.

## <a name="shader-type-attribute"></a>Shader Type-Attribut


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

 

 




