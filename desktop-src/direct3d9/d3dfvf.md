---
description: Flexible Scheitelpunkt Format Konstanten oder FVF-Codes werden verwendet, um den Inhalt von Vertices zu beschreiben, die in einem einzelnen Datenstrom verschachtelt sind, der von der Pipeline mit fester Funktionsweise verarbeitet wird.
ms.assetid: 85d9f5b2-8e4a-4f92-a587-eae5b293778c
title: D3DFVF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d4bfc1dcabdb6991b49af967bb596fd4c1e3bdd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344619"
---
# <a name="d3dfvf"></a><span data-ttu-id="4a688-103">D3DFVF</span><span class="sxs-lookup"><span data-stu-id="4a688-103">D3DFVF</span></span>

<span data-ttu-id="4a688-104">Flexible Scheitelpunkt Format Konstanten oder FVF-Codes werden verwendet, um den Inhalt von Vertices zu beschreiben, die in einem einzelnen Datenstrom verschachtelt sind, der von der Pipeline mit fester Funktionsweise verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="4a688-104">Flexible Vertex Format Constants, or FVF codes, are used to describe the contents of vertices interleaved in a single data stream that will be processed by the fixed-function pipeline.</span></span>

## <a name="vertex-data-flags"></a><span data-ttu-id="4a688-105">Vertex-datenflags</span><span class="sxs-lookup"><span data-stu-id="4a688-105">Vertex Data Flags</span></span>

<span data-ttu-id="4a688-106">Die folgenden Flags beschreiben ein Scheitelpunkt Format.</span><span class="sxs-lookup"><span data-stu-id="4a688-106">The following flags describe a vertex format.</span></span> <span data-ttu-id="4a688-107">Weitere Informationen zu Scheitelpunkt Formaten finden Sie unter [Fixed Function f VF Codes (Direct3D 9)](fixed-function-fvf-codes.md).</span><span class="sxs-lookup"><span data-stu-id="4a688-107">For information regarding vertex formats, see [Fixed Function FVF Codes (Direct3D 9)](fixed-function-fvf-codes.md).</span></span>



