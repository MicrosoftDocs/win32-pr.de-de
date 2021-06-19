---
title: Direct3D 12-Raytracing, HLSL-Systemwertinterna
description: Hier finden Sie Links zu Artikeln, in denen systeminterne HlSL-Systemwertfunktionen (High-Level Shader Language, Shadersprache) beschrieben werden, die die Direct3D 12-Raytracingpipeline unterstützen.
ms.assetid: ''
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e2790cf5df42f64071db3ca51a35e58ee9afcd5
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396435"
---
# <a name="direct3d-12-raytracing-hlsl-system-value-intrinsics"></a><span data-ttu-id="bb1fe-103">Direct3D 12-Raytracing, HLSL-Systemwertinterna</span><span class="sxs-lookup"><span data-stu-id="bb1fe-103">Direct3D 12 raytracing HLSL system value intrinsics</span></span>

<span data-ttu-id="bb1fe-104">Systemwerte werden mithilfe spezieller intrinsischer Funktionen abgerufen, anstatt Parameter mit spezieller Semantik in Ihre Shaderfunktionssignatur ein- und zu übernehmen.</span><span class="sxs-lookup"><span data-stu-id="bb1fe-104">System values are retrieved by using special intrinsic functions, rather than including parameters with special semantics in your shader function signature.</span></span> 

## <a name="in-this-section"></a><span data-ttu-id="bb1fe-105">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="bb1fe-105">In this section</span></span>

### <a name="ray-dispatch-system-values"></a><span data-ttu-id="bb1fe-106">Ray Dispatch-Systemwerte</span><span class="sxs-lookup"><span data-stu-id="bb1fe-106">Ray dispatch system values</span></span>

| <span data-ttu-id="bb1fe-107">Thema</span><span class="sxs-lookup"><span data-stu-id="bb1fe-107">Topic</span></span> | <span data-ttu-id="bb1fe-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bb1fe-108">Description</span></span> |
|-|-|
| [<span data-ttu-id="bb1fe-109">**DispatchRaysIndex**</span><span class="sxs-lookup"><span data-stu-id="bb1fe-109">**DispatchRaysIndex**</span></span>](dispatchraysindex.md) | <span data-ttu-id="bb1fe-110">Ruft die aktuelle x- und y-Position innerhalb der Breite und Höhe ab, die mit dem **systeminternen DispatchRaysDimensions-Systemwert** ermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="bb1fe-110">Gets the current x and y location within the width and height obtained with the **DispatchRaysDimensions** system value intrinsic.</span></span> |
| [<span data-ttu-id="bb1fe-111">**DispatchRaysDimensions**</span><span class="sxs-lookup"><span data-stu-id="bb1fe-111">**DispatchRaysDimensions**</span></span>](dispatchraysdimensions.md) | <span data-ttu-id="bb1fe-112">Die Werte für Breite, Höhe und Tiefe der **D3D12 \_ DISPATCH \_ RAY \_ DESC-Struktur,** die im ursprünglichen **DispatchRays-Aufruf angegeben** sind.</span><span class="sxs-lookup"><span data-stu-id="bb1fe-112">The width, height and depth values from the **D3D12\_DISPATCH\_RAYS\_DESC** structure specified in the originating **DispatchRays** call.</span></span> |

### <a name="ray-system-values"></a><span data-ttu-id="bb1fe-113">Ray-Systemwerte</span><span class="sxs-lookup"><span data-stu-id="bb1fe-113">Ray system values</span></span>

