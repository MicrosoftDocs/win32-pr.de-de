---
description: Flags, die an die traceray-Funktion übergeben werden, um Transparenz, Vererbung und frühe Ausgabeverhalten zu überschreiben.
ms.assetid: ''
title: RAY_FLAG-Enumeration
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
ms.openlocfilehash: 31d6a002e5f3f4eeb5f86e671be0904d61cb916d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345625"
---
# <a name="ray_flag-enumeration"></a><span data-ttu-id="2c8a1-103">Ray- \_ Flag-Enumeration</span><span class="sxs-lookup"><span data-stu-id="2c8a1-103">RAY\_FLAG enumeration</span></span>

<span data-ttu-id="2c8a1-104">Flags, die an die [**traceray**](traceray-function.md) -Funktion übergeben werden, um Transparenz, Vererbung und frühe Ausgabeverhalten zu überschreiben.</span><span class="sxs-lookup"><span data-stu-id="2c8a1-104">Flags passed to the [**TraceRay**](traceray-function.md) function to override transparency, culling, and early-out behavior.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c8a1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2c8a1-105">Syntax</span></span>


```
enum RAY_FLAG : uint
{
    RAY_FLAG_NONE                            = 0x00,
    RAY_FLAG_FORCE_OPAQUE                    = 0x01,
    RAY_FLAG_FORCE_NON_OPAQUE                = 0x02,
    RAY_FLAG_ACCEPT_FIRST_HIT_AND_END_SEARCH = 0x04,
    RAY_FLAG_SKIP_CLOSEST_HIT_SHADER         = 0x08,
    RAY_FLAG_CULL_BACK_FACING_TRIANGLES      = 0x10,
    RAY_FLAG_CULL_FRONT_FACING_TRIANGLES     = 0x20,
    RAY_FLAG_CULL_OPAQUE                     = 0x40,
    RAY_FLAG_CULL_NON_OPAQUE                 = 0x80,
}; 
```



## <a name="constants"></a><span data-ttu-id="2c8a1-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="2c8a1-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="2c8a1-107"><span id="RAY_FLAG_NONE"></span><span id="ray_flag_none"></span>**Ray- \_ Flag \_ None**</span><span class="sxs-lookup"><span data-stu-id="2c8a1-107"><span id="RAY_FLAG_NONE"></span><span id="ray_flag_none"></span>**RAY\_FLAG\_NONE**</span></span>
</dt> <dd>

<span data-ttu-id="2c8a1-108">Es sind keine Optionen ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="2c8a1-108">No options selected.</span></span>

</dd> <dt>

<span data-ttu-id="2c8a1-109"><span id="RAY_FLAG_FORCE_OPAQUE"></span><span id="ray_flag_force_opaque"></span>**Ray-Flag ist nicht transparent \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2c8a1-109"><span id="RAY_FLAG_FORCE_OPAQUE"></span><span id="ray_flag_force_opaque"></span>**RAY\_FLAG\_FORCE\_OPAQUE**</span></span>
</dt> <dd>

<span data-ttu-id="2c8a1-110">Alle in einem Raytrace gefundenen Ray-primitive-Schnittmengen werden als nicht transparent behandelt.</span><span class="sxs-lookup"><span data-stu-id="2c8a1-110">All ray-primitive intersections encountered in a raytrace are treated as opaque.</span></span>  <span data-ttu-id="2c8a1-111">Es werden also keine Treffer-Shader ausgeführt, unabhängig davon, ob die Treffer Geometrie das D3D12 \_ Raytracing \_ Geometry \_ -Flag nicht transparent angibt \_ und unabhängig von den instanzflags auf der Instanz, die getroffen wurde.</span><span class="sxs-lookup"><span data-stu-id="2c8a1-111">So no any hit shaders will be executed regardless of whether or not the hit geometry specifies D3D12\_RAYTRACING\_GEOMETRY\_FLAG\_OPAQUE, and regardless of the instance flags on the instance that was hit.</span></span>

