---
title: Texturobjekt
description: In Direct3D 10 geben Sie die Sampler und Texturen unabhängig voneinander an. Textursstichproben werden mithilfe eines Texturobjekts mit Vorlagen implementiert. Dieses Templated-Texture-Objekt hat ein bestimmtes Format, gibt einen bestimmten Typ zurück und implementiert mehrere Methoden.
ms.assetid: e8cb483a-d831-4942-b6fe-61dd5edb1813
keywords:
- Texturobjekt HLSL
topic_type:
- apiref
api_name:
- Texture Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d1881ba4a88e97e978e2646c92d276bb9763ffd
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/09/2021
ms.locfileid: "111825770"
---
# <a name="texture-object"></a><span data-ttu-id="e454e-105">Texturobjekt</span><span class="sxs-lookup"><span data-stu-id="e454e-105">Texture Object</span></span>

<span data-ttu-id="e454e-106">In Direct3D 10 geben Sie die Sampler und Texturen unabhängig voneinander an. Textursstichproben werden mithilfe eines Texturobjekts mit Vorlagen implementiert.</span><span class="sxs-lookup"><span data-stu-id="e454e-106">In Direct3D 10, you specify the samplers and textures independently; texture sampling is implemented by using a templated-texture object.</span></span> <span data-ttu-id="e454e-107">Dieses Templated-Texture-Objekt hat ein bestimmtes Format, gibt einen bestimmten Typ zurück und implementiert mehrere Methoden.</span><span class="sxs-lookup"><span data-stu-id="e454e-107">This templated-texture object has a specific format, returns a specific type, and implements several methods.</span></span>

<span data-ttu-id="e454e-108">Unterschiede zwischen Direct3D9 und Direct3D10:</span><span class="sxs-lookup"><span data-stu-id="e454e-108">Differences between Direct3D9 and Direct3D10:</span></span>

- <span data-ttu-id="e454e-109">In Direct3D 9 sind Sampler an bestimmte Texturen gebunden.</span><span class="sxs-lookup"><span data-stu-id="e454e-109">In Direct3D 9, samplers are bound to specific textures.</span></span>
- <span data-ttu-id="e454e-110">In Direct3D 10 sind Texturen und Sampler unabhängige Objekte.</span><span class="sxs-lookup"><span data-stu-id="e454e-110">In Direct3D 10, textures and samplers are independent objects.</span></span> <span data-ttu-id="e454e-111">Jedes Templated-Texture-Objekt implementiert Textur-Samplingmethoden, die sowohl die Textur als auch den Sampler als Eingabeparameter verwenden.</span><span class="sxs-lookup"><span data-stu-id="e454e-111">Each templated-texture object implements texture sampling methods that take both the texture and the sampler as input parameters.</span></span>



 

<span data-ttu-id="e454e-112">Hier ist die Syntax zum Erstellen aller Texturobjekte (mit Ausnahme von Objekten mit mehrerenAmpeln).</span><span class="sxs-lookup"><span data-stu-id="e454e-112">Here is the syntax for creating all texture objects (except multisampled objects).</span></span>



| <span data-ttu-id="e454e-113">\[ < *Object1-Typname;* > \] </span><span class="sxs-lookup"><span data-stu-id="e454e-113">Object1 \[<*Type*>\] *Name*;</span></span> |
|------------------------------------|



 

<span data-ttu-id="e454e-114">Für Mehrfachbeispielobjekte (Texture2DMS und Texture2DMSArray) muss die Texturgröße explizit angegeben und als Anzahl von Stichproben ausgedrückt werden.</span><span class="sxs-lookup"><span data-stu-id="e454e-114">Multisampled objects (Texture2DMS and Texture2DMSArray) require the texture size to be explicitly stated and expressed as the number of samples.</span></span>



