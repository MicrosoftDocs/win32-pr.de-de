---
description: Texturfilterkonstanten.
ms.assetid: 4434e456-670e-46a9-ba78-affdc195fe1c
title: D3DPTFILTERCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e86645ca1d0f8c1904307b80c27c2b8ce8d635229d3bb15b0f8178d6a9d70dcc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118804668"
---
# <a name="d3dptfiltercaps"></a>D3DPTFILTERCAPS

Texturfilterkonstanten.



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
<td>Das Gerät unterstützt monocolore Konvolutionsfilterung. Dieser Filter wird durch den D3DTEXF_CONVOLUTIONMONO Member des <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE-Enumerationstyps</strong></a> dargestellt. 
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
<td>Das Gerät unterstützt die Punktsamplingfilterung pro Phase zum Vergrößern von Texturen. Der Vergrößerungsfilter für Punktbeispiele wird durch den D3DTEXF_POINT Member des <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE-Enumerationstyps</strong></a> dargestellt.</td>
</tr>
<tr class="even">
<td>D3DPTFILTERCAPS_MAGFLINEAR</td>
<td>Das Gerät unterstützt die bilineare Interpolationsfilterung pro Phase zum Vergrößern von Mipmaps. Der bilineare Interpolationsfilter mipmapping wird durch den D3DTEXF_LINEAR Member des <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE-Enumerationstyps</strong></a> dargestellt.</td>
</tr>
<tr class="odd">
<td>D3DPTFILTERCAPS_MAGFANISOTROPIC</td>
<td>Das Gerät unterstützt die phasenspezifische Anisotrope Filterung zum Vergrößern von Texturen. Der Anisotrope Vergrößerungsfilter wird durch den D3DTEXF_ANISOTROPIC Member des <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE-Enumerationstyps</strong></a> dargestellt.</td>
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
<td>Das Gerät unterstützt die Punktsamplingfilterung pro Phase, um Texturen zu verminen. Der Point-Sample-Filter für die Minierung wird durch den D3DTEXF_POINT Member des <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE-Enumerationstyps</strong></a> dargestellt.</td>
</tr>
<tr class="odd">
<td>D3DPTFILTERCAPS_MINFLINEAR</td>
<td>Das Gerät unterstützt die lineare Filterung pro Stufe zum Verminen von Texturen. Der lineare Minderungsfilter wird durch den D3DTEXF_LINEAR Member des <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE-Enumerationstyps</strong></a> dargestellt.</td>
</tr>
<tr class="even">
<td>D3DPTFILTERCAPS_MINFANISOTROPIC</td>
<td>Das Gerät unterstützt die phasenspezifische Anisotrope Filterung für die Vergrößerung von Texturen. Der Anisotrope Minderungsfilter wird durch den D3DTEXF_ANISOTROPIC Member des <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE-Enumerationstyps</strong></a> dargestellt.</td>
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
<td>Das Gerät unterstützt die bilineare Interpolationsfilterung pro Phase für Mipmaps. Der bilineare Interpolationsfilter mipmapping wird durch den D3DTEXF_LINEAR Member des <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE-Enumerationstyps</strong></a> dargestellt.</td>
</tr>
</tbody>
</table>



 

Diese Konstanten werden von TextureFilterCaps-, CubeTextureFilterCaps-, VolumeTextureFilterCaps- und VertexTextureFilterCaps-Membern von [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)verwendet.

## <a name="constant-information"></a>Konstanteninformationen



|  Anforderung                        | Wert           |
|--------------------------|------------|
| Header                   | d3d9caps.h |
| Mindestbetriebssystem | Windows 98 |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Konstanten](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