|                                     |                                                                                                                                                                                                                                                                                                                                                                         |                                                                                                           |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a688-108">\#definieren</span><span class="sxs-lookup"><span data-stu-id="4a688-108">\#define</span></span>                            | <span data-ttu-id="4a688-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4a688-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                             | <span data-ttu-id="4a688-110">Datenreihen Folge und Typ</span><span class="sxs-lookup"><span data-stu-id="4a688-110">Data order and type</span></span>                                                                                       |
| <span data-ttu-id="4a688-111">D3DFVF \_ diffuses</span><span class="sxs-lookup"><span data-stu-id="4a688-111">D3DFVF\_DIFFUSE</span></span>                     | <span data-ttu-id="4a688-112">Das Vertex-Format enthält eine diffuse Farbkomponente.</span><span class="sxs-lookup"><span data-stu-id="4a688-112">Vertex format includes a diffuse color component.</span></span>                                                                                                                                                                                                                                                                                                                       | <span data-ttu-id="4a688-113">DWORD in ARGB-Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="4a688-113">DWORD in ARGB order.</span></span> <span data-ttu-id="4a688-114">Siehe [**D3DCOLOR \_ ARGB**](d3dcolor-argb.md).</span><span class="sxs-lookup"><span data-stu-id="4a688-114">See [**D3DCOLOR\_ARGB**](d3dcolor-argb.md).</span></span>                                         |
| <span data-ttu-id="4a688-115">D3DFVF \_ Normal</span><span class="sxs-lookup"><span data-stu-id="4a688-115">D3DFVF\_NORMAL</span></span>                      | <span data-ttu-id="4a688-116">Das Vertex-Format enthält einen Scheitelpunkt-normal Vektor.</span><span class="sxs-lookup"><span data-stu-id="4a688-116">Vertex format includes a vertex normal vector.</span></span> <span data-ttu-id="4a688-117">Dieses Flag kann nicht mit dem D3DFVF \_ xyzrhw-Flag verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4a688-117">This flag cannot be used with the D3DFVF\_XYZRHW flag.</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="4a688-118">float, float, float</span><span class="sxs-lookup"><span data-stu-id="4a688-118">float, float, float</span></span>                                                                                       |
| <span data-ttu-id="4a688-119">D3DFVF \_ Psize</span><span class="sxs-lookup"><span data-stu-id="4a688-119">D3DFVF\_PSIZE</span></span>                       | <span data-ttu-id="4a688-120">Das in der Punktgröße angegebene Scheitelpunkt Format.</span><span class="sxs-lookup"><span data-stu-id="4a688-120">Vertex format specified in point size.</span></span> <span data-ttu-id="4a688-121">Diese Größe wird in Kamera Raumeinheiten für Scheitel Punkte ausgedrückt, die nicht transformiert und beleuchtet werden, sowie in Einheiten für Geräteraum für Transformierte und beleuchtete Scheitel Punkte.</span><span class="sxs-lookup"><span data-stu-id="4a688-121">This size is expressed in camera space units for vertices that are not transformed and lit, and in device-space units for transformed and lit vertices.</span></span>                                                                                                                                                                          | <span data-ttu-id="4a688-122">float</span><span class="sxs-lookup"><span data-stu-id="4a688-122">float</span></span>                                                                                                     |
| <span data-ttu-id="4a688-123">D3DFVF \_ Glanz</span><span class="sxs-lookup"><span data-stu-id="4a688-123">D3DFVF\_SPECULAR</span></span>                    | <span data-ttu-id="4a688-124">Das Vertex-Format enthält eine Glanz Farben Komponente.</span><span class="sxs-lookup"><span data-stu-id="4a688-124">Vertex format includes a specular color component.</span></span>                                                                                                                                                                                                                                                                                                                      | <span data-ttu-id="4a688-125">DWORD in ARGB-Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="4a688-125">DWORD in ARGB order.</span></span> <span data-ttu-id="4a688-126">Siehe [**D3DCOLOR \_ ARGB**](d3dcolor-argb.md).</span><span class="sxs-lookup"><span data-stu-id="4a688-126">See [**D3DCOLOR\_ARGB**](d3dcolor-argb.md).</span></span>                                         |
| <span data-ttu-id="4a688-127">D3DFVF \_ XYZ</span><span class="sxs-lookup"><span data-stu-id="4a688-127">D3DFVF\_XYZ</span></span>                         | <span data-ttu-id="4a688-128">Das Vertex-Format schließt die Position eines nicht transformierten Scheitel Punkts ein.</span><span class="sxs-lookup"><span data-stu-id="4a688-128">Vertex format includes the position of an untransformed vertex.</span></span> <span data-ttu-id="4a688-129">Dieses Flag kann nicht mit dem D3DFVF \_ xyzrhw-Flag verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4a688-129">This flag cannot be used with the D3DFVF\_XYZRHW flag.</span></span>                                                                                                                                                                                                                                                  | <span data-ttu-id="4a688-130">float, float, float.</span><span class="sxs-lookup"><span data-stu-id="4a688-130">float, float, float.</span></span>                                                                                      |
| <span data-ttu-id="4a688-131">D3DFVF \_ xyzrhw</span><span class="sxs-lookup"><span data-stu-id="4a688-131">D3DFVF\_XYZRHW</span></span>                      | <span data-ttu-id="4a688-132">Das Vertex-Format schließt die Position eines transformierten Scheitel Punkts ein.</span><span class="sxs-lookup"><span data-stu-id="4a688-132">Vertex format includes the position of a transformed vertex.</span></span> <span data-ttu-id="4a688-133">Dieses Flag kann nicht mit den \_ normalen Flags D3DFVF XYZ oder D3DFVF verwendet werden \_ .</span><span class="sxs-lookup"><span data-stu-id="4a688-133">This flag cannot be used with the D3DFVF\_XYZ or D3DFVF\_NORMAL flags.</span></span>                                                                                                                                                                                                                                     | <span data-ttu-id="4a688-134">float, float, float, float.</span><span class="sxs-lookup"><span data-stu-id="4a688-134">float, float, float, float.</span></span>                                                                               |
| <span data-ttu-id="4a688-135">D3DFVF \_ XYZB1 bis D3DFVF \_ XYZB5</span><span class="sxs-lookup"><span data-stu-id="4a688-135">D3DFVF\_XYZB1 through D3DFVF\_XYZB5</span></span> | <span data-ttu-id="4a688-136">Das Vertex-Format enthält Positionsdaten und eine entsprechende Anzahl von Gewichtungs Werten (Beta), die für multimatrix-Vertex-Mischungs Vorgänge verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4a688-136">Vertex format contains position data, and a corresponding number of weighting (beta) values to use for multimatrix vertex blending operations.</span></span> <span data-ttu-id="4a688-137">Derzeit kann Direct3D mit bis zu drei Gewichtungs Werten und vier Mischungs Matrizen kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="4a688-137">Currently, Direct3D can blend with up to three weighting values and four blending matrices.</span></span> <span data-ttu-id="4a688-138">Weitere Informationen zum Verwenden von Mischungs Matrizen finden Sie unter [indiziertes Vertex-Blending (Direct3D 9)](indexed-vertex-blending.md).</span><span class="sxs-lookup"><span data-stu-id="4a688-138">For more information about using blending matrices, see [Indexed Vertex Blending (Direct3D 9)](indexed-vertex-blending.md).</span></span> | <span data-ttu-id="4a688-139">1, 2 oder 3 Gleit Komma Zahlen.</span><span class="sxs-lookup"><span data-stu-id="4a688-139">1, 2, or 3 floats.</span></span> <span data-ttu-id="4a688-140">Wenn D3DFVF \_ lastbeta \_ UBYTE4 verwendet wird, wird das letzte Mischungs Gewicht als DWORD behandelt.</span><span class="sxs-lookup"><span data-stu-id="4a688-140">When D3DFVF\_LASTBETA\_UBYTE4 is used, the last blending weight is treated as a DWORD.</span></span> |
| <span data-ttu-id="4a688-141">D3DFVF \_ xyzw</span><span class="sxs-lookup"><span data-stu-id="4a688-141">D3DFVF\_XYZW</span></span>                        | <span data-ttu-id="4a688-142">Das Vertex-Format enthält transformierte und abgeschnitten-Daten (x, y, z, w).</span><span class="sxs-lookup"><span data-stu-id="4a688-142">Vertex format contains transformed and clipped (x, y, z, w) data.</span></span> <span data-ttu-id="4a688-143">ProcessVertices Ruft den clippernicht auf, sondern gibt Daten in Clip Koordinaten aus.</span><span class="sxs-lookup"><span data-stu-id="4a688-143">ProcessVertices does not invoke the clipper, instead outputting data in clip coordinates.</span></span> <span data-ttu-id="4a688-144">Diese Konstante ist für die programmierbare Scheitelpunkt Pipeline konzipiert und kann nur mit verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4a688-144">This constant is designed for, and can only be used with, the programmable vertex pipeline.</span></span>                                                                                                                 | <span data-ttu-id="4a688-145">float, float, float, float</span><span class="sxs-lookup"><span data-stu-id="4a688-145">float, float, float, float</span></span>                                                                                |



 