| <span data-ttu-id="e454e-115">\[ < *Object2-Typ, Name der* > \] *Beispiele;*</span><span class="sxs-lookup"><span data-stu-id="e454e-115">Object2 \[<*Type, Samples*>\] *Name*;</span></span> |
|---------------------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="e454e-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="e454e-116">Parameters</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e454e-117">Element</span><span class="sxs-lookup"><span data-stu-id="e454e-117">Item</span></span></th>
<th><span data-ttu-id="e454e-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e454e-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e454e-119"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Objekt</em></span><span class="sxs-lookup"><span data-stu-id="e454e-119"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Object</em></span></span><br/></td>
<td><span data-ttu-id="e454e-120">Ein Texturobjekt.</span><span class="sxs-lookup"><span data-stu-id="e454e-120">A texture object.</span></span> <span data-ttu-id="e454e-121">Muss einer der folgenden Typen sein.</span><span class="sxs-lookup"><span data-stu-id="e454e-121">Must be one of the following types.</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e454e-122">Object1-Typ</span><span class="sxs-lookup"><span data-stu-id="e454e-122">Object1 Type</span></span></th>
<th><span data-ttu-id="e454e-123">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e454e-123">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e454e-124">Buffer</span><span class="sxs-lookup"><span data-stu-id="e454e-124">Buffer</span></span></td>
<td><span data-ttu-id="e454e-125">Buffer</span><span class="sxs-lookup"><span data-stu-id="e454e-125">Buffer</span></span> </td>
</tr>
<tr class="even">
<td><span data-ttu-id="e454e-126">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e454e-126">Texture1D</span></span></td>
<td><span data-ttu-id="e454e-127">1D-Textur</span><span class="sxs-lookup"><span data-stu-id="e454e-127">1D texture</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e454e-128">Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="e454e-128">Texture1DArray</span></span></td>
<td><span data-ttu-id="e454e-129">Array von 1D-Texturen</span><span class="sxs-lookup"><span data-stu-id="e454e-129">Array of 1D textures</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e454e-130">Texture2D</span><span class="sxs-lookup"><span data-stu-id="e454e-130">Texture2D</span></span></td>
<td><span data-ttu-id="e454e-131">2D-Textur</span><span class="sxs-lookup"><span data-stu-id="e454e-131">2D texture</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e454e-132">Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="e454e-132">Texture2DArray</span></span></td>
<td><span data-ttu-id="e454e-133">Array von 2D-Texturen</span><span class="sxs-lookup"><span data-stu-id="e454e-133">Array of 2D textures</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e454e-134">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e454e-134">Texture3D</span></span></td>
<td><span data-ttu-id="e454e-135">3D-Textur</span><span class="sxs-lookup"><span data-stu-id="e454e-135">3D texture</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e454e-136">TextureCube</span><span class="sxs-lookup"><span data-stu-id="e454e-136">TextureCube</span></span></td>
<td><span data-ttu-id="e454e-137">Cubetextur</span><span class="sxs-lookup"><span data-stu-id="e454e-137">Cube texture</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e454e-138">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="e454e-138">TextureCubeArray</span></span>  </td>
<td><span data-ttu-id="e454e-139">Array von Cubetexturen</span><span class="sxs-lookup"><span data-stu-id="e454e-139">Array of cube textures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e454e-140">Object2-Typ</span><span class="sxs-lookup"><span data-stu-id="e454e-140">Object2 Type</span></span></td>
<td><span data-ttu-id="e454e-141">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e454e-141">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e454e-142">Texture2DMS</span><span class="sxs-lookup"><span data-stu-id="e454e-142">Texture2DMS</span></span></td>
<td><span data-ttu-id="e454e-143">2D-Textur mit mehrerenAmpeln</span><span class="sxs-lookup"><span data-stu-id="e454e-143">2D multisampled texture</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e454e-144">Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="e454e-144">Texture2DMSArray</span></span></td>
<td><span data-ttu-id="e454e-145">Array von 2D-Texturen mit mehrerenAmpeln</span><span class="sxs-lookup"><span data-stu-id="e454e-145">Array of 2D multisampled textures</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<ol>
<li><span data-ttu-id="e454e-146">Der Puffertyp unterstützt die meisten Texturobjektmethoden außer GetDimensions.</span><span class="sxs-lookup"><span data-stu-id="e454e-146">The Buffer type supports most texture object methods except GetDimensions.</span></span></li>
<li><span data-ttu-id="e454e-147">TextureCubeArray ist im Shadermodell 4.1 oder höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e454e-147">TextureCubeArray is available in shader model 4.1 or higher.</span></span></li>
<li><span data-ttu-id="e454e-148">Shadermodell 4.1 ist in Direct3D 10.1 oder höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e454e-148">Shader model 4.1 is available in Direct3D 10.1 or higher.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e454e-149"><span id="Type"></span><span id="type"></span><span id="TYPE"></span><em>Typ</em></span><span class="sxs-lookup"><span data-stu-id="e454e-149"><span id="Type"></span><span id="type"></span><span id="TYPE"></span><em>Type</em></span></span></p></td>
<td><p><span data-ttu-id="e454e-150">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="e454e-150">Optional.</span></span> <span data-ttu-id="e454e-151">Jeder <a href="dx-graphics-hlsl-scalar.md">skalare HLSL-Typ oder</a> <a href="dx-graphics-hlsl-vector.md"><strong>Vektor-HLSL-Typ,</strong></a>umgeben von eckigen Klammern.</span><span class="sxs-lookup"><span data-stu-id="e454e-151">Any <a href="dx-graphics-hlsl-scalar.md">scalar HLSL type</a> or <a href="dx-graphics-hlsl-vector.md"><strong>vector HLSL type</strong></a>, surrounded by angle brackets.</span></span> <span data-ttu-id="e454e-152">Der Standardtyp ist <strong>float4.</strong></span><span class="sxs-lookup"><span data-stu-id="e454e-152">The default type is <strong>float4</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e454e-153"><span id="Name"></span><span id="name"></span><span id="NAME"></span><em>Namen</em></span><span class="sxs-lookup"><span data-stu-id="e454e-153"><span id="Name"></span><span id="name"></span><span id="NAME"></span><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="e454e-154">Eine ASCII-Zeichenfolge, die den Texturobjektnamen angibt.</span><span class="sxs-lookup"><span data-stu-id="e454e-154">An ASCII string that specifies the texture object name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e454e-155"><span id="Samples"></span><span id="samples"></span><span id="SAMPLES"></span><em>Proben</em></span><span class="sxs-lookup"><span data-stu-id="e454e-155"><span id="Samples"></span><span id="samples"></span><span id="SAMPLES"></span><em>Samples</em></span></span></p></td>
<td><p><span data-ttu-id="e454e-156">Die Anzahl der Stichproben (bereiche zwischen 1 und 128).</span><span class="sxs-lookup"><span data-stu-id="e454e-156">The number of samples (ranges between 1 and 128).</span></span></p></td>
</tr>
</tbody>
</table>



 

