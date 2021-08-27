---
description: Texturfilterkonst konstanten.
ms.assetid: 4434e456-670e-46a9-ba78-affdc195fe1c
title: D3DPTFILTERCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06624f4f8779a866d440212c205baa9b4a84839a
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122624546"
---
# <a name="d3dptfiltercaps"></a>D3DPTFILTERCAPS

Texturfilterkonst konstanten.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>#Definieren</td>
<td>Beschreibung</td>
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
<td>Das Gerät unterstützt das filtern von pyramidalen Stichproben pro Stufe für Lupentexturen. Der pyramidale Lupenfilter wird durch den D3DTEXF_PYRAMIDALQUAD des <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>aufzählten D3DTEXTUREFILTERTYPE-Typs</strong></a> dargestellt.</td>
</tr>
<tr class="odd">
<td>D3DPTFILTERCAPS_MAGFGAUSSIANQUAD</td>
<td>Das Gerät unterstützt die gaußsche Quadratfilterung pro Stufe für die Vergrößerung von Texturen.</td>
</tr>
<tr class="even">
<td>D3DPTFILTERCAPS_MINFPOINT</td>
<td>Das Gerät unterstützt die punktbasierte Stichprobenfilterung pro Stufe zum Vereinheitlichen von Texturen. Der Punktbeispiel-Minierungsfilter wird durch den D3DTEXF_POINT des <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>aufzählten D3DTEXTUREFILTERTYPE-Typs</strong></a> dargestellt.</td>
</tr>
<tr class="odd">
<td>D3DPTFILTERCAPS_MINFLINEAR</td>
<td>Das Gerät unterstützt die mehrstufige lineare Filterung zum Vereinheitlichen von Texturen. Der lineare Minierungsfilter wird durch den D3DTEXF_LINEAR des <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>aufzählten D3DTEXTUREFILTERTYPE-Typs</strong></a> dargestellt.</td>
</tr>
<tr class="even">
<td>D3DPTFILTERCAPS_MINFANISOTROPIC</td>
<td>Das Gerät unterstützt die phasenbasierte anisotrope Filterung zur Minierung von Texturen. Der anisotrope Minierungsfilter wird durch den D3DTEXF_ANISOTROPIC des <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>aufzählten D3DTEXTUREFILTERTYPE-Typs</strong></a> dargestellt.</td>
</tr>
<tr class="odd">
<td>D3DPTFILTERCAPS_MINFPYRAMIDALQUAD</td>
<td>Das Gerät unterstützt das filtern von pyramidalen Stichproben pro Stufe zum Vereinheitlichen von Texturen.</td>
</tr>
<tr class="even">
<td>D3DPTFILTERCAPS_MINFGAUSSIANQUAD</td>
<td>Das Gerät unterstützt die gaußsche Quadfilterung pro Stufe zum Verfälschen von Texturen.</td>
</tr>
<tr class="odd">
<td>D3DPTFILTERCAPS_MIPFPOINT</td>
<td>Das Gerät unterstützt die punktbasierte Punktbeispielfilterung für Mipmaps. Der mipmapping-Punktbeispielfilter wird durch den D3DTEXF_POINT des <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>aufzählten D3DTEXTUREFILTERTYPE-Typs</strong></a> dargestellt.</td>
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

 

 