<span data-ttu-id="2c8a1-112">Dieses Flag schließt sich gegenseitig aus, dass die Ray \_ -Flag nicht deckend ist, dass das \_ \_ \_ Ray-Flag nicht transparent ist \_ und das \_ \_ Ray- \_ Flag \_ \_ nicht \_ deckend ist.</span><span class="sxs-lookup"><span data-stu-id="2c8a1-112">This flag is mutually exclusive with RAY\_FLAG\_FORCE\_NON\_OPAQUE, RAY\_FLAG\_CULL\_OPAQUE and RAY\_FLAG\_CULL\_NON\_OPAQUE.</span></span>


</dd> <dt>

<span data-ttu-id="2c8a1-113"><span id="RAY_FLAG_FORCE_NON_OPAQUE"></span><span id="ray_flag_force_non_opaque"></span>**Ray-Flag "nicht deckend" \_ \_ erzwingen \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2c8a1-113"><span id="RAY_FLAG_FORCE_NON_OPAQUE"></span><span id="ray_flag_force_non_opaque"></span>**RAY\_FLAG\_FORCE\_NON\_OPAQUE**</span></span>
</dt> <dd>

<span data-ttu-id="2c8a1-114">Alle in einem Raytrace gefundenen Ray-primitive-Schnittmengen werden als nicht transparent behandelt.</span><span class="sxs-lookup"><span data-stu-id="2c8a1-114">All ray-primitive intersections encountered in a raytrace are treated as non-opaque.</span></span>  <span data-ttu-id="2c8a1-115">Alle Treffer-Shader, falls vorhanden, werden ausgeführt, unabhängig davon, ob die Treffer Geometrie das D3D12 \_ Raytracing \_ Geometry-Flag nicht transparent angibt \_ \_ und unabhängig von den instanzflags auf der Instanz, die getroffen wurde.</span><span class="sxs-lookup"><span data-stu-id="2c8a1-115">So any hit shaders, if present, will be executed regardless of whether or not the hit geometry specifies D3D12\_RAYTRACING\_GEOMETRY\_FLAG\_OPAQUE, and regardless of the instance flags on the instance that was hit.</span></span>
<span data-ttu-id="2c8a1-116">Dieses Flag schließt sich gegenseitig mit dem Ray \_ \_ -Flag FORCE_ \transparent, dem Ray \_ \_ -Flag-cullflag und dem Ray \_ - \_ Flag \_ \_ nicht \_ deckend aus.</span><span class="sxs-lookup"><span data-stu-id="2c8a1-116">This flag is mutually exclusive with RAY\_FLAG\_FORCE_\OPAQUE, RAY\_FLAG\_CULL\_OPAQUE and RAY\_FLAG\_CULL\_NON\_OPAQUE.</span></span>


</dd> <dt>

<span data-ttu-id="2c8a1-117"><span id="RAY_FLAG_ACCEPT_FIRST_HIT_AND_END_SEARCH"></span><span id="ray_flag_accept_first_hit_and_end_search"></span>**Ray \_ -Flag " \_ \_ erste \_ Treffer \_ -und \_ \_ endsuche akzeptieren"**</span><span class="sxs-lookup"><span data-stu-id="2c8a1-117"><span id="RAY_FLAG_ACCEPT_FIRST_HIT_AND_END_SEARCH"></span><span id="ray_flag_accept_first_hit_and_end_search"></span>**RAY\_FLAG\_ACCEPT\_FIRST\_HIT\_AND\_END\_SEARCH**</span></span>
</dt> <dd>

<span data-ttu-id="2c8a1-118">Die erste Strahl primitive Schnittmenge, die in einem Raytrace erkannt wird, bewirkt, dass " **Accept thitandendsearch** " unmittelbar nach dem beliebigen Treffer-Shader aufgerufen wird, einschließlich, wenn kein Treffer-Shader vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="2c8a1-118">The first ray-primitive intersection encountered in a raytrace automatically causes **AcceptHitAndEndSearch** to be called immediately after the any hit shader, including if there is no any hit shader.</span></span> 
 