## <a name="example-1"></a><span data-ttu-id="e454e-157">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e454e-157">Example 1</span></span>

<span data-ttu-id="e454e-158">Hier ist ein Beispiel für das Deklarieren eines Texturobjekts.</span><span class="sxs-lookup"><span data-stu-id="e454e-158">Here is an example of declaring a texture object.</span></span>


```
Texture2D <float4> MyTex;

Texture2DMS <float4, 128> MyMSTex;
```



## <a name="texture-object-methods"></a><span data-ttu-id="e454e-159">Texturobjektmethoden</span><span class="sxs-lookup"><span data-stu-id="e454e-159">Texture Object Methods</span></span>

<span data-ttu-id="e454e-160">Jedes Texturobjekt implementiert bestimmte Methoden. Hier ist die Tabelle, in der alle Methoden aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="e454e-160">Each texture object implements certain methods; here's the table that lists all of the methods.</span></span> <span data-ttu-id="e454e-161">Informationen dazu, welche Objekte diese Methode verwenden können, finden Sie auf der Referenzseite für die einzelnen Methoden.</span><span class="sxs-lookup"><span data-stu-id="e454e-161">See the reference page for each method to see what objects can use that method.</span></span>



| <span data-ttu-id="e454e-162">Texturmethode</span><span class="sxs-lookup"><span data-stu-id="e454e-162">Texture Method</span></span>                                                                     | <span data-ttu-id="e454e-163">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e454e-163">Description</span></span>                                                                                                       | <span data-ttu-id="e454e-164">vs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e454e-164">vs\_4\_0</span></span> | <span data-ttu-id="e454e-165">vs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="e454e-165">vs\_4\_1</span></span>  | <span data-ttu-id="e454e-166">ps \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e454e-166">ps\_4\_0</span></span> | <span data-ttu-id="e454e-167">ps \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="e454e-167">ps\_4\_1</span></span>  | <span data-ttu-id="e454e-168">gs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e454e-168">gs\_4\_0</span></span> | <span data-ttu-id="e454e-169">gs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="e454e-169">gs\_4\_1</span></span>  |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|----------|-----------|----------|-----------|----------|-----------|
| [<span data-ttu-id="e454e-170">CalculateLevelOfDetail</span><span class="sxs-lookup"><span data-stu-id="e454e-170">CalculateLevelOfDetail</span></span>](dx-graphics-hlsl-to-calculate-lod.md)                    | <span data-ttu-id="e454e-171">Berechnen Sie die LOD, und geben Sie ein geklammertes Ergebnis zurück.</span><span class="sxs-lookup"><span data-stu-id="e454e-171">Calculate the LOD, return a clamped result.</span></span>                                                                       |          |           |          | <span data-ttu-id="e454e-172">x</span><span class="sxs-lookup"><span data-stu-id="e454e-172">x</span></span>         |          |           |
| [<span data-ttu-id="e454e-173">CalculateLevelOfDetailUnclamped</span><span class="sxs-lookup"><span data-stu-id="e454e-173">CalculateLevelOfDetailUnclamped</span></span>](dx-graphics-hlsl-to-calculate-lod-unclamped.md) | <span data-ttu-id="e454e-174">Berechnen Sie die LOD, und geben Sie ein ergebnislos zurück.</span><span class="sxs-lookup"><span data-stu-id="e454e-174">Calculate the LOD, return an unclamped result.</span></span>                                                                    |          |           |          | <span data-ttu-id="e454e-175">x</span><span class="sxs-lookup"><span data-stu-id="e454e-175">x</span></span>         |          |           |
| [<span data-ttu-id="e454e-176">versammeln</span><span class="sxs-lookup"><span data-stu-id="e454e-176">Gather</span></span>](dx-graphics-hlsl-to-gather.md)                                           | <span data-ttu-id="e454e-177">Ruft die vier Stichproben (nur rote Komponente) ab, die für die bilineare Interpolation beim Sampling einer Textur verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e454e-177">Gets the four samples (red component only) that would be used for bilinear interpolation when sampling a texture.</span></span> |          | <span data-ttu-id="e454e-178">x</span><span class="sxs-lookup"><span data-stu-id="e454e-178">x</span></span>         |          | <span data-ttu-id="e454e-179">x</span><span class="sxs-lookup"><span data-stu-id="e454e-179">x</span></span>         |          | <span data-ttu-id="e454e-180">x</span><span class="sxs-lookup"><span data-stu-id="e454e-180">x</span></span>         |
| [<span data-ttu-id="e454e-181">GetDimensions</span><span class="sxs-lookup"><span data-stu-id="e454e-181">GetDimensions</span></span>](dx-graphics-hlsl-to-getdimensions.md)                             | <span data-ttu-id="e454e-182">Gibt die Texturdimension für eine angegebene Mipmapebene an.</span><span class="sxs-lookup"><span data-stu-id="e454e-182">Get the texture dimension for a specified mipmap level.</span></span>                                                           | <span data-ttu-id="e454e-183">x</span><span class="sxs-lookup"><span data-stu-id="e454e-183">x</span></span>        | <span data-ttu-id="e454e-184">x</span><span class="sxs-lookup"><span data-stu-id="e454e-184">x</span></span>         | <span data-ttu-id="e454e-185">x</span><span class="sxs-lookup"><span data-stu-id="e454e-185">x</span></span>        | <span data-ttu-id="e454e-186">x</span><span class="sxs-lookup"><span data-stu-id="e454e-186">x</span></span>         | <span data-ttu-id="e454e-187">x</span><span class="sxs-lookup"><span data-stu-id="e454e-187">x</span></span>        | <span data-ttu-id="e454e-188">x</span><span class="sxs-lookup"><span data-stu-id="e454e-188">x</span></span>         |
| [<span data-ttu-id="e454e-189">GetDimensions (MultiSample)</span><span class="sxs-lookup"><span data-stu-id="e454e-189">GetDimensions (MultiSample)</span></span>](dx-graphics-hlsl-to-getdimensions.md)               | <span data-ttu-id="e454e-190">Gibt die Texturdimension für eine angegebene Mipmapebene an.</span><span class="sxs-lookup"><span data-stu-id="e454e-190">Get the texture dimension for a specified mipmap level.</span></span>                                                           |          | <span data-ttu-id="e454e-191">x</span><span class="sxs-lookup"><span data-stu-id="e454e-191">x</span></span>         |          | <span data-ttu-id="e454e-192">x</span><span class="sxs-lookup"><span data-stu-id="e454e-192">x</span></span>         |          | <span data-ttu-id="e454e-193">x</span><span class="sxs-lookup"><span data-stu-id="e454e-193">x</span></span>         |
| [<span data-ttu-id="e454e-194">GetSamplePosition</span><span class="sxs-lookup"><span data-stu-id="e454e-194">GetSamplePosition</span></span>](dx-graphics-hlsl-to-get-sample-position.md)                   | <span data-ttu-id="e454e-195">Gibt die Position des angegebenen Beispiels an.</span><span class="sxs-lookup"><span data-stu-id="e454e-195">Get the position of the specified sample.</span></span>                                                                         |          | <span data-ttu-id="e454e-196">x</span><span class="sxs-lookup"><span data-stu-id="e454e-196">x</span></span>         |          | <span data-ttu-id="e454e-197">x</span><span class="sxs-lookup"><span data-stu-id="e454e-197">x</span></span>         |          | <span data-ttu-id="e454e-198">x</span><span class="sxs-lookup"><span data-stu-id="e454e-198">x</span></span>         |
| [<span data-ttu-id="e454e-199">Load</span><span class="sxs-lookup"><span data-stu-id="e454e-199">Load</span></span>](dx-graphics-hlsl-to-load.md)                                               | <span data-ttu-id="e454e-200">Laden von Daten ohne Filterung oder Stichprobenentnahme.</span><span class="sxs-lookup"><span data-stu-id="e454e-200">Load data without any filtering or sampling.</span></span>                                                                      | <span data-ttu-id="e454e-201">x</span><span class="sxs-lookup"><span data-stu-id="e454e-201">x</span></span>        | <span data-ttu-id="e454e-202">x</span><span class="sxs-lookup"><span data-stu-id="e454e-202">x</span></span>         | <span data-ttu-id="e454e-203">x</span><span class="sxs-lookup"><span data-stu-id="e454e-203">x</span></span>        | <span data-ttu-id="e454e-204">x</span><span class="sxs-lookup"><span data-stu-id="e454e-204">x</span></span>         | <span data-ttu-id="e454e-205">x</span><span class="sxs-lookup"><span data-stu-id="e454e-205">x</span></span>        | <span data-ttu-id="e454e-206">x</span><span class="sxs-lookup"><span data-stu-id="e454e-206">x</span></span>         |
| [<span data-ttu-id="e454e-207">Laden (Multisample)</span><span class="sxs-lookup"><span data-stu-id="e454e-207">Load (Multisample)</span></span>](dx-graphics-hlsl-to-load.md)                                 | <span data-ttu-id="e454e-208">Laden von Daten ohne Filterung oder Stichprobenentnahme.</span><span class="sxs-lookup"><span data-stu-id="e454e-208">Load data without any filtering or sampling.</span></span>                                                                      |          | <span data-ttu-id="e454e-209">x</span><span class="sxs-lookup"><span data-stu-id="e454e-209">x</span></span>         | <span data-ttu-id="e454e-210">x</span><span class="sxs-lookup"><span data-stu-id="e454e-210">x</span></span>        | <span data-ttu-id="e454e-211">x</span><span class="sxs-lookup"><span data-stu-id="e454e-211">x</span></span>         |          | <span data-ttu-id="e454e-212">x</span><span class="sxs-lookup"><span data-stu-id="e454e-212">x</span></span>         |
| [<span data-ttu-id="e454e-213">Beispiel</span><span class="sxs-lookup"><span data-stu-id="e454e-213">Sample</span></span>](dx-graphics-hlsl-to-sample.md)                                           | <span data-ttu-id="e454e-214">Beispiel für eine Textur.</span><span class="sxs-lookup"><span data-stu-id="e454e-214">Sample a texture.</span></span>                                                                                                 |          |           | <span data-ttu-id="e454e-215">x</span><span class="sxs-lookup"><span data-stu-id="e454e-215">x</span></span>        | <span data-ttu-id="e454e-216">x</span><span class="sxs-lookup"><span data-stu-id="e454e-216">x</span></span>         |          |           |
| [<span data-ttu-id="e454e-217">SampleBias</span><span class="sxs-lookup"><span data-stu-id="e454e-217">SampleBias</span></span>](dx-graphics-hlsl-to-samplebias.md)                                   | <span data-ttu-id="e454e-218">Sample a texture, after applying the bias value to the mipmap level.</span><span class="sxs-lookup"><span data-stu-id="e454e-218">Sample a texture, after applying the bias value to the mipmap level.</span></span>                                              |          |           | <span data-ttu-id="e454e-219">x</span><span class="sxs-lookup"><span data-stu-id="e454e-219">x</span></span>        | <span data-ttu-id="e454e-220">x</span><span class="sxs-lookup"><span data-stu-id="e454e-220">x</span></span>         |          |           |
| [<span data-ttu-id="e454e-221">SampleCmp</span><span class="sxs-lookup"><span data-stu-id="e454e-221">SampleCmp</span></span>](dx-graphics-hlsl-to-samplecmp.md)                                     | <span data-ttu-id="e454e-222">Beispiel für eine Textur mithilfe eines Vergleichswerts zum Ablehnen von Stichproben.</span><span class="sxs-lookup"><span data-stu-id="e454e-222">Sample a texture, using a comparison value to reject samples.</span></span>                                                     |          |           | <span data-ttu-id="e454e-223">x</span><span class="sxs-lookup"><span data-stu-id="e454e-223">x</span></span>        | <span data-ttu-id="e454e-224">x</span><span class="sxs-lookup"><span data-stu-id="e454e-224">x</span></span>         |          |           |
| [<span data-ttu-id="e454e-225">SampleCmpLevelZero</span><span class="sxs-lookup"><span data-stu-id="e454e-225">SampleCmpLevelZero</span></span>](dx-graphics-hlsl-to-samplecmplevelzero.md)                   | <span data-ttu-id="e454e-226">Beispiel für eine Textur (nur Mipmap-Ebene 0) mithilfe eines Vergleichswerts zum Ablehnen von Stichproben.</span><span class="sxs-lookup"><span data-stu-id="e454e-226">Sample a texture (mipmap level 0 only), using a comparison value to reject samples.</span></span>                               | <span data-ttu-id="e454e-227">x</span><span class="sxs-lookup"><span data-stu-id="e454e-227">x</span></span>        | <span data-ttu-id="e454e-228">x</span><span class="sxs-lookup"><span data-stu-id="e454e-228">x</span></span>         | <span data-ttu-id="e454e-229">x</span><span class="sxs-lookup"><span data-stu-id="e454e-229">x</span></span>        | <span data-ttu-id="e454e-230">x</span><span class="sxs-lookup"><span data-stu-id="e454e-230">x</span></span>         | <span data-ttu-id="e454e-231">x</span><span class="sxs-lookup"><span data-stu-id="e454e-231">x</span></span>        | <span data-ttu-id="e454e-232">x</span><span class="sxs-lookup"><span data-stu-id="e454e-232">x</span></span>         |
| [<span data-ttu-id="e454e-233">SampleGrad</span><span class="sxs-lookup"><span data-stu-id="e454e-233">SampleGrad</span></span>](dx-graphics-hlsl-to-samplegrad.md)                                   | <span data-ttu-id="e454e-234">Beispiel für eine Textur mithilfe eines Farbverlaufs, um die Berechnung der Stichprobenposition zu beeinflussen.</span><span class="sxs-lookup"><span data-stu-id="e454e-234">Sample a texture using a gradient to influence the way the sample location is calculated.</span></span>                         | <span data-ttu-id="e454e-235">x</span><span class="sxs-lookup"><span data-stu-id="e454e-235">x</span></span>        | <span data-ttu-id="e454e-236">x</span><span class="sxs-lookup"><span data-stu-id="e454e-236">x</span></span>         | <span data-ttu-id="e454e-237">x</span><span class="sxs-lookup"><span data-stu-id="e454e-237">x</span></span>        | <span data-ttu-id="e454e-238">x</span><span class="sxs-lookup"><span data-stu-id="e454e-238">x</span></span>         | <span data-ttu-id="e454e-239">x</span><span class="sxs-lookup"><span data-stu-id="e454e-239">x</span></span>        | <span data-ttu-id="e454e-240">x</span><span class="sxs-lookup"><span data-stu-id="e454e-240">x</span></span>         |
| [<span data-ttu-id="e454e-241">SampleLevel</span><span class="sxs-lookup"><span data-stu-id="e454e-241">SampleLevel</span></span>](dx-graphics-hlsl-to-samplelevel.md)                                 | <span data-ttu-id="e454e-242">Beispiel für eine Textur auf der angegebenen Mipmapebene.</span><span class="sxs-lookup"><span data-stu-id="e454e-242">Sample a texture on the specified mipmap level.</span></span>                                                                   | <span data-ttu-id="e454e-243">x</span><span class="sxs-lookup"><span data-stu-id="e454e-243">x</span></span>        | <span data-ttu-id="e454e-244">x</span><span class="sxs-lookup"><span data-stu-id="e454e-244">x</span></span>         | <span data-ttu-id="e454e-245">x</span><span class="sxs-lookup"><span data-stu-id="e454e-245">x</span></span>        | <span data-ttu-id="e454e-246">x</span><span class="sxs-lookup"><span data-stu-id="e454e-246">x</span></span>         | <span data-ttu-id="e454e-247">x</span><span class="sxs-lookup"><span data-stu-id="e454e-247">x</span></span>        | <span data-ttu-id="e454e-248">x</span><span class="sxs-lookup"><span data-stu-id="e454e-248">x</span></span>         |



 

