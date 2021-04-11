---
description: Textur Filter Konstanten.
ms.assetid: 4434e456-670e-46a9-ba78-affdc195fe1c
title: D3DPTFILTERCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c122b1260d568a43c69c336059e26a6ecfde2a0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041520"
---
# <a name="d3dptfiltercaps"></a>D3DPTFILTERCAPS

Textur Filter Konstanten.



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
<td>D3DPTFILTERCAPS_CONVOLUTIONMONO</td>
<td>Das Gerät unterstützt das Chrome-filtern. Dieser Filter wird durch den D3DTEXF_CONVOLUTIONMONO Member des <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> -Enumerationstyps dargestellt. 
<table>
<tbody>
<tr class="odd">
<td>Unterschiede zwischen Direct3D 9 und Direct3D 9Ex:<br/> Dieses Flag ist nur in Direct3D 9Ex verfügbar.<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>D3DPTFILTERCAPS_MAGFPOINT</td>
<td>Das Gerät unterstützt die Stichproben Filterung pro Phase für Lupen Texturen. Der Filter für die Punkt-Stichproben Vergrößerung wird durch den D3DTEXF_POINT Member des <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> -Enumerationstyps dargestellt.</td>
</tr>
<tr class="even">
<td>D3DPTFILTERCAPS_MAGFLINEAR</td>
<td>Das Gerät unterstützt die pro-Phase-bilineare Interpolations Filterung für lupmaps. Der bilineare Interpolations-Mipmapping-Filter wird durch den D3DTEXF_LINEAR Member des <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> -Enumerationstyps dargestellt.</td>
</tr>
<tr class="odd">
<td>D3DPTFILTERCAPS_MAGFANISOTROPIC</td>
<td>Das Gerät unterstützt die pro-Phase-anisotrope Filterung für Lupen Texturen. Der anisotrope Vergrößerungs Filter wird durch den D3DTEXF_ANISOTROPIC Member des <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> -Enumerationstyps dargestellt.</td>
</tr>
<tr class="even">
<td>D3DPTFILTERCAPS_MAGFPYRAMIDALQUAD</td>
<td>Das Gerät unterstützt eine einstufige, pyramidenförmige Beispiel Filterung für Lupen Texturen. Der pyramidenförmige Lupen Filter wird durch den D3DTEXF_PYRAMIDALQUAD Member des <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> -Enumerationstyps dargestellt.</td>
</tr>
<tr class="odd">
<td>D3DPTFILTERCAPS_MAGFGAUSSIANQUAD</td>
<td>Das Gerät unterstützt das pro-Phase-Gaußsche Quad-Filtern für Lupen.</td>
</tr>
<tr class="even">
<td>D3DPTFILTERCAPS_MINFPOINT</td>
<td>Das Gerät unterstützt die phasenweise-Stichproben Filterung zum Minimieren von Texturen. Der Punkt-Sample-minierationsfilter wird durch den D3DTEXF_POINT Member des <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> -Enumerationstyps dargestellt.</td>
</tr>
<tr class="odd">
<td>D3DPTFILTERCAPS_MINFLINEAR</td>
<td>Das Gerät unterstützt das stufenweise lineare Filtern zum Minimieren von Texturen. Der lineare minierationsfilter wird durch den D3DTEXF_LINEAR Member des <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> -Enumerationstyps dargestellt.</td>
</tr>
<tr class="even">
<td>D3DPTFILTERCAPS_MINFANISOTROPIC</td>
<td>Das Gerät unterstützt die pro-Phase-anisotrope Filterung zum Minimieren von Texturen. Der anisotrope Minimierung-Filter wird durch den D3DTEXF_ANISOTROPIC Member des <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> -Enumerationstyps dargestellt.</td>
</tr>
<tr class="odd">
<td>D3DPTFILTERCAPS_MINFPYRAMIDALQUAD</td>
<td>Das Gerät unterstützt eine einstufige, pyramidenförmige Beispiel Filterung für das Minimieren von Texturen.</td>
</tr>
<tr class="even">
<td>D3DPTFILTERCAPS_MINFGAUSSIANQUAD</td>
<td>Das Gerät unterstützt die stufenweise gausische Quad-Filterung für das Minimieren von Texturen.</td>
</tr>
<tr class="odd">
<td>D3DPTFILTERCAPS_MIPFPOINT</td>
<td>Das Gerät unterstützt eine pro-Phase-Punkt-Beispiel Filterung für Mipmaps. Der "Point-Sample Mipmapping"-Filter wird durch den D3DTEXF_POINT Member des <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> -Enumerationstyps dargestellt.</td>
</tr>
<tr class="even">
<td>D3DPTFILTERCAPS_MIPFLINEAR</td>
<td>Das Gerät unterstützt die pro-Phase-bilineare Interpolations Filterung für Mipmaps. Der bilineare Interpolations-Mipmapping-Filter wird durch den D3DTEXF_LINEAR Member des <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> -Enumerationstyps dargestellt.</td>
</tr>
</tbody>
</table>



 

Diese Konstanten werden von den Elementen TextureFilterCaps, cubetexturefiltercaps, volumetexturefiltercaps und vertextexturefiltercaps von [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)verwendet.

## <a name="constant-information"></a>Konstante Informationen



|                          |            |
|--------------------------|------------|
| Header                   | d3d9caps. h |
| Mindestens Betriebssystem | Windows 98 |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Konstanten](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
