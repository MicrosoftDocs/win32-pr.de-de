---
title: Direct3D 12-Raytracing, HLSL-Systemwertinterna
description: Die folgenden HLSL-Shader unterstützen die Direct3D 12-Raytracing-Pipeline.
ms.assetid: ''
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a20282e7bc0e9e4898fd361b0959cd6b6f32253
ms.sourcegitcommit: 4e4f9e7c90d25af0774deec1d44bd49fa9b6daa9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2020
ms.locfileid: "106338100"
---
# <a name="direct3d-12-raytracing-hlsl-system-value-intrinsics"></a><span data-ttu-id="bb247-103">Direct3D 12-Raytracing, HLSL-Systemwertinterna</span><span class="sxs-lookup"><span data-stu-id="bb247-103">Direct3D 12 raytracing HLSL system value intrinsics</span></span>

<span data-ttu-id="bb247-104">System Werte werden mithilfe spezieller intrinsischer Funktionen abgerufen, anstatt Parameter mit spezieller Semantik in die Signatur der Shaderfunktionen einzuschließen.</span><span class="sxs-lookup"><span data-stu-id="bb247-104">System values are retrieved by using special intrinsic functions, rather than including parameters with special semantics in your shader function signature.</span></span> 

## <a name="in-this-section"></a><span data-ttu-id="bb247-105">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="bb247-105">In this section</span></span>

### <a name="ray-dispatch-system-values"></a><span data-ttu-id="bb247-106">System Werte von Ray Dispatch</span><span class="sxs-lookup"><span data-stu-id="bb247-106">Ray dispatch system values</span></span>

| <span data-ttu-id="bb247-107">Thema</span><span class="sxs-lookup"><span data-stu-id="bb247-107">Topic</span></span> | <span data-ttu-id="bb247-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bb247-108">Description</span></span> |
|-|-|
| [<span data-ttu-id="bb247-109">**Dispatchraysindex**</span><span class="sxs-lookup"><span data-stu-id="bb247-109">**DispatchRaysIndex**</span></span>](dispatchraysindex.md) | <span data-ttu-id="bb247-110">Ruft die aktuelle x-und y-Position innerhalb der Breite und Höhe ab, die mit dem systeminternen **dispatchraysdimensions** -System Wert abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="bb247-110">Gets the current x and y location within the width and height obtained with the **DispatchRaysDimensions** system value intrinsic.</span></span> |
| [<span data-ttu-id="bb247-111">**DispatchRaysDimensions**</span><span class="sxs-lookup"><span data-stu-id="bb247-111">**DispatchRaysDimensions**</span></span>](dispatchraysdimensions.md) | <span data-ttu-id="bb247-112">Die Werte für Breite, Höhe und Tiefe der **D3D12 \_ Dispatch \_ Rays \_** -Struktur, die in den ursprünglichen **dispatchrays** -aufrufen angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="bb247-112">The width, height and depth values from the **D3D12\_DISPATCH\_RAYS\_DESC** structure specified in the originating **DispatchRays** call.</span></span> |

### <a name="ray-system-values"></a><span data-ttu-id="bb247-113">Ray-System Werte</span><span class="sxs-lookup"><span data-stu-id="bb247-113">Ray system values</span></span>