### <a name="return-type"></a><span data-ttu-id="e454e-249">Rückgabetyp</span><span class="sxs-lookup"><span data-stu-id="e454e-249">Return Type</span></span>

<span data-ttu-id="e454e-250">Der Rückgabetyp einer Texturobjektmethode ist float4, sofern nicht anders angegeben, mit Ausnahme der Multisampled-Texturobjekte mit Antialiasing, die immer den angegebenen Typ und die angegebene Stichprobenanzahl benötigen.</span><span class="sxs-lookup"><span data-stu-id="e454e-250">The return type of a texture object method is float4 unless specified otherwise, with the exception of the multisampled anti-aliased texture objects that always need the type and sample count specified.</span></span> <span data-ttu-id="e454e-251">Der Rückgabetyp ist identisch mit dem Texturressourcentyp ([**DXGI \_ FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)).</span><span class="sxs-lookup"><span data-stu-id="e454e-251">The return type is the same as the texture resource type ([**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)).</span></span> <span data-ttu-id="e454e-252">Anders ausgedrückt: Dies kann einer der folgenden Typen sein.</span><span class="sxs-lookup"><span data-stu-id="e454e-252">In other words, it can be any of the following types.</span></span>



| <span data-ttu-id="e454e-253">Typ</span><span class="sxs-lookup"><span data-stu-id="e454e-253">Type</span></span>                       | <span data-ttu-id="e454e-254">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e454e-254">Description</span></span>                                                                                                                                                             |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e454e-255">float</span><span class="sxs-lookup"><span data-stu-id="e454e-255">float</span></span>                      | <span data-ttu-id="e454e-256">32-Bit-Gleitkommazahl (siehe [Gleitkommaregeln](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules) für Unterschiede zu IEEE float)</span><span class="sxs-lookup"><span data-stu-id="e454e-256">32-bit float (see [Floating-Point Rules](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules) for differences from IEEE float)</span></span>                            |
| <span data-ttu-id="e454e-257">INT</span><span class="sxs-lookup"><span data-stu-id="e454e-257">int</span></span>                        | <span data-ttu-id="e454e-258">32-Bit-Ganzzahl mit Vorzeichen</span><span class="sxs-lookup"><span data-stu-id="e454e-258">32-bit signed integer</span></span>                                                                                                                                                   |
| <span data-ttu-id="e454e-259">unsigned int</span><span class="sxs-lookup"><span data-stu-id="e454e-259">unsigned int</span></span>               | <span data-ttu-id="e454e-260">32-Bit-Ganzzahl ohne Vorzeichen</span><span class="sxs-lookup"><span data-stu-id="e454e-260">32-bit unsigned integer</span></span>                                                                                                                                                 |
| <span data-ttu-id="e454e-261">snorm</span><span class="sxs-lookup"><span data-stu-id="e454e-261">snorm</span></span>                      | <span data-ttu-id="e454e-262">32-Bit-Gleitkommazahl im Bereich -1 bis einschließlich 1 (siehe [Gleitkommaregeln](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules) für Unterschiede zu IEEE float)</span><span class="sxs-lookup"><span data-stu-id="e454e-262">32-bit float in range -1 to 1 inclusive (see [Floating-Point Rules](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules) for differences from IEEE float)</span></span> |
| <span data-ttu-id="e454e-263">unorm</span><span class="sxs-lookup"><span data-stu-id="e454e-263">unorm</span></span>                      | <span data-ttu-id="e454e-264">32-Bit-Gleitkommazahl im Bereich von 0 bis einschließlich 1 (siehe [Gleitkommaregeln](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules) für Unterschiede zu IEEE float)</span><span class="sxs-lookup"><span data-stu-id="e454e-264">32-bit float in range 0 to 1 inclusive (see [Floating-Point Rules](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules) for differences from IEEE float)</span></span>  |
| <span data-ttu-id="e454e-265">beliebiger Texturtyp oder Struktur</span><span class="sxs-lookup"><span data-stu-id="e454e-265">any texture type or struct</span></span> | <span data-ttu-id="e454e-266">Die Anzahl der zurückgegebenen Komponenten muss zwischen 1 und 3 (einschließlich) liegen.</span><span class="sxs-lookup"><span data-stu-id="e454e-266">The number of components returned must be between 1 and 3 inclusive.</span></span>                                                                                                    |



 

