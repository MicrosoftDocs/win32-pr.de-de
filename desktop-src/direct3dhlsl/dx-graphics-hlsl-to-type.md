---
title: Texture-Objekt
description: In Direct3D 10 geben Sie die Samplern und Texturen unabhängig an. Textur Stichproben werden mithilfe eines Vorlagen basierten Textur Objekts implementiert. Dieses auf Vorlagen basierende Textur Objekt hat ein bestimmtes Format, gibt einen bestimmten Typ zurück und implementiert mehrere Methoden.
ms.assetid: e8cb483a-d831-4942-b6fe-61dd5edb1813
keywords:
- Textur Objekt HLSL
topic_type:
- apiref
api_name:
- Texture Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b075ddc1f659923efd03d9fe9d21ee3238e656e9
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/10/2021
ms.locfileid: "104219411"
---
# <a name="texture-object"></a><span data-ttu-id="998e6-105">Texture-Objekt</span><span class="sxs-lookup"><span data-stu-id="998e6-105">Texture Object</span></span>

<span data-ttu-id="998e6-106">In Direct3D 10 geben Sie die Samplern und Texturen unabhängig an. Textur Stichproben werden mithilfe eines Vorlagen basierten Textur Objekts implementiert.</span><span class="sxs-lookup"><span data-stu-id="998e6-106">In Direct3D 10, you specify the samplers and textures independently; texture sampling is implemented by using a templated-texture object.</span></span> <span data-ttu-id="998e6-107">Dieses auf Vorlagen basierende Textur Objekt hat ein bestimmtes Format, gibt einen bestimmten Typ zurück und implementiert mehrere Methoden.</span><span class="sxs-lookup"><span data-stu-id="998e6-107">This templated-texture object has a specific format, returns a specific type, and implements several methods.</span></span>




|                                                                                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="998e6-108">Unterschiede zwischen von Direct3D9 und Direct3D10: in Direct3D 9 sind Samplern an bestimmte Texturen gebunden. in Direct3D 10 sind Texturen und Samplern unabhängige Objekte.</span><span class="sxs-lookup"><span data-stu-id="998e6-108">Differences between Direct3D9 and Direct3D10: In Direct3D 9, samplers are bound to specific textures; in Direct3D 10, textures and samplers are independent objects.</span></span> <span data-ttu-id="998e6-109">Jedes Vorlagen Struktur Objekt implementiert Textur-Samplingmethoden, die sowohl die Textur als auch den Sampler als Eingabeparameter annehmen.</span><span class="sxs-lookup"><span data-stu-id="998e6-109">Each templated-texture object implements texture sampling methods that take both the texture and the sampler as input parameters.</span></span><br/> |



 

<span data-ttu-id="998e6-110">Hier ist die Syntax zum Erstellen aller Textur Objekte (mit Ausnahme von Multisampling-Objekten).</span><span class="sxs-lookup"><span data-stu-id="998e6-110">Here is the syntax for creating all texture objects (except multisampled objects).</span></span>



| <span data-ttu-id="998e6-111">Objekt1 \[ <  > \] *Typname*;</span><span class="sxs-lookup"><span data-stu-id="998e6-111">Object1 \[<*Type*>\] *Name*;</span></span> |
|------------------------------------|



 

<span data-ttu-id="998e6-112">Multisampling-Objekte (Texture2DMS und Texture2DMSArray) erfordern, dass die Textur Größe explizit angegeben und als Anzahl von Stichproben ausgedrückt wird.</span><span class="sxs-lookup"><span data-stu-id="998e6-112">Multisampled objects (Texture2DMS and Texture2DMSArray) require the texture size to be explicitly stated and expressed as the number of samples.</span></span>



