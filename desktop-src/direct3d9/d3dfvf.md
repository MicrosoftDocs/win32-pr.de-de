---
description: Flexible Vertexformatkonstanten oder FVF-Codes werden verwendet, um den Inhalt von Scheitelpunkten zu beschreiben, die sich in einem einzelnen Datenstrom überlappen und von der Pipeline mit festen Funktionen verarbeitet werden.
ms.assetid: 85d9f5b2-8e4a-4f92-a587-eae5b293778c
title: D3DFVF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a088dda530904c320720371c76601fd4fb254481
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343260"
---
# <a name="d3dfvf"></a>D3DFVF

Flexible Vertexformatkonstanten oder FVF-Codes werden verwendet, um den Inhalt von Scheitelpunkten zu beschreiben, die sich in einem einzelnen Datenstrom überlappen und von der Pipeline mit festen Funktionen verarbeitet werden.

## <a name="vertex-data-flags"></a>Vertexdatenflags

Die folgenden Flags beschreiben ein Scheitelpunktformat. Informationen zu Vertexformaten finden Sie unter [FVF-Codes für feste Funktionen (Direct3D 9).](fixed-function-fvf-codes.md)



| \#Definieren                            | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                             | Datenreihenfolge und -typ                                                                                       |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| D3DFVF \_ DIFFUSE                     | Das Scheitelpunktformat enthält eine diffuse Farbkomponente.                                                                                                                                                                                                                                                                                                                       | DWORD in ARGB-Reihenfolge. Siehe [**D3DCOLOR \_ ARGB**](d3dcolor-argb.md).                                         |
| D3DFVF \_ NORMAL                      | Das Scheitelpunktformat enthält einen vertex-Normalvektor. Dieses Flag kann nicht mit dem D3DFVF \_ XYZRHW-Flag verwendet werden.                                                                                                                                                                                                                                                                   | float, float, float                                                                                       |
| D3DFVF \_ PSIZE                       | In Punktgröße angegebenes Scheitelpunktformat. Diese Größe wird in Kameraraumeinheiten für Scheitelpunkte ausgedrückt, die nicht transformiert und beleuchtet werden, und in Geräteraumeinheiten für transformierte und beleuchtete Scheitelpunkte.                                                                                                                                                                          | float                                                                                                     |
| D3DFVF \_ SPECULAR                    | Das Scheitelpunktformat enthält eine Specular-Farbkomponente.                                                                                                                                                                                                                                                                                                                      | DWORD in ARGB-Reihenfolge. Siehe [**D3DCOLOR \_ ARGB**](d3dcolor-argb.md).                                         |
| D3DFVF \_ XYZ                         | Das Scheitelpunktformat enthält die Position eines nicht übersetzten Scheitelpunkts. Dieses Flag kann nicht mit dem Flag D3DFVF \_ XYZRHW verwendet werden.                                                                                                                                                                                                                                                  | float, float, float.                                                                                      |
| D3DFVF \_ XYZRHW                      | Das Scheitelpunktformat enthält die Position eines transformierten Scheitelpunkts. Dieses Flag kann nicht mit den Flags D3DFVF \_ XYZ oder D3DFVF \_ NORMAL verwendet werden.                                                                                                                                                                                                                                     | float, float, float, float.                                                                               |
| D3DFVF \_ XYZB1 bis D3DFVF \_ XYZB5 | Das Vertexformat enthält Positionsdaten und eine entsprechende Anzahl von Gewichtungswerten (Beta), die für Multimatrix-Vertexblendingvorgänge verwendet werden. Derzeit kann Direct3D mit bis zu drei Gewichtungswerten und vier Mischungsmatrizen kombiniert werden. Weitere Informationen zur Verwendung von Blendingmatrizen finden Sie unter [Indiziertes Vertexblending (Direct3D 9).](indexed-vertex-blending.md) | 1, 2 oder 3 gleitkomma. Wenn D3DFVF LASTBETA UBYTE4 verwendet wird, wird die letzte \_ \_ Mischungsgewichtung als DWORD behandelt. |
| D3DFVF \_ XYZW                        | Das Scheitelpunktformat enthält transformierte und abgeschnittene Daten (x, y, z, w). ProcessVertices ruft den Clipper nicht auf, sondern gibt Daten in Clipkoordinaten aus. Diese Konstante ist für die programmierbare Scheitelpunktpipeline konzipiert und kann nur mit dieser verwendet werden.                                                                                                                 | float, float, float, float                                                                                |



 