<span data-ttu-id="e454e-267">Darüber hinaus kann der Rückgabetyp ein beliebiger Texturtyp sein, einschließlich einer -Struktur, aber er muss kleiner als 4 Komponenten sein, z. B. ein float1-Typ, der eine Komponente zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="e454e-267">In addition, the return type can be any texture type including a structure but, it must be less than 4 components such as a float1 type which returns one component.</span></span>

## <a name="default-values-for-missing-components-in-a-texture"></a><span data-ttu-id="e454e-268">Standardwerte für fehlende Komponenten in einer Textur</span><span class="sxs-lookup"><span data-stu-id="e454e-268">Default Values for Missing Components in a Texture</span></span>

<span data-ttu-id="e454e-269">Der Standardwert für fehlende Komponenten in einem Texturressourcentyp ist 0 (null) für jede Komponente mit Ausnahme der Alphakomponente (A). Der Standardwert für das fehlende A ist 1.</span><span class="sxs-lookup"><span data-stu-id="e454e-269">The default value for missing components in a texture resource type is zero for any component except the alpha component (A); the default value for the missing A is one.</span></span> <span data-ttu-id="e454e-270">Die Art und Weise, wie diese im Shader angezeigt wird, hängt vom Texturressourcentyp ab.</span><span class="sxs-lookup"><span data-stu-id="e454e-270">The way that this one appears to the shader depends on the texture resource type.</span></span> <span data-ttu-id="e454e-271">Sie hat die Form der ersten typierten Komponente, die tatsächlich im Texturressourcentyp vorhanden ist (beginnend von links in RGBA-Reihenfolge).</span><span class="sxs-lookup"><span data-stu-id="e454e-271">It takes the form of the first typed component that is actually present in the texture resource type (starting from the left in RGBA order).</span></span> <span data-ttu-id="e454e-272">Wenn dieses Formular UNORM oder FLOAT ist, ist der Standardwert für das fehlende A 1,0f.</span><span class="sxs-lookup"><span data-stu-id="e454e-272">If this form is UNORM or FLOAT, the default value for the missing A is 1.0f.</span></span> <span data-ttu-id="e454e-273">Wenn das Formular SINT oder UINT ist, wird der Standardwert für das fehlende A 0x1.</span><span class="sxs-lookup"><span data-stu-id="e454e-273">If the form is SINT or UINT, the default value for the missing A is 0x1.</span></span>