| <span data-ttu-id="998e6-113">Objekt2 \[ < *Type, Samples* > \] *Name*;</span><span class="sxs-lookup"><span data-stu-id="998e6-113">Object2 \[<*Type, Samples*>\] *Name*;</span></span> |
|---------------------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="998e6-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="998e6-114">Parameters</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="998e6-115">Element</span><span class="sxs-lookup"><span data-stu-id="998e6-115">Item</span></span></th>
<th><span data-ttu-id="998e6-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="998e6-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="998e6-117"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Objekt</em></span><span class="sxs-lookup"><span data-stu-id="998e6-117"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Object</em></span></span><br/></td>
<td><span data-ttu-id="998e6-118">Ein Textur Objekt.</span><span class="sxs-lookup"><span data-stu-id="998e6-118">A texture object.</span></span> <span data-ttu-id="998e6-119">Muss einer der folgenden Typen sein:</span><span class="sxs-lookup"><span data-stu-id="998e6-119">Must be one of the following types.</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="998e6-120">Objekt1-Typ</span><span class="sxs-lookup"><span data-stu-id="998e6-120">Object1 Type</span></span></th>
<th><span data-ttu-id="998e6-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="998e6-121">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="998e6-122">Buffer</span><span class="sxs-lookup"><span data-stu-id="998e6-122">Buffer</span></span></td>
<td><span data-ttu-id="998e6-123">Buffer</span><span class="sxs-lookup"><span data-stu-id="998e6-123">Buffer</span></span> </td>
</tr>
<tr class="even">
<td><span data-ttu-id="998e6-124">Texture1D</span><span class="sxs-lookup"><span data-stu-id="998e6-124">Texture1D</span></span></td>
<td><span data-ttu-id="998e6-125">1D-Textur</span><span class="sxs-lookup"><span data-stu-id="998e6-125">1D texture</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="998e6-126">Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="998e6-126">Texture1DArray</span></span></td>
<td><span data-ttu-id="998e6-127">Array von 1D-Texturen</span><span class="sxs-lookup"><span data-stu-id="998e6-127">Array of 1D textures</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="998e6-128">Texture2D</span><span class="sxs-lookup"><span data-stu-id="998e6-128">Texture2D</span></span></td>
<td><span data-ttu-id="998e6-129">2D-Textur</span><span class="sxs-lookup"><span data-stu-id="998e6-129">2D texture</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="998e6-130">Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="998e6-130">Texture2DArray</span></span></td>
<td><span data-ttu-id="998e6-131">Array von 2D-Texturen</span><span class="sxs-lookup"><span data-stu-id="998e6-131">Array of 2D textures</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="998e6-132">Texture3D</span><span class="sxs-lookup"><span data-stu-id="998e6-132">Texture3D</span></span></td>
<td><span data-ttu-id="998e6-133">3D-Textur</span><span class="sxs-lookup"><span data-stu-id="998e6-133">3D texture</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="998e6-134">TextureCube</span><span class="sxs-lookup"><span data-stu-id="998e6-134">TextureCube</span></span></td>
<td><span data-ttu-id="998e6-135">Cube-Textur</span><span class="sxs-lookup"><span data-stu-id="998e6-135">Cube texture</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="998e6-136">Texturecubearray</span><span class="sxs-lookup"><span data-stu-id="998e6-136">TextureCubeArray</span></span>  </td>
<td><span data-ttu-id="998e6-137">Array von Cube-Texturen</span><span class="sxs-lookup"><span data-stu-id="998e6-137">Array of cube textures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="998e6-138">Objekt2-Typ</span><span class="sxs-lookup"><span data-stu-id="998e6-138">Object2 Type</span></span></td>
<td><span data-ttu-id="998e6-139">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="998e6-139">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="998e6-140">Texture2DMS</span><span class="sxs-lookup"><span data-stu-id="998e6-140">Texture2DMS</span></span></td>
<td><span data-ttu-id="998e6-141">2D-Textur mit Multisampling</span><span class="sxs-lookup"><span data-stu-id="998e6-141">2D multisampled texture</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="998e6-142">Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="998e6-142">Texture2DMSArray</span></span></td>
<td><span data-ttu-id="998e6-143">Array von 2D-Multisampling-Texturen</span><span class="sxs-lookup"><span data-stu-id="998e6-143">Array of 2D multisampled textures</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<ol>
<li><span data-ttu-id="998e6-144">Der Puffertyp unterstützt die meisten Textur Objektmethoden außer GetDimensions.</span><span class="sxs-lookup"><span data-stu-id="998e6-144">The Buffer type supports most texture object methods except GetDimensions.</span></span></li>
<li><span data-ttu-id="998e6-145">Texturecubearray ist im Shader-Modell 4,1 oder höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="998e6-145">TextureCubeArray is available in shader model 4.1 or higher.</span></span></li>
<li><span data-ttu-id="998e6-146">Das Shader-Modell 4,1 ist in Direct3D 10,1 oder höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="998e6-146">Shader model 4.1 is available in Direct3D 10.1 or higher.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="998e6-147"><span id="Type"></span><span id="type"></span><span id="TYPE"></span><em>Sorte</em></span><span class="sxs-lookup"><span data-stu-id="998e6-147"><span id="Type"></span><span id="type"></span><span id="TYPE"></span><em>Type</em></span></span></p></td>
<td><p><span data-ttu-id="998e6-148">Optional.</span><span class="sxs-lookup"><span data-stu-id="998e6-148">Optional.</span></span> <span data-ttu-id="998e6-149">Alle <a href="dx-graphics-hlsl-scalar.md">skalaren HLSL-Typen</a> oder <a href="dx-graphics-hlsl-vector.md"><strong>Vektor-HLSL-Typen</strong></a>, umgeben von spitzen Klammern.</span><span class="sxs-lookup"><span data-stu-id="998e6-149">Any <a href="dx-graphics-hlsl-scalar.md">scalar HLSL type</a> or <a href="dx-graphics-hlsl-vector.md"><strong>vector HLSL type</strong></a>, surrounded by angle brackets.</span></span> <span data-ttu-id="998e6-150">Der Standardtyp ist <strong>float4</strong>.</span><span class="sxs-lookup"><span data-stu-id="998e6-150">The default type is <strong>float4</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="998e6-151"><span id="Name"></span><span id="name"></span><span id="NAME"></span><em>Benennen</em></span><span class="sxs-lookup"><span data-stu-id="998e6-151"><span id="Name"></span><span id="name"></span><span id="NAME"></span><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="998e6-152">Eine ASCII-Zeichenfolge, die den Textur Objektnamen angibt.</span><span class="sxs-lookup"><span data-stu-id="998e6-152">An ASCII string that specifies the texture object name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="998e6-153"><span id="Samples"></span><span id="samples"></span><span id="SAMPLES"></span><em>Stich</em></span><span class="sxs-lookup"><span data-stu-id="998e6-153"><span id="Samples"></span><span id="samples"></span><span id="SAMPLES"></span><em>Samples</em></span></span></p></td>
<td><p><span data-ttu-id="998e6-154">Die Anzahl der Stichproben (Bereiche zwischen 1 und 128).</span><span class="sxs-lookup"><span data-stu-id="998e6-154">The number of samples (ranges between 1 and 128).</span></span></p></td>
</tr>
</tbody>
</table>



 

