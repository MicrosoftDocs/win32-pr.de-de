---
description: Flexible Vertexformatkonstanten oder FVF-Codes werden verwendet, um den Inhalt von Scheitelpunkten zu beschreiben, die sich in einem einzelnen Datenstrom überlappen, der von der Pipeline mit festen Funktionen verarbeitet wird.
ms.assetid: 85d9f5b2-8e4a-4f92-a587-eae5b293778c
title: D3DFVF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25a12b4f6008023a388bd204440a0b544db85c19
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999437"
---
# <a name="d3dfvf"></a><span data-ttu-id="ea897-103">D3DFVF</span><span class="sxs-lookup"><span data-stu-id="ea897-103">D3DFVF</span></span>

<span data-ttu-id="ea897-104">Flexible Vertexformatkonstanten oder FVF-Codes werden verwendet, um den Inhalt von Scheitelpunkten zu beschreiben, die sich in einem einzelnen Datenstrom überlappen, der von der Pipeline mit festen Funktionen verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="ea897-104">Flexible Vertex Format Constants, or FVF codes, are used to describe the contents of vertices interleaved in a single data stream that will be processed by the fixed-function pipeline.</span></span>

## <a name="vertex-data-flags"></a><span data-ttu-id="ea897-105">Vertexdatenflags</span><span class="sxs-lookup"><span data-stu-id="ea897-105">Vertex Data Flags</span></span>

<span data-ttu-id="ea897-106">Die folgenden Flags beschreiben ein Scheitelpunktformat.</span><span class="sxs-lookup"><span data-stu-id="ea897-106">The following flags describe a vertex format.</span></span> <span data-ttu-id="ea897-107">Informationen zu Scheitelpunktformaten finden Sie unter [FVF-Codes für feste Funktionen (Direct3D 9).](fixed-function-fvf-codes.md)</span><span class="sxs-lookup"><span data-stu-id="ea897-107">For information regarding vertex formats, see [Fixed Function FVF Codes (Direct3D 9)](fixed-function-fvf-codes.md).</span></span>