<span data-ttu-id="2c8a1-119">Die einzige Ausnahme ist, wenn der vorangehende Treffer-Shader **ignorehit** aufruft. in diesem Fall bleibt der Strahl unverändert, sodass der nächste Treffer zu einem anderen Kandidaten wird, der als erster Treffer fungiert.</span><span class="sxs-lookup"><span data-stu-id="2c8a1-119">The only exception is when the preceding any hit shader calls **IgnoreHit**, in which case the ray continues unaffected such that the next hit becomes another candidate to be the first hit.</span></span>  <span data-ttu-id="2c8a1-120">Damit diese Ausnahme angewendet werden kann, muss der beliebige Treffer-Shader tatsächlich ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="2c8a1-120">For this exception to apply, the any hit shader has to actually be executed.</span></span>  <span data-ttu-id="2c8a1-121">Wenn also der Treffer-Shader übersprungen wird, weil der Treffer als nicht transparent behandelt wird (z. b. weil das Flag für die ntflag-Flag "nicht transparent" \_ \_ oder " \_ D3D12 \_ Raytracing \_ Geometry Flag nicht transparent" oder das Flag " \_ \_ D3D12 \_ Raytracing- \_ \_ instanzflag nicht transparent" \_ festgelegt wird), wird " **Accepted**</span><span class="sxs-lookup"><span data-stu-id="2c8a1-121">So if the any hit shader is skipped because the hit is treated as opaque (e.g. due to RAY\_FLAG\_FORCE\_OPAQUE or D3D12\_RAYTRACING\_GEOMETRY\_FLAG\_OPAQUE or D3D12\_RAYTRACING\_INSTANCE\_FLAG\_OPAQUE being set), then **AcceptHitAndEndSearch** is called.</span></span>

<span data-ttu-id="2c8a1-122">Wenn beim ersten Treffer ein nächster Treffer-Shader vorhanden ist, wird er aufgerufen, es sei denn, das Ray- \_ Flag über \_ springt den \_ nächstgelegenen \_ Treffer- \_ Shader.</span><span class="sxs-lookup"><span data-stu-id="2c8a1-122">If a closest hit shader is present at the first hit, it gets invoked unless RAY\_FLAG\_SKIP\_CLOSEST\_HIT\_SHADER is also present.</span></span>  <span data-ttu-id="2c8a1-123">Der gefundene Treffer wird als "nächstgelegene" angesehen, auch wenn andere potenzielle Treffer, die möglicherweise näher am Strahl liegen, nicht besucht wurden.</span><span class="sxs-lookup"><span data-stu-id="2c8a1-123">The one hit that was found is considered “closest”, even though other potential hits that might be closer on the ray may not have been visited.</span></span>

<span data-ttu-id="2c8a1-124">Eine typische Verwendung für dieses Flag ist für Schatten, bei denen nur ein einziger Treffer gefunden werden muss.</span><span class="sxs-lookup"><span data-stu-id="2c8a1-124">A typical use for this flag is for shadows, where only a single hit needs to be found.</span></span>


</dd> <dt>

<span data-ttu-id="2c8a1-125"><span id="RAY_FLAG_SKIP_CLOSEST_HIT_SHADER"></span><span id="ray_flag_skip_closest_hit_shader"></span>**Ray- \_ Flag \_ Skip \_ nächster Treffer- \_ \_ Shader überspringen**</span><span class="sxs-lookup"><span data-stu-id="2c8a1-125"><span id="RAY_FLAG_SKIP_CLOSEST_HIT_SHADER"></span><span id="ray_flag_skip_closest_hit_shader"></span>**RAY\_FLAG\_SKIP\_CLOSEST\_HIT\_SHADER**</span></span>
</dt> <dd>

<span data-ttu-id="2c8a1-126">Auch wenn für mindestens ein Treffer ein Commit ausgeführt wurde und die Treffer Gruppe für den nächstgelegenen Treffer einen nächsten Treffer-Shader enthält, überspringen Sie die Ausführung dieses Shaders.</span><span class="sxs-lookup"><span data-stu-id="2c8a1-126">Even if at least one hit has been committed, and the hit group for the closest hit contains a closest hit shader, skip execution of that shader.</span></span> 

</dd> <dt>