## <a name="texture-flags"></a>Texturflags

Die folgenden Flags beschreiben Texturflags, die von der Pipeline mit festen Funktionen verwendet werden.



| \#Definieren                          | BESCHREIBUNG                                                                                                                                                                                                                                                                        |
|-----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DFVF \_ TEX0 – D3DFVF \_ TEX8       | Anzahl der Texturkoordinatensätze für diesen Scheitelpunkt. Die tatsächlichen Werte für diese Flags sind nicht sequenziell.                                                                                                                                                                           |
| D3DFVF \_ TEXCOORDSIZEN(coordIndex) | Definieren Sie ein Texturkoordinaten-Dataset. n gibt die Dimension der Texturkoordinaten an. coordIndex gibt die Nummer des Texturkoordinatenindexes an. Siehe [**D3DFVF \_ TEXCOORDSIZEN**](d3dfvf-texcoordsizen.md) und [Texturkoordinaten und Texturstufen](texture-coordinates.md). |



 

## <a name="mask-flags"></a>Maskierungsflags

Die folgenden Flags beschreiben Maskenflags, die von der Pipeline mit festen Funktionen verwendet werden.



| \#Definieren                             | BESCHREIBUNG                                           |
|--------------------------------------|-------------------------------------------------------|
| D3DFVF \_ \_ POSITIONSMASKE               | Maske für Positionsbits.                               |
| D3DFVF \_ RESERVED0, D3DFVF \_ RESERVED2 | Maskieren Sie Werte für reservierte Bits in der FVF. Darf nicht verwendet werden. |
| D3DFVF \_ TEXCOUNT \_ MASK               | Mask-Wert für Texturflagbits.                     |



 

## <a name="miscellaneous-flags"></a>Verschiedene Flags

Die folgenden Flags beschreiben eine Vielzahl von Flags, die von der Fixed Function-Pipeline verwendet werden.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>#Definieren</td>
<td>BESCHREIBUNG</td>
</tr>
<tr class="even">
<td>D3DFVF_LASTBETA_D3DCOLOR</td>
<td>Das letzte Betafeld in den Scheitelpunktpositionsdaten ist vom Typ D3DCOLOR. Die Daten in den Betafeldern werden mit Matrixpaletten-Skinning verwendet, um Matrixindizes anzugeben.</td>
</tr>
<tr class="odd">
<td>D3DFVF_LASTBETA_UBYTE4</td>
<td>Das letzte Betafeld in den Scheitelpunktpositionsdaten ist vom Typ UBYTE4. Die Daten in den Betafeldern werden mit Matrixpaletten-Skinning verwendet, um Matrixindizes anzugeben. <span data-codelanguage=""></span>
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

<p>Die FVF wird als deklariert: D3DFVF_XYZB5 | D3DFVF_LASTBETA_UBYTE4. Weight und MatrixIndices sind in beta[5] enthalten, wobei D3DFVF_LASTBETA_UBYTE4 besagt, dass das letzte DWORD in beta[5] als Typ UBYTE4 interpretiert werden soll.</p></td>
</tr>
<tr class="even">
<td>D3DFVF_TEXCOUNT_SHIFT</td>
<td>Die Anzahl der Bits, um die ein ganzzahliger Wert verschoben werden soll, der die Anzahl der Texturkoordinaten für einen Scheitelpunkt angibt. Dieser Wert kann wie unten gezeigt verwendet werden.
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



 

### <a name="examples"></a>Beispiele

In den folgenden Beispielen werden andere gängige Flagkombinationen gezeigt.


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



## <a name="constant-information"></a>Konstante Informationen



| Anforderung                         | Wert            |
|--------------------------|-------------|
| Header                   | d3d9types.h |
| Mindestbetriebssystem | Windows 98  |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Konstanten](dx9-graphics-reference-d3d-constants.md)
</dt> <dt>

[Feste FVF-Codes der Funktion (Direct3D 9)](fixed-function-fvf-codes.md)
</dt> <dt>

[Geometriemischung (Direct3D 9)](geometry-blending.md)
</dt> </dl>

 

 



