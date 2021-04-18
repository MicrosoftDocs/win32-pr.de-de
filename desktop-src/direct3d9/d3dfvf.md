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
# <a name="d3dfvf"></a>D3DFVF

Flexible Scheitelpunkt Format Konstanten oder FVF-Codes werden verwendet, um den Inhalt von Vertices zu beschreiben, die in einem einzelnen Datenstrom verschachtelt sind, der von der Pipeline mit fester Funktionsweise verarbeitet wird.

## <a name="vertex-data-flags"></a>Vertex-datenflags

Die folgenden Flags beschreiben ein Scheitelpunkt Format. Weitere Informationen zu Scheitelpunkt Formaten finden Sie unter [Fixed Function f VF Codes (Direct3D 9)](fixed-function-fvf-codes.md).



|                                     |                                                                                                                                                                                                                                                                                                                                                                         |                                                                                                           |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| \#definieren                            | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                             | Datenreihen Folge und Typ                                                                                       |
| D3DFVF \_ diffuses                     | Das Vertex-Format enthält eine diffuse Farbkomponente.                                                                                                                                                                                                                                                                                                                       | DWORD in ARGB-Reihenfolge. Siehe [**D3DCOLOR \_ ARGB**](d3dcolor-argb.md).                                         |
| D3DFVF \_ Normal                      | Das Vertex-Format enthält einen Scheitelpunkt-normal Vektor. Dieses Flag kann nicht mit dem D3DFVF \_ xyzrhw-Flag verwendet werden.                                                                                                                                                                                                                                                                   | float, float, float                                                                                       |
| D3DFVF \_ Psize                       | Das in der Punktgröße angegebene Scheitelpunkt Format. Diese Größe wird in Kamera Raumeinheiten für Scheitel Punkte ausgedrückt, die nicht transformiert und beleuchtet werden, sowie in Einheiten für Geräteraum für Transformierte und beleuchtete Scheitel Punkte.                                                                                                                                                                          | float                                                                                                     |
| D3DFVF \_ Glanz                    | Das Vertex-Format enthält eine Glanz Farben Komponente.                                                                                                                                                                                                                                                                                                                      | DWORD in ARGB-Reihenfolge. Siehe [**D3DCOLOR \_ ARGB**](d3dcolor-argb.md).                                         |
| D3DFVF \_ XYZ                         | Das Vertex-Format schließt die Position eines nicht transformierten Scheitel Punkts ein. Dieses Flag kann nicht mit dem D3DFVF \_ xyzrhw-Flag verwendet werden.                                                                                                                                                                                                                                                  | float, float, float.                                                                                      |
| D3DFVF \_ xyzrhw                      | Das Vertex-Format schließt die Position eines transformierten Scheitel Punkts ein. Dieses Flag kann nicht mit den \_ normalen Flags D3DFVF XYZ oder D3DFVF verwendet werden \_ .                                                                                                                                                                                                                                     | float, float, float, float.                                                                               |
| D3DFVF \_ XYZB1 bis D3DFVF \_ XYZB5 | Das Vertex-Format enthält Positionsdaten und eine entsprechende Anzahl von Gewichtungs Werten (Beta), die für multimatrix-Vertex-Mischungs Vorgänge verwendet werden. Derzeit kann Direct3D mit bis zu drei Gewichtungs Werten und vier Mischungs Matrizen kombiniert werden. Weitere Informationen zum Verwenden von Mischungs Matrizen finden Sie unter [indiziertes Vertex-Blending (Direct3D 9)](indexed-vertex-blending.md). | 1, 2 oder 3 Gleit Komma Zahlen. Wenn D3DFVF \_ lastbeta \_ UBYTE4 verwendet wird, wird das letzte Mischungs Gewicht als DWORD behandelt. |
| D3DFVF \_ xyzw                        | Das Vertex-Format enthält transformierte und abgeschnitten-Daten (x, y, z, w). ProcessVertices Ruft den clippernicht auf, sondern gibt Daten in Clip Koordinaten aus. Diese Konstante ist für die programmierbare Scheitelpunkt Pipeline konzipiert und kann nur mit verwendet werden.                                                                                                                 | float, float, float, float                                                                                |



 