## <a name="texture-flags"></a><span data-ttu-id="4a688-146">Textur-Flags</span><span class="sxs-lookup"><span data-stu-id="4a688-146">Texture Flags</span></span>

<span data-ttu-id="4a688-147">Die folgenden Flags beschreiben die Textur-Flags, die von der Pipeline mit fester Funktionsweise verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4a688-147">The following flags describe texture flags used by the fixed-function pipeline.</span></span>



|                                   |                                                                                                                                                                                                                                                                                    |
|-----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a688-148">\#definieren</span><span class="sxs-lookup"><span data-stu-id="4a688-148">\#define</span></span>                          | <span data-ttu-id="4a688-149">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4a688-149">Description</span></span>                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="4a688-150">D3DFVF \_ TEX0-D3DFVF \_ TEX8</span><span class="sxs-lookup"><span data-stu-id="4a688-150">D3DFVF\_TEX0 - D3DFVF\_TEX8</span></span>       | <span data-ttu-id="4a688-151">Anzahl der Texturkoordinaten Sätze für diesen Scheitelpunkt.</span><span class="sxs-lookup"><span data-stu-id="4a688-151">Number of texture coordinate sets for this vertex.</span></span> <span data-ttu-id="4a688-152">Die tatsächlichen Werte für diese Flags sind nicht sequenziell.</span><span class="sxs-lookup"><span data-stu-id="4a688-152">The actual values for these flags are not sequential.</span></span>                                                                                                                                                                           |
| <span data-ttu-id="4a688-153">D3DFVF \_ texcoordsizen (coordindex)</span><span class="sxs-lookup"><span data-stu-id="4a688-153">D3DFVF\_TEXCOORDSIZEN(coordIndex)</span></span> | <span data-ttu-id="4a688-154">Definieren Sie ein Texturkoordinaten DataSet.</span><span class="sxs-lookup"><span data-stu-id="4a688-154">Define a texture coordinate data set.</span></span> <span data-ttu-id="4a688-155">n gibt die Dimension der Texturkoordinaten an.</span><span class="sxs-lookup"><span data-stu-id="4a688-155">n indicates the dimension of the texture coordinates.</span></span> <span data-ttu-id="4a688-156">coordindex gibt eine Texturkoordinaten Index-Nummer an.</span><span class="sxs-lookup"><span data-stu-id="4a688-156">coordIndex indicates texture coordinate index number.</span></span> <span data-ttu-id="4a688-157">Weitere Informationen finden Sie unter [**D3DFVF \_ texcoordsizen**](d3dfvf-texcoordsizen.md) und [Texturkoordinaten und Textur Stufen](texture-coordinates.md).</span><span class="sxs-lookup"><span data-stu-id="4a688-157">See [**D3DFVF\_TEXCOORDSIZEN**](d3dfvf-texcoordsizen.md) and [Texture coordinates and Texture Stages](texture-coordinates.md).</span></span> |



 