<span data-ttu-id="e454e-274">Wenn ein Shader beispielsweise den [**Ressourcentyp DXGI \_ FORMAT \_ R24 \_ UNORM \_ X8 \_ TYPELESS**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) liest, Die Standardwerte für G und B sind 0 (null), und der Standardwert für A ist 1,0f. Wenn ein Shader den [**DXGI FORMAT \_ \_ R16G16 \_ UINT-Texturressourcentyp**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) liest, ist der Standardwert für B 0 (null), und der Standardwert für A ist 0x00000001. Wenn ein Shader den [**DXGI FORMAT \_ \_ R16 \_ SINT-Texturressourcentyp**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) liest, sind die Standardwerte für G und B null, und der Standardwert für A ist 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="e454e-274">For example, when a shader reads the [**DXGI\_FORMAT\_R24\_UNORM\_X8\_TYPELESS**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) texture resource type, the default values for G and B are zero and the default value for A is 1.0f; when a shader reads the [**DXGI\_FORMAT\_R16G16\_UINT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) texture resource type, the default value for B is zero and the default value for A is 0x00000001; when a shader reads the [**DXGI\_FORMAT\_R16\_SINT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) texture resource type, the default values for G and B are zero and the default value for A is 0x00000001.</span></span>

## <a name="example-2"></a><span data-ttu-id="e454e-275">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="e454e-275">Example 2</span></span>