| <span data-ttu-id="ea897-108">\#Definieren</span><span class="sxs-lookup"><span data-stu-id="ea897-108">\#define</span></span>                            | <span data-ttu-id="ea897-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ea897-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                             | <span data-ttu-id="ea897-110">Datenreihenfolge und -typ</span><span class="sxs-lookup"><span data-stu-id="ea897-110">Data order and type</span></span>                                                                                       |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea897-111">D3DFVF \_ DIFFUSE</span><span class="sxs-lookup"><span data-stu-id="ea897-111">D3DFVF\_DIFFUSE</span></span>                     | <span data-ttu-id="ea897-112">Das Scheitelpunktformat enthält eine diffuse Farbkomponente.</span><span class="sxs-lookup"><span data-stu-id="ea897-112">Vertex format includes a diffuse color component.</span></span>                                                                                                                                                                                                                                                                                                                       | <span data-ttu-id="ea897-113">DWORD in ARGB-Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="ea897-113">DWORD in ARGB order.</span></span> <span data-ttu-id="ea897-114">Siehe [**D3DCOLOR \_ ARGB**](d3dcolor-argb.md).</span><span class="sxs-lookup"><span data-stu-id="ea897-114">See [**D3DCOLOR\_ARGB**](d3dcolor-argb.md).</span></span>                                         |
| <span data-ttu-id="ea897-115">D3DFVF \_ NORMAL</span><span class="sxs-lookup"><span data-stu-id="ea897-115">D3DFVF\_NORMAL</span></span>                      | <span data-ttu-id="ea897-116">Das Scheitelpunktformat enthält einen Vertexnorm normaler Vektor.</span><span class="sxs-lookup"><span data-stu-id="ea897-116">Vertex format includes a vertex normal vector.</span></span> <span data-ttu-id="ea897-117">Dieses Flag kann nicht mit dem D3DFVF \_ XYZRHW-Flag verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ea897-117">This flag cannot be used with the D3DFVF\_XYZRHW flag.</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="ea897-118">float, float, float</span><span class="sxs-lookup"><span data-stu-id="ea897-118">float, float, float</span></span>                                                                                       |
| <span data-ttu-id="ea897-119">D3DFVF \_ PSIZE</span><span class="sxs-lookup"><span data-stu-id="ea897-119">D3DFVF\_PSIZE</span></span>                       | <span data-ttu-id="ea897-120">In Punktgröße angegebenes Scheitelpunktformat.</span><span class="sxs-lookup"><span data-stu-id="ea897-120">Vertex format specified in point size.</span></span> <span data-ttu-id="ea897-121">Diese Größe wird in Kameraraumeinheiten für Scheitelpunkte ausgedrückt, die nicht transformiert und beleuchtet werden, und in Geräteraumeinheiten für transformierte und beleuchtete Scheitelpunkte.</span><span class="sxs-lookup"><span data-stu-id="ea897-121">This size is expressed in camera space units for vertices that are not transformed and lit, and in device-space units for transformed and lit vertices.</span></span>                                                                                                                                                                          | <span data-ttu-id="ea897-122">float</span><span class="sxs-lookup"><span data-stu-id="ea897-122">float</span></span>                                                                                                     |
| <span data-ttu-id="ea897-123">D3DFVF \_ SPECULAR</span><span class="sxs-lookup"><span data-stu-id="ea897-123">D3DFVF\_SPECULAR</span></span>                    | <span data-ttu-id="ea897-124">Das Scheitelpunktformat enthält eine Specular-Farbkomponente.</span><span class="sxs-lookup"><span data-stu-id="ea897-124">Vertex format includes a specular color component.</span></span>                                                                                                                                                                                                                                                                                                                      | <span data-ttu-id="ea897-125">DWORD in ARGB-Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="ea897-125">DWORD in ARGB order.</span></span> <span data-ttu-id="ea897-126">Siehe [**D3DCOLOR \_ ARGB**](d3dcolor-argb.md).</span><span class="sxs-lookup"><span data-stu-id="ea897-126">See [**D3DCOLOR\_ARGB**](d3dcolor-argb.md).</span></span>                                         |
| <span data-ttu-id="ea897-127">D3DFVF \_ XYZ</span><span class="sxs-lookup"><span data-stu-id="ea897-127">D3DFVF\_XYZ</span></span>                         | <span data-ttu-id="ea897-128">Das Scheitelpunktformat enthält die Position eines nicht übersetzten Scheitelpunkts.</span><span class="sxs-lookup"><span data-stu-id="ea897-128">Vertex format includes the position of an untransformed vertex.</span></span> <span data-ttu-id="ea897-129">Dieses Flag kann nicht mit dem Flag D3DFVF \_ XYZRHW verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ea897-129">This flag cannot be used with the D3DFVF\_XYZRHW flag.</span></span>                                                                                                                                                                                                                                                  | <span data-ttu-id="ea897-130">float, float, float.</span><span class="sxs-lookup"><span data-stu-id="ea897-130">float, float, float.</span></span>                                                                                      |
| <span data-ttu-id="ea897-131">D3DFVF \_ XYZRHW</span><span class="sxs-lookup"><span data-stu-id="ea897-131">D3DFVF\_XYZRHW</span></span>                      | <span data-ttu-id="ea897-132">Das Scheitelpunktformat enthält die Position eines transformierten Scheitelpunkts.</span><span class="sxs-lookup"><span data-stu-id="ea897-132">Vertex format includes the position of a transformed vertex.</span></span> <span data-ttu-id="ea897-133">Dieses Flag kann nicht mit den Flags D3DFVF \_ XYZ oder D3DFVF \_ NORMAL verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ea897-133">This flag cannot be used with the D3DFVF\_XYZ or D3DFVF\_NORMAL flags.</span></span>                                                                                                                                                                                                                                     | <span data-ttu-id="ea897-134">float, float, float, float.</span><span class="sxs-lookup"><span data-stu-id="ea897-134">float, float, float, float.</span></span>                                                                               |
| <span data-ttu-id="ea897-135">D3DFVF \_ XYZB1 bis D3DFVF \_ XYZB5</span><span class="sxs-lookup"><span data-stu-id="ea897-135">D3DFVF\_XYZB1 through D3DFVF\_XYZB5</span></span> | <span data-ttu-id="ea897-136">Das Vertexformat enthält Positionsdaten und eine entsprechende Anzahl von Gewichtungswerten (Beta), die für Multimatrix-Vertexblendingvorgänge verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ea897-136">Vertex format contains position data, and a corresponding number of weighting (beta) values to use for multimatrix vertex blending operations.</span></span> <span data-ttu-id="ea897-137">Derzeit kann Direct3D mit bis zu drei Gewichtungswerten und vier Mischungsmatrizen kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="ea897-137">Currently, Direct3D can blend with up to three weighting values and four blending matrices.</span></span> <span data-ttu-id="ea897-138">Weitere Informationen zur Verwendung von Blendingmatrizen finden Sie unter [Indiziertes Vertexblending (Direct3D 9).](indexed-vertex-blending.md)</span><span class="sxs-lookup"><span data-stu-id="ea897-138">For more information about using blending matrices, see [Indexed Vertex Blending (Direct3D 9)](indexed-vertex-blending.md).</span></span> | <span data-ttu-id="ea897-139">1, 2 oder 3 gleitkomma.</span><span class="sxs-lookup"><span data-stu-id="ea897-139">1, 2, or 3 floats.</span></span> <span data-ttu-id="ea897-140">Wenn D3DFVF LASTBETA UBYTE4 verwendet wird, wird die letzte \_ \_ Mischungsgewichtung als DWORD behandelt.</span><span class="sxs-lookup"><span data-stu-id="ea897-140">When D3DFVF\_LASTBETA\_UBYTE4 is used, the last blending weight is treated as a DWORD.</span></span> |
| <span data-ttu-id="ea897-141">D3DFVF \_ XYZW</span><span class="sxs-lookup"><span data-stu-id="ea897-141">D3DFVF\_XYZW</span></span>                        | <span data-ttu-id="ea897-142">Das Scheitelpunktformat enthält transformierte und abgeschnittene Daten (x, y, z, w).</span><span class="sxs-lookup"><span data-stu-id="ea897-142">Vertex format contains transformed and clipped (x, y, z, w) data.</span></span> <span data-ttu-id="ea897-143">ProcessVertices ruft den Clipper nicht auf, sondern gibt Daten in Clipkoordinaten aus.</span><span class="sxs-lookup"><span data-stu-id="ea897-143">ProcessVertices does not invoke the clipper, instead outputting data in clip coordinates.</span></span> <span data-ttu-id="ea897-144">Diese Konstante ist für die programmierbare Scheitelpunktpipeline konzipiert und kann nur mit dieser verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ea897-144">This constant is designed for, and can only be used with, the programmable vertex pipeline.</span></span>                                                                                                                 | <span data-ttu-id="ea897-145">float, float, float, float</span><span class="sxs-lookup"><span data-stu-id="ea897-145">float, float, float, float</span></span>                                                                                |



 