## <a name="example-1"></a><span data-ttu-id="998e6-155">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="998e6-155">Example 1</span></span>

<span data-ttu-id="998e6-156">Im folgenden finden Sie ein Beispiel für das Deklarieren eines Textur Objekts.</span><span class="sxs-lookup"><span data-stu-id="998e6-156">Here is an example of declaring a texture object.</span></span>


```
Texture2D <float4> MyTex;

Texture2DMS <float4, 128> MyMSTex;
```



## <a name="texture-object-methods"></a><span data-ttu-id="998e6-157">Textur Objektmethoden</span><span class="sxs-lookup"><span data-stu-id="998e6-157">Texture Object Methods</span></span>

<span data-ttu-id="998e6-158">Jedes Textur Objekt implementiert bestimmte Methoden. Hier ist die Tabelle, in der alle Methoden aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="998e6-158">Each texture object implements certain methods; here's the table that lists all of the methods.</span></span> <span data-ttu-id="998e6-159">Auf der Referenzseite für jede Methode finden Sie Informationen dazu, welche Objekte diese Methode verwenden können.</span><span class="sxs-lookup"><span data-stu-id="998e6-159">See the reference page for each method to see what objects can use that method.</span></span>



| <span data-ttu-id="998e6-160">Texture-Methode</span><span class="sxs-lookup"><span data-stu-id="998e6-160">Texture Method</span></span>                                                                     | <span data-ttu-id="998e6-161">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="998e6-161">Description</span></span>                                                                                                       | <span data-ttu-id="998e6-162">vs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="998e6-162">vs\_4\_0</span></span> | <span data-ttu-id="998e6-163">vs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="998e6-163">vs\_4\_1</span></span>  | <span data-ttu-id="998e6-164">PS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="998e6-164">ps\_4\_0</span></span> | <span data-ttu-id="998e6-165">PS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="998e6-165">ps\_4\_1</span></span>  | <span data-ttu-id="998e6-166">GS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="998e6-166">gs\_4\_0</span></span> | <span data-ttu-id="998e6-167">GS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="998e6-167">gs\_4\_1</span></span>  |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|----------|-----------|----------|-----------|----------|-----------|
| [<span data-ttu-id="998e6-168">Calculatelevelof-Detail</span><span class="sxs-lookup"><span data-stu-id="998e6-168">CalculateLevelOfDetail</span></span>](dx-graphics-hlsl-to-calculate-lod.md)                    | <span data-ttu-id="998e6-169">Berechnen Sie das Lod, und geben Sie ein gespanntes Ergebnis zurück.</span><span class="sxs-lookup"><span data-stu-id="998e6-169">Calculate the LOD, return a clamped result.</span></span>                                                                       |          |           |          | <span data-ttu-id="998e6-170">x</span><span class="sxs-lookup"><span data-stu-id="998e6-170">x</span></span>         |          |           |
| [<span data-ttu-id="998e6-171">Calculatelevelof detailunklamed</span><span class="sxs-lookup"><span data-stu-id="998e6-171">CalculateLevelOfDetailUnclamped</span></span>](dx-graphics-hlsl-to-calculate-lod-unclamped.md) | <span data-ttu-id="998e6-172">Berechnen Sie das Lod, und geben Sie ein nicht angehaltene Ergebnis zurück.</span><span class="sxs-lookup"><span data-stu-id="998e6-172">Calculate the LOD, return an unclamped result.</span></span>                                                                    |          |           |          | <span data-ttu-id="998e6-173">x</span><span class="sxs-lookup"><span data-stu-id="998e6-173">x</span></span>         |          |           |
| [<span data-ttu-id="998e6-174">Informieren</span><span class="sxs-lookup"><span data-stu-id="998e6-174">Gather</span></span>](dx-graphics-hlsl-to-gather.md)                                           | <span data-ttu-id="998e6-175">Ruft die vier Stichproben (nur rote Komponente) ab, die bei der Stichprobenentnahme einer Textur für die bilineare interpolung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="998e6-175">Gets the four samples (red component only) that would be used for bilinear interpolation when sampling a texture.</span></span> |          | <span data-ttu-id="998e6-176">x</span><span class="sxs-lookup"><span data-stu-id="998e6-176">x</span></span>         |          | <span data-ttu-id="998e6-177">x</span><span class="sxs-lookup"><span data-stu-id="998e6-177">x</span></span>         |          | <span data-ttu-id="998e6-178">x</span><span class="sxs-lookup"><span data-stu-id="998e6-178">x</span></span>         |
| [<span data-ttu-id="998e6-179">GetDimensions</span><span class="sxs-lookup"><span data-stu-id="998e6-179">GetDimensions</span></span>](dx-graphics-hlsl-to-getdimensions.md)                             | <span data-ttu-id="998e6-180">Die Textur Dimension für eine angegebene MipMap-Ebene wird abgerufen.</span><span class="sxs-lookup"><span data-stu-id="998e6-180">Get the texture dimension for a specified mipmap level.</span></span>                                                           | <span data-ttu-id="998e6-181">x</span><span class="sxs-lookup"><span data-stu-id="998e6-181">x</span></span>        | <span data-ttu-id="998e6-182">x</span><span class="sxs-lookup"><span data-stu-id="998e6-182">x</span></span>         | <span data-ttu-id="998e6-183">x</span><span class="sxs-lookup"><span data-stu-id="998e6-183">x</span></span>        | <span data-ttu-id="998e6-184">x</span><span class="sxs-lookup"><span data-stu-id="998e6-184">x</span></span>         | <span data-ttu-id="998e6-185">x</span><span class="sxs-lookup"><span data-stu-id="998e6-185">x</span></span>        | <span data-ttu-id="998e6-186">x</span><span class="sxs-lookup"><span data-stu-id="998e6-186">x</span></span>         |
| [<span data-ttu-id="998e6-187">GetDimensions (Multisample)</span><span class="sxs-lookup"><span data-stu-id="998e6-187">GetDimensions (MultiSample)</span></span>](dx-graphics-hlsl-to-getdimensions.md)               | <span data-ttu-id="998e6-188">Die Textur Dimension für eine angegebene MipMap-Ebene wird abgerufen.</span><span class="sxs-lookup"><span data-stu-id="998e6-188">Get the texture dimension for a specified mipmap level.</span></span>                                                           |          | <span data-ttu-id="998e6-189">x</span><span class="sxs-lookup"><span data-stu-id="998e6-189">x</span></span>         |          | <span data-ttu-id="998e6-190">x</span><span class="sxs-lookup"><span data-stu-id="998e6-190">x</span></span>         |          | <span data-ttu-id="998e6-191">x</span><span class="sxs-lookup"><span data-stu-id="998e6-191">x</span></span>         |
| [<span data-ttu-id="998e6-192">Getsampleposition</span><span class="sxs-lookup"><span data-stu-id="998e6-192">GetSamplePosition</span></span>](dx-graphics-hlsl-to-get-sample-position.md)                   | <span data-ttu-id="998e6-193">Gibt die Position des angegebenen Beispiels an.</span><span class="sxs-lookup"><span data-stu-id="998e6-193">Get the position of the specified sample.</span></span>                                                                         |          | <span data-ttu-id="998e6-194">x</span><span class="sxs-lookup"><span data-stu-id="998e6-194">x</span></span>         |          | <span data-ttu-id="998e6-195">x</span><span class="sxs-lookup"><span data-stu-id="998e6-195">x</span></span>         |          | <span data-ttu-id="998e6-196">x</span><span class="sxs-lookup"><span data-stu-id="998e6-196">x</span></span>         |
| [<span data-ttu-id="998e6-197">Load</span><span class="sxs-lookup"><span data-stu-id="998e6-197">Load</span></span>](dx-graphics-hlsl-to-load.md)                                               | <span data-ttu-id="998e6-198">Laden von Daten ohne filtern oder Sampling.</span><span class="sxs-lookup"><span data-stu-id="998e6-198">Load data without any filtering or sampling.</span></span>                                                                      | <span data-ttu-id="998e6-199">x</span><span class="sxs-lookup"><span data-stu-id="998e6-199">x</span></span>        | <span data-ttu-id="998e6-200">x</span><span class="sxs-lookup"><span data-stu-id="998e6-200">x</span></span>         | <span data-ttu-id="998e6-201">x</span><span class="sxs-lookup"><span data-stu-id="998e6-201">x</span></span>        | <span data-ttu-id="998e6-202">x</span><span class="sxs-lookup"><span data-stu-id="998e6-202">x</span></span>         | <span data-ttu-id="998e6-203">x</span><span class="sxs-lookup"><span data-stu-id="998e6-203">x</span></span>        | <span data-ttu-id="998e6-204">x</span><span class="sxs-lookup"><span data-stu-id="998e6-204">x</span></span>         |
| [<span data-ttu-id="998e6-205">Load (Multisample)</span><span class="sxs-lookup"><span data-stu-id="998e6-205">Load (Multisample)</span></span>](dx-graphics-hlsl-to-load.md)                                 | <span data-ttu-id="998e6-206">Laden von Daten ohne filtern oder Sampling.</span><span class="sxs-lookup"><span data-stu-id="998e6-206">Load data without any filtering or sampling.</span></span>                                                                      |          | <span data-ttu-id="998e6-207">x</span><span class="sxs-lookup"><span data-stu-id="998e6-207">x</span></span>         | <span data-ttu-id="998e6-208">x</span><span class="sxs-lookup"><span data-stu-id="998e6-208">x</span></span>        | <span data-ttu-id="998e6-209">x</span><span class="sxs-lookup"><span data-stu-id="998e6-209">x</span></span>         |          | <span data-ttu-id="998e6-210">x</span><span class="sxs-lookup"><span data-stu-id="998e6-210">x</span></span>         |
| [<span data-ttu-id="998e6-211">Beispiel</span><span class="sxs-lookup"><span data-stu-id="998e6-211">Sample</span></span>](dx-graphics-hlsl-to-sample.md)                                           | <span data-ttu-id="998e6-212">Beispiel für eine Textur.</span><span class="sxs-lookup"><span data-stu-id="998e6-212">Sample a texture.</span></span>                                                                                                 |          |           | <span data-ttu-id="998e6-213">x</span><span class="sxs-lookup"><span data-stu-id="998e6-213">x</span></span>        | <span data-ttu-id="998e6-214">x</span><span class="sxs-lookup"><span data-stu-id="998e6-214">x</span></span>         |          |           |
| [<span data-ttu-id="998e6-215">Samplebias</span><span class="sxs-lookup"><span data-stu-id="998e6-215">SampleBias</span></span>](dx-graphics-hlsl-to-samplebias.md)                                   | <span data-ttu-id="998e6-216">Beispiel für eine Textur, nachdem der Wert "Bias" auf die MipMap-Ebene angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="998e6-216">Sample a texture, after applying the bias value to the mipmap level.</span></span>                                              |          |           | <span data-ttu-id="998e6-217">x</span><span class="sxs-lookup"><span data-stu-id="998e6-217">x</span></span>        | <span data-ttu-id="998e6-218">x</span><span class="sxs-lookup"><span data-stu-id="998e6-218">x</span></span>         |          |           |
| [<span data-ttu-id="998e6-219">Samplecmp</span><span class="sxs-lookup"><span data-stu-id="998e6-219">SampleCmp</span></span>](dx-graphics-hlsl-to-samplecmp.md)                                     | <span data-ttu-id="998e6-220">Beispiel für eine Textur mit einem Vergleichswert zum ablehnen von Beispielen.</span><span class="sxs-lookup"><span data-stu-id="998e6-220">Sample a texture, using a comparison value to reject samples.</span></span>                                                     |          |           | <span data-ttu-id="998e6-221">x</span><span class="sxs-lookup"><span data-stu-id="998e6-221">x</span></span>        | <span data-ttu-id="998e6-222">x</span><span class="sxs-lookup"><span data-stu-id="998e6-222">x</span></span>         |          |           |
| [<span data-ttu-id="998e6-223">Samplecmplevelzero</span><span class="sxs-lookup"><span data-stu-id="998e6-223">SampleCmpLevelZero</span></span>](dx-graphics-hlsl-to-samplecmplevelzero.md)                   | <span data-ttu-id="998e6-224">Beispiel für eine Textur (nur MipMap-Ebene 0) unter Verwendung eines Vergleichs Werts zum ablehnen von Beispielen.</span><span class="sxs-lookup"><span data-stu-id="998e6-224">Sample a texture (mipmap level 0 only), using a comparison value to reject samples.</span></span>                               | <span data-ttu-id="998e6-225">x</span><span class="sxs-lookup"><span data-stu-id="998e6-225">x</span></span>        | <span data-ttu-id="998e6-226">x</span><span class="sxs-lookup"><span data-stu-id="998e6-226">x</span></span>         | <span data-ttu-id="998e6-227">x</span><span class="sxs-lookup"><span data-stu-id="998e6-227">x</span></span>        | <span data-ttu-id="998e6-228">x</span><span class="sxs-lookup"><span data-stu-id="998e6-228">x</span></span>         | <span data-ttu-id="998e6-229">x</span><span class="sxs-lookup"><span data-stu-id="998e6-229">x</span></span>        | <span data-ttu-id="998e6-230">x</span><span class="sxs-lookup"><span data-stu-id="998e6-230">x</span></span>         |
| [<span data-ttu-id="998e6-231">Samplegrad</span><span class="sxs-lookup"><span data-stu-id="998e6-231">SampleGrad</span></span>](dx-graphics-hlsl-to-samplegrad.md)                                   | <span data-ttu-id="998e6-232">Beispiel für eine Textur mit einem Farbverlauf, um die Art und Weise zu beeinflussen, wie der Beispiel Speicherort berechnet</span><span class="sxs-lookup"><span data-stu-id="998e6-232">Sample a texture using a gradient to influence the way the sample location is calculated.</span></span>                         | <span data-ttu-id="998e6-233">x</span><span class="sxs-lookup"><span data-stu-id="998e6-233">x</span></span>        | <span data-ttu-id="998e6-234">x</span><span class="sxs-lookup"><span data-stu-id="998e6-234">x</span></span>         | <span data-ttu-id="998e6-235">x</span><span class="sxs-lookup"><span data-stu-id="998e6-235">x</span></span>        | <span data-ttu-id="998e6-236">x</span><span class="sxs-lookup"><span data-stu-id="998e6-236">x</span></span>         | <span data-ttu-id="998e6-237">x</span><span class="sxs-lookup"><span data-stu-id="998e6-237">x</span></span>        | <span data-ttu-id="998e6-238">x</span><span class="sxs-lookup"><span data-stu-id="998e6-238">x</span></span>         |
| [<span data-ttu-id="998e6-239">Samplelevel</span><span class="sxs-lookup"><span data-stu-id="998e6-239">SampleLevel</span></span>](dx-graphics-hlsl-to-samplelevel.md)                                 | <span data-ttu-id="998e6-240">Beispiel für eine Textur auf der angegebenen MipMap-Ebene.</span><span class="sxs-lookup"><span data-stu-id="998e6-240">Sample a texture on the specified mipmap level.</span></span>                                                                   | <span data-ttu-id="998e6-241">x</span><span class="sxs-lookup"><span data-stu-id="998e6-241">x</span></span>        | <span data-ttu-id="998e6-242">x</span><span class="sxs-lookup"><span data-stu-id="998e6-242">x</span></span>         | <span data-ttu-id="998e6-243">x</span><span class="sxs-lookup"><span data-stu-id="998e6-243">x</span></span>        | <span data-ttu-id="998e6-244">x</span><span class="sxs-lookup"><span data-stu-id="998e6-244">x</span></span>         | <span data-ttu-id="998e6-245">x</span><span class="sxs-lookup"><span data-stu-id="998e6-245">x</span></span>        | <span data-ttu-id="998e6-246">x</span><span class="sxs-lookup"><span data-stu-id="998e6-246">x</span></span>         |



 