## <a name="texture-flags"></a>Textur-Flags

Die folgenden Flags beschreiben die Textur-Flags, die von der Pipeline mit fester Funktionsweise verwendet werden.



|                                   |                                                                                                                                                                                                                                                                                    |
|-----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \#definieren                          | BESCHREIBUNG                                                                                                                                                                                                                                                                        |
| D3DFVF \_ TEX0-D3DFVF \_ TEX8       | Anzahl der Texturkoordinaten Sätze für diesen Scheitelpunkt. Die tatsächlichen Werte für diese Flags sind nicht sequenziell.                                                                                                                                                                           |
| D3DFVF \_ texcoordsizen (coordindex) | Definieren Sie ein Texturkoordinaten DataSet. n gibt die Dimension der Texturkoordinaten an. coordindex gibt eine Texturkoordinaten Index-Nummer an. Weitere Informationen finden Sie unter [**D3DFVF \_ texcoordsizen**](d3dfvf-texcoordsizen.md) und [Texturkoordinaten und Textur Stufen](texture-coordinates.md). |



 

## <a name="mask-flags"></a>Masken-Flags

Die folgenden Flags beschreiben Masken-Flags, die von der Pipeline mit fester Funktionsweise verwendet werden.



|                                      |                                                       |
|--------------------------------------|-------------------------------------------------------|
| \#definieren                             | BESCHREIBUNG                                           |
| D3DFVF \_ Positions \_ Maske               | Maske für Positions Bits.                               |
| D3DFVF \_ RESERVED0, D3DFVF \_ "reserved2" | Masken Werte für reservierte Bits in der "f". Darf nicht verwendet werden. |
| D3DFVF \_ texcount- \_ Maske               | Maskenwert für Texturflagbits.                     |



 

## <a name="miscellaneous-flags"></a>Verschiedene Flags

Die folgenden Flags beschreiben eine Vielzahl von Flags, die von der Pipeline mit fester Funktionsweise verwendet werden.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>#definieren</td>
<td>BESCHREIBUNG</td>
</tr>
<tr class="even">
<td>D3DFVF_LASTBETA_D3DCOLOR</td>
<td>Das letzte Beta-Feld in den Scheitelpunkt Positionsdaten ist vom Typ D3DCOLOR. Die Daten in den Beta-Feldern werden bei der Matrix Palette zum Angeben von Matrix Indizes verwendet.</td>
</tr>
<tr class="odd">
<td>D3DFVF_LASTBETA_UBYTE4</td>
<td>Das letzte Beta-Feld in den Scheitelpunkt Positionsdaten ist vom Typ UBYTE4. Die Daten in den Beta-Feldern werden bei der Matrix Palette zum Angeben von Matrix Indizes verwendet. <span data-codelanguage=""></span>
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

<p>Da der Wert D3DFVF_XYZB5 für "f. D3DFVF_LASTBETA_UBYTE4. Gewichtung und matrixindizes sind in der Beta Version [5] enthalten, in der D3DFVF_LASTBETA_UBYTE4 das letzte DWORD in der Beta Version [5] als Typ "UBYTE4" interpretieren.</p></td>
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

In den folgenden Beispielen werden andere gängige Flag-Kombinationen gezeigt.


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



|                          |             |
|--------------------------|-------------|
| Header                   | d3d9types. h |
| Mindestens Betriebssystem | Windows 98  |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Konstanten](dx9-graphics-reference-d3d-constants.md)
</dt> <dt>

[Code der Fixed-Funktion (Direct3D 9)](fixed-function-fvf-codes.md)
</dt> <dt>

[Geometrie Mischung (Direct3D 9)](geometry-blending.md)
</dt> </dl>

 

 