## <a name="texture-flags"></a><span data-ttu-id="ea897-146">Texturflags</span><span class="sxs-lookup"><span data-stu-id="ea897-146">Texture Flags</span></span>

<span data-ttu-id="ea897-147">Die folgenden Flags beschreiben Texturflags, die von der Pipeline mit festen Funktionen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ea897-147">The following flags describe texture flags used by the fixed-function pipeline.</span></span>



| <span data-ttu-id="ea897-148">\#Definieren</span><span class="sxs-lookup"><span data-stu-id="ea897-148">\#define</span></span>                          | <span data-ttu-id="ea897-149">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ea897-149">Description</span></span>                                                                                                                                                                                                                                                                        |
|-----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea897-150">D3DFVF \_ TEX0 – D3DFVF \_ TEX8</span><span class="sxs-lookup"><span data-stu-id="ea897-150">D3DFVF\_TEX0 - D3DFVF\_TEX8</span></span>       | <span data-ttu-id="ea897-151">Anzahl der Texturkoordinatensätze für diesen Scheitelpunkt.</span><span class="sxs-lookup"><span data-stu-id="ea897-151">Number of texture coordinate sets for this vertex.</span></span> <span data-ttu-id="ea897-152">Die tatsächlichen Werte für diese Flags sind nicht sequenziell.</span><span class="sxs-lookup"><span data-stu-id="ea897-152">The actual values for these flags are not sequential.</span></span>                                                                                                                                                                           |
| <span data-ttu-id="ea897-153">D3DFVF \_ TEXCOORDSIZEN(coordIndex)</span><span class="sxs-lookup"><span data-stu-id="ea897-153">D3DFVF\_TEXCOORDSIZEN(coordIndex)</span></span> | <span data-ttu-id="ea897-154">Definieren Sie ein Texturkoordinaten-Dataset.</span><span class="sxs-lookup"><span data-stu-id="ea897-154">Define a texture coordinate data set.</span></span> <span data-ttu-id="ea897-155">n gibt die Dimension der Texturkoordinaten an.</span><span class="sxs-lookup"><span data-stu-id="ea897-155">n indicates the dimension of the texture coordinates.</span></span> <span data-ttu-id="ea897-156">coordIndex gibt die Nummer des Texturkoordinatenindexes an.</span><span class="sxs-lookup"><span data-stu-id="ea897-156">coordIndex indicates texture coordinate index number.</span></span> <span data-ttu-id="ea897-157">Weitere Informationen finden Sie unter [**D3DFVF \_ TEXCOORDSIZEN**](d3dfvf-texcoordsizen.md) und [Texturkoordinaten und Texturstufen.](texture-coordinates.md)</span><span class="sxs-lookup"><span data-stu-id="ea897-157">See [**D3DFVF\_TEXCOORDSIZEN**](d3dfvf-texcoordsizen.md) and [Texture coordinates and Texture Stages](texture-coordinates.md).</span></span> |



 