| <span data-ttu-id="bb1fe-114">Thema</span><span class="sxs-lookup"><span data-stu-id="bb1fe-114">Topic</span></span> | <span data-ttu-id="bb1fe-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bb1fe-115">Description</span></span> |
|-|-|
| [<span data-ttu-id="bb1fe-116">**WorldRayOrigin**</span><span class="sxs-lookup"><span data-stu-id="bb1fe-116">**WorldRayOrigin**</span></span>](worldrayorigin.md) | <span data-ttu-id="bb1fe-117">Der Ursprung des aktuellen Strahls in der Welt.</span><span class="sxs-lookup"><span data-stu-id="bb1fe-117">The world-space origin of the current ray.</span></span> |
| [<span data-ttu-id="bb1fe-118">**WorldRayDirection**</span><span class="sxs-lookup"><span data-stu-id="bb1fe-118">**WorldRayDirection**</span></span>](worldraydirection.md) | <span data-ttu-id="bb1fe-119">Die Weltraumrichtung für den aktuellen Strahl.</span><span class="sxs-lookup"><span data-stu-id="bb1fe-119">The world-space direction for the current ray.</span></span> |
| [<span data-ttu-id="bb1fe-120">**RayTMin**</span><span class="sxs-lookup"><span data-stu-id="bb1fe-120">**RayTMin**</span></span>](raytmin.md) | <span data-ttu-id="bb1fe-121">Ein Gleitkommawert, der den aktuellen parametrischen Ausgangspunkt für den Strahl darstellt.</span><span class="sxs-lookup"><span data-stu-id="bb1fe-121">A float representing the current parametric starting point for the ray.</span></span> |
| [<span data-ttu-id="bb1fe-122">**RayTCurrent**</span><span class="sxs-lookup"><span data-stu-id="bb1fe-122">**RayTCurrent**</span></span>](raytcurrent.md) | <span data-ttu-id="bb1fe-123">Ein Gleitkommawert, der den aktuellen parametrischen Endpunkt für den Strahl darstellt.</span><span class="sxs-lookup"><span data-stu-id="bb1fe-123">A float representing the current parametric ending point for the ray.</span></span>  |
| [<span data-ttu-id="bb1fe-124">**RayFlags**</span><span class="sxs-lookup"><span data-stu-id="bb1fe-124">**RayFlags**</span></span>](rayflags.md) | <span data-ttu-id="bb1fe-125">Eine ganze Zahl ohne Vorzeichen, die die aktuellen **ray_flag** enthält.</span><span class="sxs-lookup"><span data-stu-id="bb1fe-125">An unsigned integer containing the current **ray_flag** flags.</span></span> |

### <a name="primitiveobject-space-system-values"></a><span data-ttu-id="bb1fe-126">Primitive/Objektraum-Systemwerte</span><span class="sxs-lookup"><span data-stu-id="bb1fe-126">Primitive/object space system values</span></span>

