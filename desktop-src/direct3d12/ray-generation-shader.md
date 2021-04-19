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
# <a name="ray-generation-shader"></a><span data-ttu-id="6f223-103">Ray Generation-Shader</span><span class="sxs-lookup"><span data-stu-id="6f223-103">Ray Generation Shader</span></span>

<span data-ttu-id="6f223-104">Ein Shader, der [**traceray**](traceray-function.md) aufruft, um Strahlen zu generieren.</span><span class="sxs-lookup"><span data-stu-id="6f223-104">A shader that calls [**TraceRay**](traceray-function.md) to generate rays.</span></span> <span data-ttu-id="6f223-105">Die ursprüngliche benutzerdefinierte Ray-Nutzlast für jeden Strahl wird der **traceray** -Website für Anrufe bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="6f223-105">The initial user-defined ray payload for each ray is provided to the **TraceRay** call site.</span></span>  <span data-ttu-id="6f223-106">[**Callshader**](callshader-function.md) kann auch in Ray-Generierungs-Shadern verwendet werden, um [Aufruf Bare Shader](callable-shader.md)aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="6f223-106">[**CallShader**](callshader-function.md) may also be used in ray generation shaders to invoke [callable shaders](callable-shader.md).</span></span>

<span data-ttu-id="6f223-107">**Dispatchrays** Ruft ein Raster von Shader-Aufrufen der Ray-Generierung auf.</span><span class="sxs-lookup"><span data-stu-id="6f223-107">**DispatchRays** invokes a grid of ray generation shader invocations.</span></span>  <span data-ttu-id="6f223-108">Jeder Aufruf (Thread) eines Ray-Generierungs-Shaders kennt seinen Speicherort im Gesamt Raster, kann beliebige Strahlen über [**traceray**](traceray-function.md)generieren und funktioniert unabhängig von anderen aufrufen.</span><span class="sxs-lookup"><span data-stu-id="6f223-108">Each invocation (thread) of a ray generation shader knows its location in the overall grid, can generate arbitrary rays via [**TraceRay**](traceray-function.md), and operates independently of other invocations.</span></span> <span data-ttu-id="6f223-109">Es gibt keine definierte Reihenfolge der Ausführung von Threads in Bezug zueinander.</span><span class="sxs-lookup"><span data-stu-id="6f223-109">There is no defined order of execution of threads with respect to each other.</span></span>

## <a name="shader-type-attribute"></a><span data-ttu-id="6f223-110">Shader Type-Attribut</span><span class="sxs-lookup"><span data-stu-id="6f223-110">Shader Type attribute</span></span>


```
[shader("raygeneration")]
```



## <a name="example"></a><span data-ttu-id="6f223-111">Beispiel</span><span class="sxs-lookup"><span data-stu-id="6f223-111">Example</span></span>

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

 

 