## <a name="mask-flags"></a><span data-ttu-id="ea897-158">Maskierungsflags</span><span class="sxs-lookup"><span data-stu-id="ea897-158">Mask Flags</span></span>

<span data-ttu-id="ea897-159">Die folgenden Flags beschreiben mask-Flags, die von der Fixed-Function-Pipeline verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ea897-159">The following flags describe mask flags used by the fixed-function pipeline.</span></span>



| <span data-ttu-id="ea897-160">\#Definieren</span><span class="sxs-lookup"><span data-stu-id="ea897-160">\#define</span></span>                             | <span data-ttu-id="ea897-161">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ea897-161">Description</span></span>                                           |
|--------------------------------------|-------------------------------------------------------|
| <span data-ttu-id="ea897-162">D3DFVF \_ \_ POSITIONSMASKE</span><span class="sxs-lookup"><span data-stu-id="ea897-162">D3DFVF\_POSITION\_MASK</span></span>               | <span data-ttu-id="ea897-163">Maske für Positionsbits.</span><span class="sxs-lookup"><span data-stu-id="ea897-163">Mask for position bits.</span></span>                               |
| <span data-ttu-id="ea897-164">D3DFVF \_ RESERVED0, D3DFVF \_ RESERVED2</span><span class="sxs-lookup"><span data-stu-id="ea897-164">D3DFVF\_RESERVED0, D3DFVF\_RESERVED2</span></span> | <span data-ttu-id="ea897-165">Maskieren Sie Werte für reservierte Bits in der FVF.</span><span class="sxs-lookup"><span data-stu-id="ea897-165">Mask values for reserved bits in the FVF.</span></span> <span data-ttu-id="ea897-166">Darf nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ea897-166">Do not use.</span></span> |
| <span data-ttu-id="ea897-167">D3DFVF \_ TEXCOUNT \_ MASK</span><span class="sxs-lookup"><span data-stu-id="ea897-167">D3DFVF\_TEXCOUNT\_MASK</span></span>               | <span data-ttu-id="ea897-168">Mask-Wert für Texturflagbits.</span><span class="sxs-lookup"><span data-stu-id="ea897-168">Mask value for texture flag bits.</span></span>                     |



 