## <a name="mask-flags"></a><span data-ttu-id="4a688-158">Masken-Flags</span><span class="sxs-lookup"><span data-stu-id="4a688-158">Mask Flags</span></span>

<span data-ttu-id="4a688-159">Die folgenden Flags beschreiben Masken-Flags, die von der Pipeline mit fester Funktionsweise verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4a688-159">The following flags describe mask flags used by the fixed-function pipeline.</span></span>



|                                      |                                                       |
|--------------------------------------|-------------------------------------------------------|
| <span data-ttu-id="4a688-160">\#definieren</span><span class="sxs-lookup"><span data-stu-id="4a688-160">\#define</span></span>                             | <span data-ttu-id="4a688-161">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4a688-161">Description</span></span>                                           |
| <span data-ttu-id="4a688-162">D3DFVF \_ Positions \_ Maske</span><span class="sxs-lookup"><span data-stu-id="4a688-162">D3DFVF\_POSITION\_MASK</span></span>               | <span data-ttu-id="4a688-163">Maske für Positions Bits.</span><span class="sxs-lookup"><span data-stu-id="4a688-163">Mask for position bits.</span></span>                               |
| <span data-ttu-id="4a688-164">D3DFVF \_ RESERVED0, D3DFVF \_ "reserved2"</span><span class="sxs-lookup"><span data-stu-id="4a688-164">D3DFVF\_RESERVED0, D3DFVF\_RESERVED2</span></span> | <span data-ttu-id="4a688-165">Masken Werte für reservierte Bits in der "f".</span><span class="sxs-lookup"><span data-stu-id="4a688-165">Mask values for reserved bits in the FVF.</span></span> <span data-ttu-id="4a688-166">Darf nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4a688-166">Do not use.</span></span> |
| <span data-ttu-id="4a688-167">D3DFVF \_ texcount- \_ Maske</span><span class="sxs-lookup"><span data-stu-id="4a688-167">D3DFVF\_TEXCOUNT\_MASK</span></span>               | <span data-ttu-id="4a688-168">Maskenwert für Texturflagbits.</span><span class="sxs-lookup"><span data-stu-id="4a688-168">Mask value for texture flag bits.</span></span>                     |



 

## <a name="miscellaneous-flags"></a><span data-ttu-id="4a688-169">Verschiedene Flags</span><span class="sxs-lookup"><span data-stu-id="4a688-169">Miscellaneous Flags</span></span>