| <span data-ttu-id="bb247-114">Thema</span><span class="sxs-lookup"><span data-stu-id="bb247-114">Topic</span></span> | <span data-ttu-id="bb247-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bb247-115">Description</span></span> |
|-|-|
| [<span data-ttu-id="bb247-116">**Worldrayorigin**</span><span class="sxs-lookup"><span data-stu-id="bb247-116">**WorldRayOrigin**</span></span>](worldrayorigin.md) | <span data-ttu-id="bb247-117">Der Welt Raum Ursprung des aktuellen Strahls.</span><span class="sxs-lookup"><span data-stu-id="bb247-117">The world-space origin of the current ray.</span></span> |
| [<span data-ttu-id="bb247-118">**Worldraydirection**</span><span class="sxs-lookup"><span data-stu-id="bb247-118">**WorldRayDirection**</span></span>](worldraydirection.md) | <span data-ttu-id="bb247-119">Die Welt Raum Richtung für das aktuelle Ray.</span><span class="sxs-lookup"><span data-stu-id="bb247-119">The world-space direction for the current ray.</span></span> |
| [<span data-ttu-id="bb247-120">**Raytmin**</span><span class="sxs-lookup"><span data-stu-id="bb247-120">**RayTMin**</span></span>](raytmin.md) | <span data-ttu-id="bb247-121">Ein float-Wert, der den aktuellen parametrischen Anfangspunkt für den Strahl darstellt.</span><span class="sxs-lookup"><span data-stu-id="bb247-121">A float representing the current parametric starting point for the ray.</span></span> |
| [<span data-ttu-id="bb247-122">**Raycurrent**</span><span class="sxs-lookup"><span data-stu-id="bb247-122">**RayTCurrent**</span></span>](raytcurrent.md) | <span data-ttu-id="bb247-123">Ein float-Wert, der den aktuellen parametrischen Endpunkt für den Strahl darstellt.</span><span class="sxs-lookup"><span data-stu-id="bb247-123">A float representing the current parametric ending point for the ray.</span></span>  |
| [<span data-ttu-id="bb247-124">**Rayflags**</span><span class="sxs-lookup"><span data-stu-id="bb247-124">**RayFlags**</span></span>](rayflags.md) | <span data-ttu-id="bb247-125">Eine ganze Zahl ohne Vorzeichen, die die aktuellen **ray_flag** Flags enthält.</span><span class="sxs-lookup"><span data-stu-id="bb247-125">An unsigned integer containing the current **ray_flag** flags.</span></span> |

### <a name="primitiveobject-space-system-values"></a><span data-ttu-id="bb247-126">Primitive/Objekt Raum System Werte</span><span class="sxs-lookup"><span data-stu-id="bb247-126">Primitive/object space system values</span></span>