## <a name="miscellaneous-flags"></a><span data-ttu-id="ea897-169">Verschiedene Flags</span><span class="sxs-lookup"><span data-stu-id="ea897-169">Miscellaneous Flags</span></span>

<span data-ttu-id="ea897-170">Die folgenden Flags beschreiben eine Vielzahl von Flags, die von der Fixed Function-Pipeline verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ea897-170">The following flags describe a variety of flags used by the fixed-function pipeline.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ea897-171">#Definieren</span><span class="sxs-lookup"><span data-stu-id="ea897-171">#define</span></span></td>
<td><span data-ttu-id="ea897-172">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ea897-172">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ea897-173">D3DFVF_LASTBETA_D3DCOLOR</span><span class="sxs-lookup"><span data-stu-id="ea897-173">D3DFVF_LASTBETA_D3DCOLOR</span></span></td>
<td><span data-ttu-id="ea897-174">Das letzte Betafeld in den Scheitelpunktpositionsdaten ist vom Typ D3DCOLOR.</span><span class="sxs-lookup"><span data-stu-id="ea897-174">The last beta field in the vertex position data will be of type D3DCOLOR.</span></span> <span data-ttu-id="ea897-175">Die Daten in den Betafeldern werden mit Matrixpaletten-Skinning verwendet, um Matrixindizes anzugeben.</span><span class="sxs-lookup"><span data-stu-id="ea897-175">The data in the beta fields are used with matrix palette skinning to specify matrix indices.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ea897-176">D3DFVF_LASTBETA_UBYTE4</span><span class="sxs-lookup"><span data-stu-id="ea897-176">D3DFVF_LASTBETA_UBYTE4</span></span></td>
<td><span data-ttu-id="ea897-177">Das letzte Betafeld in den Scheitelpunktpositionsdaten ist vom Typ UBYTE4.</span><span class="sxs-lookup"><span data-stu-id="ea897-177">The last beta field in the vertex position data will be of type UBYTE4.</span></span> <span data-ttu-id="ea897-178">Die Daten in den Betafeldern werden mit Matrixpaletten-Skinning verwendet, um Matrixindizes anzugeben.</span><span class="sxs-lookup"><span data-stu-id="ea897-178">The data in the beta fields are used with matrix palette skinning to specify matrix indices.</span></span> <span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>// Given the following vertex data definition: 
struct VERTEXPOSITION
{
   float pos[3];
   union 
   {
      float beta[5];
      struct
      {
         float weights[4];
         DWORD MatrixIndices;  // Used as UBYTEs
      }
   }
};</code></pre></td>
</tr>
</tbody>
</table>