### <a name="return-type"></a><span data-ttu-id="998e6-247">Rückgabetyp</span><span class="sxs-lookup"><span data-stu-id="998e6-247">Return Type</span></span>

<span data-ttu-id="998e6-248">Der Rückgabetyp einer Textur Objektmethode ist float4, sofern nichts anderes angegeben wird, mit Ausnahme der Multisampling-Textur Objekte mit Antialiasing, für die immer der angegebene Typ und die angegebene Stichproben Anzahl benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="998e6-248">The return type of a texture object method is float4 unless specified otherwise, with the exception of the multisampled anti-aliased texture objects that always need the type and sample count specified.</span></span> <span data-ttu-id="998e6-249">Der Rückgabetyp ist identisch mit dem Textur Ressourcentyp ([**DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)).</span><span class="sxs-lookup"><span data-stu-id="998e6-249">The return type is the same as the texture resource type ([**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)).</span></span> <span data-ttu-id="998e6-250">Das heißt, es kann sich um einen der folgenden Typen handeln:</span><span class="sxs-lookup"><span data-stu-id="998e6-250">In other words, it can be any of the following types.</span></span>



| <span data-ttu-id="998e6-251">type</span><span class="sxs-lookup"><span data-stu-id="998e6-251">Type</span></span>                       | <span data-ttu-id="998e6-252">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="998e6-252">Description</span></span>                                                                                                                                                             |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="998e6-253">float</span><span class="sxs-lookup"><span data-stu-id="998e6-253">float</span></span>                      | <span data-ttu-id="998e6-254">32-Bit Float (siehe Gleit [Komma Regeln](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules) für Unterschiede von IEEE Float)</span><span class="sxs-lookup"><span data-stu-id="998e6-254">32-bit float (see [Floating-Point Rules](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules) for differences from IEEE float)</span></span>                            |
| <span data-ttu-id="998e6-255">INT</span><span class="sxs-lookup"><span data-stu-id="998e6-255">int</span></span>                        | <span data-ttu-id="998e6-256">32-Bit-Ganzzahl mit Vorzeichen</span><span class="sxs-lookup"><span data-stu-id="998e6-256">32-bit signed integer</span></span>                                                                                                                                                   |
| <span data-ttu-id="998e6-257">unsigned int</span><span class="sxs-lookup"><span data-stu-id="998e6-257">unsigned int</span></span>               | <span data-ttu-id="998e6-258">32-Bit-Ganzzahl ohne Vorzeichen</span><span class="sxs-lookup"><span data-stu-id="998e6-258">32-bit unsigned integer</span></span>                                                                                                                                                 |
| <span data-ttu-id="998e6-259">snorm</span><span class="sxs-lookup"><span data-stu-id="998e6-259">snorm</span></span>                      | <span data-ttu-id="998e6-260">32-Bit Float im Bereich von-1 bis 1 einschließlich (siehe Gleit [Komma Regeln](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules) für Unterschiede von IEEE Float)</span><span class="sxs-lookup"><span data-stu-id="998e6-260">32-bit float in range -1 to 1 inclusive (see [Floating-Point Rules](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules) for differences from IEEE float)</span></span> |
| <span data-ttu-id="998e6-261">unorm</span><span class="sxs-lookup"><span data-stu-id="998e6-261">unorm</span></span>                      | <span data-ttu-id="998e6-262">32-Bit-Gleit Komma Zahl im Bereich von 0 bis 1 einschließlich (siehe Gleit [Komma Regeln](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules) für Unterschiede von IEEE Float)</span><span class="sxs-lookup"><span data-stu-id="998e6-262">32-bit float in range 0 to 1 inclusive (see [Floating-Point Rules](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules) for differences from IEEE float)</span></span>  |
| <span data-ttu-id="998e6-263">beliebige Textur Typen oder-Struktur</span><span class="sxs-lookup"><span data-stu-id="998e6-263">any texture type or struct</span></span> | <span data-ttu-id="998e6-264">Die Anzahl der zurückgegebenen Komponenten muss zwischen 1 und 3 liegen.</span><span class="sxs-lookup"><span data-stu-id="998e6-264">The number of components returned must be between 1 and 3 inclusive.</span></span>                                                                                                    |



 