<span data-ttu-id="2c8a1-127"><span id="RAY_FLAG_CULL_BACK_FACING_TRIANGLES"></span><span id="ray_flag_cull_back_facing_triangles"></span>**Ray-Flag, das auf den \_ \_ \_ \_ \_ Dreiecke zurückgeht**</span><span class="sxs-lookup"><span data-stu-id="2c8a1-127"><span id="RAY_FLAG_CULL_BACK_FACING_TRIANGLES"></span><span id="ray_flag_cull_back_facing_triangles"></span>**RAY\_FLAG\_CULL\_BACK\_FACING\_TRIANGLES**</span></span>
</dt> <dd>

<span data-ttu-id="2c8a1-128">Ermöglicht das Berechnen von zurück gerichteten Dreiecken.</span><span class="sxs-lookup"><span data-stu-id="2c8a1-128">Enables culling of back facing triangles.</span></span> <span data-ttu-id="2c8a1-129">Siehe **D3D12 \_ Raytracing \_ - \_ instanzflags** , um auszuwählen, welche Dreiecke zurückstehen, pro Instanz.</span><span class="sxs-lookup"><span data-stu-id="2c8a1-129">See **D3D12\_RAYTRACING\_INSTANCE\_FLAGS** for selecting which triangles are back facing, per-instance.</span></span>

<span data-ttu-id="2c8a1-130">Bei Instanzen, die D3D12 \_ Raytracing \_ instance \_ Flag- \_ Dreieck- \_ cull \_ Deaktivieren angeben, hat dieses Flag keine Auswirkungen.</span><span class="sxs-lookup"><span data-stu-id="2c8a1-130">On instances that specify D3D12\_RAYTRACING\_INSTANCE\_FLAG\_TRIANGLE\_CULL\_DISABLE, this flag has no effect.</span></span>

<span data-ttu-id="2c8a1-131">Bei geometry-Typen außer D3D12 \_ Raytracing \_ Geometry \_ Type \_ Dreiecke hat dieses Flag keine Auswirkungen.</span><span class="sxs-lookup"><span data-stu-id="2c8a1-131">On geometry types other than D3D12\_RAYTRACING\_GEOMETRY\_TYPE\_TRIANGLES, this flag has no effect.</span></span>

<span data-ttu-id="2c8a1-132">Dieses Flag schließt sich mit dem Ray-Flag für die Vorder-und-Ecke gegenseitig aus \_ \_ \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="2c8a1-132">This flag is mutually exclusive with RAY\_FLAG\_CULL\_FRONT\_FACING\_TRIANGLES.</span></span>


</dd> <dt>

<span data-ttu-id="2c8a1-133"><span id="RAY_FLAG_CULL_FRONT_FACING_TRIANGLES"></span><span id="ray_flag_cull_front_facing_trianglesag_none"></span>**Ray- \_ Flag- \_ \_ Spitzen \_ \_ Ecke**</span><span class="sxs-lookup"><span data-stu-id="2c8a1-133"><span id="RAY_FLAG_CULL_FRONT_FACING_TRIANGLES"></span><span id="ray_flag_cull_front_facing_trianglesag_none"></span>**RAY\_FLAG\_CULL\_FRONT\_FACING\_TRIANGLES**</span></span>
</dt> <dd>

<span data-ttu-id="2c8a1-134">Ermöglicht das Berechnen von Front-ELN-Dreiecke.</span><span class="sxs-lookup"><span data-stu-id="2c8a1-134">Enables culling of front facing triangles.</span></span> <span data-ttu-id="2c8a1-135">Siehe **D3D12 \_ Raytracing \_ - \_ instanzflags** , um auszuwählen, welche Dreiecke zurückstehen, pro Instanz.</span><span class="sxs-lookup"><span data-stu-id="2c8a1-135">See **D3D12\_RAYTRACING\_INSTANCE\_FLAGS** for selecting which triangles are back facing, per-instance.</span></span>

<span data-ttu-id="2c8a1-136">Bei Instanzen, die D3D12 \_ Raytracing \_ instance \_ Flag- \_ Dreieck- \_ cull \_ Deaktivieren angeben, hat dieses Flag keine Auswirkungen.</span><span class="sxs-lookup"><span data-stu-id="2c8a1-136">On instances that specify D3D12\_RAYTRACING\_INSTANCE\_FLAG\_TRIANGLE\_CULL\_DISABLE, this flag has no effect.</span></span>