<span data-ttu-id="e454e-276">Im Folgenden finden Sie ein Beispiel für texturiertes Sampling mithilfe einer Texturmethode.</span><span class="sxs-lookup"><span data-stu-id="e454e-276">Here is an example of texture sampling using a texture method.</span></span>


```
sampler MySamp;
Texture2D <float4> MyTex;
 
float4 main( float2 TexCoords[2] : TEXCOORD ) : SV_Target
{
    return MyTex.Sample( MySamp, TexCoords[0] ));
}
```



## <a name="minimum-shader-model"></a><span data-ttu-id="e454e-277">Minimales Shadermodell</span><span class="sxs-lookup"><span data-stu-id="e454e-277">Minimum Shader Model</span></span>

<span data-ttu-id="e454e-278">Dieses Objekt wird in den folgenden Shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e454e-278">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="e454e-279">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="e454e-279">Shader Model</span></span>                                                        | <span data-ttu-id="e454e-280">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="e454e-280">Supported</span></span> |
|---------------------------------------------------------------------|-----------|
| <span data-ttu-id="e454e-281">[Shadermodell 4](dx-graphics-hlsl-sm4.md) und höher– Shadermodelle</span><span class="sxs-lookup"><span data-stu-id="e454e-281">[Shader Model 4](dx-graphics-hlsl-sm4.md) and higher shader models</span></span> | <span data-ttu-id="e454e-282">ja</span><span class="sxs-lookup"><span data-stu-id="e454e-282">yes</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="e454e-283">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e454e-283">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e454e-284">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="e454e-284">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