<span data-ttu-id="998e6-265">Außerdem kann der Rückgabetyp ein beliebiger Textur Typ sein, einschließlich einer Struktur, muss jedoch kleiner als vier Komponenten sein, z. b. ein float1-Typ, der eine Komponente zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="998e6-265">In addition, the return type can be any texture type including a structure but, it must be less than 4 components such as a float1 type which returns one component.</span></span>

## <a name="default-values-for-missing-components-in-a-texture"></a><span data-ttu-id="998e6-266">Standardwerte für fehlende Komponenten in einer Textur</span><span class="sxs-lookup"><span data-stu-id="998e6-266">Default Values for Missing Components in a Texture</span></span>

<span data-ttu-id="998e6-267">Der Standardwert für fehlende Komponenten in einem Textur Ressourcentyp ist für alle Komponenten mit Ausnahme der Alpha Komponente (a) 0 (null). der Standardwert für das fehlende A ist 1.</span><span class="sxs-lookup"><span data-stu-id="998e6-267">The default value for missing components in a texture resource type is zero for any component except the alpha component (A); the default value for the missing A is one.</span></span> <span data-ttu-id="998e6-268">Die Art und Weise, wie diese für den Shader angezeigt wird, hängt vom Textur Ressourcentyp ab.</span><span class="sxs-lookup"><span data-stu-id="998e6-268">The way that this one appears to the shader depends on the texture resource type.</span></span> <span data-ttu-id="998e6-269">Sie nimmt die Form der ersten typisierten Komponente an, die tatsächlich im Textur Ressourcentyp vorhanden ist (beginnend von Links in RGBA-Reihenfolge).</span><span class="sxs-lookup"><span data-stu-id="998e6-269">It takes the form of the first typed component that is actually present in the texture resource type (starting from the left in RGBA order).</span></span> <span data-ttu-id="998e6-270">Wenn dieses Formular unorm oder float ist, ist der Standardwert für das fehlende A 1.0 f.</span><span class="sxs-lookup"><span data-stu-id="998e6-270">If this form is UNORM or FLOAT, the default value for the missing A is 1.0f.</span></span> <span data-ttu-id="998e6-271">Wenn das Formular "Sint" oder "uint" ist, ist der Standardwert für das fehlende "A" 0x1.</span><span class="sxs-lookup"><span data-stu-id="998e6-271">If the form is SINT or UINT, the default value for the missing A is 0x1.</span></span>

