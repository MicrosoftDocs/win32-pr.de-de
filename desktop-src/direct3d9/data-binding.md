---
description: Verwenden Sie die sashostparametervalue-Auflistung, um die Auflistung von Host Anwendungs Werten sowie deren Typ und Member zu definieren, die für Effekte verfügbar gemacht werden.
ms.assetid: 3fef353d-323a-4cc1-a8c9-2bf154754835
title: Datenbindung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b67305d4acc8a4ed9e0827203e4602db26a99da
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104341539"
---
# <a name="data-binding"></a><span data-ttu-id="3a3aa-103">Datenbindung</span><span class="sxs-lookup"><span data-stu-id="3a3aa-103">Data Binding</span></span>

<span data-ttu-id="3a3aa-104">Verwenden Sie die [sashostparametervalue](#sashostparametervalue-collection) -Auflistung, um die Auflistung von Host Anwendungs Werten sowie deren Typ und Member zu definieren, die für Effekte verfügbar gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="3a3aa-104">Use [SasHostParameterValue Collection](#sashostparametervalue-collection) to define the collection of host application values, as well as their type and members, exposed to effects.</span></span> <span data-ttu-id="3a3aa-105">Verwenden Sie die [sasbindaddress](#sasbindaddress) -Anmerkung in einer Effect-Datei, um einen Effektparameter mit dem entsprechenden Parameter in der Host Anwendung zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="3a3aa-105">Use the [SasBindAddress](#sasbindaddress) annotation in an effect file to associate an effect parameter with its corresponding parameter in the host application.</span></span>

## <a name="sashostparametervalue-collection"></a><span data-ttu-id="3a3aa-106">Sashostparametervalue-Auflistung</span><span class="sxs-lookup"><span data-stu-id="3a3aa-106">SasHostParameterValue Collection</span></span>

<span data-ttu-id="3a3aa-107">Sashostparametervalue wird mithilfe der Effekt Datei Syntax (. fx) definiert.</span><span class="sxs-lookup"><span data-stu-id="3a3aa-107">The SasHostParameterValue is defined using effect file (.fx) syntax.</span></span> <span data-ttu-id="3a3aa-108">Obwohl die Syntax der Effekt Datei Syntax sehr ähnlich ist, gibt es einige Unterschiede.</span><span class="sxs-lookup"><span data-stu-id="3a3aa-108">While the syntax is very similar to the effect file syntax, some differences exist.</span></span> <span data-ttu-id="3a3aa-109">Beispielsweise sind Objekttypen, z. b. Texture2D, Samplers und Zeichen folgen, in tatsächlichen Effekt Dateien ungültig, sind aber im sashostparametervalue gültig.</span><span class="sxs-lookup"><span data-stu-id="3a3aa-109">For example, object types, such as texture2d, samplers, and strings, are not valid in actual effect files, but are valid in the SasHostParameterValue.</span></span> <span data-ttu-id="3a3aa-110">Eine Host Anwendung kann sashostparametervalue in beliebiger Weise implementieren, solange Sie der Beschreibung unten entspricht. die tatsächliche Definition befindet sich in der Include-Datei des dxsas-Standard Effekts ( \[ SDK Root \] /Utilities/Source/SAS/SAS.fxh).</span><span class="sxs-lookup"><span data-stu-id="3a3aa-110">A host application can implement SasHostParameterValue in any way so long as it conforms to the description below; the actual definition is located in the DXSAS standard effect include file (\[SDK Root\]/Utilities/Source/Sas/Sas.fxh).</span></span>

<span data-ttu-id="3a3aa-111">Beachten Sie, dass Arrays in sashostparametervalue, z. b. Lights oder Kameras, eine unbegrenzte Länge aufweisen.</span><span class="sxs-lookup"><span data-stu-id="3a3aa-111">Note that arrays in the SasHostParameterValue such as Lights or Cameras have unbounded length.</span></span> <span data-ttu-id="3a3aa-112">Dies bedeutet, dass Effekte an einen beliebigen Index in diesen Arrays gebunden werden können, und Host Anwendungen müssen sinnvolle Standardwerte in Fällen bereitstellen, in denen kein Anwendungs Wert bereitgestellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="3a3aa-112">This means that effects can bind to any arbitrary index in those arrays and host applications must provide meaningful defaults in the cases where no application value can be provided.</span></span>

<span data-ttu-id="3a3aa-113">Einige Typen und Konstanten müssen in der dxsas-Standard Include definiert werden, wie in der Definition der standardmäßigen Include-Datei angegeben.</span><span class="sxs-lookup"><span data-stu-id="3a3aa-113">Some types and constants are required to be defined in the DXSAS standard include, as noted in the definition of the standard include.</span></span> <span data-ttu-id="3a3aa-114">Dadurch können aggregierte Werte leicht aus dem sashostparametervalue an strukturierte Effektparameter gebunden werden.</span><span class="sxs-lookup"><span data-stu-id="3a3aa-114">This allows effects to easily bind aggregated values from the SasHostParameterValue to structured effect parameters.</span></span>



| <span data-ttu-id="3a3aa-115">Sashostparametervalue-Auflistung</span><span class="sxs-lookup"><span data-stu-id="3a3aa-115">SasHostParameterValue Collection</span></span>    | <span data-ttu-id="3a3aa-116">Typ</span><span class="sxs-lookup"><span data-stu-id="3a3aa-116">Type</span></span>            | <span data-ttu-id="3a3aa-117">Member</span><span class="sxs-lookup"><span data-stu-id="3a3aa-117">Member</span></span>                                       |
|-------------------------------------|-----------------|----------------------------------------------|
| [<span data-ttu-id="3a3aa-118">Time</span><span class="sxs-lookup"><span data-stu-id="3a3aa-118">Time</span></span>](#time)                       | <span data-ttu-id="3a3aa-119">float</span><span class="sxs-lookup"><span data-stu-id="3a3aa-119">float</span></span>           | <span data-ttu-id="3a3aa-120">SAS. time. Now</span><span class="sxs-lookup"><span data-stu-id="3a3aa-120">Sas.Time.Now</span></span>                                 |
|                                     | <span data-ttu-id="3a3aa-121">float</span><span class="sxs-lookup"><span data-stu-id="3a3aa-121">float</span></span>           | <span data-ttu-id="3a3aa-122">SAS. time. Last</span><span class="sxs-lookup"><span data-stu-id="3a3aa-122">Sas.Time.Last</span></span>                                |
|                                     | <span data-ttu-id="3a3aa-123">INT</span><span class="sxs-lookup"><span data-stu-id="3a3aa-123">int</span></span>             | <span data-ttu-id="3a3aa-124">SAS. time. frameNum</span><span class="sxs-lookup"><span data-stu-id="3a3aa-124">Sas.Time.FrameNumber</span></span>                         |
| [<span data-ttu-id="3a3aa-125">Umgebungs Zuordnung</span><span class="sxs-lookup"><span data-stu-id="3a3aa-125">Environment Map</span></span>](#environment-map) | <span data-ttu-id="3a3aa-126">texturecube</span><span class="sxs-lookup"><span data-stu-id="3a3aa-126">textureCUBE</span></span>     | <span data-ttu-id="3a3aa-127">SAS. Umgebungskarte</span><span class="sxs-lookup"><span data-stu-id="3a3aa-127">Sas.EnvironmentMap</span></span>                           |
| [<span data-ttu-id="3a3aa-128">Kamera</span><span class="sxs-lookup"><span data-stu-id="3a3aa-128">Camera</span></span>](#camera)                   | <span data-ttu-id="3a3aa-129">Sascamera</span><span class="sxs-lookup"><span data-stu-id="3a3aa-129">SasCamera</span></span>       | <span data-ttu-id="3a3aa-130">SAS. Camera</span><span class="sxs-lookup"><span data-stu-id="3a3aa-130">Sas.Camera</span></span>                                   |
|                                     | <span data-ttu-id="3a3aa-131">float4x4</span><span class="sxs-lookup"><span data-stu-id="3a3aa-131">float4x4</span></span>        | <span data-ttu-id="3a3aa-132">SAS. Camera. worldum View</span><span class="sxs-lookup"><span data-stu-id="3a3aa-132">Sas.Camera.WorldToView</span></span>                       |
|                                     | <span data-ttu-id="3a3aa-133">float4x4</span><span class="sxs-lookup"><span data-stu-id="3a3aa-133">float4x4</span></span>        | <span data-ttu-id="3a3aa-134">SAS. Camera. Projection</span><span class="sxs-lookup"><span data-stu-id="3a3aa-134">Sas.Camera.Projection</span></span>                        |
|                                     | <span data-ttu-id="3a3aa-135">float2</span><span class="sxs-lookup"><span data-stu-id="3a3aa-135">float2</span></span>          | <span data-ttu-id="3a3aa-136">SAS. Camera. nearfarclipping</span><span class="sxs-lookup"><span data-stu-id="3a3aa-136">Sas.Camera.NearFarClipping</span></span>                   |
| [<span data-ttu-id="3a3aa-137">Hell</span><span class="sxs-lookup"><span data-stu-id="3a3aa-137">Light</span></span>](#light)                     | <span data-ttu-id="3a3aa-138">Sasambientlight</span><span class="sxs-lookup"><span data-stu-id="3a3aa-138">SasAmbientLight</span></span> | <span data-ttu-id="3a3aa-139">AmbientLight \[ ZeroOrMore \] ;</span><span class="sxs-lookup"><span data-stu-id="3a3aa-139">AmbientLight\[ZeroOrMore\];</span></span>                  |
|                                     | <span data-ttu-id="3a3aa-140">INT</span><span class="sxs-lookup"><span data-stu-id="3a3aa-140">int</span></span>             | <span data-ttu-id="3a3aa-141">SAS. numambientlights</span><span class="sxs-lookup"><span data-stu-id="3a3aa-141">Sas.NumAmbientLights</span></span>                         |
|                                     | <span data-ttu-id="3a3aa-142">Sasambientlight</span><span class="sxs-lookup"><span data-stu-id="3a3aa-142">SasAmbientLight</span></span> | <span data-ttu-id="3a3aa-143">DirectionalLight \[ ZeroOrMore \] ;</span><span class="sxs-lookup"><span data-stu-id="3a3aa-143">DirectionalLight\[ZeroOrMore\];</span></span>              |
|                                     | <span data-ttu-id="3a3aa-144">INT</span><span class="sxs-lookup"><span data-stu-id="3a3aa-144">int</span></span>             | <span data-ttu-id="3a3aa-145">SAS. numdirectionallights</span><span class="sxs-lookup"><span data-stu-id="3a3aa-145">Sas.NumDirectionalLights</span></span>                     |
|                                     | <span data-ttu-id="3a3aa-146">Sasambientlight</span><span class="sxs-lookup"><span data-stu-id="3a3aa-146">SasAmbientLight</span></span> | <span data-ttu-id="3a3aa-147">PointLight \[ nullt \] ;</span><span class="sxs-lookup"><span data-stu-id="3a3aa-147">PointLight\[ZeroOrMore\];</span></span>                    |
|                                     | <span data-ttu-id="3a3aa-148">INT</span><span class="sxs-lookup"><span data-stu-id="3a3aa-148">int</span></span>             | <span data-ttu-id="3a3aa-149">SAS. numpointlights</span><span class="sxs-lookup"><span data-stu-id="3a3aa-149">Sas.NumPointLights</span></span>                           |
|                                     | <span data-ttu-id="3a3aa-150">Sasambientlight</span><span class="sxs-lookup"><span data-stu-id="3a3aa-150">SasAmbientLight</span></span> | <span data-ttu-id="3a3aa-151">Spotlight \[ nullt \] ;</span><span class="sxs-lookup"><span data-stu-id="3a3aa-151">SpotLight\[ZeroOrMore\];</span></span>                     |
|                                     | <span data-ttu-id="3a3aa-152">INT</span><span class="sxs-lookup"><span data-stu-id="3a3aa-152">int</span></span>             | <span data-ttu-id="3a3aa-153">SAS. numspotlights</span><span class="sxs-lookup"><span data-stu-id="3a3aa-153">Sas.NumSpotLights</span></span>                            |
| [<span data-ttu-id="3a3aa-154">Shadow</span><span class="sxs-lookup"><span data-stu-id="3a3aa-154">Shadow</span></span>](#shadow)                   | <span data-ttu-id="3a3aa-155">float4x4</span><span class="sxs-lookup"><span data-stu-id="3a3aa-155">float4x4</span></span>        | <span data-ttu-id="3a3aa-156">SAS. Shadow \[ ZeroOrMore \] . Worldschshadow</span><span class="sxs-lookup"><span data-stu-id="3a3aa-156">Sas.Shadow\[ZeroOrMore\].WorldToShadow</span></span>       |
|                                     | <span data-ttu-id="3a3aa-157">texture2D</span><span class="sxs-lookup"><span data-stu-id="3a3aa-157">texture2D</span></span>       | <span data-ttu-id="3a3aa-158">SAS. Shadow \[ ZeroOrMore \] . Shadowmap</span><span class="sxs-lookup"><span data-stu-id="3a3aa-158">Sas.Shadow\[ZeroOrMore\].ShadowMap</span></span>           |
| [<span data-ttu-id="3a3aa-159">Ele</span><span class="sxs-lookup"><span data-stu-id="3a3aa-159">Skeleton</span></span>](#skeleton)               | <span data-ttu-id="3a3aa-160">float4x4</span><span class="sxs-lookup"><span data-stu-id="3a3aa-160">float4x4</span></span>        | <span data-ttu-id="3a3aa-161">SAS. Skeleton. meshtojointtoworld \[ oneOrMore\]</span><span class="sxs-lookup"><span data-stu-id="3a3aa-161">Sas.Skeleton.MeshToJointToWorld\[OneOrMore\]</span></span> |
|                                     | <span data-ttu-id="3a3aa-162">INT</span><span class="sxs-lookup"><span data-stu-id="3a3aa-162">int</span></span>             | <span data-ttu-id="3a3aa-163">SAS. Skeleton. numjoints</span><span class="sxs-lookup"><span data-stu-id="3a3aa-163">Sas.Skeleton.NumJoints</span></span>                       |



 

### <a name="time"></a><span data-ttu-id="3a3aa-164">Time</span><span class="sxs-lookup"><span data-stu-id="3a3aa-164">Time</span></span>

<span data-ttu-id="3a3aa-165">Der Wert für die virtuelle Uhr oder den Uhrzeitwert der Host Anwendung.</span><span class="sxs-lookup"><span data-stu-id="3a3aa-165">The host application's virtual clock or time value.</span></span> <span data-ttu-id="3a3aa-166">Zu den Mitgliedern gehören:</span><span class="sxs-lookup"><span data-stu-id="3a3aa-166">Members include:</span></span>

-   <span data-ttu-id="3a3aa-167">SAS. time. Now: der Wert der virtuellen Uhr der Host Anwendung an dem Punkt, an dem der Effekt gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="3a3aa-167">Sas.Time.Now - the value of the host application virtual clock at the point at which the effect will be rendered.</span></span>
-   <span data-ttu-id="3a3aa-168">SAS. time. Last-der Wert von Now beim vorherigen Rendering.</span><span class="sxs-lookup"><span data-stu-id="3a3aa-168">Sas.Time.Last - the value of Now at the previous render.</span></span>
-   <span data-ttu-id="3a3aa-169">SAS. time. framenumber: der Wert des Leistungs Zählers, der einmal pro gerendertem Frame inkrementiert wird.</span><span class="sxs-lookup"><span data-stu-id="3a3aa-169">Sas.Time.FrameNumber - the counter value that is incremented once per rendered frame.</span></span>

<span data-ttu-id="3a3aa-170">Effekte müssen die Tatsache, dass die Werte dieser Member bei extrem langen Ausführungszeiten möglicherweise umschlossen werden können, ordnungsgemäß behandeln.</span><span class="sxs-lookup"><span data-stu-id="3a3aa-170">Effects must properly handle the fact that the values of these members can potentially wrap around during extremely long execution times.</span></span> <span data-ttu-id="3a3aa-171">Jetzt und Last haben möglicherweise sehr hohe Werte.</span><span class="sxs-lookup"><span data-stu-id="3a3aa-171">Now and Last may have very large values.</span></span>

### <a name="environment-map"></a><span data-ttu-id="3a3aa-172">Umgebungs Zuordnung</span><span class="sxs-lookup"><span data-stu-id="3a3aa-172">Environment Map</span></span>

<span data-ttu-id="3a3aa-173">Eine kubische Umgebungs Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="3a3aa-173">A cubic environment map.</span></span> <span data-ttu-id="3a3aa-174">Host Anwendungen müssen eine gültige cubetextur bereitstellen, wenn ein Effekt versucht, eine Bindung an SAS. Umgebungs Map herzustellen.</span><span class="sxs-lookup"><span data-stu-id="3a3aa-174">Host applications must provide a valid cube texture if an effect attempts to bind to Sas.EnvironmentMap.</span></span>

### <a name="camera"></a><span data-ttu-id="3a3aa-175">Kamera</span><span class="sxs-lookup"><span data-stu-id="3a3aa-175">Camera</span></span>

<span data-ttu-id="3a3aa-176">Die Kamera, die gerade gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="3a3aa-176">The camera currently being rendered.</span></span> <span data-ttu-id="3a3aa-177">Zu den Mitgliedern gehören:</span><span class="sxs-lookup"><span data-stu-id="3a3aa-177">Members include:</span></span>

-   <span data-ttu-id="3a3aa-178">SAS. Camera. worldpoview: die zusammengesetzte World-View-Matrix für die Kamera.</span><span class="sxs-lookup"><span data-stu-id="3a3aa-178">Sas.Camera.WorldToView - the composite world-view matrix for the camera.</span></span>
-   <span data-ttu-id="3a3aa-179">SAS. Camera. Projection: die Projektions Matrix für die Kamera.</span><span class="sxs-lookup"><span data-stu-id="3a3aa-179">Sas.Camera.Projection - the projection matrix for the camera.</span></span>
-   <span data-ttu-id="3a3aa-180">SAS. Camera. nearfarclipping: die Werte der Near-und Far-Clipping-Ebenen.</span><span class="sxs-lookup"><span data-stu-id="3a3aa-180">Sas.Camera.NearFarClipping - the values of the near and far clipping planes.</span></span>

### <a name="light"></a><span data-ttu-id="3a3aa-181">Hell</span><span class="sxs-lookup"><span data-stu-id="3a3aa-181">Light</span></span>

<span data-ttu-id="3a3aa-182">Ein oder mehrere Szenen Leuchten.</span><span class="sxs-lookup"><span data-stu-id="3a3aa-182">One or more scene lights.</span></span> <span data-ttu-id="3a3aa-183">Die Sammlung von Lichtern wird als Array deklariert, wobei Folgendes gilt:</span><span class="sxs-lookup"><span data-stu-id="3a3aa-183">The collection of lights is declared as an array where:</span></span>

-   <span data-ttu-id="3a3aa-184">Farbe: eine RGB-Farbe.</span><span class="sxs-lookup"><span data-stu-id="3a3aa-184">Color - an RGB color.</span></span> <span data-ttu-id="3a3aa-185">Der Standardwert ist (0,0,0).</span><span class="sxs-lookup"><span data-stu-id="3a3aa-185">The default value is (0,0,0).</span></span>
-   <span data-ttu-id="3a3aa-186">Richtung: die helle Richtung.</span><span class="sxs-lookup"><span data-stu-id="3a3aa-186">Direction - the light direction.</span></span> <span data-ttu-id="3a3aa-187">Der Standardwert ist (0,0,0).</span><span class="sxs-lookup"><span data-stu-id="3a3aa-187">The default value is (0,0,0).</span></span>
-   <span data-ttu-id="3a3aa-188">Bereich: die Entfernung vom Licht, in der die Lichtstrahlen keine Auswirkung auf die Szene haben.</span><span class="sxs-lookup"><span data-stu-id="3a3aa-188">Range - the distance from the light where the light rays have no effect on the scene.</span></span> <span data-ttu-id="3a3aa-189">Der Standardwert ist 0.</span><span class="sxs-lookup"><span data-stu-id="3a3aa-189">The default value is 0.</span></span>
-   <span data-ttu-id="3a3aa-190">Der TA-der innere Kegelwinkel eines Spotlight, gemessen im Bogenmaß.</span><span class="sxs-lookup"><span data-stu-id="3a3aa-190">Theta - the inner cone angle of a spotlight, measured in radians.</span></span> <span data-ttu-id="3a3aa-191">Der Standardwert ist 0.</span><span class="sxs-lookup"><span data-stu-id="3a3aa-191">The default value is 0.</span></span>
-   <span data-ttu-id="3a3aa-192">Phi: der äußere Kegelwinkel eines Spotlight, gemessen im Bogenmaß.</span><span class="sxs-lookup"><span data-stu-id="3a3aa-192">Phi - the outer cone angle of a spotlight, measured in radians.</span></span> <span data-ttu-id="3a3aa-193">Der Standardwert ist 0.</span><span class="sxs-lookup"><span data-stu-id="3a3aa-193">The default value is 0.</span></span>

<span data-ttu-id="3a3aa-194">Die Anzahl der Beleuchtung muss auf die Anzahl der an das zugeordneten Array gebundenen Lichterfest gelegt werden.</span><span class="sxs-lookup"><span data-stu-id="3a3aa-194">The number of lights must be set to the number of lights bound into the associated array.</span></span> <span data-ttu-id="3a3aa-195">Effekte können die Anzahl der Lichter ignorieren und an ein beliebiges Element eines der hellen Arrays binden.</span><span class="sxs-lookup"><span data-stu-id="3a3aa-195">Effects can choose to ignore the number of lights and bind to any element of one of the light arrays.</span></span> <span data-ttu-id="3a3aa-196">Daher müssen Host Anwendungen eine gültige Bindung für Elemente bereitstellen, die über die Anzahl der Lichter im Array hinausgehen.</span><span class="sxs-lookup"><span data-stu-id="3a3aa-196">Therefore, host applications must provide a valid binding for elements beyond the number of lights in the array.</span></span>

<span data-ttu-id="3a3aa-197">ZeroOrMore impliziert, dass das Array eine beliebige Anzahl von Elementen aufweisen kann.</span><span class="sxs-lookup"><span data-stu-id="3a3aa-197">ZeroOrMore implies that the array may have any number of elements.</span></span>

### <a name="shadow"></a><span data-ttu-id="3a3aa-198">Shadow</span><span class="sxs-lookup"><span data-stu-id="3a3aa-198">Shadow</span></span>

<span data-ttu-id="3a3aa-199">Schatten Puffer, die aus folgendem bestehen:</span><span class="sxs-lookup"><span data-stu-id="3a3aa-199">Shadow buffers which consists of:</span></span>

-   <span data-ttu-id="3a3aa-200">Worldteshadow: ein Array von Matrizen.</span><span class="sxs-lookup"><span data-stu-id="3a3aa-200">WorldToShadow - an array of matrices.</span></span>
-   <span data-ttu-id="3a3aa-201">Shadowmap: eine 2D-Textur Datei.</span><span class="sxs-lookup"><span data-stu-id="3a3aa-201">ShadowMap - a 2D texture file.</span></span>

<span data-ttu-id="3a3aa-202">Nullen impliziert, dass das Array eine beliebige Anzahl von Elementen aufweisen kann (Null bedeutet ein leeres Array).</span><span class="sxs-lookup"><span data-stu-id="3a3aa-202">ZeroOrMore implies that the array may have any number of elements (zero means an empty array).</span></span>

<span data-ttu-id="3a3aa-203">Ein Effekt würde einen Sampler wie folgt deklarieren:</span><span class="sxs-lookup"><span data-stu-id="3a3aa-203">An effect would declare a sampler as follows:</span></span>


```
texture2D Shadow 
<
  string SasBindAddress = "Sas.Shadow[0].ShadowMap";
>;

sampler ShadowSampler = shadow_sampler(Shadow);
```



### <a name="skeleton"></a><span data-ttu-id="3a3aa-204">Ele</span><span class="sxs-lookup"><span data-stu-id="3a3aa-204">Skeleton</span></span>

<span data-ttu-id="3a3aa-205">Der Satz von Frames, der das derzeit Renderingobjekt bildet.</span><span class="sxs-lookup"><span data-stu-id="3a3aa-205">The set of frames that compose the currently rendering object.</span></span> <span data-ttu-id="3a3aa-206">Frame Beispiele sind Knochen und Transformationen.</span><span class="sxs-lookup"><span data-stu-id="3a3aa-206">Frame examples are bones and transforms.</span></span> <span data-ttu-id="3a3aa-207">Dies schließt Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="3a3aa-207">This includes:</span></span>

-   <span data-ttu-id="3a3aa-208">Meshtjointum World: ein Array von Matrizen.</span><span class="sxs-lookup"><span data-stu-id="3a3aa-208">MeshToJointToWorld - an array of matrices.</span></span>
-   <span data-ttu-id="3a3aa-209">Numjoints: die Anzahl von Gelenken im Gerüst.</span><span class="sxs-lookup"><span data-stu-id="3a3aa-209">NumJoints - the number of joints in the skeleton.</span></span>

<span data-ttu-id="3a3aa-210">OneOrMore impliziert, dass das Array über mindestens ein verfügt und eine beliebige Anzahl von Elementen enthalten kann.</span><span class="sxs-lookup"><span data-stu-id="3a3aa-210">OneOrMore implies that the array has at least one and may contain any number of elements.</span></span>

<span data-ttu-id="3a3aa-211">Die Definition unterstützt sowohl feste als auch häufte Mesh-Objekte, die denselben Satz von [sashostparametervalue](#sashostparametervalue-collection) -Auflistungs Werten mit unterschiedlicher Interpretation verwenden.</span><span class="sxs-lookup"><span data-stu-id="3a3aa-211">The definition supports both rigid and skinned mesh objects using the same set of [SasHostParameterValue Collection](#sashostparametervalue-collection) values with different interpretation.</span></span>

## <a name="sasbindaddress"></a><span data-ttu-id="3a3aa-212">Sasbindaddress</span><span class="sxs-lookup"><span data-stu-id="3a3aa-212">SasBindAddress</span></span>

<span data-ttu-id="3a3aa-213">Diese Anmerkung wird am Anfang einer Effekt Datei hinzugefügt, um einen Effektparameter mit dem entsprechenden Parameter, der in der [sashostparametervalue](#sashostparametervalue-collection)-Auflistung definiert ist, zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="3a3aa-213">This annotation is added to the top of an effect file to associate an effect parameter with its corresponding parameter defined in the [SasHostParameterValue Collection](#sashostparametervalue-collection).</span></span> <span data-ttu-id="3a3aa-214">Die-Anmerkung wird wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="3a3aa-214">The annotation is declared like this:</span></span>


```
string SasBindAddress = "SasHostParameterValue";
```



<span data-ttu-id="3a3aa-215">In diesem Beispiel wird die Effekt-Weltmatrix an die meshyjointyworld-Matrix gebunden:</span><span class="sxs-lookup"><span data-stu-id="3a3aa-215">This example binds the effect world matrix to the MeshToJointToWorld matrix:</span></span>


```
float4x3 World
<
  string SasBindAddress = "Sas.Skeleton.MeshToJointToWorld[0]";
>;
```



<span data-ttu-id="3a3aa-216">Diese Anmerkung weist die Host Anwendung an, dass Sie den Wert der "Effect World Matrix" mithilfe der Daten in der meshonjointyworld-Matrix festlegen muss.</span><span class="sxs-lookup"><span data-stu-id="3a3aa-216">This annotation tells the host application that it needs to set the value of the effect world matrix using the data in the MeshToJointToWorld matrix.</span></span>

<span data-ttu-id="3a3aa-217">Die Syntax BIND Address Anmerkung wurde so definiert, dass Sie mit der Syntax, die von [**ID3DXEffect**](id3dxeffect.md) verwendet wird, um Effektparameter zu erhalten und festzulegen.</span><span class="sxs-lookup"><span data-stu-id="3a3aa-217">The bind address annotation syntax was defined to be very similar with the syntax used by [**ID3DXEffect**](id3dxeffect.md) to get and set effect parameters.</span></span> <span data-ttu-id="3a3aa-218">Der einzige Unterschied zwischen der dxsas-Grammatik und der **ID3DXEffect** -Methode ist das Hinzufügen des Sternchen-Index Tokens.</span><span class="sxs-lookup"><span data-stu-id="3a3aa-218">The only difference between the DXSAS grammar and **ID3DXEffect** methods is the addition of the asterisk index token.</span></span> <span data-ttu-id="3a3aa-219">Hier ist ein weiteres Beispiel für die Verwendung des Sternchen-Indexes:</span><span class="sxs-lookup"><span data-stu-id="3a3aa-219">Here is another example using the asterisk index:</span></span>


```
float3 LightColors[6]
<
  string SasBindAddress = "Sas.Light[*].Color";
>;
```



<span data-ttu-id="3a3aa-220">Das Sternchen-Index Token gibt an, dass alle Elemente des jeweiligen Host-Wert Arrays (in diesem Fall die Farbe) im zugeordneten Parameter gebunden werden sollen.</span><span class="sxs-lookup"><span data-stu-id="3a3aa-220">The asterisk index token denotes that all elements of the particular host envirnmant value array (color in this case) should be bound in the associated parameter.</span></span> <span data-ttu-id="3a3aa-221">Mit mehreren Sternchen-Index Token können Effekte an unter Elemente eines Arrays von Strukturen gebunden werden, ohne dass die gesamte Struktur selbst gebunden werden muss.</span><span class="sxs-lookup"><span data-stu-id="3a3aa-221">Multiple asterisk index tokens allow effects to bind to sub-elements of an array of structures without the need to bind the entire structure itself.</span></span> <span data-ttu-id="3a3aa-222">In diesem Beispiel werden die Farbwerte der ersten sechs Lichter an einen Effektparameter gebunden.</span><span class="sxs-lookup"><span data-stu-id="3a3aa-222">This example binds the color values of the first six lights to an effect parameter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3a3aa-223">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3a3aa-223">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3a3aa-224">DirectX-Standard Anmerkungen und Semantik Referenz</span><span class="sxs-lookup"><span data-stu-id="3a3aa-224">DirectX Standard Annotations and Semantics Reference</span></span>](dx9-graphics-reference-effects-dxsas.md)
</dt> </dl>

 

 



