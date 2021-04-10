---
description: Verschiedene Treiber primitive funktionsflags.
ms.assetid: 7912c682-c179-453b-8a34-e87958217500
title: D3DPMISCCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76af50a1e7f78f6441af9e985f55e42ee2298b46
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214238"
---
# <a name="d3dpmisccaps"></a>D3DPMISCCAPS

Verschiedene Treiber primitive funktionsflags.



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
<td>D3DPMISCCAPS_MASKZ</td>
<td>0x00000002L</td>
<td>Das Gerät kann die Änderung des tiefen Puffers bei Pixel Vorgängen aktivieren und deaktivieren.</td>
</tr>
<tr class="odd">
<td>D3DPMISCCAPS_CULLNONE</td>
<td>0x00000010L</td>
<td>Der Treiber führt keine Dreiecks Berechnung durch. Dies entspricht dem D3DCULL_NONE-Member des <a href="/windows/desktop/direct3d9/d3dcull"><strong>D3DCULL</strong></a> -enumerierten Typs.</td>
</tr>
<tr class="even">
<td>D3DPMISCCAPS_CULLCW</td>
<td>0x00000020l</td>
<td>Der Treiber unterstützt die Dreiecks Berechnung im Uhrzeigersinn durch den D3DRS_CULLMODE Zustand. (Dies gilt nur für Dreiecks primitive.) Dieses Flag entspricht dem D3DCULL_CW-Member des <a href="/windows/desktop/direct3d9/d3dcull"><strong>D3DCULL</strong></a> -enumerierten Typs.</td>
</tr>
<tr class="odd">
<td>D3DPMISCCAPS_CULLCCW</td>
<td>0x00000040l</td>
<td>Der Treiber unterstützt gegen den Uhrzeigersinn im Uhrzeigersinn durch den D3DRS_CULLMODE Zustand. (Dies gilt nur für Dreiecks primitive.) Dieses Flag entspricht dem D3DCULL_CCW-Member des <a href="/windows/desktop/direct3d9/d3dcull"><strong>D3DCULL</strong></a> -enumerierten Typs.</td>
</tr>
<tr class="even">
<td>D3DPMISCCAPS_COLORWRITEENABLE</td>
<td>0x00000100l</td>
<td>Das Gerät unterstützt pro-Channel-Schreibvorgänge für den Renderziel-Farb Puffer durch den D3DRS_COLORWRITEENABLE Zustand.</td>
</tr>
<tr class="odd">
<td>D3DPMISCCAPS_CLIPPLANESCALEDPOINTS</td>
<td>0x00000200l</td>
<td>Das Gerät schneidet skalierte Punkte mit einer Größe von mehr als 1,0 auf benutzerdefinierte Clippingebenen.</td>
</tr>
<tr class="even">
<td>D3DPMISCCAPS_CLIPTLVERTS</td>
<td>0x00000200l</td>
<td>Geräte Clips nach umgewandelten Scheitel Punkten. Geben Sie D3DUSAGE_DONOTCLIP an, wenn die Pipeline kein Clipping durchführen soll. In diesem Fall muss möglicherweise zur zeichnungszeit ein zusätzliches Software Clipping durchgeführt werden, sodass der Vertex-Puffer sich im Systemspeicher befinden muss.<br/></td>
</tr>
<tr class="odd">
<td>D3DPMISCCAPS_TSSARGTEMP</td>
<td>0x00000400l</td>
<td>Das Gerät unterstützt <a href="d3dta.md">D3DTA</a> für ein temporäres Register.</td>
</tr>
<tr class="even">
<td>D3DPMISCCAPS_BLENDOP</td>
<td>0x00000800l</td>
<td>Das Gerät unterstützt andere Alpha-Mischungs Vorgänge als D3DBLENDOP_ADD.</td>
</tr>
<tr class="odd">
<td>D3DPMISCCAPS_NULLREFERENCE</td>
<td>0x00000100l</td>
<td>Ein Referenzgerät, das nicht angezeigt wird.</td>
</tr>
<tr class="even">
<td>D3DPMISCCAPS_INDEPENDENTWRITEMASKS</td>
<td>0x00004000l</td>
<td>Das Gerät unterstützt unabhängige Schreib Masken für mehrere Element Texturen oder mehrere Renderingziele.</td>
</tr>
<tr class="odd">
<td>D3DPMISCCAPS_PERSTAGECONSTANT</td>
<td>0x00008000l</td>
<td>Das Gerät unterstützt stufenübergreifende Konstanten. Siehe D3DTSS_CONSTANT in <a href="/windows/desktop/direct3d9/d3dtexturestagestatetype"><strong>D3DTEXTURESTAGESTATETYPE</strong></a>.</td>
</tr>
<tr class="even">
<td>D3DPMISCCAPS_POSTBLENDSRGBCONVERT</td>
<td>0x00200000l</td>
<td>Das Gerät unterstützt nach dem mischen die Konvertierung in sRGB. 
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
<td>D3DPMISCCAPS_FOGANDSPECULARALPHA</td>
<td>0x00010000l</td>
<td>Das Gerät unterstützt separate Nebel-und Glanz alpha. Viele Geräte verwenden den Glanz Alphakanal, um den Nebel Faktor zu speichern.</td>
</tr>
<tr class="even">
<td>D3DPMISCCAPS_SEPARATEALPHABLEND</td>
<td>0x00020000l</td>
<td>Das Gerät unterstützt separate Blend-Einstellungen für den Alphakanal.</td>
</tr>
<tr class="odd">
<td>D3DPMISCCAPS_MRTINDEPENDENTBITDEPTHS</td>
<td>0x00040000l</td>
<td>Das Gerät unterstützt verschiedene Bits-tiefen für mehrere Renderziele.</td>
</tr>
<tr class="even">
<td>D3DPMISCCAPS_MRTPOSTPIXELSHADERBLENDING</td>
<td>0x00080000l</td>
<td>Das Gerät unterstützt Post-Pixel-Shader-Vorgänge für mehrere Renderziele.</td>
</tr>
<tr class="odd">
<td>D3DPMISCCAPS_FOGVERTEXCLAMPED</td>
<td>0x00100000l</td>
<td>Geräte Klammern blenden Sie den Faktor pro Scheitelpunkt aus.</td>
</tr>
</tbody>
</table>



 

Diese Konstanten werden vom primitivefehlcaps-Member von [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)verwendet.

## <a name="constant-information"></a>Konstante Informationen



|                          |            |
|--------------------------|------------|
| Header                   | d3d9caps. h |
| Mindestens Betriebssystem | Windows 98 |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Konstanten](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
