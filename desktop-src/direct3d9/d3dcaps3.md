---
description: Treiberfunktionsflags.
ms.assetid: d9cd7388-3413-472d-aacb-0b8c9c60031a
title: D3DCAPS3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a165ff1d550612ba302c94a0b8181affe040921
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106341148"
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
<td>#definieren</td>
<td>Wert</td>
<td>BESCHREIBUNG</td>
</tr>
<tr class="even">
<td>D3DCAPS3_ALPHA_FULLSCREEN_FLIP_OR_DISCARD</td>
<td>0x00000020l</td>
<td>Gibt an, dass das Gerät den D3DRS_ALPHABLENDENABLE renderzustand im Vollbildmodus berücksichtigen kann, während er den Swap-oder Verwerfungs Effekt verwendet. Dies gilt nur, wenn die D3DRS_SRCBLEND oder D3DRS_DESTBLEND Zustände auf einen der folgenden Werte festgelegt sind:
<ul>
<li>D3DBLEND_DESTALPHA</li>
<li>D3DBLEND_INVDESTALPHA</li>
<li>D3DBLEND_DESTCOLOR</li>
<li>D3DBLEND_INVDESTCOLOR</li>
</ul></td>
</tr>
<tr class="odd">
<td>D3DCAPS3_COPY_TO_VIDMEM</td>
<td>0x00000100l</td>
<td>Das Gerät kann eine Speicher Kopie aus dem Systemspeicher in den lokalen Videospeicher beschleunigen. Dadurch wird sichergestellt, dass <a href="/windows/desktop/api"><strong>updatesurface</strong></a> -und <a href="/windows/desktop/api"><strong>UpdateTexture</strong></a> -Aufrufe Hardware beschleunigt werden. Wenn diese Obergrenze fehlt, sind diese Aufrufe zwar erfolgreich, aber langsamer.</td>
</tr>
<tr class="even">
<td>D3DCAPS3_COPY_TO_SYSTEMMEM</td>
<td>0x00000200l</td>
<td>Das Gerät kann eine Speicher Kopie aus lokalem Videospeicher in den Systemspeicher beschleunigen. Diese Obergrenze gewährleistet, dass <a href="/windows/desktop/api"><strong>GetRenderTargetData</strong></a> -Aufrufe Hardware beschleunigt werden. Wenn diese Obergrenze fehlt, wird dieser Vorgang zwar erfolgreich ausgeführt, wird jedoch langsamer.</td>
</tr>
<tr class="odd">
<td>D3DCAPS3_DXVAHD</td>
<td>0x00000400l</td>
<td>Der Anzeigetreiber unterstützt den DXVA-HD-DDI. Weitere Informationen zu DXVA-HD DDI finden Sie unter <a href="https://msdn.microsoft.com/library/dd835176.aspx">verarbeiten High-Definition Videos</a>.<br/> 
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
<td>0x00000080l</td>
<td>Gibt an, dass das Gerät eine Gammakorrektur von einem Fenster Hintergrund Puffer (mit linearem Inhalt) zu einem sRGB-Desktop ausführen kann.</td>
</tr>
<tr class="odd">
<td>D3DCAPS3_RESERVED</td>
<td>0x8000001fl</td>
<td>Bleiben nicht verwendet.</td>
</tr>
</tbody>
</table>



 

Diese Konstanten werden vom D3CAPS3-Member von [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)verwendet.

## <a name="constant-information"></a>Konstante Informationen



|                          |            |
|--------------------------|------------|
| Header                   | d3d9caps. h |
| Mindestens Betriebssystem | Windows 98 |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Konstanten](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 