<p><span data-ttu-id="ea897-179">Die FVF wird als deklariert: D3DFVF_XYZB5 | D3DFVF_LASTBETA_UBYTE4.</span><span class="sxs-lookup"><span data-stu-id="ea897-179">Given the FVF is declared as: D3DFVF_XYZB5 | D3DFVF_LASTBETA_UBYTE4.</span></span> <span data-ttu-id="ea897-180">Weight und MatrixIndices sind in beta[5] enthalten, wobei D3DFVF_LASTBETA_UBYTE4 besagt, dass das letzte DWORD in beta[5] als Typ UBYTE4 interpretiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="ea897-180">Weight and MatrixIndices are included in beta[5], where D3DFVF_LASTBETA_UBYTE4 says to interpret the last DWORD in beta[5] as type UBYTE4.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ea897-181">D3DFVF_TEXCOUNT_SHIFT</span><span class="sxs-lookup"><span data-stu-id="ea897-181">D3DFVF_TEXCOUNT_SHIFT</span></span></td>
<td><span data-ttu-id="ea897-182">Die Anzahl der Bits, um die ein ganzzahliger Wert verschoben werden soll, der die Anzahl der Texturkoordinaten für einen Scheitelpunkt angibt.</span><span class="sxs-lookup"><span data-stu-id="ea897-182">The number of bits by which to shift an integer value that identifies the number of texture coordinates for a vertex.</span></span> <span data-ttu-id="ea897-183">Dieser Wert kann wie unten gezeigt verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ea897-183">This value might be used as shown below.</span></span>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>DWORD dwNumTextures = 1;  // Vertex has only one set of coordinates.

// Shift the value for use when creating a 
//   flexible vertex format (FVF) combination.
dwFVF = dwNumTextures << D3DFVF_TEXCOUNT_SHIFT;

// Now, create an FVF combination using the shifted value.</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

### <a name="examples"></a><span data-ttu-id="ea897-184">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ea897-184">Examples</span></span>

<span data-ttu-id="ea897-185">In den folgenden Beispielen werden andere gängige Flagkombinationen gezeigt.</span><span class="sxs-lookup"><span data-stu-id="ea897-185">The following examples show other common flag combinations.</span></span>


```
// Untransformed vertex for lit, untextured, Gouraud-shaded content.
dwFVF = ( D3DFVF_XYZ | D3DFVF_DIFFUSE );
```




```
// Untransformed vertex for unlit, untextured, Gouraud-shaded 
//   content with diffuse material color specified per vertex.
dwFVF = ( D3DFVF_XYZ | D3DFVF_NORMAL | D3DFVF_DIFFUSE );
```




```
// Untransformed vertex for light-map-based lighting.
dwFVF = ( D3DFVF_XYZ | D3DFVF_TEX2 );
```




```
// Transformed vertex for light-map-based lighting with shared rhw.
dwFVF = ( D3DFVF_XYZRHW | D3DFVF_TEX2 );
```




```
// Heavyweight vertex for unlit, colored content with two 
//   sets of texture coordinates.
dwFVF = ( D3DFVF_XYZ | D3DFVF_NORMAL | D3DFVF_DIFFUSE | 
          D3DFVF_SPECULAR | D3DFVF_TEX2 );
```



## <a name="constant-information"></a><span data-ttu-id="ea897-186">Konstante Informationen</span><span class="sxs-lookup"><span data-stu-id="ea897-186">Constant Information</span></span>



|                          |             |
|--------------------------|-------------|
| <span data-ttu-id="ea897-187">Header</span><span class="sxs-lookup"><span data-stu-id="ea897-187">Header</span></span>                   | <span data-ttu-id="ea897-188">d3d9types.h</span><span class="sxs-lookup"><span data-stu-id="ea897-188">d3d9types.h</span></span> |
| <span data-ttu-id="ea897-189">Mindestbetriebssystem</span><span class="sxs-lookup"><span data-stu-id="ea897-189">Minimum operating system</span></span> | <span data-ttu-id="ea897-190">Windows 98</span><span class="sxs-lookup"><span data-stu-id="ea897-190">Windows 98</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="ea897-191">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ea897-191">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ea897-192">Direct3D-Konstanten</span><span class="sxs-lookup"><span data-stu-id="ea897-192">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> <dt>

[<span data-ttu-id="ea897-193">FVF-Codes der Funktion korrigiert (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="ea897-193">Fixed Function FVF Codes (Direct3D 9)</span></span>](fixed-function-fvf-codes.md)
</dt> <dt>

[<span data-ttu-id="ea897-194">Geometriemischung (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="ea897-194">Geometry Blending (Direct3D 9)</span></span>](geometry-blending.md)
</dt> </dl>

 

 