| <span data-ttu-id="bb247-127">Thema</span><span class="sxs-lookup"><span data-stu-id="bb247-127">Topic</span></span> | <span data-ttu-id="bb247-128">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bb247-128">Description</span></span> |
|-|-|
| [<span data-ttu-id="bb247-129">**Instanceingedex**</span><span class="sxs-lookup"><span data-stu-id="bb247-129">**InstanceIndex**</span></span>](instanceindex.md) | <span data-ttu-id="bb247-130">Der automatisch generierte Index der aktuellen Instanz in der Raytracing-Beschleunigungs Struktur der obersten Ebene.</span><span class="sxs-lookup"><span data-stu-id="bb247-130">The autogenerated index of the current instance in the top-level raytracing acceleration structure.</span></span> |
| [<span data-ttu-id="bb247-131">**InstanceId**</span><span class="sxs-lookup"><span data-stu-id="bb247-131">**InstanceID**</span></span>](instanceid.md) | <span data-ttu-id="bb247-132">Der vom Benutzer bereitgestellte Bezeichner für die-Instanz auf der unteren Ebene der Beschleunigungs Struktur Instanz innerhalb der Struktur der obersten Ebene.</span><span class="sxs-lookup"><span data-stu-id="bb247-132">The user-provided identifier for the instance on the bottom-level acceleration structure instance within the top-level structure.</span></span> |
| [<span data-ttu-id="bb247-133">**Primitiveingedex**</span><span class="sxs-lookup"><span data-stu-id="bb247-133">**PrimitiveIndex**</span></span>](primitiveindex.md) | <span data-ttu-id="bb247-134">Der automatisch generierte Index des primitiven innerhalb der Geometrie innerhalb der Beschleunigung der Beschleunigung-Struktur der untersten Ebene.</span><span class="sxs-lookup"><span data-stu-id="bb247-134">The autogenerated index of the primitive within the geometry inside the bottom-level acceleration structure instance.</span></span> |
| [<span data-ttu-id="bb247-135">**Objectrayorigin**</span><span class="sxs-lookup"><span data-stu-id="bb247-135">**ObjectRayOrigin**</span></span>](objectrayorigin.md) | <span data-ttu-id="bb247-136">Der Objekt Raum Ursprung für das aktuelle Ray.</span><span class="sxs-lookup"><span data-stu-id="bb247-136">The object-space origin for the current ray.</span></span> |
| [<span data-ttu-id="bb247-137">**Objectraydirection**</span><span class="sxs-lookup"><span data-stu-id="bb247-137">**ObjectRayDirection**</span></span>](objectraydirection.md) | <span data-ttu-id="bb247-138">Die Richtung des Objekt Raums für das aktuelle Ray.</span><span class="sxs-lookup"><span data-stu-id="bb247-138">The object-space direction for the current ray.</span></span> |
| [<span data-ttu-id="bb247-139">**ObjectToWorld3x4**</span><span class="sxs-lookup"><span data-stu-id="bb247-139">**ObjectToWorld3x4**</span></span>](objecttoworld3x4.md) | <span data-ttu-id="bb247-140">Eine Matrix zum Transformieren von Objekt Raum in Raum.</span><span class="sxs-lookup"><span data-stu-id="bb247-140">A matrix for transforming from object-space to world-space.</span></span> |
| [<span data-ttu-id="bb247-141">**ObjectToWorld4x3**</span><span class="sxs-lookup"><span data-stu-id="bb247-141">**ObjectToWorld4x3**</span></span>](objecttoworld4x3.md) | <span data-ttu-id="bb247-142">Eine Matrix zum Transformieren von Objekt Raum in Raum.</span><span class="sxs-lookup"><span data-stu-id="bb247-142">A matrix for transforming from object-space to world-space.</span></span> |
| [<span data-ttu-id="bb247-143">**WorldToObject3x4**</span><span class="sxs-lookup"><span data-stu-id="bb247-143">**WorldToObject3x4**</span></span>](worldtoobject3x4.md) | <span data-ttu-id="bb247-144">Eine Matrix zum Transformieren von Welt Raum zu Objekt Raum</span><span class="sxs-lookup"><span data-stu-id="bb247-144">A matrix for transforming from world-space to object-space</span></span> |
| [<span data-ttu-id="bb247-145">**WorldToObject4x3**</span><span class="sxs-lookup"><span data-stu-id="bb247-145">**WorldToObject4x3**</span></span>](worldtoobject4x3.md) | <span data-ttu-id="bb247-146">Eine Matrix zum Transformieren von Welt Raum zu Objekt Raum</span><span class="sxs-lookup"><span data-stu-id="bb247-146">A matrix for transforming from world-space to object-space</span></span> |
### <a name="hit-specific-system-values"></a><span data-ttu-id="bb247-147">Treffer spezifische System Werte</span><span class="sxs-lookup"><span data-stu-id="bb247-147">Hit-specific system values</span></span>

| <span data-ttu-id="bb247-148">Thema</span><span class="sxs-lookup"><span data-stu-id="bb247-148">Topic</span></span> | <span data-ttu-id="bb247-149">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bb247-149">Description</span></span> |
|-|-|
| [<span data-ttu-id="bb247-150">**Hitkind**</span><span class="sxs-lookup"><span data-stu-id="bb247-150">**HitKind**</span></span>](hitkind.md) | <span data-ttu-id="bb247-151">Gibt den Wert zurück, der als **hitkind** -Parameter an Report [**Thread**](reporthit-function.md)übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="bb247-151">Returns the value passed as the **HitKind** parameter to [**ReportHit**](reporthit-function.md).</span></span> |

## <a name="related-topics"></a><span data-ttu-id="bb247-152">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="bb247-152">Related topics</span></span>

* [<span data-ttu-id="bb247-153">Kern Referenz</span><span class="sxs-lookup"><span data-stu-id="bb247-153">Core Reference</span></span>](direct3d-12-core-reference.md)
* [<span data-ttu-id="bb247-154">Referenz für Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="bb247-154">Direct3D 12 Reference</span></span>](direct3d-12-reference.md)