<span data-ttu-id="2c8a1-137">Bei geometry-Typen außer D3D12 \_ Raytracing \_ Geometry \_ Type \_ Dreiecke hat dieses Flag keine Auswirkungen.</span><span class="sxs-lookup"><span data-stu-id="2c8a1-137">On geometry types other than D3D12\_RAYTRACING\_GEOMETRY\_TYPE\_TRIANGLES, this flag has no effect.</span></span>

<span data-ttu-id="2c8a1-138">Dieses Flag schließt sich mit dem Ray-Flag zurück, das auf \_ \_ \_ \_ \_ Dreiecke ausgerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="2c8a1-138">This flag is mutually exclusive with RAY\_FLAG\_CULL\_BACK\_FACING\_TRIANGLES.</span></span>


</dd> <dt>

<span data-ttu-id="2c8a1-139"><span id="RAY_FLAG_CULL_OPAQUE"></span><span id="ray_flag_cull_opaque"></span>**Das Ray-Flag ist nicht transparent. \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2c8a1-139"><span id="RAY_FLAG_CULL_OPAQUE"></span><span id="ray_flag_cull_opaque"></span>**RAY\_FLAG\_CULL\_OPAQUE**</span></span>
</dt> <dd>

<span data-ttu-id="2c8a1-140">Culls alle primitiven, die auf der Grundlage ihrer Geometry-und instanzflags als nicht transparent eingestuft werden.</span><span class="sxs-lookup"><span data-stu-id="2c8a1-140">Culls all primitives that are considered opaque based on their geometry and instance flags.</span></span>

<span data-ttu-id="2c8a1-141">Dieses Flag schließt sich gegenseitig aus, dass die Ray \_ \_ -Flag nicht transparent ist, dass die \_ Ray \_ -Flag nicht deckend ist und das \_ \_ \_ Ray- \_ Flag \_ \_ nicht \_ deckend ist.</span><span class="sxs-lookup"><span data-stu-id="2c8a1-141">This flag is mutually exclusive with RAY\_FLAG\_FORCE\_OPAQUE, RAY\_FLAG\_FORCE\_NON\_OPAQUE, and RAY\_FLAG\_CULL\_NON\_OPAQUE.</span></span>


</dd> <dt>

<span data-ttu-id="2c8a1-142"><span id="RAY_FLAG_CULL_NON_OPAQUE"></span><span id="ray_flag_cull_non_opaque"></span>**Das Ray- \_ Flag ist \_ \_ nicht \_ deckend.**</span><span class="sxs-lookup"><span data-stu-id="2c8a1-142"><span id="RAY_FLAG_CULL_NON_OPAQUE"></span><span id="ray_flag_cull_non_opaque"></span>**RAY\_FLAG\_CULL\_NON\_OPAQUE**</span></span>
</dt> <dd>

<span data-ttu-id="2c8a1-143">Culls alle primitiven, die auf der Grundlage ihrer Geometry-und instanzflags als nicht transparent angesehen werden.</span><span class="sxs-lookup"><span data-stu-id="2c8a1-143">Culls all primitives that are considered non-opaque based on their geometry and instance flags.</span></span>

<span data-ttu-id="2c8a1-144">Dieses Flag schließt sich gegenseitig aus, wenn die Ray \_ \_ -Flag \_ \_ nicht transparent, Ray \_ -Flag nicht deckend \_ und Ray-Flag nicht transparent ist \_ \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="2c8a1-144">This flag is mutually exclusive with RAY\_FLAG\_FORCE\_OPAQUE, RAY\_FLAG\_FORCE\_NON\_OPAQUE, and RAY\_FLAG\_CULL\_OPAQUE.</span></span>


</dd>

## <a name="requirements"></a><span data-ttu-id="2c8a1-145">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2c8a1-145">Requirements</span></span>



## <a name="see-also"></a><span data-ttu-id="2c8a1-146">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="2c8a1-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c8a1-147">Direct3D 12-Raytracing, HLSL-Referenz</span><span class="sxs-lookup"><span data-stu-id="2c8a1-147">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