<span data-ttu-id="998e6-272">Wenn ein Shader z. b. den typlosen Textur Ressourcentyp " [**DXGI- \_ Format \_ R24 \_ unorm \_ X8 \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) " liest, sind die Standardwerte für "G" und "B" 0 und der Standardwert für "1.0 f;". Wenn ein Shader den [**\_ \_ R16G16 \_ uint**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) -Textur Ressourcentyp im DXGI-Format liest, ist der Standardwert für b 0 (null), und der Standardwert für eine ist 0x00000001; wenn ein Shader den-Textur Ressourcentyp " [**DXGI- \_ Format \_ \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) .</span><span class="sxs-lookup"><span data-stu-id="998e6-272">For example, when a shader reads the [**DXGI\_FORMAT\_R24\_UNORM\_X8\_TYPELESS**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) texture resource type, the default values for G and B are zero and the default value for A is 1.0f; when a shader reads the [**DXGI\_FORMAT\_R16G16\_UINT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) texture resource type, the default value for B is zero and the default value for A is 0x00000001; when a shader reads the [**DXGI\_FORMAT\_R16\_SINT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) texture resource type, the default values for G and B are zero and the default value for A is 0x00000001.</span></span>

## <a name="example-2"></a><span data-ttu-id="998e6-273">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="998e6-273">Example 2</span></span>