<span data-ttu-id="4a688-170">Die folgenden Flags beschreiben eine Vielzahl von Flags, die von der Pipeline mit fester Funktionsweise verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4a688-170">The following flags describe a variety of flags used by the fixed-function pipeline.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4a688-171">#definieren</span><span class="sxs-lookup"><span data-stu-id="4a688-171">#define</span></span></td>
<td><span data-ttu-id="4a688-172">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4a688-172">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4a688-173">D3DFVF_LASTBETA_D3DCOLOR</span><span class="sxs-lookup"><span data-stu-id="4a688-173">D3DFVF_LASTBETA_D3DCOLOR</span></span></td>
<td><span data-ttu-id="4a688-174">Das letzte Beta-Feld in den Scheitelpunkt Positionsdaten ist vom Typ D3DCOLOR.</span><span class="sxs-lookup"><span data-stu-id="4a688-174">The last beta field in the vertex position data will be of type D3DCOLOR.</span></span> <span data-ttu-id="4a688-175">Die Daten in den Beta-Feldern werden bei der Matrix Palette zum Angeben von Matrix Indizes verwendet.</span><span class="sxs-lookup"><span data-stu-id="4a688-175">The data in the beta fields are used with matrix palette skinning to specify matrix indices.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4a688-176">D3DFVF_LASTBETA_UBYTE4</span><span class="sxs-lookup"><span data-stu-id="4a688-176">D3DFVF_LASTBETA_UBYTE4</span></span></td>
<td><span data-ttu-id="4a688-177">Das letzte Beta-Feld in den Scheitelpunkt Positionsdaten ist vom Typ UBYTE4.</span><span class="sxs-lookup"><span data-stu-id="4a688-177">The last beta field in the vertex position data will be of type UBYTE4.</span></span> <span data-ttu-id="4a688-178">Die Daten in den Beta-Feldern werden bei der Matrix Palette zum Angeben von Matrix Indizes verwendet.</span><span class="sxs-lookup"><span data-stu-id="4a688-178">The data in the beta fields are used with matrix palette skinning to specify matrix indices.</span></span> <span data-codelanguage=""></span>
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

<p><span data-ttu-id="4a688-179">Da der Wert D3DFVF_XYZB5 für "f. D3DFVF_LASTBETA_UBYTE4.</span><span class="sxs-lookup"><span data-stu-id="4a688-179">Given the FVF is declared as: D3DFVF_XYZB5 | D3DFVF_LASTBETA_UBYTE4.</span></span> <span data-ttu-id="4a688-180">Gewichtung und matrixindizes sind in der Beta Version [5] enthalten, in der D3DFVF_LASTBETA_UBYTE4 das letzte DWORD in der Beta Version [5] als Typ "UBYTE4" interpretieren.</span><span class="sxs-lookup"><span data-stu-id="4a688-180">Weight and MatrixIndices are included in beta[5], where D3DFVF_LASTBETA_UBYTE4 says to interpret the last DWORD in beta[5] as type UBYTE4.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4a688-181">D3DFVF_TEXCOUNT_SHIFT</span><span class="sxs-lookup"><span data-stu-id="4a688-181">D3DFVF_TEXCOUNT_SHIFT</span></span></td>
<td><span data-ttu-id="4a688-182">Die Anzahl der Bits, um die ein ganzzahliger Wert verschoben werden soll, der die Anzahl der Texturkoordinaten für einen Scheitelpunkt angibt.</span><span class="sxs-lookup"><span data-stu-id="4a688-182">The number of bits by which to shift an integer value that identifies the number of texture coordinates for a vertex.</span></span> <span data-ttu-id="4a688-183">Dieser Wert kann wie unten gezeigt verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4a688-183">This value might be used as shown below.</span></span>
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



 

### <a name="examples"></a><span data-ttu-id="4a688-184">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4a688-184">Examples</span></span>

<span data-ttu-id="4a688-185">In den folgenden Beispielen werden andere gängige Flag-Kombinationen gezeigt.</span><span class="sxs-lookup"><span data-stu-id="4a688-185">The following examples show other common flag combinations.</span></span>


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



## <a name="constant-information"></a><span data-ttu-id="4a688-186">Konstante Informationen</span><span class="sxs-lookup"><span data-stu-id="4a688-186">Constant Information</span></span>



|                          |             |
|--------------------------|-------------|
| <span data-ttu-id="4a688-187">Header</span><span class="sxs-lookup"><span data-stu-id="4a688-187">Header</span></span>                   | <span data-ttu-id="4a688-188">d3d9types. h</span><span class="sxs-lookup"><span data-stu-id="4a688-188">d3d9types.h</span></span> |
| <span data-ttu-id="4a688-189">Mindestens Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="4a688-189">Minimum operating system</span></span> | <span data-ttu-id="4a688-190">Windows 98</span><span class="sxs-lookup"><span data-stu-id="4a688-190">Windows 98</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="4a688-191">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4a688-191">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4a688-192">Direct3D-Konstanten</span><span class="sxs-lookup"><span data-stu-id="4a688-192">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> <dt>

[<span data-ttu-id="4a688-193">Code der Fixed-Funktion (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="4a688-193">Fixed Function FVF Codes (Direct3D 9)</span></span>](fixed-function-fvf-codes.md)
</dt> <dt>

[<span data-ttu-id="4a688-194">Geometrie Mischung (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="4a688-194">Geometry Blending (Direct3D 9)</span></span>](geometry-blending.md)
</dt> </dl>

 

 