| <span data-ttu-id="bb1fe-127">Thema</span><span class="sxs-lookup"><span data-stu-id="bb1fe-127">Topic</span></span> | <span data-ttu-id="bb1fe-128">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bb1fe-128">Description</span></span> |
|-|-|
| [<span data-ttu-id="bb1fe-129">**InstanceIndex**</span><span class="sxs-lookup"><span data-stu-id="bb1fe-129">**InstanceIndex**</span></span>](instanceindex.md) | <span data-ttu-id="bb1fe-130">Der automatisch generierte Index der aktuellen Instanz in der Raytracingbeschleunigungsstruktur der obersten Ebene.</span><span class="sxs-lookup"><span data-stu-id="bb1fe-130">The autogenerated index of the current instance in the top-level raytracing acceleration structure.</span></span> |
| [<span data-ttu-id="bb1fe-131">**Instanceid**</span><span class="sxs-lookup"><span data-stu-id="bb1fe-131">**InstanceID**</span></span>](instanceid.md) | <span data-ttu-id="bb1fe-132">Der vom Benutzer bereitgestellte Bezeichner für die -Instanz in der Instanz der Beschleunigungsstruktur auf unterer Ebene innerhalb der Struktur der obersten Ebene.</span><span class="sxs-lookup"><span data-stu-id="bb1fe-132">The user-provided identifier for the instance on the bottom-level acceleration structure instance within the top-level structure.</span></span> |
| [<span data-ttu-id="bb1fe-133">**PrimitiveIndex**</span><span class="sxs-lookup"><span data-stu-id="bb1fe-133">**PrimitiveIndex**</span></span>](primitiveindex.md) | <span data-ttu-id="bb1fe-134">Der automatisch generierte Index des Primitiven innerhalb der Geometrie innerhalb der Instanz der Beschleunigungsstruktur auf unterer Ebene.</span><span class="sxs-lookup"><span data-stu-id="bb1fe-134">The autogenerated index of the primitive within the geometry inside the bottom-level acceleration structure instance.</span></span> |
| [<span data-ttu-id="bb1fe-135">**ObjectRayOrigin**</span><span class="sxs-lookup"><span data-stu-id="bb1fe-135">**ObjectRayOrigin**</span></span>](objectrayorigin.md) | <span data-ttu-id="bb1fe-136">Der Objektraum-Ursprung für den aktuellen Strahl.</span><span class="sxs-lookup"><span data-stu-id="bb1fe-136">The object-space origin for the current ray.</span></span> |
| [<span data-ttu-id="bb1fe-137">**ObjectRayDirection**</span><span class="sxs-lookup"><span data-stu-id="bb1fe-137">**ObjectRayDirection**</span></span>](objectraydirection.md) | <span data-ttu-id="bb1fe-138">Die Objektraumrichtung für den aktuellen Strahl.</span><span class="sxs-lookup"><span data-stu-id="bb1fe-138">The object-space direction for the current ray.</span></span> |
| [<span data-ttu-id="bb1fe-139">**ObjectToWorld3x4**</span><span class="sxs-lookup"><span data-stu-id="bb1fe-139">**ObjectToWorld3x4**</span></span>](objecttoworld3x4.md) | <span data-ttu-id="bb1fe-140">Eine Matrix für die Transformation von Objektraum in Raum.</span><span class="sxs-lookup"><span data-stu-id="bb1fe-140">A matrix for transforming from object-space to world-space.</span></span> |
| [<span data-ttu-id="bb1fe-141">**ObjectToWorld4x3**</span><span class="sxs-lookup"><span data-stu-id="bb1fe-141">**ObjectToWorld4x3**</span></span>](objecttoworld4x3.md) | <span data-ttu-id="bb1fe-142">Eine Matrix für die Transformation von Objektraum in Raum.</span><span class="sxs-lookup"><span data-stu-id="bb1fe-142">A matrix for transforming from object-space to world-space.</span></span> |
| [<span data-ttu-id="bb1fe-143">**WorldToObject3x4**</span><span class="sxs-lookup"><span data-stu-id="bb1fe-143">**WorldToObject3x4**</span></span>](worldtoobject3x4.md) | <span data-ttu-id="bb1fe-144">Eine Matrix für die Transformation vom Raum in den Objektraum</span><span class="sxs-lookup"><span data-stu-id="bb1fe-144">A matrix for transforming from world-space to object-space</span></span> |
| [<span data-ttu-id="bb1fe-145">**WorldToObject4x3**</span><span class="sxs-lookup"><span data-stu-id="bb1fe-145">**WorldToObject4x3**</span></span>](worldtoobject4x3.md) | <span data-ttu-id="bb1fe-146">Eine Matrix für die Transformation vom Raum in den Objektraum</span><span class="sxs-lookup"><span data-stu-id="bb1fe-146">A matrix for transforming from world-space to object-space</span></span> |
### <a name="hit-specific-system-values"></a><span data-ttu-id="bb1fe-147">Trefferspezifische Systemwerte</span><span class="sxs-lookup"><span data-stu-id="bb1fe-147">Hit-specific system values</span></span>

| <span data-ttu-id="bb1fe-148">Thema</span><span class="sxs-lookup"><span data-stu-id="bb1fe-148">Topic</span></span> | <span data-ttu-id="bb1fe-149">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bb1fe-149">Description</span></span> |
|-|-|
| [<span data-ttu-id="bb1fe-150">**HitKind**</span><span class="sxs-lookup"><span data-stu-id="bb1fe-150">**HitKind**</span></span>](hitkind.md) | <span data-ttu-id="bb1fe-151">Gibt den Wert zurück, der als **HitKind-Parameter** an [**ReportHit übergeben wird.**](reporthit-function.md)</span><span class="sxs-lookup"><span data-stu-id="bb1fe-151">Returns the value passed as the **HitKind** parameter to [**ReportHit**](reporthit-function.md).</span></span> |

## <a name="related-topics"></a><span data-ttu-id="bb1fe-152">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="bb1fe-152">Related topics</span></span>

* [<span data-ttu-id="bb1fe-153">Kernreferenz</span><span class="sxs-lookup"><span data-stu-id="bb1fe-153">Core Reference</span></span>](direct3d-12-core-reference.md)
* [<span data-ttu-id="bb1fe-154">Referenz für Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="bb1fe-154">Direct3D 12 Reference</span></span>](direct3d-12-reference.md)
