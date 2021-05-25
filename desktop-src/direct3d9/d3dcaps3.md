---
description: Treiberfunktionsflags.
ms.assetid: d9cd7388-3413-472d-aacb-0b8c9c60031a
title: D3DCAPS3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fda81aa7f77dcaf03eb06b357ebfb91b4956f6d4
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343365"
---
# <a name="d3dcaps3"></a>D3DCAPS3

Treiberfunktionsflags.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td>#Definieren</td>
<td>Wert</td>
<td>BESCHREIBUNG</td>
</tr>
<tr class="even">
<td>D3DCAPS3_ALPHA_FULLSCREEN_FLIP_OR_DISCARD</td>
<td>0x00000020L</td>
<td>Gibt an, dass das Gerät den D3DRS_ALPHABLENDENABLE Im Vollbildmodus rendern kann, während die Swap-Auswirkung FLIP oder DISCARD verwendet wird. Dies gilt nur, wenn D3DRS_SRCBLEND oder D3DRS_DESTBLEND auf einen der folgenden Zustände festgelegt sind:
<ul>
<li>D3DBLEND_DESTALPHA</li>
<li>D3DBLEND_INVDESTALPHA</li>
<li>D3DBLEND_DESTCOLOR</li>
<li>D3DBLEND_INVDESTCOLOR</li>
</ul></td>
</tr>
<tr class="odd">
<td>D3DCAPS3_COPY_TO_VIDMEM</td>
<td>0x00000100L</td>
<td>Das Gerät kann eine Speicherkopie aus dem Systemspeicher in den lokalen Videospeicher beschleunigen. Diese Obergrenze garantiert, dass <a href="/windows/desktop/api"><strong>UpdateSurface-</strong></a> und <a href="/windows/desktop/api"><strong>UpdateTexture-Aufrufe</strong></a> hardwarebeschleunigt werden. Wenn diese Obergrenze nicht vorhanden ist, werden diese Aufrufe erfolgreich, aber langsamer.</td>
</tr>
<tr class="even">
<td>D3DCAPS3_COPY_TO_SYSTEMMEM</td>
<td>0x00000200L</td>
<td>Das Gerät kann eine Speicherkopie vom lokalen Videospeicher in den Systemspeicher beschleunigen. Diese Obergrenze garantiert, dass <a href="/windows/desktop/api"><strong>GetRenderTargetData-Aufrufe</strong></a> hardwarebeschleunigte Aufrufe werden. Wenn diese Obergrenze nicht vorhanden ist, ist dieser Aufruf zwar erfolgreich, ist aber langsamer.</td>
</tr>
<tr class="odd">
<td>D3DCAPS3_DXVAHD</td>
<td>0x00000400L</td>
<td>Der Anzeigetreiber unterstützt die DXVA-HD DDI. Weitere Informationen zu DXVA-HD DDI finden Sie unter <a href="https://msdn.microsoft.com/library/dd835176.aspx">Processing High-Definition Video</a>.<br/> 
<table>
<tbody>
<tr class="odd">
<td>Unterschiede zwischen Direct3D 9 und Direct3D 9Ex:<br/> Dieses Flag ist nur in Direct3D 9Ex verfügbar.<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>D3DCAPS3_LINEAR_TO_SRGB_PRESENTATION</td>
<td>0x00000080L</td>
<td>Gibt an, dass das Gerät eine Gammakorrektur von einem gefensterten Hintergrundpuffer (mit linearen Inhalten) zu einem sRGB-Desktop durchführen kann.</td>
</tr>
<tr class="odd">
<td>D3DCAPS3_RESERVED</td>
<td>0x8000001fL</td>
<td>Reserviert; wird nicht verwendet.</td>
</tr>
</tbody>
</table>



 

Diese Konstanten werden vom D3CAPS3-Member von [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)verwendet.

## <a name="constant-information"></a>Konstanteninformationen



|  Anforderung                        | Wert           |
|--------------------------|------------|
| Header                   | d3d9caps.h |
| Mindestbetriebssystem | Windows 98 |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Konstanten](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 