<span data-ttu-id="998e6-274">Im folgenden finden Sie ein Beispiel für die Textur Stichproben Verwendung einer Textur Methode.</span><span class="sxs-lookup"><span data-stu-id="998e6-274">Here is an example of texture sampling using a texture method.</span></span>


```
sampler MySamp;
Texture2D <float4> MyTex;
 
float4 main( float2 TexCoords[2] : TEXCOORD ) : SV_Target
{
    return MyTex.Sample( MySamp, TexCoords[0] ));
}
```



## <a name="minimum-shader-model"></a><span data-ttu-id="998e6-275">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="998e6-275">Minimum Shader Model</span></span>

<span data-ttu-id="998e6-276">Dieses Objekt wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="998e6-276">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="998e6-277">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="998e6-277">Shader Model</span></span>                                                        | <span data-ttu-id="998e6-278">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="998e6-278">Supported</span></span> |
|---------------------------------------------------------------------|-----------|
| <span data-ttu-id="998e6-279">[Shader Model 4](dx-graphics-hlsl-sm4.md) und höhere shadermodelle</span><span class="sxs-lookup"><span data-stu-id="998e6-279">[Shader Model 4](dx-graphics-hlsl-sm4.md) and higher shader models</span></span> | <span data-ttu-id="998e6-280">ja</span><span class="sxs-lookup"><span data-stu-id="998e6-280">yes</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="998e6-281">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="998e6-281">See also</span></span>

<dl> <dt>

[<span data-ttu-id="998e6-282">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="998e6-282">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

