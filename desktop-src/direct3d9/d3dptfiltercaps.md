---
description: Texturfilterkonst konstanten.
ms.assetid: 4434e456-670e-46a9-ba78-affdc195fe1c
title: D3DPTFILTERCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46adc4759290691e93ef68a8a4e212eacf5b6451
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343085"
---
# <a name="d3dptfiltercaps"></a>D3DPTFILTERCAPS

Texturfilterkonst konstanten.



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
<td>D3DPTFILTERCAPS_CONVOLUTIONMONO</td>
<td>Das Gerät unterstützt monotone Konvolutionsfilterung. Dieser Filter wird durch den D3DTEXF_CONVOLUTIONMONO des <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>aufzählten D3DTEXTUREFILTERTYPE-Typs</strong></a> dargestellt. 
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
<td>Das Gerät unterstützt die punktbasierte Stichprobenfilterung pro Stufe für die Vergrößerung von Texturen. Der Punktbeispiel-Vergrößerungsfilter wird durch den D3DTEXF_POINT des <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>aufzählten D3DTEXTUREFILTERTYPE-Typs</strong></a> dargestellt.</td>
</tr>
<tr class="even">
<td>D3DPTFILTERCAPS_MAGFLINEAR</td>
<td>Das Gerät unterstützt die mehrstufige bilineare Interpolationsfilterung für die Vergrößerung von Mipmaps. Der mipmapping-Filter für die bilineare Interpolation wird durch den D3DTEXF_LINEAR des <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>aufzählten D3DTEXTUREFILTERTYPE-Typs</strong></a> dargestellt.</td>
</tr>
<tr class="odd">
<td>D3DPTFILTERCAPS_MAGFANISOTROPIC</td>
<td>Das Gerät unterstützt die phasenbasierte anisotrope Filterung für die Vergrößerung von Texturen. Der anisotrope Vergrößerungsfilter wird durch den D3DTEXF_ANISOTROPIC des <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>aufzählten D3DTEXTUREFILTERTYPE-Typs</strong></a> dargestellt.</td>
</tr>
<tr class="even">
<td>D3DPTFILTERCAPS_MAGFPYRAMIDALQUAD</td>
<td>Das Gerät unterstützt das filtern von pyramidalen Stichproben pro Stufe zum Vergrößern von Texturen. Der pyramidale Lupenfilter wird durch den D3DTEXF_PYRAMIDALQUAD Member des <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE-Enumerationstyps</strong></a> dargestellt.</td>
</tr>
<tr class="odd">
<td>D3DPTFILTERCAPS_MAGFGAUSSIANQUAD</td>
<td>Das Gerät unterstützt die Pro-Stage-Filterung von Gaußschen Quadern zum Vergrößern von Texturen.</td>
</tr>
<tr class="even">
<td>D3DPTFILTERCAPS_MINFPOINT</td>
<td>Das Gerät unterstützt die Punktsamplingfilterung pro Phase, um Texturen zu verminen. Der Point-Sample-Minderfilter wird durch den D3DTEXF_POINT Member des <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE-Enumerationstyps</strong></a> dargestellt.</td>
</tr>
<tr class="odd">
<td>D3DPTFILTERCAPS_MINFLINEAR</td>
<td>Das Gerät unterstützt die lineare Filterung pro Stufe zum Verminen von Texturen. Der lineare Minderungsfilter wird durch den D3DTEXF_LINEAR Member des <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE-Enumerationstyps</strong></a> dargestellt.</td>
</tr>
<tr class="even">
<td>D3DPTFILTERCAPS_MINFANISOTROPIC</td>
<td>Das Gerät unterstützt die phasenspezifische Anisotrope Filterung für die Vergrößerung von Texturen. Der Filter für die anisotrope Minification wird durch den D3DTEXF_ANISOTROPIC Member des <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE-Enumerationstyps</strong></a> dargestellt.</td>
</tr>
<tr class="odd">
<td>D3DPTFILTERCAPS_MINFPYRAMIDALQUAD</td>
<td>Das Gerät unterstützt das filtern von pyramidalen Stichproben pro Stufe, um Texturen zu verminen.</td>
</tr>
<tr class="even">
<td>D3DPTFILTERCAPS_MINFGAUSSIANQUAD</td>
<td>Das Gerät unterstützt die Pro-Stage-Filterung von Gaußschen Quadern zum Verminen von Texturen.</td>
</tr>
<tr class="odd">
<td>D3DPTFILTERCAPS_MIPFPOINT</td>
<td>Das Gerät unterstützt die Punktbeispielfilterung pro Phase für Mipmaps. Der point-sample mipmapping-Filter wird durch den D3DTEXF_POINT Member des <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE-Enumerationstyps</strong></a> dargestellt.</td>
</tr>
<tr class="even">
<td>D3DPTFILTERCAPS_MIPFLINEAR</td>
<td>Das Gerät unterstützt die mehrstufige bilineare Interpolationsfilterung für Mipmaps. Der mipmapping-Filter für die bilineare Interpolation wird durch den D3DTEXF_LINEAR des <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>aufzählten D3DTEXTUREFILTERTYPE-Typs</strong></a> dargestellt.</td>
</tr>
</tbody>
</table>



 

Diese Konstanten werden von TextureFilterCaps-, CubeTextureFilterCaps-, VolumeTextureFilterCaps- und VertexTextureFilterCaps-Membern von [**D3DCAPS9 verwendet.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)

## <a name="constant-information"></a>Konstante Informationen



|  Anforderung                        | Wert           |
|--------------------------|------------|
| Header                   | d3d9caps.h |
| Mindestbetriebssystem | Windows 98 |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Konstanten](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
